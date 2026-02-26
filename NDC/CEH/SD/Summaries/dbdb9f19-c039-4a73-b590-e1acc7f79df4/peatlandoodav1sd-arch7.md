# Object oriented data analysis of surface motion time series in peatland landscapes

## Overview
- Purpose: Generic object-oriented data analysis framework to analyze surface motion time series in peatland landscapes and assess peatland condition, demonstrated on the Flow Country, Scotland.
- Approach: Decomposes each time series into trend and oscillatory components, warps oscillations to a sine waveform template, and measures differences using SRVF-based distances. Clusters time series via a Gibbs sampling scheme with spatial smoothing to account for neighbouring peatlands. Assignment uncertainty is captured by how often a time series falls into each cluster.
- Outputs: Cluster assignments with uncertainty, plus a suite of intermediate and final results suitable for map-based visualization.

## Data input
- Input format: CSV file with the following structure:
  - Dates row: first row lists time points (YYYY-MM-DD). NA entries in the first two columns (lon, lat); remaining columns correspond to dates.
  - Longitude row: first column NA, subsequent cells contain longitude values.
  - Latitude row: first column NA, subsequent cells contain latitude values.
  - Time series data rows: each subsequent row provides a peatland site’s surface motion values for each date (ts_t1 to ts_tK), starting from the third column onward.
- File organization: Dates, Longitude, and Latitude are separated from the surface motion time series for processing.

## Running the model code
- Prerequisites: Install R and the required packages (fdasrvf, mvtnorm, invgamma) plus dependencies.
- Execution options:
  - Copy the model code into an R terminal and run.
  - Open and run individual functions from the file PeatlandOODA.R.
- Inputs required: A CSV file in the specified format.

## Processing workflow (four chunks)
- Chunk 1: Splitting trend and oscillations
  - Separate overall trends from oscillatory components to quantify differences between series.
- Chunk 2: Warping oscillations to template
  - Warp oscillations to a sine-wave template and quantify timing differences; use a sine template with domain-specific interpretation (e.g., peaks aligned to May 5).
- Chunk 3: Finding distance measures
  - Compute distance measures in accordance with the warped oscillations and trends (SRVF-based distances; includes standardization steps).
- Chunk 4: Assigning clusters
  - Apply a Gibbs sampling scheme to cluster time series with spatial smoothing across neighbouring peatlands.
- Preamble and tunable parameters
  - Each chunk includes adjustable settings (e.g., number of clusters, allowed warp) to suit user aims; defaults are available.

## Key outputs and their meaning
- Time-series and smooth representations:
  - smooth.mat2: TimeMax x p matrix of oscillation-related smooth functions.
  - smooth.mat: TimeMax x p matrix for overall trends and oscillations.
  - templateSin: Sine-wave template vector; used for timing comparisons.
  - gammat_fc_osc: Warping functions capturing timing differences in oscillations.
  - qtilde_fc_osc: Registered oscillation SRVFs (warped).
  - qtilde_fc_tre: SRVFs of trend (unregistered).
- Distance measures:
  - dist90osc2.pl: Distance between oscillations and sine template in SRVF space.
  - dist22osc.pl: Distance between warping function and identity warp.
  - identityvec.pl: Summed occurrences where the warping exceeds identity.
  - dist90tre2.pl: Distance between trends and the overall mean trend in SRVF space.
- Clustering results (Gibbs sampling with thinning for independence):
  - m1, m1t: Initial and loop-specific cluster assignments.
  - mean.centres: Cluster centers across loops and clusters.
  - beta1t: Cluster variances across loops.
  - probmat: Probability of each time series belonging to each cluster.
  - mapclust: Most likely cluster for each peatland location.
  - m1tTHIN, mean.centresTHIN: Thinned versions for robust probabilistic summaries and mapping.
- Outputs facilitate generation of plots and tables to summarize peatland condition by cluster and spatial pattern.

## How this maps to GIS work
- Produces map-ready cluster assignments and uncertainty for peatland sites, enabling spatial visualization of condition groups across peatland landscapes.
- Handles multi-site time series with differing resolutions by extracting consistent trend and oscillation features and smoothing spatially across neighboring peatlands.
- Supports iterative refinement through user-tunable parameters and feedback.

## Practical notes
- The approach relies on time series data quality and consistent sampling; addressing data gaps and varying resolutions is inherent to preprocessing and harmonization steps.
- Referenced methodology: Mitchell et al. (2022) for object-oriented data analysis of surface motion time series in peatland landscapes.

## Reference
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187