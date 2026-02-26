# Dataset Originator

## Overview
- ECN Data Centre (Centre for Ecology and Hydrology) as the dataset originator.
- Dataset Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies (including AFSI, BBSRC, Cyfoeth Naturiol Cymru, Dstl, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, Scottish Natural Heritage).
- Request acknowledgement of data use and sending one reprint of any publication that cites ECN data.

## Protocol
- Standard operating procedures to ensure data comparability across sites.
- Refer to the accompanying ma.pdf for explanations of data collection methods.

## Usage Notes
- Data are hourly summaries derived from 5-second samplings by Automatic Weather Stations (AWS).
- Some sites operate more than one AWS at the same location; AWSNO identifies each unit. When AWSs run concurrently, be aware of AWSNO for correct usage and cross-checks.
- Replacement AWSs indicated by AWSNo; use the accompanying quality information when analyzing data.

## Data Download Structure
- SITECODE: unique code for each ECN Site.
- AWSNO: individual AWS at a location (sites may have multiple AWS; can be concurrent).
- SDATE: sampling date.
- SHOUR: sampling hour.
- FIELDNAME: variable measured.
- VALUE: measured value.

## Supporting Documentation
- ECN_MA_qtext.csv: site managers attach quality-related notes explaining data quality issues.
- Fields in quality notes: SITECODE, AWSNO, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.

## Explanatory Information: Site Codes
- T01 Drayton; coordinates provided; notes indicate two AWSs; remember to note AWSNO when using data.
- T02 Glensaugh; coordinates; two AWSs.
- T03 Hillsborough; coordinates; two AWSs.
- T04 Moor House - Upper Teesdale; coordinates; two AWSs.
- T05 North Wyke; coordinates; two AWSs.
- T06 Rothamsted; coordinates; notes not specified.
- T07 Sourhope; coordinates; two AWSs.
- T08 Wytham; coordinates; two AWSs.
- T09 Alice Holt; coordinates; two AWSs (text includes garbled formatting but indicates multiple AWS).
- T10 Porton Down; coordinates; two AWSs.
- T11 Y Wyddfa - Snowdon; coordinates; notes about multiple AWSs.
- T12 Cairngorms; notes indicate two AWSs.

Further information about ECN sites is available at:
- https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

## Explanatory Information: Variables (FIELDNAME)
- ALBGRD: Albedo (ground) in Wm-2; separate mention of Albedo Sky (ALBSKY) with units Wm-2.
- DRYTMP: Dry bulb temperature (°C); DRTYMP_RH: dry bulb temp within RH sensor (°C).
- NETRAD: Net Radiation (Wm-2).
- RAIN: Rainfall (total) in mm.
- RH: Relative Humidity (%).
- SOLAR: Solar Radiation (Wm-2).
- STMP10: Soil temperature at 10 cm (°C); STMP30: Soil temperature at 30 cm (°C).
- SURWET: Surface wetness (minutes within the hour).
- SWATER: Soil moisture - gypsum block (units of bars).
- SWATER_T: Soil moisture - theta probe at 20 cm (%).
- SWATER_T10: Soil moisture - theta probe at 10 cm (%).
- SWATER_VWC: Soil moisture content at 20 cm (volumetric water content, dimensionless).
- WDIR: Wind direction (degrees).
- WETTMP: Wet bulb temperature (°C).
- WSPEED: Wind speed (m s-1).

Note: Some variables have multiple descriptors or units as indicated in the data documentation.