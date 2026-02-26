# UK Environmental Change Network (ECN) meteorology data: 1992-2012

## Overview
- Originator: ECN Data Centre (Centre for Ecology and Hydrology); ECN dataset funded by a consortium of UK government departments and agencies.
- Owners and purpose: ECN programme for understanding environmental change; data used to support research and monitoring, with acknowledgement and publication requests.
- Data scope: Hourly summaries derived from 5-second samplings taken by Automatic Weather Stations (AWS) across ECN sites, covering 1992–2012.
- Reuse guidance: Acknowledge data use; provide one reprint of any publication citing the data; protocol reference MA.pdf for re-use details.
- Documentation and quality: Use accompanying quality information; protocol and metadata available via the EIDC Hub data holdings page.

## Data Content and Structure
- Data source and sampling: Hourly aggregates from 5-second AWS measurements; many sites used more than one AWS in the same location to enable cross-checking (replacement AWSs indicated by AWSNo).
- Site coverage and temporal details: 12 ECN sites (T01–T12) with AWS1 and/or AWS2 operations and distinct date ranges per AWS (e.g., AWS1 and AWS2 periods vary by site; some sites have overlapping data from concurrent AWS units).
- Site list (examples):
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
  - T11 Snowdon (Y Wyddfa)
  - T12 Cairngorms
- Data model and fields (highlights):
  - Site codes and names; AWS identifiers; date ranges for sampling; sampling hours.
  - Meteorological variables collected (examples): Albedo (ground/sky), Dry/Wet bulb temperatures, Net Radiation, Rainfall, Relative Humidity, Solar Radiation, Soil Temperature (10 cm, 30 cm), Soil Moisture (gypsum block, theta probe at 10 cm and 20 cm), Surface Wetness, Wind Direction and Wind Speed, among others.
  - Data representation: Structured tables with coded fields for site, AWS, sampling date/time, field names, values, and units.
- Data quality and metadata:
  - QA/QC information is provided and should be consulted when using the data.
  - The dataset includes a detailed field taxonomy and units to support consistent interpretation.

## Usage Guidance for Data Stewards
- Provenance and traceability: Track AWSNo to distinguish concurrent/replacement sensors and ensure correct time-series stitching.
- Quality assurance: Always consult accompanying quality information and cross-check data across concurrent AWS units where applicable.
- Documentation: Reference the Protocol MA.pdf for reuse rules and processing steps; ensure proper acknowledgement and citation in any dissemination.
- Data integration: When combining data across sites or AWSs, align on AWSNo and site code, and account for potential gaps during AWS replacements.
- Discovery and sharing: Maintain metadata records that capture site, AWS, date ranges, and variable definitions to facilitate reuse and discovery by data users.

## Limitations and Considerations
- Data continuity issues may arise from AWS replacements and concurrent operation; careful handling of AWSNo is required.
- The dataset spans 1992–2012, and some sites have discontinuities or gaps between AWS1 and AWS2 periods.
- As with older, multi-system environmental datasets, expect varying data completeness and metadata richness across sites and sensors.