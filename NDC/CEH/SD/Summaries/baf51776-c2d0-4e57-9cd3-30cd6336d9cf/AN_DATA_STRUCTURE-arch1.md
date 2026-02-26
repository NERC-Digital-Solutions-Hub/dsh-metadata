# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk)

## Overview

- The UK Environmental Change Network (ECN) dataset focuses on nitrogen dioxide (NO2) using passive diffusion tubes.
- Tubes are deployed for a two-week period to measure NO2 concentration.
- Data include measurements, deployment metadata, and quality codes to support comparability across sites.
- Site details and variable definitions are provided to aid interpretation and cross-site analyses.

## Dataset Owners and Sponsorship

- The ECN programme is sponsored by a consortium of UK government departments and agencies funding site monitoring or network coordination.
- Member organisations include: Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DSTL; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- Usage acknowledgement: Please credit ECN data and send one reprint of any publication that cites ECN data.

## Protocol and Quality Assurance

- ECN maintains standard operating procedures to ensure data comparability across sites.
- Two-week deployment cycle for NO2 diffusion tubes.
- Quality check with blank tubes that are unexposed on deployment and analyzed with experimental tubes.
- Users should apply accompanying quality information when using the data.

## Data Structure and Files

- Data download fields (core dataset):
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - TUBEID: Tube identifier (E = Experimental; B = Blank)
  - FIELDNAME: Variable measured (see below)
  - VALUE: Measured value
- Supporting Documentation - ECN_AN2.csv
  - DEPDATE: Tube deployment date
  - DEPHOUR/DEPMINS: Deployment time
  - SDATE/SHOUR/SMINS: Sampling date and time
- Supporting Documentation - ECN_AN_qtext.csv
  - Quality notes: site managers assign quality codes to factors affecting data quality; unusual events flagged with code 999 (see ECN_AN_qtext.csv for text)
- Explanatory Site Codes (Site details)
  - T01 to T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) and geographic coordinates
- Variable being measured (FIELDNAME)
  - WEIGHTNO2: Weight of NO2 on the mesh (micrograms)
  - NO2: NO2 concentration (micrograms per cubic meter)
  - NO2PPB: NO2 concentration (ppb)
  - TDIFF: Exposure time (minutes)
  - Q1–Q8: Quality codes (integers)
- Data quality and interpretation
  - Quality codes range from 100 (No information available) to 513 and 999 (Unusual event). Codes cover issues such as sample loss, contamination, equipment problems, environmental interference, and other data quality concerns.

## Site Codes and Variables

- Site codes (T01–T12) map to specific ECN sites with names and coordinates.
- Field names detail what is measured and how it is recorded (NO2 in two units, exposure duration, and per-measurement quality flags).

## Quality Codes (Examples of Meaning)

- 100: No information available - data lost
- 101–189: Various local issues (e.g., no sample, sample loss, contamination, debris, environmental interferences)
- 200–241: Adverse sampling conditions or measurement issues (weather, light, blocking, etc.)
- 501–513: Laboratory or measurement issues (e.g., no sample, loss, contamination, instrument problems)
- 999: Unusual event (see accompanying quality text)

## Usage Notes

- Follow the accompanying quality information to assess data suitability for analyses.
- Be mindful of potential data gaps or quality flags when assembling datasets across sites or time periods.
- Units: NO2 reported as micrograms per cubic meter or converted to ppb where applicable; TDIFF in minutes.

## Supporting Documentation and Access

- ECN_AN2.csv provides deployment and sampling timing details for each tube.
- ECN_AN_qtext.csv contains detailed quality text explanations for quality codes.
- Full site definitions, coordinates, and variable descriptions are provided to facilitate data integration and interpretation.

## Practical Considerations for Analysts

- Data at local scales may have gaps or quality concerns; cross-site standardization and quality flag interpretation are essential.
- Accessing and harmonizing multiple ECN datasets may require navigating varied quality codes and documentation files.
- Acknowledgement and citation of ECN data are encouraged; include a reprint of publications citing the data.