# Object oriented data analysis of surface motion time series in peatland landscapes

## Purpose
- Presents a model code that enables generic object oriented data analysis of surface motion time series in peatland landscapes to assess peatland condition.
- Demonstrates the approach using Flow Country, Scotland (Mitchell et al. 2022).
- Methodology: compare each time series by differences in overall trend and oscillatory behaviour, including timing and amplitude of oscillations via warping to a sine template; cluster series with a Gibbs sampling scheme and apply spatial smoothing; assign peatlands to the most representative cluster with assignment uncertainty.

## Running the model code
- Prerequisites: install R and the packages fdasrvf, mvtnorm, invgamma (and dependencies).
- Workflow: upload a CSV of surface motion time series, then run the model code by pasting it into an R terminal, or run individual functions via the PeatlandOODA.R file.

## Using the model code (input data format)
- Required CSV structure:
  - Dates row: first row contains Dates in YYYY-MM-DD format for time points t1…tK; first two columns contain NA (for Longitude and Latitude).
  - Longitude row: column 1 is the longitude, first entry NA.
  - Latitude row: column 2 is the latitude, first entry NA.
  - ts_t1 … ts_tK: subsequent columns contain surface motion data for each peatland location, arranged such that row 2 corresponds to the first peatland, row 3 to the second, etc.
- Processing steps split the data into four chunks (with optional preambles to adjust settings):
  1. Splitting trend and oscillations
  2. Warping oscillations to a sine template (to capture timing differences)
  3. Finding distance measures (based on warping, trends, and SRVF representations)
  4. Assigning clusters using a Gibbs sampling scheme with spatial smoothing
- Configuration options include the number of clusters and the allowed level of warping; defaults run without changes but can be adjusted to fit aims.

## Model structure and workflow
- Key operations:
  - Separate trend from oscillations for each time series
  - Warp oscillations to a sine template to compare timing
  - Compute distance measures in SRVF space
  - Cluster time series with Gibbs sampling, incorporating spatial smoothing
- Outputs are generated per chunk (with helpful defaults and optional outputs):
  - TimeMax, p (number of series), n (subsampled time points), nit (Gibbs iterations), kclust (clusters)
  - smooth.mat2: (TimeMax x p) matrix of smooth oscillatory trends
  - smooth.mat: smooth representations of overall trends and oscillatory components
  - templateSin: sine-wave timing template
  - gammat_fc_osc, qtilde_fc_osc: warp functions and registered oscillations
  - qtilde_fc_tre, qtilde_fc_tre: trend SRVFs after processing
  - dist90osc2.pl, dist22osc.pl: distance measures for oscillations and warps
  - identityvec.pl: summary of warp function deviations from identity
  - m1, m1t: initial and Gibbs-sampled cluster assignments
  - mean.centres: cluster centers across iterations
  - beta1t: cluster variances
  - probmat: cluster membership probabilities
  - mapclust: most likely cluster per peatland
  - Thinned versions: m1tTHIN, mean.centresTHIN for independent probmat and mapclust
- Outputs can be used to generate plots and tables summarising peatland condition and cluster assignments.

## Outputs and interpretation
- Provides probabilistic clustering and assignment uncertainty for peatland condition.
- Spatial smoothing accounts for neighboring peatlands, enabling coherent regional assessments.
- Outputs support monitoring reports, dashboards, and stakeholder communication with quantified uncertainty.

## Practical considerations for monitoring frameworks
- Data requirements and governance:
  - Requires a structured CSV of time series with clear metadata (locations, dates, and series values).
  - Public sharing of underlying data and metadata is desirable for transparency but may pose barriers; ensure appropriate data governance and provenance.
- Data quality and compatibility:
  - The method relies on time series of sufficient length and quality; overcoming missing data and metadata gaps is important.
  - Warping and SRVF representations enable robust comparison across diverse peatland sites but require careful preprocessing.
- Data access and integration:
  - Addresses data silos by providing a unified workflow for trend and oscillation analysis and clustering.
  - Can be integrated into monitoring programs to classify peatlands into clusters representing condition states, with uncertainty measures to inform decisions.
- Communication of results:
  - The approach yields interpretable cluster assignments plus uncertainty, facilitating clear reporting to policymakers and stakeholders.
  - Customizable number of clusters and warping tolerance allow alignment with policy questions and monitoring scales.

## Reference
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187