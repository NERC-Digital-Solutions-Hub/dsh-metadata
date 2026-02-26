# ECN Macrolepidoptera dataset

- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
- Dataset Owners/Sponsors: UK Environmental Change Network (ECN) programme; sponsored by a consortium of UK government departments and agencies including AFBI, BBSRC, NRW, DSTL, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, and others
- Usage acknowledgement: ECN requests acknowledgement of data use and sending one reprint of any publication citing the data
- Protocol and scope: Macrolepidoptera detected with a standard light trap; Rothamsted Insect Survey methodology; data recorded nightly
- Metadata guidance: Use the accompanying quality information when using the data

## Data structure and content

- Data structure (Table 1 overview):
  - SITECODE: site code
  - LCODE: location code (usually 1, since one moth trap per site)
  - SDATE: sampling date (dd-mmm-yyyy)
  - FIELDNAME: either a quality code or a species code
  - VALUE: if FIELDNAME is a quality code, the detailed quality code; if FIELDNAME is a species code, the observed count
- Sites included (example entries):
  - T01 to T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Cairngorms) and their coordinates
  - Observation date ranges spanning 1992–2012 (varies by site)
- Taxonomy and codes (Table 3a and 3b):
  - Quality codes: Q1–Q8 (and 999 for unusual events)
  - Species codes: extensive list linking numeric codes to Latin and common names (e.g., 100 = Furcula bicuspis; many hundreds of entries with both Latin and common names)
- Quality and data integrity:
  - Quality codes capture data quality, sample handling, and environmental conditions
  - Supplementary quality codes and notes exist (Table 4)
- Supplemental data files:
  - ECN_IM2.csv: period over which moth traps were set (e.g., PERIOD = 1 for daily empties)
  - ECN_IM_qtext.csv: quality text for unusual or additional notes

## Quality, codes, and documentation

- Quality codes (Table 4):
  - Range 100–509 and beyond cover information gaps, sample handling issues, environmental factors, laboratory issues, etc.
  - 999 indicates an unusual event with accompanying text in quality information
- Site-level quality coding:
  - ECN site managers assign codes from a standard list to indicate data quality and procedural factors
- Supplemental quality information:
  - Additional context for absences or anomalies is provided in ECN_IM_qtext.csv

## Data governance, access, and attribution

- Ownership and stewardship:
  - ECN Data Centre maintains the dataset; data are shared under ECN governance
- Attribution and publication:
  - Researchers must acknowledge ECN data use and provide one reprint of any publication citing the data
- Access and use notes:
  - Data are accompanied by detailed metadata, quality codes, and crosswalks between codes and observations
  - Supplemental files provide trap-period information and quality notes to support data interpretation
- Data portals and discoverability:
  - Additional site information and data context available via ECN catalogues and the ECN data portal

## Data management and updates

- Data lifecycle:
  - Historical data spanning 1992–2012 across multiple ECN sites
  - Protocol is stable (standard light trap; Rothamsted Insect Survey methodology)
- Data updates:
  - Supplemental files document trap open periods and text quality notes; ongoing data ingestion should align with these structures
- Documentation and transparency:
  - Rich code dictionaries (quality codes and species codes) improve interpretability and interoperability with other datasets

## Considerations for Data Stewards (challenges and mitigations)

- Incomplete user needs:
  - Provide clear data dictionaries, usage notes, and example queries to facilitate discovery and reuse
- Timeliness of data:
  - Maintain a schedule for data updates and ensure timely propagation to data portals; document any embargoes or delays
- Standards and metadata quality:
  - Maintain controlled vocabularies for site, location codes, and species codes; align with broader metadata standards where possible
- Interoperability and formats:
  - Preserve the detailed code tables; provide crosswalks to common taxonomies and data schemas to support integration with other datasets
- Handling large, multi-year data:
  - Implement robust indexing by site, date, and species; consider data partitioning and scalable storage strategies
- Legacy/bespoke systems:
  - Document data structures and provide migration paths or mappings to more interoperable schemas; preserve original fields while enabling standard queries

## Supplemental information

- Supplemental files:
  - ECN_IM2.csv: trap-period data
  - ECN_IM_qtext.csv: quality contextual text
- Data usage notes:
  - The dataset’s comprehensive quality and species coding, alongside site metadata, supports detailed ecological analyses and reproducibility of results