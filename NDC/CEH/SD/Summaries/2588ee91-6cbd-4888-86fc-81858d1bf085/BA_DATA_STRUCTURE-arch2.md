# ECN Bat Survey Data Documentation

## Overview
- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk), ecn@ceh.ac.uk
- Dataset Owners: UK Environmental Change Network (ECN) program, sponsored by multiple UK government departments and agencies (list includes AFBI, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NI Environment Agency, SEPA, Scottish Government, and others)
- Purpose: Monitor environmental change using standardized datasets to assess environmental health and policy performance over time; data are intended for cross-site comparability and long-term monitoring
- Acknowledgement: Users should acknowledge ECN data use and send one reprint of any publication citing ECN data

## Data Management and Standards
- Protocols: ECN uses standard operating procedures to ensure data comparability across sites; a separate accompanying PDF explains data collection methods
- Quality and Documentation: Use accompanying quality information (ECN_BA_qtext.csv) to assess data quality; data are cleaned, quality-assured, and transformed as needed
- Outputs and Accessibility: Findings are presented in clear formats (reports, maps, charts); datasets are stored and uploaded to appropriate portals for access

## Data Structure and Main Dataset
- Primary data fields (example structure):
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - TRANSECT: Transect identifier
  - BATLOC_ID: Location where a bat was seen or heard (unique per survey date)
  - FIELDNAME: Variable measured (species codes or habitat measurements)
  - VALUE: Value of the measured variable
  - ACTS: Activity code - bat seen
  - ACTH: Activity code - bat heard
  - ACTF: Activity code - bat feeding buzz heard
- Supporting Documentation:
  - ECN_BA2.csv: Survey conduct details (bat detector type, frequency settings, reference recordings, etc.)
  - ECN_BA3.csv: Habitats observed on transect (habitat type codes)
  - ECN_BA_qtext.csv: Quality notes attached by site managers (text explanations of data quality or circumstances)
- Site Codes (Explanatory Information):
  - T01–T11 with site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, etc.) and geographic coordinates
  - Additional information available at CEH Catalogue link
- Species Codes (Explanatory Information):
  - Codes for bat species (e.g., Bb = Barbastella barbastellus; Pp = Pipistrellus; Nn = Nyctalus noctula; XX = No bats found; UU = Unidentified bat; and others)
- Habitat Codes (Explanatory Information):
  - HAB1, HAB2, HAB3: Primary habitat types recorded near sighting
  - 43 habitat type codes with descriptions (from hedgerows and treelines to built land, water bodies, grasslands, and other land covers)

## Site, Species, and Habitat Codes
- Site Codes: T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Y Wyddfa - Snowdon; coordinates provided
- Species Codes: Comprehensive list mapping short codes to Latin and common names for a wide range of bat species and a no-bat flag
- Habitat Codes: Detailed, enumerated set of 43 habitat types with plain-language descriptions (e.g., hedgerows, treelines, stone walls, various water bodies, broadleaved and coniferous woodlands, grasslands, arable land, built land, and other)

## Usage Notes
- Methodology: Bat detection via bat detectors; transect walks four times per year in four three-week periods; surveys paused in heavy rain or strong winds
- Limitations: The method provides limited information on precise relationships between bat populations and environmental changes; linking ECN results with other monitoring programs can mitigate limitations
- Data Quality: Apply quality notes from ECN_BA_qtext.csv; ensure use of accompanying quality information when analyzing data

## Data Access and Attribution
- Data Download Structure: Records include SITECODE, SDATE, TRANSECT, BATLOC_ID, FIELDNAME, VALUE, ACTS, ACTH, ACTF (with supporting context in ECN_BA2.csv and ECN_BA3.csv)
- Supporting Documentation: ECN_BA2.csv (survey configuration), ECN_BA3.csv (habitat observations), ECN_BA_qtext.csv (quality notes)
- Further Information: Additional site information available at CEH Catalogue and ECN contact for guidance (ecn@ceh.ac.uk)

## Contact and Further Information
- Primary contact: ECN Data Centre, ecn@ceh.ac.uk
- Additional information: ECN Catalogue entry available online; reference to accompanying PDFs and CSVs for data collection details and quality context