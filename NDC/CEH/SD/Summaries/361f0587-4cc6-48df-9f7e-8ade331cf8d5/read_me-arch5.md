# Data collected by Vicky Bowskill (https://orcid.org/0000-0003-0293-327X) as part of PhD research with School of Environment, Earth and Ecosystem Sciences, Faculty of Science, Technology, Engineering and Mathematics, The Open University, Walton Hall, Milton Keynes, MK7 6AA

## Overview
- PhD research dataset on nutritive characteristics of floodplain meadow hay in central England.
- Funded by NERC CENTA2 grant NE/S007350/1.
- Data file: 1 CSV containing measured nutritive variables; linked publications provide full method description.
- Publication references: two DOIs provided (Biocon 2023 and OU repository).

## Dataset Details
- File format: 1 .csv
- Structure: columns represent variables; rows represent records.
- Sampling design:
  - Sites: 3 (note discrepancy in document mentioning 4 sites).
  - Years: 2.
  - Samples per site: 6 (bulked pairwise in year 2 to reduce costs).
  - Replicates per sample: 2; data point is the mean of two replicates.
  - Year 2 samples are bulked to reduce sampling costs.
- Lab methods:
  - Near Infrared Spectroscopy (NIRS) for CP, ME, ADF, NDF.
  - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) for P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn.
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) for I.
- Data labels (examples): GDD (Growing Degree-days), AET (Actual Evapotranspiration), GFratio (Graminoid:Forb ratio), CP, ME, ADF, NDF.
- Units:
  - gm2 (grams per metre square)
  - gkg (grams per kilogram)
  - mgkg (milligrams per kilogram)
  - percent
  - offtake (calculated as (% of yield))
  - Mjkg (MegaJoules per kilogram)

## Data Provenance and Metadata
- Data collector: Vicky Bowskill.
- Context: Nutritive measurements for floodplain meadow hay from central England.
- Documentation:
  - Linked publications provide full method description.
  - Methods described across NIRS, ICP-OES, and ICP-MS analyses.
  - ORCID and institutional affiliation provided for traceability.
- Documentation gaps to note for governance:
  - Explicit data license or usage terms are not stated; governance should capture licensing and access rights.

## Data Quality and Curation Considerations
- Replicate handling: data points are means of two replicates; this should be clearly documented in metadata and data dictionaries.
- Inconsistency to resolve: statement of “4 sites” in the description vs. “Sites: 3” in structure. Requires clarification to ensure dataset integrity.
- Derived variables: offtake calculation method noted; ensure reproducibility by including formula in metadata.
- Metadata completeness: ensure full variable descriptions, unit definitions, and lab methods are captured in a machine-readable data dictionary.

## Data Stewardship and Governance Actions
- Data inventory and normalization:
  - Confirm the exact number of sites (3 vs 4) and reconcile any conflicts in the dataset record.
  - Ensure consistent naming conventions for sites, years, and samples.
- Metadata and documentation:
  - Create or update a comprehensive data dictionary including variable names, abbreviations, units, methods, and processing steps (e.g., averaging replicates).
  - Include provenance details: collection date ranges, site locations, sampling design, and any data transformations.
  - Attach or link licensing information and usage rights; provide citation guidance referencing linked publications and DOIs.
- Data quality controls:
  - Capture measurement uncertainties, detection limits, and QA/QC procedures for NIRS, ICP-OES, and ICP-MS analyses.
  - Flag any data points affected by bulked year-2 samples or potential sampling biases.
- Data storage and discoverability:
  - Store the CSV in an appropriate data repository with a stable DOI or accession number.
  - Ensure connections to linked method descriptions and publications are maintained.
  - Provide a concise metadata record for discovery portals, including authors, affiliation, grant, sampling design, and data access conditions.
- Reuse guidance:
  - Include recommended citation format referencing the DOIs and the Open University/affiliations.
  - Document any restrictions or embargoes if applicable.
- Action items for follow-up:
  - Obtain clarification on site count and update metadata accordingly.
  - Confirm licensing terms and attach to the dataset record.
  - Validate unit consistency across variables and harmonize if needed.