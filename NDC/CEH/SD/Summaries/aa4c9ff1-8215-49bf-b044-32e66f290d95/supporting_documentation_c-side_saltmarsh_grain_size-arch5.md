# Grain size distributions from 459 soil samples collected from across UK saltmarshes between 2018 - 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC (NE/R010846/1).
- Dataset purpose: Grain size distributions for 459 soil samples collected from UK saltmarshes, 2018–2021.
- Relevance for Data Stewards: Provides a well-documented, standardized sediment property dataset suitable for discovery, reuse, and integration with related soil and environmental data.

## Dataset details
- Data resource: Grain size distributions from 459 soil samples across UK saltmarshes (2018–2021).
- Primary data file: C_SIDE_saltmarsh_grain_size.csv
  - Core metadata: Core_ID (text), Location (saltmarsh name, text), Core_depth_cm (numeric), Core_mid-depth_cm (numeric).
  - Grain size variables: Grain_size_1 to Grain_size_100 (numeric), representing grain size distributions from 0.02244 to 2000 µm.
  - Grain size mapping: Each Grain_size_N corresponds to a specific grain size in micrometres as listed in the dataset (bin centers from 0.02244 µm up to 1782.50 µm).
- Sampling scope: 459 samples collected from across UK saltmarshes to represent diverse saltmarsh habitats.
- Observations: Data capture includes grain size distribution across multiple depth sub-samples per core where applicable.

## Location and sampling details
- Geographic coverage: United Kingdom coastal saltmarshes.
- Spatial extent: Site coordinates provided as decimal degrees (WGS84); includes a bounding set of coordinates that defines UK-wide coverage.
- Site descriptions: All sites located in environmentally similar regional contexts to enable comparable grain size data; selected to represent UK saltmarsh diversity.

## Methods and quality assurance
- Grain size analysis method: Malvern Laser Granulometer (laser diffraction).
- Pre-treatment procedures: Air-dried samples; break up with pestle and mortar; sieve through 0.5 mm to remove large debris; dissolve in 10 ml of 30% H2O2, with stirs and heating steps up to ~50°C to enhance dispersion before measurement.
- Calibration: Malvern Laser Granulometer calibrated with a 0.152–0.422 mm standard sand.
- Quality control: Lab equipment calibrated according to University of York laboratory practices.
- Statistical treatment: Not specified (NA) in the metadata; statistical analysis details are not provided.
- Data check/verification: Routine calibration of laboratory equipment reported; no further statistical QA described.

## Metadata, standards, and data format
- Data format: CSV (.csv).
- Metadata conventions: Includes Core_ID, Location, Core_depth_cm, Core_mid-depth_cm, and 100 grain-size distribution columns.
- Units: Grain sizes in micrometres (µm); depth measurements in centimetres.
- Data notes: "NA indicates no data in cells" reflects some potential missing values in the dataset.
- Data provenance: Tied to the C-SIDE project; dataset description explicitly mentions calibration and QA steps.

## Data governance, access, and updates
- Governance: Dataset described within the C-SIDE project framework; alignment with data sharing expectations and update mechanisms.
- Sharing and updates: Statements indicate systems in place to respect sharing limitations and to manage dataset updates.
- Accessibility: Core metadata and grain size distribution data are provided in a structured CSV format suitable for discovery, integration, and reuse.

## Use cases and considerations for Data Stewards
- Reuse potential: Cross-site comparisons of sediment grain size distributions; integration with related soil carbon, hydrology, or coastal ecology datasets; supports analyses of sediment transport and deposition in saltmarsh environments.
- Standards alignment: The dataset follows a consistent grain size bin approach and uses a common coordinate system (WGS84), aiding interoperability.
- Documentation needs: Consider expanding statistical treatment details and data validation steps to improve interpretability and reuse.
- Quality considerations: Be aware of NA fields and potential minor data-quality notes (e.g., minor inconsistencies in the grain_size labeling due to formatting in the source). Ensure clear mapping of grain_size_N to µm values in any data catalog.
- Governance implications: Ensure updates, provenance, and licensing are clearly recorded in the dataset catalog to support discovery and long-term stewardship.