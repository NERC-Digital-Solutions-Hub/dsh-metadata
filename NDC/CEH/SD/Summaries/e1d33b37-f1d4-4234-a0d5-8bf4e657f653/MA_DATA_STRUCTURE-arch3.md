# UK Environmental Change Network (ECN) meteorology data: 1992-2012

## Overview
- A dataset of meteorology observations from the UK Environmental Change Network (ECN) covering 1992–2012.
- Data are hourly summaries derived from 5-second samplings by Automatic Weather Stations (AWS) across multiple ECN sites.
- Supports understanding of environmental change and provides a basis for monitoring framework development, data governance, and policy evaluation.

## Dataset origin and ownership
- Originator: ECN Data Centre (website: data.ecn.ac.uk; contact: ecn@ceh.ac.uk), Centre for Ecology and Hydrology.
- Owners: ECN programme sponsored by a consortium of UK government departments/agencies funding site monitoring or network coordination (e.g., Defra, Environment Agency, Natural England, NERC councils, devolved administrations, etc.).
- Acknowledgement: Users are asked to acknowledge data usage and provide one reprint of any publication citing the data.

## Scope, collection, and site details
- Data type: hourly summaries of measurements from AWS, each capturing high-frequency 5-second samples (with cross-checks where multiple AWSs operated at the same site).
- Site coverage: 12 named ECN sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) with precise coordinates and operation periods.
- AWS configuration: some sites operated more than one AWS over time (AWS1, AWS2), with replacement units noted by AWSNo; important for data interpretation and cross-checking.
- Time periods: individual AWSs have period ranges (e.g., AWS1: start–end dates; AWS2: start–end dates), with overall coverage 1992–2012.
- Data quality: accompanying quality information is provided and should be consulted to ensure data suitability.

## Data structure and metadata
- Data organization references:
  - Site codes and site names, with date ranges for each site's AWS installations.
  - AWS identifiers (AWS numbers) and their active periods per site.
  - Field definitions and units for environmental measurements.
- Example fields (selected):
  - ALBGRD: Albedo Ground (average) – W m^-2
  - ALBSKY: Albedo Sky (average) – W m^-2
  - DRYTMP: Dry bulb temperature (average) – °C
  - NETRAD: Net Radiation (average) – W m^-2
  - RAIN: Rainfall (total) – m
  - RH: Relative Humidity (average) – %
  - SOLAR: Solar Radiation (average) – W m^-2
  - STMP10/STMP30: Soil temperature at 10 cm / 30 cm (average) – °C
  - SURWET: Surface wetness (minutes per hour) – minutes
  - SWATER/SWATER_T/SWATER_V: Soil moisture measurements (various methods) – units vary
  - WDIR: Wind direction (average) – degrees
  - WSPEED: Wind speed (average) – m s^-1
  - WETTMP: Wet bulb temperature (average) – °C
- Data tables and naming conventions:
  - ODE: Site (Site), ODE, N0: AWS details, E fields related to sampling date and time, FIELD definitions, and EVAL values for measurements.
  - Site Codes: include site name, geographic coordinates, and AWS active date ranges.
- The dataset emphasizes the need to use the accompanying quality information and to be aware of AWS numbering when leveraging concurrent sensors.

## Protocol, access, and usage guidance
- Protocol reference: MA.pdf (document detailing data reuse) available with the dataset.
- Access notes:
  - Documentation for re-use is provided in the ECN data holdings (EIDC Hub data holdings page).
  - Users should consult the protocol and quality information before analysis.
- Usage and attribution:
  - Acknowledge the ECN data and, where applicable, share resulting outputs or reprints as requested.
  - Ensure proper interpretation of AWSNo when multiple AWS units exist at a site.

## Relevance for Monitoring Frameworks Authors
- Demonstrates practical data governance needs: metadata completeness, data provenance, and consistent data sharing practices.
- Highlights challenges common to monitoring frameworks: data gaps, access constraints, silo effects, and the burden of transforming varying data formats into usable inputs.
- Provides a rich, multi-site, long-term data resource suitable for testing indicators, dashboards, and policy-scrutiny mechanisms related to environmental change.
- Underlines importance of:
  - Maintaining quality information alongside raw data.
  - Clear documentation of data structure, units, and sensor configurations.
  - Transparent acknowledgement and data-sharing practices to support reproducible monitoring and decision-making.