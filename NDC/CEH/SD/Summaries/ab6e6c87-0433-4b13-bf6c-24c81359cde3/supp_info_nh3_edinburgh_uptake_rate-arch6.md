# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

## Overview
- Initial results from a study to determine the uptake rate for ALPHA® passive samplers prepared and analysed at UKCEH Edinburgh for the UK and similar climates.
- Local site operator duties carried out by UKCEH staff, AFBI (Hillsborough), and Ricardo AEA; analysis performed by Centre for Ecology and Hydrology Edinburgh.
- Samplers exposed monthly at each site to measure ammonia concentrations.

## UKCEH ALPHA® sampler method
- Passive sampler uses a citric acid coated filter to capture NH3; protected by a white PTFE membrane, with the membrane facing down during exposure.
- Samplers mounted on a shelter at about 1.5 m above ground; run in replicates for reliable concentration estimates.

## Analysis and uptake rate
- Exposed samplers are extracted into deionised water and analysed by SEAL AA3 using colorimetry to determine ammonium concentration.
- Ammonia concentration in air is derived from the ammonium concentration using a known uptake rate of 0.003241315 m3 hr⁻¹ and the exposure duration.
- Data are flagged where concerns exist (see data quality section).

## Data quality and flags
- Quality checks include a coefficient of variation (CV) threshold: CV < 15% across replicates supports data validity; if CV > 15%, replicates are evaluated for possible discard; if accepted, the average is considered representative and flagged as valid (103).
- Some measurements exceed calibration range but are still considered valid if re-analysis is not possible due to instrument limitations.
- Missing data or metadata are indicated by -9999.
- The dataset includes data flags and metadata following EMEP conventions (see flag definitions below).

## Data product
- Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv.
- Each row corresponds to one month of data for a single site; columns include site name, start/end dates, ammonia concentration for the exposure period, and a data flag.
- Concentrations are reported as micrograms of NH3 per cubic metre of air (µg NH3 m⁻³).
- Data and site information are accompanied by spatial identifiers and a detailed column description.

## Column details (key fields)
- site_id: unique site identifier
- site_name: site name
- network_id: network identifier (RSW)
- parameter_id: type of measurement (alpha_NH3_g)
- measurement_start_date/time: exposure start date and time
- measurement_end_date/time: exposure end date and time
- measurement: ammonia concentration (µg NH3 m⁻³)
- less_than: flag for values below detection limit (0 or 1)
- verification_id: data verification status (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
- unit_id: units (24 = µg NH3 m⁻³)
- data_capture: data capture percentage
- validity_id: 1 = valid, -1 = not valid
- emep_code: data status code and flags as per EMEP
- Month-Year: month and year of measurement
- Comments: data notes

- EMEP flags provide context for data validity and quality, including reasons such as contamination, detection limits, sampling conditions, and nearby influences (e.g., traffic, agricultural activity). Examples include:
  - 999: missing measurement or not captured
  - 781, 780, 654, 653, etc.: various validity and quality reasons
  - 103: CV of replicates > 15% but still considered valid

## Site information
- Edinburgh uptake rate OTC: start 01/03/2020; ongoing; coordinates 55.863150, -3.209845; inlet height 1.5 m; collocated with UKA00128.
- Edinburgh uptake rate Auch: start 01/03/2020; ongoing; coordinates 55.792160, -3.242900; inlet height 1.5 m; collocated with UKA00451.
- Edinburgh uptake rate Hills: start 01/03/2020; ongoing; coordinates 54.452500, -6.083340; inlet height 1.5 m; collocated with UKA00293.
- Edinburgh uptake rate Chilbolton: start 01/01/2021; ongoing; coordinates 51.149617, -1.438228; inlet height 1.5 m; collocated with UKA00614.

## How to use the data
- Use the final NH3_Edinburgh_Uptake_Rate_2021.csv dataset to analyze monthly NH3 uptake at each site, applying CV and validity flags to filter reliable data.
- Combine with site metadata for spatial analyses or comparisons across sites.
- Leverage the documented uptake rate and method to interpret concentration measurements and to compare with other UK or climate contexts.