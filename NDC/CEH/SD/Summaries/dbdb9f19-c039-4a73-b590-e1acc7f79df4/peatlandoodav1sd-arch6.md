# Object oriented data analysis of surface motion time series in peatland landscapes

## Purpose and scope
- Provides a generic implementation of object oriented data analysis for surface motion time series in peatlands to assess peatland condition.
- Based on the approach demonstrated by Mitchell et al. (2022) for the Flow Country, Scotland.
- Analyzes differences in overall trend and oscillatory behavior, along with timing and amplitude differences, to classify peatland sites into clusters with uncertainty captured by cluster assignment frequencies.

## Data and inputs
- Requires a CSV file uploaded by the user, with a strict format:
  - Dates: first row contains time points in YYYY-MM-DD format; first two columns are NA for longitudes and latitudes; remaining columns are time series data for each date.
  - Longitude: first column after header, with NA in the first entry.
  - Latitude: second column after header, with NA in the first entry.
  - ts_t1 … ts_tK: successive columns contain surface motion values for each peatland location (rows 2 onward contain data for each site).
- The model code splits the CSV into separate components (dates, lon/lat, time series) for processing.
- Time points, locations, and time series can be subsampled to speed up computations.

## How the model works (four processing chunks)
- Chunk 1: Splitting trend and oscillations
  - Separates overall trend from oscillatory components for each time series.
- Chunk 2: Warping oscillations to a template
  - Warps oscillations to a sine template to capture timing differences; produces registration fields.
- Chunk 3: Finding distance measures
  - Computes distance measures in SRVF space; includes various distance evaluations and standardizations.
- Chunk 4: Assigning clusters
  - Uses a Gibbs sampling scheme to perform clustering with spatial smoothing; parallel outputs include cluster assignments across iterations.

## Outputs and data products
- Outputs per chunk (examples of produced objects):
  - smooth.mat2: TimeMax x p matrix of smoothed oscillatory components.
  - smooth.mat: TimeMax x p matrix of smoothed trends and oscillations.
  - templateSin: Sine wave template for timing comparison.
  - gammat_fc_osc: Warping functions capturing timing differences.
  - qtilde_fc_osc, qtilde_fc_tre: SRVF representations of registered oscillations and trends.
  - dist90osc2.pl, dist22osc.pl, identityvec.pl, dist90tre2.pl: Distance measures and related metrics.
  - m1, m1t: Initial and iteration-based cluster assignments.
  - mean.centres: Cluster centers across iterations (dimensions: clusters x iterations x number of clusters).
  - beta1t: Cluster variances across iterations.
  - probmat: Probability of each time series belonging to each cluster.
  - mapclust: Most likely cluster for each peatland location.
  - m1tTHIN, mean.centresTHIN: Thinned versions for obtaining independent probabilistic outputs used in probmat and mapclust.
- Outputs enable creation of plots and tables to summarise peatland condition and cluster membership, including uncertainty in assignments.

## Running the model (environment and workflow)
- Prerequisites
  - R and dependent packages: fdasrvf, mvtnorm, invgamma (and their dependencies).
- How to run
  - Copy the provided model code into an R terminal and run.
  - Alternatively, run individual functions from the R file named PeatlandOODA.R.
- Configuration
  - The model provides preambles in each section describing user-adjustable features (e.g., number of clusters, allowable warping in registration).
  - While the code runs with defaults, adjusting these settings is recommended to align with specific aims (see Mitchell et al. 2022 for details).

## Outputs interpretation and use
- Clustering results classify peatland sites into groups based on differences in trend and oscillatory behavior, with spatial smoothing linking neighboring sites.
- Assignment uncertainty is captured by how often a site falls into each cluster across Gibbs iterations.
- Outputs support end-user exploration and self-service analyses, with options to generate summary plots and tables to communicate peatland condition.

## Tunable parameters and recommendations
- Number of clusters (kclust): adjustable to reflect expected peatland groupings.
- Warping allowance during oscillation registration: configurable to match the desired flexibility in timing differences.
- Other section-specific presets: available but optional; defaults will work but may be tailored to study aims (e.g., different temporal resolutions, subsampling).

## Reference
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187