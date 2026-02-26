# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

## Overview and context
- A set of transect sites through Ballynahone National Park, an Area of Special Scientific Interest (ASSI/SAC) and a Ramsar site in Northern Ireland.
- The park is an ammonia-sensitive peatland ecosystem managed locally by Ulster Wildlife Trust (UWT).
- Data were collected due to concerns that Ballynahone Bog may be affected by NH3 emissions from local poultry livestock installations.
- Local site operator: Ulster Wildlife Trust; analysis conducted by Centre for Ecology and Hydrology Edinburgh (CEH).
- Purpose: monitor ammonia concentrations along the transect to support environmental health assessment and policy performance tracking over time.

## Monitoring approach and methods
- Instrument: CEH ALPHA® passive samplers using a citric acid coated filter to capture NH3.
- Diffusion-controlled sampling through a white PTFE membrane; membrane facing downwards during exposure.
- Replicate samplers deployed at a shelter on a pole at about 1.5 m above ground to improve reliability.
- Exposure cycle: samplers exposed monthly at the beginning of each month.
- Analysis: exposed samplers extracted into deionised water; NH3 concentration measured with SEAL AA3 colorimetric analysis.
- Conversion: sampler concentrations converted to average air concentration using a known uptake rate of 0.003241315 m3 hr-1 and the exposure duration.

## Data quality, validation, and flags
- Some samples were incorrect or weather/animal-interference led to loss; such samples are not used for deposition estimates and are flagged.
- Final dataset: UWT_Ballynahone_Bog_Data_2018.csv with accepted data values and appropriate flags.
- Key quality rules:
  - Coefficient of variation (CV) across replicate samplers: CV < 15% considered representative; if CV > 15%, replicates reviewed and may be discarded; otherwise dataset may be marked valid with 103 flag.
  - Missing samplers: represented as -9999.00 and marked invalid (-1).
  - Sampler duration anomalies: longer or shorter than normal exposure period; flagged accordingly.
  - Local contamination or influences: flagged based on site operator notes; affected results discarded; final reported value is the average of remaining results.
- Data fields include: site name, exposure start/end dates, ammonia concentration (µg NH3 m-3), data flag, verification, unit, data capture percentage, validity, and EMEP-related codes.

## Dataset structure and contents
- Final dataset name: UWT_Ballynahone_Bog_Data_2018.csv.
- Each row represents one month of data for a single site; columns include:
  - Site name, start date, end date (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Data flag and related metadata (verification id, unit id, data capture percentage, validity id, EMEP code)
  - Month-Year of measurement (MMM-YY)
  - Additional flags indicating detection limit status and notes on data validity and quality
- Data capture and flags align with UK-AIR and EMEP conventions for data status and quality.

## Site information and layout
- Ballynahone bog_1 to Ballynahone bog_8 with:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Coordinates (latitude/longitude) for each site
  - Height of air inlet above ground: 1.5 m
- Example site properties:
  - bog_1: 54.82223827, -6.67860685
  - bog_2: 54.82303694, -6.67686906
  - bog_3: 54.82331637, -6.67530382
  - bog_4: 54.82396942, -6.67339952
  - bog_5: 54.82446239, -6.67000651
  - bog_6: 54.82514962, -6.67946104
  - bog_7: 54.82165647, -6.67468906
  - bog_8: 54.81616100, -6.65596700

## Practical context and intended use
- Supports long-term environmental monitoring of NH3 in a sensitive peatland ecosystem.
- Provides standardized, quality-assured data suitable for assessing environmental health and informing policy performance over time.
- Data and metadata enable replication, cross-site comparisons, and integration with other datasets while maintaining data provenance.

## Data access and further information
- Raw data quality checks and site-level details (including flags, noted concerns, and data handling rules) are described in the supporting information.
- Data are prepared for sharing with appropriate portals, with clear documentation of data validity, detection limits, and contamination flags to enable others to access the underlying data and reproduce outputs.