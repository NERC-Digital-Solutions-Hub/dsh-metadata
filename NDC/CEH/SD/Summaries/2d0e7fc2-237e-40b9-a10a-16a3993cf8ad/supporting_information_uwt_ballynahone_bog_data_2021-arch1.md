# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Objective and context
- Monitor ammonia (NH3) concentrations in air at Ballynahone Bog, a peatland in Ballynahone National Park, Northern Ireland.
- Site managed by Ulster Wildlife Trust; analysis performed by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Study location along a transect through Ballynahone National Park to assess potential NH3 deposition from nearby poultry livestock installations.
- Data collected on a monthly basis during 2021 using UKCEH ALPHA® passive samplers.

## Sampling method and exposure
- Instrument: UKCEH ALPHA® passive samplers with citric acid coated filters; PTFE membrane protects the filter.
- Deployment: samplers placed on shelters at about 1.5 m above ground, with replicate samplers per site for reliability.
- Exposure cycle: monthly exposure periods, initiated at the beginning of each month.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - NH3 concentration measured with SEAL AA3 colorimetric analyser.
  - Concentrations converted to average air concentration using uptake rate = 0.003241315 m3 hr-1 and the exposure duration.

## Data quality assurance and processing
- Data quality controls applied to raw data:
  - Exclude samples exposed incorrectly or lost due to weather; flagged for validity concerns.
  - Flagged data indicators include data capture, detection limits, and contamination notes.
- Validation rules:
  - Coefficient of variation (CV) of replicates: CV < 15% considered valid; otherwise replicates evaluated for potential discards. Validated results flagged accordingly (103).
  - Missing samplers: assigned -9999.00 and marked invalid (-1).
  - Abnormal sampler duration (long/short): flagged as non-standard but noted.
  - Local contamination or influences: flagged based on site operator notes; results may be discarded if not representative; final site value is the average of remaining valid results.
- Final dataset: UWT_Ballynahone_Bog_Data_2021.csv containing accepted data values with appropriate flags and site identifiers.

## Dataset structure and content
- Data rows: one row per month per site (site-level records).
- Key columns (examples):
  - Site name, unique site identifier, network_id (BE), parameter_id (alpha_NH3_g)
  - Measurement start date/time and end date/time
  - Ammonia concentration (units: µg NH3 m-3)
  - Less than detection flag, verification id, unit id
  - Data capture percentage, validity_id, EMEP code
  - Month-Year of measurement
- Data status and flags:
  - EMEP data status and multiple flag codes indicate capture quality, detection limits, contamination, and sampling period compliance.
  - Common outcomes include valid measurements, measurements below detection/quantification limits, and various contamination/invalidity reasons.
- Dataset scope:
  - Site coordinates and metadata for Ballynahone bog sites (ballynahone bog_1 to bog_8) including start_date 01/09/2014 and ongoing end date.
  - Inlet height consistently 1.5 m above ground.
  - Geographic coordinates provided for each site.

## Site information and geography
- Ballynahone bog_1 to bog_8 with specific latitude/longitude coordinates and 1.5 m inlet height.
- Each site has a start date of 01/09/2014 and an ongoing end date, indicating long-term monitoring capability.

## Use and interpretation notes
- Data are suitable for identifying spatial and temporal patterns of ambient NH3 within the transect and assessing potential deposition from nearby activities.
- Analysts should consider data flags and QC notes when aggregating or modeling NH3 concentrations.
- Data provenance is maintained via explicit flags, replicate-based QC, and standardized measurement protocols, enabling reproducibility and discoverability for further analyses or cross-dataset comparisons.