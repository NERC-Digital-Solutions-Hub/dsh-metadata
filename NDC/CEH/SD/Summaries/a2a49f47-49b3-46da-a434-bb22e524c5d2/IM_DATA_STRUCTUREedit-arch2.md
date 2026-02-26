# Dataset Description - ECN Macrolepidoptera Data (Light Trap)

- Overview
  - Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
  - Dataset Owners: UK Environmental Change Network (ECN) programme funded by multiple UK government departments and agencies
  - Purpose: Provide standardized, comparable Macrolepidoptera (moth) data from ECN sites to monitor environmental health and policy performance over time
  - Acknowledgement: Users should acknowledge use of ECN data and send one reprint of any publication citing the data

- Protocol and Data Quality
  - Standard Operating Procedures: Protocols ensure data comparability across sites (im.pdf accompanies the document)
  - Data Collection Method: Standard light-trap method, Rothamsted Insect Survey protocol
  - Sampling Frequency: Data recorded nightly
  - Supplemental Quality Information: Use accompanying quality information when using the data
  - Quality Assurance: Site managers assign predefined quality codes; unusual events may be documented with text (see ECN_IM_qtext.csv)

- Data Download and Structure
  - Core Data Codes: Each record uses
    - SITECODE: Unique ECN Site code
    - LCODE: Location identifier within site
    - SDATE: Sampling date
    - FIELDNAME: Variable measured (e.g., quality codes Q1–Q8 or species codes)
    - VALUE: Measured value
  - Supporting Documentation:
    - ECN_IM2.csv: Details the trap period (SPERIOD_D) and timing (FROMDATE, SDATE, YEAR, WEEK); most traps were emptied daily (PERIOD = 1)
    - ECN_IM_qtext.csv: Quality text accompanying quality codes; includes date ranges, ongoing status, and descriptions; uses quality code 999 for unusual events
  - Data Portals: Datasets are stored and uploaded to appropriate ECN portals

- Site Codes and Locations
  - T01 Drayton (52°11'37.95"N, 1°45'51.95"W)
  - T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W)
  - T03 Hillsborough (54°27'12.24"N, 6°4'41.26"W)
  - T04 Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W)
  - T05 North Wyke (50°46'54.96"N, 3°55'4.10"W)
  - T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W)
  - T07 Sourhope (55°29'23.47"N, 2°12'43.32"W)
  - T08 Wytham (51°46'52.86"N, 1°20'9.81"W)
  - T09 Alice Holt (51°9'16.46"N, 0°51'47.58"W)
  - T10 Porton Down (51°7'37.83"N, 1°38'23.46"W)
  - T12 Cairngorms (57°6'58.84"N, 3°49'46.98"W)
  - Additional site metadata and broader ECN site information are available in the provided documentation

- Variables and Data Coding
  - FIELDNAME: Includes quality code fields (Q1–Q8) and a long list of coded species (e.g., numerical codes correspond to common moth species names)
  - Example: Several hundred species and quality code mappings are defined (e.g., 100 = Alder Kitten, many codes for moth species), with a detailed mapping in the Explanatory Information sections
  - Note on complex mappings: Some codes represent species groups or pairs (e.g., 3392 Mesapamea secalis/didyma; 3394 Amphipyra berbera berbera) that may be merged or split in records depending on dissection

- Quality Codes
  - Quality Codes: A set of codes describing data quality issues or conditions (e.g., 100 = No information available; 101 = No sample/reading taken; numerous codes for debris, weather, equipment, habitat disturbance, etc.)
  - Unusual Events: 999 indicates an unusual event; accompanying ECN_IM_qtext.csv provides text descriptions

- Special Notes and Considerations
  - Some codes require expert identification; certain species pairs cannot be separated without dissection
  - Cross-referencing: The same site/species entries may appear under different codes or be consolidated in later records (e.g., Amphipyra berbera berbera also appearing as 2507)

- Practical Use for Analysts
  - Time-series and spatially comparative analysis of moth communities across multiple ECN sites
  - Evaluation of environmental change indicators via standardized night-time light-trap data
  - Data quality awareness through structured quality codes and accompanying text notes
  - Ability to link dataset outputs to standard formats (reports, maps, charts) and to upload and store derived datasets in appropriate portals

- Publication and Data Use
  - Acknowledge ECN data use in publications
  - Provide one reprint of any work citing ECN data