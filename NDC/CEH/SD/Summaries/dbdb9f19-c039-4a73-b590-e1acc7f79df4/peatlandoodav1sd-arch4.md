# Object oriented data analysis of surface motion time series in peatland landscapes

## Overview
- Describes a generic, object oriented approach to analyze surface motion time series in peatland landscapes to assess peatland condition.
- Combines differences in trend and oscillations, warping to a sine template, and spatial smoothing to cluster peatland time series.
- Final peatland condition is inferred from the most frequent cluster assignment, with assignment uncertainty captured by cluster-frequency across iterations.

## What the model does
- Separates and compares trend versus oscillatory components across time series.
- Warps oscillations to a sine wave template to capture timing differences and amplitude differences.
- Computes distance measures in SRVF space to quantify differences between series.
- Clusters surface motion time series using a Gibbs sampling scheme with spatial smoothing to account for neighbouring peatlands.
- Outputs include cluster assignments and uncertainty, enabling interpretation of peatland condition and change.

## Running the model
- Requires a working R environment and the following packages: fdasrvf, mvtnorm, invgamma (and dependencies).
- Process:
  - Prepare a CSV with peatland time series in the specified format.
  - Copy the model code into an R terminal to run, or run individual functions from the file PeatlandOODA.R.
- There are predefined sections (chunks) in the code that can be adjusted to suit aims, including number of clusters and allowable warping.

## Using the model: data input format and processing steps
- Input CSV format must include:
  - Dates row: first row containing time stamps (YYYY-MM-DD) for ts_t1 to ts_tK; first two columns are NA (longitudes and latitudes), remaining columns match dates.
  - Longitude column: first data row NA.
  - Latitude column: second column NA for the first row.
  - ts_t1 ... ts_tK: surface motion values for each peatland site, starting from row 2 (site 1), row 3 (site 2), etc.
- Processing is organized into four chunks:
  1) Splitting trend and oscillations (and separating for analysis)
  2) Warping oscillations to a sine template (and measuring timing)
  3) Finding distance measures (based on prior steps)
  4) Assigning clusters via Gibbs sampling with spatial smoothing
- Each chunk has configurable preambles to adjust aspects such as the number of clusters and allowed warp.
- Key outputs per chunk include:
  - TimeMax x p matrices of smooth and trend/oscillation representations
  - Smooth and oscillation-specific representations (trend SRVFs, oscillation SRVFs)
  - Warping templates and registered oscillations
  - Distance measures capturing oscillation-template differences and trend differences
  - Initial and iterated cluster assignments, cluster centers, cluster variances, and probability matrices
  - Most likely cluster per peatland and thinned versions for dependency reduction and probabilistic mapping
- Time series and cluster results are designed for downstream plots and reporting.

## Outputs and interpretation
- Outputs include:
  - smooth.mat2: oscillation-smoothed representations
  - templateSin: sine-wave timing template
  - gammat_fc_osc, qtilde_fc_osc: warped oscillations and registered SRVFs
  - qtilde_fc_tre, dist90tre2.pl, dist90osc2.pl, dist22osc.pl, identityvec.pl: distance and warping measures
  - m1, m1t, mean.centres, beta1t, probmat, mapclust: clustering results, cluster statistics, and per-site cluster probabilities
  - Thinned versions (m1tTHIN, mean.centresTHIN, etc.) for reducing dependency and enabling robust probability-based summaries
- Outputs enable:
  - Assignment of each peatland to a cluster representing its surface motion characteristics
  - Quantification of uncertainty via iteration-based counts and probabilities
  - Visualization and reporting of peatland condition across landscapes

## Data governance and practical considerations for Data Leaders
- Data quality and provenance:
  - Clear input data specification is required to ensure reproducibility and correct interpretation of time series.
  - Metadata should capture time sampling, units, and any preprocessing steps applied prior to analysis.
- Standards, discoverability, and reuse:
  - Versioned model code (PeatlandOODA.R) and parameter settings should be documented for auditability.
  - Outputs should be catalogued with descriptive metadata (time span, number of sites, number of time points, cluster count).
- Reproducibility and governance:
  - The workflow supports re-running with updated data or adjusted cluster/warp parameters; maintain a changelog of parameter adjustments.
  - Dependency management for R and required packages should be tracked (environment files or containerization can help).
- Stakeholder alignment:
  - Outputs support data-driven decisions about peatland condition and prioritization by aligning cluster results with user needs (policy colleagues, conservation teams).
  - The method enables co-ownership of data products by providing transparent clustering logic and uncertainty measures.
- Data access and privacy considerations:
  - Ensure appropriate access controls if peatland locations are sensitive; manage data sharing in line with governance policies.

## Challenges and considerations
- Input data requirements are strict; formatting errors can impede execution.
- Choice of parameters (number of clusters, warp allowances) influences results and may require domain expert input.
- Spatial smoothing quality depends on the quality and granularity of location data (lat/long accuracy, site density).
- Interpretation of clusters requires careful linking to ecological meaning and management actions.

## References
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187