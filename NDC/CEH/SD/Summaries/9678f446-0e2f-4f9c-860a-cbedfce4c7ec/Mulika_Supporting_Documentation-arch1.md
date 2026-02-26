# Materials and Methods

- Study objective and setting
  - Ozone (O3) exposure experiment conducted April–August 2015 at the Centre for Ecology and Hydrology (CEH) air pollution facility, Abergwyngregyn, North Wales.
  - Species: wheat Triticum aestivum L., cv. Mulika; grown in 25-L pots with John Innes No.3 compost; seed density ~260 seedlings/m2; pots inoculated with field soil microbial communities.

- Experimental design and environment
  - Eight ventilated solardomes used for ozone exposure, with random allocation of treatments to minimize environmental gradient effects.
  - Two ozone profiles:
    - Four solardomes: low background (28–32 ppb) with high midday peaks (36–115 ppb) during the day.
    - Four solardomes: high background (25–59 ppb) with small daily peaks (max 32–65 ppb).
  - Ozone generation and monitoring:
    - Ozone produced from oxygen; air changes at 2 per minute with charcoal-filtered air.
    - Continuous monitoring of ozone in all solardomes (30-minute cycle) using two calibrated O3 analyzers.
    - Additional microclimate monitoring in one solardome (automatic weather station for temperature, PAR, relative humidity).
  - Experimental limitations and analysis:
    - No replication of treatments due to limited solardomes; pseudoreplication countered via mixed-model statistical analyses.
    - Climatic conditions between solardomes previously shown not to vary significantly.

- Treatments
  - Watering regimes (three levels):
    - Well-watered
    - Early-season drought: 10-day drought during booting/flag leaf expansion (growth stages ~40–46)
    - Late-season drought: 10-day drought during late milk/early dough (growth stages ~78–84)
  - Biotic and chemical inputs:
    - Fungicide: one application (Unix, Cyprodnil, 1.6 kg/ha)
    - Insecticides: three applications (pyrethrum)
    - Fertiliser: ammonium nitrate post-anthesis (80 kg/ha)

- Measurements and data collection
  - Growth monitoring
    - Growth stage assessments using the Tottman decimal code on four dates (9 June, 30 June, 14 July, 27 July); maximum growth stage per pot recorded.
  - Plant physiology
    - Chlorophyll Content Index (CCI): 523 measurements across 28 days, on the most recently fully expanded leaf; measured with CCM-200 chlorophyll meter; two meters used with a calibration line.
    - Stomatal conductance to water (gsto): 318 measurements across 9 days (27 May–22 July) on the flag leaf; measured with AP4 porometer; paired with soil water content (SWC) and CCI; diurnal measurements (10:00–16:00); porometer calibrated daily.
  - Harvest and yield
    - Harvested 5–12 August 2015 after flag leaf senescence; non-edge plants harvested; straw separated from ears; grains threshed; fresh and dry weights recorded (65 °C drying); data validated and anomalous values re-weighed.
  - Data structure and datasets
    - Mulika_growth_stage_data_2015.csv: 320 observations, 9 variables (Date_of_measurement, Day_of_year, solardome_number, Ozone_profile, Seasonal_POD6_bespoke_DO3SE, 24h_mean_ozone_ppb, Watering_treatment, Pot_ID, Maximum_decimal_growth_stage).
    - Mulika_harvest_2015.csv: 96 observations, 26 variables (Dome_number, Ozone_profile, Target_24h_mean_O3, Measured_24h_mean_O3, AOT40_ppm, POD6_bespokeDO3SE, Watering_treatment, and yield-related metrics such as Yield_kg/m2 and Yield_kg/ha, among others).
    - Mulika_CCI_2015.csv: 524 observations, 11 variables (Person_measuring, Date_of_measurement, Day_of_year, time, solardome_number, pot_ID, watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, Soil_moisture_content_%).
    - Mulika_stomatal_conductance_2015.csv: 318 observations, 17 variables (Date_of_measurement, Day_of_year, time_of_day, Solardome_number, Watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, Time_canopy_computer_recording, Relative_humidity_in_dome7, PAR_in_dome7, corrected_dome_7_temperature, corrected_dome_7_VPD).
  - Additional metrics
    - POD6_bespokeDO3SE: phytotoxic ozone dose (mmolm-2) over a threshold of 6, season-long, calculated with cultivar-specific parameters based on DO3SE.

- Data quality and handling
  - Measurements intentionally varied across a range of meteorological conditions to support model parameterisation.
  - Data uploaded with metadata and prepared for compatibility with future modelling and cross-dataset analyses.