# Object oriented data analysis of surface motion time series in peatland landscapes

## Purpose
- Provides a generic object-oriented framework for analyzing surface motion time series in peatland landscapes to assess peatland condition.
- Detects differences in overall trend and oscillatory behavior between series, including timing (via warping to a sine template) and amplitude differences.
- Clusters time series using a Gibbs sampling scheme with spatial smoothing.
- Outputs assignment uncertainty based on cluster membership frequencies.

## Running the model code
- Required: Install R and packages fdasrvf, mvtnorm, invgamma (and their dependencies).
- Process: Upload a CSV of surface motion time series, then run the model code by pasting it into an R terminal (or run individual functions from the file PeatlandOODA.R).
- The workflow is modular, with four main chunks implemented sequentially.

## Using the model code
- The code separates inputs (dates, longitudes, latitudes) from the surface motion time series data for analysis.
- Four processing chunks (with optional preambles to adjust settings):
  1) Splitting trend and oscillations
  2) Warping oscillations to the template
  3) Finding distance measures
  4) Assigning clusters (Gibbs sampler with spatial smoothing)
- Users can adjust optional settings such as the number of clusters and the allowed amount of warping; defaults will run but may be tuned to match aims.

## Data format (CSV)
- The CSV must include:
  - Dates row: time stamps in YYYY-MM-DD across columns (ts_t1 to ts_tK). First two entries in the first row are NA for longitude and latitude.
  - Longitude column: first entry NA; subsequent rows contain peatland longitudes.
  - Latitude column: first entry NA; subsequent rows contain peatland latitudes.
  - ts_t1 ... ts_tK columns: surface motion values for each peatland location, with row 2 containing the first location, row 3 the second, etc.
- The model splits date, longitude, and latitude from the time series data.

## Analysis pipeline and outputs
- Chunk 1: Splitting trend and oscillations
  - Produces smooth representations of the trend and of oscillatory components.
- Chunk 2: Warping oscillations to template
  - Warps oscillatory series to a sine template to align timing of peaks.
- Chunk 3: Finding distance measures
  - Computes distance metrics in SRVF space between oscillations and template, and related comparisons (with standardisation options).
- Chunk 4: Assigning clusters (Gibbs sampling with spatial smoothing)
  - Performs clustering over iterations; outputs include cluster labels, centres, variances, and assignment probabilities.
- Key outputs (examples and meanings):
  - smooth.mat2: (TimeMax x p) matrix of oscillatory components; smooth.mat1: trend components; smooth.mat: overall smooths.
  - templateSin: sine template vector used for timing alignment.
  - gammat_fc_osc: warping functions capturing timing differences.
  - qtilde_fc_osc, qtilde_fc_tre: registered oscillation and trend SRVF representations.
  - dist90osc2.pl, dist22osc.pl, identityvec.pl: distance measures and warping identity relations.
  - m1, m1t: cluster assignments (initial and across iterations).
  - mean.centres: cluster mean centres across iterations and clusters.
  - beta1t: cluster variances over iterations.
  - probmat: matrix of cluster assignment probabilities for each peatland.
  - mapclust: most likely cluster per peatland location.
  - m1tTHIN, mean.centresTHIN: thinned samples for downstream probability summaries and mapclust.
- Outputs are designed to be used for creating plots and tables to summarise peatland condition by cluster, with assignment uncertainty reflected in the results.

## Outputs interpretation and use
- The clustering results indicate common patterns of surface motion (trend and oscillations) across peatlands.
- Spatial smoothing accounts for neighbouring sites, improving regional coherence.
- Assignment uncertainty (via multiple cluster appearances) informs confidence in peatland condition classification.
- Users can generate visualisations and tables from the provided outputs to communicate findings and support decision-making.

## Reference
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187