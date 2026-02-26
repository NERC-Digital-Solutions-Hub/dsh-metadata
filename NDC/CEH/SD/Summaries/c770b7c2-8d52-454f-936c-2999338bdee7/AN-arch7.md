# AN Protocol ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

## Overview
- Purpose: detect and define changes in periodic mean atmospheric nitrogen dioxide (NO2) concentrations, with emphasis on urban sources and health/ecosystem effects.
- NO2 is measured as the key pollutant from NOx sources (traffic, power, industry); diffusion tubes provide a low-cost, passive method suitable for long-term monitoring.
- Scope: current method uses passive diffusion tubes; extension to other pollutants is under consideration but currently not implemented due to reliability concerns.

## Data collection design and spatial deployment
- Sampling approach: three diffusion tubes per site (experimental) and three blanks per site for quality control.
- Deployment height and placement: mounted on posts or poles at 1.5 m above ground; if a meteorological enclosure exists, placement is within it or nearby.
- Location and site identifiers: sites are coded (e.g., Site ID like Moor House) with a unique ECN site code and location code to differentiate sampling points.
- Monitoring cadence: sampling occurs every two weeks (fortnightly) with tubes deployed for the full 14-day period.

## Sample handling, labeling, and field procedures
- Tube handling: prior to deployment, tubes are prepared and labeled; three blank tubes accompany each set and are not exposed.
- Label schema: ECN Measurement Code (AN), ECN Site ID Number, Location Code, tube code (E1–E3 for exposed tubes; B1–B3 for blanks), and collection date.
- Field records: detailed recording forms are used; data are later transferred to the ECN database with a unique reference for each sample.

## Analytical procedure and data products
- Lab analysis: absorbent in diffusion tubes is chemically analyzed to obtain total NO2 absorption for the sampling period.
- Calculation: NO2 concentration over the sampling period is derived from absorbed nitrite, tube geometry, and exposure duration; results are reported as NO2 concentration (ppb) and mass (µg) for quality checks.
- Analysis reagents: nitrite-based colorimetric method using sulphanilamide and N-1-naphthylethylene-diamine dihydrochloride (NEDA); absorbance read at 542 nm.
- Quality controls: utilize three blanks to account for background; samples are processed with fresh reagents and strict hygiene to prevent contamination.

## Data specifications, metadata, and transfer
- Core measurement and dataset structure: core measurement code “AN” (atmospheric chemistry – nitrogen dioxide) with standardized fields for spatial and temporal tagging.
- Required dataset fields (core identifiers):
  - Site Identification Code (unique site)
  - Core Measurement Code (AN)
  - Location Code (sampling point within site)
  - Sampling Date/Time (and, if applicable, GMT 24-h clock)
  - Tube Code (E1, E2, E3 or B1, B2, B3)
  - Weights or calculated NO2 values (µg, with 3 significant figures)
- Time and data granularity: fortnightly measurements with precise timing to the minute where required; expects coordination with the ECNCCU data transfer documentation.
- Data transfer: results and metadata are transferred to the ECN database; standard Site Managers’ extranet documents govern dataset formats and conventions.

## Equipment and field/lab considerations (summary)
- Equipment: diffusion tubes (plastic), stainless steel mesh discs, colored/clear caps; prepared in a standardized workflow.
- Field handling: tubes are deployed vertically with open ends downward; collected after two weeks; tubes and blanks handled with care to avoid contamination.
- Safety and handling notes: operator gloves required; laboratory analysis follows established reagent preparation and storage guidelines; samples kept refrigerated during the sampling period and prior to analysis.

## GIS-relevant takeaways for data products
- Provides spatially distributed NO2 measurements suitable for map-based visualization of urban exposure patterns.
- Data structure supports linking measurements to site geometry, timing, and replicate tubes, enabling spatial QA and uncertainty assessment.
- Replication (three tubes per site plus blanks) supports data quality and calibration when aggregating to site-level NO2 estimates.
- Metadata conventions (site code, location code, sampling date/time, tube codes) facilitate integration with other environmental datasets and long-term monitoring databases.