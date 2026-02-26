# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - ECN data consist of hourly summaries derived from 5-second samplings taken by Automatic Weather Stations (AWS) across multiple sites.
  - Some sites have had concurrent AWS installations for cross-checking; AWSNo identifies individual sensors when multiple are present.
  - Data cover multiple ECN sites (T01–T12) and a range of environmental variables; accompanying quality and site-specific notes are provided.

- Dataset Ownership and Citation
  - Owned/managed by the UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
  - Users are asked to acknowledge data use and to send one reprint of any publication citing ECN data.

- Protocol and Data Quality
  - Standard operating procedures ensure data comparability across sites; refer to the accompanying ma.pdf for data collection methods.
  - Use the provided quality information to assess data suitability; ECNMA_qtext.csv contains site-specific quality notes.

- Data Structure and Content
  - Data Download fields:
    - SITECODE (site code), AWSNO (individual AWS at a site), SDATE (sampling date), SHOUR (sampling hour), FIELDNAME (variable), VALUE (measured value).
  - ECN_MA_qtext.csv provides qualitative notes on data quality for specific site/AWS/variable combinations, with date ranges and ongoing status.

- Site Codes and Notes
  - T01–T12 sites with names, coordinates, and notes (e.g., many sites have two AWS units; note the AWSNO when using data).
  - Example sites include Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms.
  - Site notes emphasize concurrent AWS and the need to reference AWSNO for data integrity.

- Variables Measured (FIELDNAME)
  - Albedo (ground and sky), Dry bulb temperature (various averages), Net Radiation, Rainfall, Relative Humidity, Solar Radiation, Soil temperature (10 cm, 30 cm), Surface wetness, Soil moisture (gypsum block, theta probe at 20 cm and 10 cm, VWC), Wind direction, Wet-bulb temperature, Wind speed.
  - Units and descriptions are provided for each variable (e.g., °C for temperature, Wm-2 for radiation, mm for rainfall, % for RH, etc.).

- Access and Catalogue Information
  - Additional information about ECN sites and datasets available at the ECN catalogue link: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

- Contact
  - For dataset inquiries: ECN Data Centre (ecn@ceh.ac.uk)