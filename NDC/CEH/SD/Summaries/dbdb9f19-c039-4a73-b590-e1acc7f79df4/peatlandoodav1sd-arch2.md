# Object oriented data analysis of surface motion time series in peatland landscapes

## Overview
- A generic, object‑oriented framework for analyzing surface motion time series in peatland landscapes to assess peatland condition.
- Demonstrates a workflow (as in Mitchell et al., 2022) that compares trends and oscillatory behavior across peatland sites, then clusters sites and accounts for spatial relationships.
- Outputs enable standardized reporting and facilitate monitoring over time.

## Data inputs and format
- Requires a CSV file containing peatland surface motion time series.
- Format elements:
  - Dates: first row (YYYY-MM-DD) for time points ts_t1 … ts_tK.
  - Longitude, Latitude: header rows with NA in the first entries.
  - ts_t1 … ts_tK: surface motion values for each peatland location, starting from row 2 (one location per row).
- The workflow splits metadata (dates, lon, lat) from the time series data for processing.

## How the model works (workflow)
- Four processing chunks, each with optional preambles to adjust settings:
  1) Splitting trend and oscillations
     - Treats overall trend and oscillatory components separately.
  2) Warping oscillations to a template
     - Aligns oscillations to a sine-template to capture timing differences.
  3) Finding distance measures
     - Computes distances based on the trend and warped oscillations (e.g., SRVF-derived distances).
  4) Assigning clusters
     - Uses a Gibbs sampling scheme to cluster sites with spatial smoothing; captures assignment uncertainty by cluster‑membership frequency.
- Outputs for each chunk include representations of trends, oscillations, templates, and distance measures that feed the clustering.

## Running and using the code
- Requirements:
  - R and the packages: fdasrvf, mvtnorm, invgamma (plus dependencies).
- How to run:
  - Upload the CSV file in the specified format.
  - Copy the model code into an R terminal and run, or run individual functions via the PeatlandOODA.R file.
- Customization (recommended to adjust as needed):
  - Number of clusters
  - Amount of warping in the registration phase
  - Other features as described in Mitchell et al. (2022) for specific aims

## Outputs and interpretation
- Key outputs (examples):
  - TimeMax x p matrices and smooth representations of trend and oscillations.
  - SRVF-based representations for trends and oscillations (after processing).
  - Distance measures comparing oscillations to templates and trends to mean trends.
  - Cluster assignments and management of uncertainty:
    - Initial random cluster labels
    - Cluster labels across Gibbs iterations
    - Cluster means and variances for each loop
    - Probability matrices for cluster membership
    - Most likely cluster per peatland location
  - Thinned outputs (post-burn-in) for probabilistic summaries and mapping
- Outputs support:
  - Creation of plots and tables to summarise peatland condition and spatial patterns.
  - Potential integration into monitoring dashboards and data portals.

## Practical relevance for environmental monitoring
- Provides a standardised, reproducible method to classify peatland sites by surface motion behavior, aiding condition assessment over time.
- Incorporates spatial smoothing to respect neighbourhood relationships between peatlands.
- Produces clear, map-ready and tabular outputs suitable for policy performance reporting and environmental health monitoring.
- Emphasizes transparency and adaptability (parameters can be tuned to suit monitoring objectives).

## Reference
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J., and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187