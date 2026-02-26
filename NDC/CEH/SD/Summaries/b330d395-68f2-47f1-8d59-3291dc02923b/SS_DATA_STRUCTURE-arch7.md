# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- A soil solution chemistry dataset from the ECN (Environmental Change Network) with standardized procedures to enable cross-site comparability.
- Designed for GIS-based map visualisations and spatial analysis to support understanding environmental change.

## Data provenance and ownership
- Dataset originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset owners: The UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies (e.g., Defra, NE, NERC, EA, NHS, etc.).
- Usage acknowledgement: Please acknowledge the use of ECN data and send one reprint of any publication citing the dataset.

## Protocol and data quality
- Standard operating procedures ensure data comparability across sites (refer to the accompanying ss.pdf for collection details).
- Usage notes:
  - Suction samplers measure soil solution chemistry; samples collected fortnightly.
  - If a sampler is replaced, a new replicate ID (RID) is recorded.
  - If insufficient sample is collected, samples for the sampling day may be bulked (RID XXS for shallow, XXD for deep).
  - A standard QC solution is analyzed with field samples; QC data are available and should be used for quality assessment.

## Data structure and download
- Primary data fields in the main download:
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - RID: Replicate ID
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation files:
  - ECN_SS2.csv: Lab analysis information
  - ECN_SS_qtext.csv: Quality text associated with site managers’ quality codes
  - ECN_QC1.csv and ECN_QC2.csv: Quality control data and additional lab analysis details
- Explanatory information:
  - FIELDNAME values include a wide range of chemical and physical parameters (e.g., ALKY, ALUMINIUM, CALCIUM, CHLORIDE, CONDY, DOC, pH, NO3N, PO4P, etc.) with respective units.
  - Q1–Q5: Quality code fields associated with each measurement

## Quality codes
- Quality codes cover data loss, sampling issues, laboratory issues, and unusual events. Examples include:
  - 100: No information available
  - 101–111, 113, 115: Various sampling issues (e.g., no sample, lost sample, debris)
  - 200–223: Adverse weather, non-standard sampling times/dates
  - 501–508, 511: Laboratory-related issues (e.g., no sample, contamination, filter deposits)
  - 999: Unusual event (see accompanying quality text)
- The quality codes are accompanied by descriptive text in ECN_SS_qtext.csv for detailed context.

## Site codes and locations
- Sites labeled T01 to T12 with corresponding site names and coordinates:
  - T01: Drayton
  - T02: Glensaugh
  - T03: Hillsborough
  - T04: Moor House - Upper Teesdale
  - T05: North Wyke
  - T06: Rothamsted
  - T07: Sourhope
  - T08: Wytham
  - T09: Alice Holt
  - T10: Porton Down
  - T11: Y Wyddfa - Snowdon
  - T12: Cairngorms
- Coordinates are provided for mapping (degrees, minutes, seconds format) and further site information is available via the ECN catalogue link.

## Explanatory information and variables
- FIELDNAME definitions and units:
  - Examples include ALKY (Alkalinity, mg/L), CALCIUM (mg/L), CHLORIDE (mg/L), CONDY (conductivity, µS/cm), DOC (mg/L), pH, NO3N (mg/L), PO4P (mg/L), etc., plus other parameters (e.g., VOLUME, PRESSURE-related fields, QC-related fields).
- Units are specified per variable; QC fields (Q1–Q5) indicate data quality per observation.

## Usage and GIS integration guidance
- Join main data (SITECODE, SDATE, RID, FIELDNAME, VALUE) with site coordinates for mapping and spatial analysis.
- Use accompanying QC information (ECN_SS_qtext.csv and QC CSVs) to assess data reliability before visualization or analysis.
- Be mindful of bulked samples (RID XXS/XXD) and replaced samplers (new RID) when aggregating data or calculating trends.
- Acknowledge ECN data usage in publications and consult the accompanying documentation for lab analysis details and quality contexts.

## Additional notes
- Full site context and deeper metadata available at the ECN catalogue link provided in the dataset.
- The dataset emphasizes data comparability across sites, standardization, and quality control to support robust GIS-driven environmental change analysis.