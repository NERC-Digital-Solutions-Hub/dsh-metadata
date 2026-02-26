# ECN Data Centre Dataset Description and Usage Notes

- Overview
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
  - Dataset Owners: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies
  - Funders/Contributors: Agri-Food and Biosciences Institute; BBSRC; Cyfoeth Naturiol Cymru; Defence Science & Technology Laboratory; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; NIEA; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage
  - Acknowledgement: please acknowledge use of ECN data; send one reprint of any publication citing ECN data

- Data Collection and Protocol
  - Standardized protocols: ECN has SOPs to ensure data comparability across sites (ma.pdf provides collection details)
  - Data type: hourly summaries from 5-second samplings collected by Automatic Weather Stations (AWS)
  - Multiple AWS: many sites operate more than one AWS at the same location; AWSNO identifies each unit; concurrent operation enables cross-checking
  - Quality information: accompany data with quality metadata; use ECN quality notes when analyzing

- Data Structure and Download
  - Data columns for download: SITECODE (ECN Site), AWSNO (individual AWS), SDATE (sampling date), SHOUR (sampling hour), FIELDNAME (variable measured), VALUE (measured value)
  - Supporting documentation: ECN_MA_qtext.csv (site managers’ text explaining factors affecting data quality)
  - Quality text fields: SITECODE, AWSNO, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION

- Metadata and Documentation
  - Explanatory Site Codes: list of ECN sites (T01–T12) with site names, locations, and notes about AWSNO (e.g., many sites with two AWS units)
  - Example site notes: Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms
  - Additional information: more site details available at ECN site catalog URL

- Variables and Field Names
  - Examples of measured variables (FIELDNAME) and units:
    - ALBGRD Albedo (W m-2) and Albedo Sky (W m-2)
    - DRYTMP Dry bulb temperature (°C) and DRYTMP_RH (within RH sensor) (°C)
    - NETRAD Net Radiation (W m-2)
    - RAIN Rainfall (mm, total)
    - RH Relative Humidity (%)
    - SOLAR Solar Radiation (W m-2)
    - STMP10 Soil temperature at 10 cm (°C)
    - STMP30 Soil temperature at 30 cm (°C)
    - SURWET Surface wetness (minutes in hour)
    - SWATER Soil moisture (gypsum block, bars) and SWATER_T/ SWATER_T10 (theta probe)
    - SWATER_VWC Volumetric water content
    - WDIR Wind direction (degrees)
    - WETTMP Wet bulb temperature (°C)
    - WSPEED Wind speed (m s-1)
  - Note: field names and units are standardized across sites to enable cross-site comparisons

- Access, Usage, and Documentation Links
  - Data access format: SITECODE, AWSNO, SDATE, SHOUR, FIELDNAME, VALUE
  - Quality metadata: ECN_MA_qtext.csv provides site-specific quality notes
  - Site information: ECN site catalog and explanatory materials available online
  - Reuse and citation: acknowledge ECN data usage and consider sending a reprint of publications citing ECN data

- Monitoring and Data Use Aims (Analysts Perspective)
  - Standardized, comparable data across sites to assess environmental health and policy performance over time
  - Data verification, quality assurance, cleaning, and transformation to produce consistent outputs
  - Clear presentation of results via reports, maps, and charts
  - Datasets stored and uploaded to appropriate data portals for broader access

- Particular Challenges for ECN Data Users
  - Increasing data value by integrating ECN datasets with additional relevant data (avoiding single-use analyses)
  - Enabling access to the underlying data used to generate published outputs for transparency and reuse

- How this dataset supports environmental monitoring
  - Provides hourly meteorological and environmental measurements from multiple AWS units across UK sites
  - Facilitates cross-site comparisons and long-term trend analysis through standardized protocols and documentation
  - Supports validation and calibration efforts by enabling cross-checks between concurrently operated AWS units