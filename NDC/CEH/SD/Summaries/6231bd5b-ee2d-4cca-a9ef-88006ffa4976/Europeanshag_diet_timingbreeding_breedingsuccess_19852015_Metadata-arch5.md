# JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

- The document describes three related datasets focused on European shag phenology and its mismatch with environmental variables, curated by JAE_Keogan.
- Datasets address phenology, diet, and bivariate relationships between shag and prey (sandeel) metrics; each dataset includes year-based temporal data and metadata-ready variables for governance and reuse.

## Dataset 1: JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

- Key variables and concepts
  - year: calendar year
  - laydate, day first egg in nest laid: nest laying timing
  - chicks.fledged (and chicks.fledged.all): number of chicks fledged in the first clutch and across all clutches
  - failedeggsfirst, failedeggsall: counts of failed eggs (up to four per clutch)
  - Mean.Lay: average lay date per year
  - Relative.lay: lay date relative to annual mean lay date (in days)
  - SST.past, SST.present: average February/March sea surface temperature in year −1 and current year
  - pop.size: population size in breeding pairs
  - yearcentre: year centered around the study's average year
- Data governance and quality notes for stewardship
  - Ensure consistent naming and units across fields (e.g., eggs, chicks, SST)
  - Capture and document data provenance, collection methods, and any embargoes or limitations
  - Maintain consistency of relative and centered time metrics to support cross-year comparisons
  - Facilitate updates and notifications when underlying datasets are revised
  - Prepare data for sharing via portals; consider documenting any data transformations or cleaning steps

## Dataset 2: JAE_Keogan_Europeanshag_phenologymismatch_dietdataset

- Key variables and concepts
  - Year: calendar year
  - Date: sample collection date (since Jan 1st)
  - Age: chick or adult sample
  - SST: average February/March SST in the current year
  - yearcentre: year centered around the study average
  - meandate: average date of sample collection per year
  - datediff: sample collection date centered around the annual mean
  - SE1:SE0_proportion: proportion of 1+ sandeels relative to all sandeels in the sample
  - logitSE1:SE0: logit-transformed proportion (for statistical modeling)
- Data governance and quality notes for stewardship
  - Ensure clear documentation of sample collection methods, age classification, and sequencing
  - Maintain accurate date handling (meandate, datediff) and consistent SST values
  - Record the transformation steps (logit) and preserve original proportions
  - Define data access rules, potential embargoes, and permissions for sharing diet-related data
  - Facilitate interoperability with the shag dataset by aligning naming and units where appropriate

## Dataset 3: JAE_Keogan_Europeanshag_phenologymismatch_bivariatedataset

- Key variables and concepts
  - Year: calendar year
  - Species: shag or sandeel
  - chicks.fledged: number of shag chicks fledged
  - failedeggs: number of potential failed eggs
  - sandeelproportion: proportion of 1+ sandeels relative to all sandeels in the sample
  - dayofyear: for shag (lay date) or for sandeel (sample collection date)
  - Mean.Lay: average lay date in each year
  - Relative: day of year centered around the average lay date (either in-shag lay date or sample date context)
- Data governance and quality notes for stewardship
  - Align cross-dataset variable definitions to enable integrated analyses (e.g., dayofyear, relative)
  - Document species-specific measurements and any cross-species data merging rules
  - Ensure metadata describe sampling contexts for both shag and sandeel data
  - Manage data access and licensing for bivariate analyses, including any restrictions on combining species data
  - Implement quality checks for consistency between annual summaries (Mean.Lay, Relative) and raw observations

## Cross-cutting Data Stewardship Considerations

- Metadata and discoverability
  - Provide comprehensive metadata for each dataset, including variable definitions, units, data collection methods, and processing steps
  - Use consistent variable naming conventions and versioning to support discovery and reuse
- Data quality and provenance
  - Implement quality assurance steps to verify completeness, accuracy, and internal consistency across all three datasets
  - Track data provenance to allow reproducibility of results and transformations
- Access, sharing, and governance
  - Clarify data access controls, embargo periods, and licensing suitable for data portals and wider reuse
  - Prepare datasets for upload to data portals with proper cataloging and documentation
- Interoperability and usability
  - Align key fields (e.g., year, dayofyear, Mean.Lay, Relative) to facilitate cross-dataset analyses
  - Provide easy-to-use formats and clear mapping between variables across datasets
- Documentation of transformations
  - Record any cleaning, normalization, or feature engineering performed (e.g., centering year, logit transformation)
  - Include notes on handling missing data and potential biases in sampling or measurements

- Overall aim alignment
  - Ensure the datasets support understanding of phenology mismatch, diet composition, and predator-prey dynamics, while remaining well-governed, up-to-date, and readily discoverable by data users.