# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

- Objective: Report initial results to determine the uptake rate for UKCEH’s ALPHA® passive ammonia samplers in UK climate conditions and to provide a dataset of monthly measurements for four network sites.
- Participating organisations: UKCEH Edinburgh (sampler preparation and analysis), AFBI Hillsborough and Ricardo AEA (site duties).

## UKCEH ALPHA® Sampler Method

- Principle: Passive sampler using a citric acid coated filter to capture NH3; a PTFE membrane protects the filter and allows diffusion of ammonia.
- Exposure setup: Replicate samplers mounted on a shelter on a pole at about 1.5 m above ground; multiple samplers per site to improve reliability.
- Analysis workflow: Exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry after extraction.
- Uptake rate: Calculations use a known uptake rate of 0.003241315 m3 h-1 and the documented exposure duration to convert sampler results to ambient NH3 concentration.
- Data flags: Data flagged to indicate concerns; details provided in the dataset documentation.

## Data collection, processing and calculation

- Exposure schedule: Samplers are exposed in monthly cycles at the beginning of each month.
- Concentration calculation: The average NH3 concentration in air for the exposure period is derived from the measured ammonium concentration on the sampler using the uptake rate and exposure duration.
- Data quality rules:
  - Coefficient of variation (CV) of replicates must be less than 15% for results to be considered representative; such data are flagged as 103.
  - Some data may be above the calibration range but still considered valid if re-measurement/recovery isn’t possible.
  - Missing data or meta-data are marked with a -9999 placeholder.
- Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv containing accepted data values with appropriate data flags; site identifiers and spatial details provided in accompanying pages.

## Dataset contents and interpretation

- Units: Ammonia concentration in air expressed as micrograms of NH3 per cubic metre of air (µg NH3 m-3).
- Primary columns (high level): site name, exposure start date/time, exposure end date/time, ammonia concentration for the exposure period, and a data flag.
- Data status and flags:
  - Data capture and validity indicators (e.g., Valid/Invalid, Verification status).
  - EMEP data status flags (e.g., sampling period duration and data quality notes) explained in the documentation.
  - Less than detection limit flags and related interpretations (e.g., below detection limit, estimated value).
- Metadata and provenance: Data sources and quality notes are tracked; datasets can be linked to the site identifiers and their spatial coordinates.

## Site information and context

- Edinburgh uptake rate OTC
  - Start date: 01/03/2020; End date: ongoing
  - Coordinates: 55.863150, -3.209845
  - Inlet height: 1.5 m
  - Collocated with UKA00128
- Edinburgh uptake rate Auch
  - Start date: 01/03/2020; End date: ongoing
  - Coordinates: 55.792160, -3.242900
  - Inlet height: 1.5 m
  - Collocated with UKA00451
- Edinburgh uptake rate Hills
  - Start date: 01/03/2020; End date: ongoing
  - Coordinates: 54.452500, -6.083340
  - Inlet height: 1.5 m
  - Collocated with UKA00293
- Edinburgh uptake rate Chilbolton
  - Start date: 01/01/2021; End date: ongoing
  - Coordinates: 51.149617, -1.438228
  - Inlet height: 1.5 m
  - Collocated with UKA00614

- The four sites are collocated with distinct UK Air/UK-AIR identifiers and are documented alongside spatial identifiers in the dataset.