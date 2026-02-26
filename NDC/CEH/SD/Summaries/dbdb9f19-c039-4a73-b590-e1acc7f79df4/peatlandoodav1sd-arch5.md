# Object oriented data analysis of surface motion time series in peatland landscapes

## Purpose
- Presents a model code for generic, object-oriented analysis of peatland surface motion time series to assess peatland condition.
- Procedure: compare differences in overall trend and oscillatory behavior across time series, including timing differences to a sine-wave template via warping and amplitude differences.
- Cluster time series using a Gibbs sampling scheme with spatial smoothing; determine peatland condition by the cluster most frequently assigned to each series.
- Outputs are generated from a user-uploaded CSV containing the surface motion time series.

## Running the model code
- Requires installing R and the packages fdasrvf, mvtnorm, invgamma (and their dependencies).
- Run by:
  - Uploading the specified CSV file, then
  - Copying the model code into an R terminal and executing, or
  - Opening and running the individual functions from the file PeatlandOODA.R.
- Users can adjust settings (e.g., number of clusters, warping allowance) in the preamble of the code.

## Using the model code
- Input file requirements:
  - A CSV with a specific format:
    - Dates: time points across the first row.
    - Longitude: first data row/column with NA in the first entry.
    - Latitude: second data row/column with NA in the first entry.
    - ts_t1 to ts_tK: surface motion values for each peatland location, organized by rows.
  - The code splits out the date, longitude, and latitude information from the surface motion time series.
- Processing steps (four chunks):
  1. Splitting trend and oscillations.
  2. Warping oscillations to a sine template and quantifying timing differences.
  3. Computing distance measures in SRVF space for trends and oscillations.
  4. Clustering via Gibbs sampling with spatial smoothing.
- Each chunk has configurable preambles (e.g., number of clusters, warping allowances).
- Outputs per chunk include various matrices, smooth functions, warping templates, distance metrics, and cluster-related objects.

## Outputs and interpretation
- Outputs enable:
  - Representations of trends and oscillations (smooth.mat, smooth.mat2).
  - Warped oscillations to template and related registrations (templateSin, gammat_fc_osc, qtilde_fc_osc, qtilde_fc_tre).
  - Distance measures used for clustering (dist90osc2.pl, dist22osc.pl, identityvec.pl, dist90tre2.pl).
  - Clustering results and diagnostics (m1, m1t, mean.centres, beta1t, probmat, mapclust).
  - Thinned/post-burnin results for probabilistic summaries (m1tTHIN, mean.centresTHIN).
- Final outputs include cluster assignments for each peatland location and associated uncertainty, as well as summaries and plots to interpret peatland condition by cluster.

## Data governance and stewardship considerations
- Metadata and standards:
  - Ensure clear documentation of the CSV schema used (Dates, Longitude, Latitude, ts_t1…ts_tK), including units and time cadence.
  - Record software version and package versions (R, fdasrvf, mvtnorm, invgamma) for reproducibility.
  - Document any parameter choices (kclust, warping limits, nit iterations) and rationale.
- Provenance and reproducibility:
  - Preserve the exact code version (PeatlandOODA.R) and any preamble changes.
  - Maintain a traceable data lineage from the original time series through to the clustering outputs.
- Data quality and governance:
  - Note data limitations, embargoes, or proprietary restrictions that affect data sharing.
  - For large datasets, consider processing in chunks or sub-sampling (as suggested by the TimeMax, n, and nits parameters) to manage compute resources.
- Discoverability and interoperability:
  - Provide a concise data dictionary and a README describing the dataset format, analysis workflow, and outputs.
  - Where possible, offer alternative export formats or summaries to support interoperability with other systems.
- Privacy and rights:
  - While peatland data is typically geospatial and public, ensure any sensitive locations or restricted sites are handled according to policy.

## Practical considerations for Data Stewards
- Given potential challenges with incomplete user needs and diverse data formats, ensure that:
  - The dataset includes sufficient metadata to interpret results (time range, spatial coverage, sampling cadence, data quality notes).
  - There is a clear plan for updating the time series and re-running analyses, with version control for both data and code.
- Be mindful of resource requirements for large datasets, as the analysis can involve high-dimensional time series and Gibbs sampling iterations.
- Align data sharing with governance policies, including licensing of the code and outputs, and documenting any updates or changes to the processing pipeline.

## References
- Mitchell E.G., Dryden I.L., Fallaize C.J., Andersen R., Bradley A.V., Large D.J. and Sowter A. (2022). Object oriented data analysis of surface motion time series in peatland landscapes. https://doi.org/10.48550/arXiv.2209.14187