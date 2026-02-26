# Materials and Methods

## Overview
- Describes an ozone (O3) exposure experiment with wheat (Triticum aestivum L., cv. Mulika) conducted April–August 2015 at CEH air pollution facility, Abergwyngregyn, North Wales (approx. 53.2°N, 4.0°W).
- Eight solardomes (ventilated hemispherical glasshouses) used to apply different O3 concentration profiles over 82 days.
- Study design integrates ozone exposure with watering regimes to assess growth, physiology, and yield responses; includes data collection on growth stage, chlorophyll content, stomatal conductance, soil moisture, and harvest metrics.
- Data produced include multiple structured CSV datasets with detailed metadata, suitable for GIS-enabled spatial-temporal analysis (per solardome and pot).

## Experimental setup and environment (spatial and operational context)
- Location and structure
  - CEH air pollution facility at Abergwyngregyn (North Wales); eight solardomes used for O3 exposure.
  - Temperature, PAR, and relative humidity continuously monitored in at least one solardome; O3 monitored every 30 minutes in all solardomes with matched-calibration analysers.
- Experimental units and planting
  - Wheat: Triticum aestivum L. cv. Mulika; 25-litre pots with John Innes No.3 compost; sowing density ~260 seedlings per m2.
  - Seeds inoculated with soil microbial communities from a nearby field.
- Ozone exposure and treatments
  - O3 exposure began 15 May and lasted 82 days.
  - Concentrations: eight profiles with a 24-hour mean range of 27–57 ppb; two profile types:
    - Low background with high midday peaks (36–115 ppb maxima).
    - High background with small daily peaks (32–65 ppb maxima).
  - Random allocation of ozone treatments to solardomes to minimize environmental gradient effects.
  - No replication at the treatment level due to limited solardomes; pseudoreplication addressed in statistics via mixed models.
  - Air supplied as charcoal-filtered air with added O3; two air changes per minute.
- Additional growth conditions
  - Drought/watering regimes: well-watered, early-season drought (booting/flag leaf stages), late-season drought (late milk to early dough).
  - Fungicide and insecticide applications as needed; fertilizer applied once post-anthesis.

## Measurements and data collected
- Growth and development
  - Growth stage assessments (Tottman scale) on four dates: 9 Jun, 30 Jun, 14 Jul, 27 Jul.
- Physiological and biochemical measurements
  - Chlorophyll Content Index (CCI): 523 measurements across treatments, 28 Jul to early Jul; measured on most recently fully expanded leaf; calibration line used.
  - Stomatal conductance to water (gsto) via AP4 porometer: 318 measurements across 9 days; paired with soil water content (SWC) and CCI; measurements taken during physiologically active daytime hours (10:00–16:00).
  - Soil moisture content (SWC) measured with ThetaProbe at 10 cm depth.
  - Measurements performed across a range of meteorological conditions to support model parameterisation.
- Harvest and yield
  - Harvest 5–12 Aug 2015: non-edge plants collected; fresh and dry weights recorded after drying; grains removed and weighed; data used to compute yield, biomass, and harvest index.
  - Data checked for anomalies and re-weighed as needed.

## Data and datasets (structure and key variables)
- Mulika_growth_stage_data_2015.csv
  - 320 observations, 9 variables
  - Key variables: Date_of_measurement, Day_of_year, solardome_number, Ozone_profile, Seasonal_POD6_bespoke_DO3SE (POD6), 24h_mean_ozone_ppb, Watering_treatment, Pot_ID, Maximum_decimal_growth_stage.
  - Purpose: link plant growth stage to time, dome, and ozone profile.
- Mulika_harvest_2015.csv
  - 96 observations, 26 variables
  - Key variables: Dome_number, Ozone_profile, Target_24h_mean_O3, Measured_24h_mean_O3, AOT40_ppm, POD6_bespokeDO3SE, Watering_treatment, Pot_ID, plus extensive harvest metrics (e.g., ear counts, grain/biomass weights, yields in kg/m2 and kg/ha, harvest index, etc.).
  - Purpose: relate final yield and component traits to ozone exposure, watering regime, and pot-level factors.
- Mulika_CCI_2015.csv
  - 524 observations, 11 variables
  - Key variables: Person_measuring, Date_of_measurement, Day_of_year, solardome_number, pot_ID, watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, Soil_moisture_content_%, time-related fields.
  - Purpose: provide daily leaf-level chlorophyll measurements linked to canopy and soil conditions.
- Mulika_stomatal_conductance_2015.csv
  - 318 observations, 17 variables
  - Key variables: Date_of_measurement, Day_of_year, time_of_day, Solardome_number, Watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, Time_canopy_computer_recording, Relative_humidity_in_dome7, PAR_in_dome7, corrected_dome_7_temperature, corrected_dome_7_VPD.
  - Purpose: quantify stomatal responses to water and ozone under varying canopy conditions and meteorology; includes azimuth of both leaf surfaces and ozone-related stomatal flux calculations.

## Data quality, calibration, and notes for GIS use
- Calibration and measurement quality
  - O3 analysers calibrated identically; 30-minute cycle ozone data ensured comparability across solardomes.
  - Chlorophyll meter (CCI) calibrated via a standard line; leaf measurements standardized to the most recently fully expanded leaf.
  - Porometer calibrations performed at start of measurement days; PAR, humidity, and temperature recorded with automatic weather equipment.
- Experimental considerations for mapping
  - Each observation is associated with solardome and/or pot identifiers, enabling spatial joins to solardome locations and to growth environment factors.
  - Randomized treatment allocation to solardomes supports spatial analysis of treatment effects while allowing correction for potential gradients.
  - Documented drought timings and irrigation status enable temporal layering in GIS (time-enabled analyses).
- Limitations relevant to GIS and analysis
  - No replication of ozone treatments at the dome level; mixed models advised for statistical analysis to counter potential pseudoreplication.
  - Some measurements are ad-hoc across days and plants, which should be considered when aggregating to per-dome or per-pot summaries.

## Potential GIS-related applications
- Spatial visualization of ozone profiles and their relationship with physiological responses across solardomes.
- Map-based dashboards showing growth stages, CCI, stomatal conductance, soil moisture, and yield by dome and treatment.
- Temporal GIS analysis integrating daily CCI and stomatal metrics with environmental variables (PAR, temperature, humidity) to explore spatial-temporal patterns.
- Integration of harvest metrics (yield, harvest index) with ozone exposure levels to support policy or management questions regarding air quality impacts on crop performance.