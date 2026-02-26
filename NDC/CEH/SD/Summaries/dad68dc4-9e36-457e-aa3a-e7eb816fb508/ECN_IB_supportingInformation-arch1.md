Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- UK Environmental Change Network (ECN) butterfly monitoring data, sourced from multiple UK partners and coordinated by ECN.
- Data collected via standardized transects across 12 sites, focusing on butterfly presence/abundance over time.
- Site-level and weather-related context provided to support time-series and correlational analyses.

## Data provenance and usage
- Data providers include a consortium of government departments and agencies (e.g., DEFRA, Natural England, NERC, Scottish Government, etc.).
- ECN requests acknowledgement of data use and one reprint of any publication citing ECN data.

## Protocol and collection design
- Butterfly data follow the national Butterfly Monitoring Scheme methodology (Biological Records Centre, CEH).
- Transect details:
  - Up to 15 sections per transect.
  - Weekly walks from 1 April to 29 September each year.
  - Observers record butterflies flying within a defined 5m x 5m x 5m box.
- Environmental conditions:
  - Temperature 13–17°C and at least 60% sunshine for data quality.
- Quality information accompanies data for robust analysis.

## Core data structure and variables
- Primary data fields:
  - SITECODE: ECN site code
  - LCODE: Location ID
  - SDATE: Date of observation
  - SECTION: Transect section ID
  - FIELDNAME: Species code
  - VALUE: Measured value (count/level)
- Additional information available in ECN_IB2.csv:
  - SHOUR, SMINS: Sampling time
  - RECORDER, RECCODE: Recorder details
  - TEMP, SUNPERC: Temperature and sunshine
  - WSPEEDB: Wind speed (Beaufort scale)
  - WEEK: Week number
- Quality information in ECN_IB_qtext.csv (location, field, date range, quality descriptors).

## Site coverage
- Sites coded T01–T12 with names, coordinates, and data date ranges:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms

## Species coverage
- Extensive butterfly species list (codes and both Latin and common names), covering a wide range of UK species (e.g., Aglais urticae, Pieris rapae, Lycaena dispar, Vanessa atalanta, Colias spp., etc.).
- Species list is structured with numerical codes and corresponding Latin and common names.

## Additional information and metadata
- Additional dataset documentation referenced: ECN_IB2.csv (sampling details and metadata) and ECN_IB_qtext.csv (quality notes).
- Quality notes provide guidance on data reliability, temporal applicability, and any continuing issues.

## Practical considerations for analysts
- Strengths:
  - Longitudinal, multi-site butterfly data with standardized methodology.
  - Rich ancillary variables (weather, timing, recorder) enabling robust correlations and predictive modeling.
  - Metadata support via accompanying quality files to assess data reliability.
- Challenges to anticipate:
  - Local-scale data gaps or site-specific differences across years.
  - Data accessibility and integration with other datasets may require navigating multiple files (ECN_IB2.csv, ECN_IB_qtext.csv).
  - Ensuring consistent interpretation of FIELDNAME codes (species) across years and sites.
- Potential analyses:
  - Temporal trends in species abundance and phenology.
  - Associations between butterfly counts and weather variables (TEMP, SUNPERC, WSPEEDB).
  - Spatial comparisons across sites and grouping by habitat types.
  - Data quality checks using the provided quality metadata before modeling.