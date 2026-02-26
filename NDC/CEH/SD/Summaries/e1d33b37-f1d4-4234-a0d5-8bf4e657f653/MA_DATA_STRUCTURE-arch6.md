# UK Environmental Change Network (ECN) meteorology data: 1992-2012

## Dataset provenance and ownership
- Originator: ECN Data Centre, Centre for Ecology and Hydrology (data.ecn.ac.uk; ecn@ceh.ac.uk)
- Owners: UK ECN programme funded by a consortium of government departments and agencies; list includes DEFRA, Natural England, Environment Agency, NERC, Scottish Government, and others
- Acknowledgement and sharing: Users are asked to acknowledge data use and to send one reprint of any publication citing the data

## Access, reuse, and documentation
- Protocol reference: See the Protocol MA.pdf in the Documents section of the ECN data holdings (EIDC Hub)
- Usage notes: Data are hourly summaries derived from 5-second Automatic Weather Station (AWS) samples; many sites ran more than one AWS in the same location for cross-checks; AWSNo indicates the specific unit, important when multiple AWSs operated concurrently
- Quality and context: Always use the accompanying quality information when using the data

## Data characteristics and scope
- Temporal coverage: Meteorology data from 1992 to 2012
- Spatial coverage: 12 ECN sites across the UK (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms)
- Data type: Hourly summaries derived from high-frequency (5-second) measurements recorded by AWS sensors
- Data structure note: Repositories describe data via a coded schema (Site, AWS, Sampling Date/Hour, Field name, and Value) with accompanying site and field metadata tables

## Site metadata and coverage
- Site codes and names are provided (T01–T12) with:
  - Geographic coordinates
  - AWS installation history and dates (AWS1, AWS2) per site
  - Date ranges for each AWS at a location
- This metadata supports data linking, temporal alignment, and cross-site comparisons

## Variables and units (Fields)
- Example fields and meanings (units indicated):
  - ALBGRD: Albedo Ground (surface albedo average) – W m^-2 (context: reflectance, surface energy)
  - ALBSKY: Albedo Sky (average) – W m^-2
  - DRYTMP: Dry bulb temperature (average) – °C
  - DRTYMP_R: Dry bulb temperature within the RH sensor (average) – °C
  - NETRAD: Net radiation (average) – W m^-2
  - RAIN: Rainfall (total) – m
  - RH: Relative humidity (average) – %
  - SOLAR: Solar Radiation (average) – W m^-2
  - STMP10/STMP30: Soil temperature at 10 cm / 30 cm (average) – °C
  - SURWET: Surface wetness (minutes of the hour the surface was wet) – minutes
  - SWATER: Soil moisture (gypsum block, average) – unknown units (context: soil moisture)
  - SWATER_T: Soil moisture (theta probe at 20 cm, average) – %
  - SWATER_V: Soil moisture (volumetric water content at 20 cm, average) – m^3 m^-3
  - WDIR: Wind direction (average) – degrees
  - WSPEED: Wind speed (average) – m s^-1
  - WETTMP: Wet bulb temperature (average) – °C
- Note: The data schema includes numerous additional field descriptors and technical notes; practitioners should reference the data dictionary in the documentation for precise definitions and units

## Data usage considerations for data support
- Data quality and completeness: Expect variable data availability across sites and years; the dataset emphasizes quality flags corresponding to measurements
- Data integration: When combining datasets from multiple AWS at a single site or across sites, use AWSNo and site metadata to align time stamps and handle overlapping measurements
- Temporal alignment: Base analyses on the hourly summaries, but leverage the original 5-second sampling context for quality checks and anomaly detection
- Documentation and reproducibility: Rely on the Protocol MA.pdf and accompanying metadata tables to reproduce site-specific conditions and sensor configurations

## Practical applications for data-support activities
- Data preparation: Clean and harmonize data across sites and AWS units; handle missing values and quality flags
- Data enrichment: Join hourly meteorological variables with site metadata (coordinates, active periods, AWS versions)
- Dashboard and report development: Create self-serve data products (time series, heatmaps, anomaly reports) using the standardized fields and units
- Stakeholder communication: Provide clear provenance, usage guidelines, and citation requirements to end users
- Data dissemination advocacy: Highlight availability of structured site and field metadata to promote data reuse and cross-site analyses

## Reuse and publication guidance
- Acknowledge ECN data use in publications
- Share one reprint of any publication that cites the ECN meteorology data
- Consult the Protocol MA.pdf for detailed reuse procedures and ensure alignment with the data’s quality information and site-specific constraints