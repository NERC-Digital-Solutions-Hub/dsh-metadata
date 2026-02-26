# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Overview
- Report presents initial results from a study to determine uptake rate for ALPHA® passive samplers used to measure NH3 concentrations in air, prepared and analyzed at UKCEH Edinburgh for the UK and similar climates.
- Local site operator duties are performed by UKCEH, AFBI (Hillsborough), and Ricardo AEA; analysis by CEH Edinburgh.
- Samplers are exposed in monthly cycles at the beginning of each month; data for 2022 are compiled in a final dataset.

## UKCEH ALPHA® sampler method
- Passive sampler design: citric acid coated filter to capture ammonia; a white PTFE (Teflon) membrane protects the filter and allows diffusion; membrane faces downward during exposure; non-exposed end sealed.
- Deployment: replicate samplers mounted on a shelter on a pole at ~1.5 m above ground; multiple replicates improve reliability.
- Analysis workflow: exposed samplers are extracted into deionised water and analysed by SEAL AA3 using a colorimetric response to determine ammonium concentration.
- Concentration calculation: converts sampler ammonium concentration to ambient NH3 concentration using a known uptake rate of 0.0038422 m3 hr-1 and the exposure duration.
- Data quality: data flagged for concerns; detailed quality checks described in the dataset notes.

## Data quality assurance and flags
- Data are examined against QA rules and flagged accordingly (see page 4 in the full report):
  - Coefficient of variation (CV) < 15% across replicates suggests reliable samplers; if CV > 15%, replicates may be discarded or results reevaluated; valid data are flagged 103.
  - Results may be greater than calibration range but still valid if re-measurement was not possible due to instrument issues.
  - Missing measurements or metadata are marked with -9999.
- The final dataset used for submission is submissions_ED_UR_NH3_2022.csv and includes accepted data values with appropriate flags.
- Data status and metadata are encoded with an EMEP flag system (detailed code meanings provided in accompanying tables). Examples include:
  - 103: CV > 15% but valid measurement
  - 781/780/654/653: various conditions such as values below detection limit, below detection/quantification, or representative sampling periods
  - 999: missing data capture or missing measurement
  - 559/558/557/556/555: contamination or local influence considered valid or invalid based on context
- Data fields capture measurement value in micrograms NH3 per cubic metre (µg NH3 m-3), along with data capture percentage and validity indicators.

## Dataset structure and contents
- Final dataset file: submissions_ED_UR_NH3_2022.csv
- Each row represents one month of data for a single site.
- Columns include:
  - Site id and site name
  - network_id (ED_UR)
  - parameter_id (alpha_NH3_g)
  - measurement start date and start time
  - measurement end date and end time
  - measurement (ammonia concentration, units: µg NH3 m-3)
  - less than (indicator if below detection limit)
  - verification id (1: Verified, 2: Preliminary verified, 3: Not verified)
  - unit id (24: µg NH3 m-3)
  - Data capture (percentage)
  - Validity_id (1: valid, -1: not valid)
  - EMEP code and Data status code flags
  - Month-Year
  - Comments
- Reports provide a structured, self-serve dataset with clear provenance and quality flags.

## Site information
- Edinburgh uptake rate OTC
  - Start_date: 01/03/2020
  - End_date: ongoing
  - Latitude: 55.863150; Longitude: -3.209845
  - Height of air inlet: 1.5 m
  - Further details: Collocated with UKEAP UKA00128
- Edinburgh uptake rate Auch
  - Start_date: 01/03/2020
  - End_date: ongoing
  - Latitude: 55.792160; Longitude: -3.242900
  - Height of air inlet: 1.5 m
  - Collocated with UKEAP UKA00451
- Edinburgh uptake rate Hills
  - Start_date: 01/03/2020
  - End_date: ongoing
  - Latitude: 54.452500; Longitude: -6.083340
  - Height of air inlet: 1.5 m
  - Collocated with UKEAP UKA00293
- Edinburgh uptake rate Chilbolton
  - Start_date: 01/01/2021
  - End_date: ongoing
  - Latitude: 51.149617; Longitude: -1.438228
  - Height of air inlet: 1.5 m
  - Collocated with UKEAP UKA00614

Notes
- All concentration data are reported as the average concentration for the specified exposure period.
- Units are micrograms of NH3 per cubic metre of air (µg NH3 m-3).