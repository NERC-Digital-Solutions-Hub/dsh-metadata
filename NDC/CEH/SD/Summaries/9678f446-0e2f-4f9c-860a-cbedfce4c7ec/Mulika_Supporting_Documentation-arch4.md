# Materials and Methods

- Location and organism: Ozone (O3) exposure experiment conducted April–August 2015 at the Centre for Ecology and Hydrology (CEH) air pollution facility, Abergwyngregyn, North Wales. Plant material: wheat (Triticum aestivum L., cv. Mulika) grown in 25-liter pots with John Innes No.3 compost.
- Experimental setup: Seeds sown in rows (7 cm apart) with 40 seeds per pot, achieving ~260 seedlings per m². Pots inoculated with soil microbial communities from a nearby wheat field via soil slurry.
- Ozone exposure: Eight solardomes used for O3 treatment (randomly allocated to minimize environmental gradients). Exposure lasted 82 days starting 15 May. 24-hour mean O3 ranged from 27 to 57 ppb across treatments; four treatments featured low background with high midday peaks (36–115 ppb) and four featured high background with small daily peaks (32–65 ppb). No replication of treatments within the same dome due to limited domes; pseudoreplication addressed in analysis using mixed models. Climatic conditions shown to be similar across domes.
- Environmental control and monitoring: Dome ventilation at two air changes per minute with charcoal-filtered air; controlled addition of O3 from oxygen. One solardome continuously monitored for temperature, PAR, and relative humidity via automatic weather station; O3 concentrations tracked every 30 minutes with two calibrated analyzers.
- Watering regimes and stress events: Three watering regimes—well-watered, early-season drought (10 days without water, mid-drought maintenance), and late-season drought (10 days without water). Drought timing aligned with key growth stages (pre-anthesis to post-anthesis).
- Pests, diseases, and fertilization: Fungicide (Unix, Cyprodnil) applied once for powdery mildew; three insecticide applications (pyrethrum). Fertilizer applied once after anthesis (ammonium nitrate, ~80 kg N/ha).
- Measurements and timing: Growth stages assessed using the Tottman decimal code on four dates (9 Jun, 30 Jun, 14 Jul, 27 Jul). Chlorophyll content index (CCI) measured 523 times across 28 days using CCM-200 meters. Stomatal conductance (gs) measured 318 times across 9 days with an AP4 porometer; paired with soil water content (SWC) and CCI. Calibration performed at measurement start; measurements spread across varied meteorological conditions to inform future model parameterisation.
- Harvest and yield assessment: Harvested 5–12 Aug 2015 after flag leaf senescence and grain drying; ears and straw separated, grains threshed, and fresh/dry weights recorded (65 °C drying for a week). Data checked for anomalies and re-weighed as needed.
- Data and references: Study references provided for related ozone and plant response work.

- Data management and datasets (structure and variables):
  - Mulika_growth_stage_data_2015.csv
    - 9 variables, 320 observations
    - Key fields: Date_of_measurement, Day_of_year, solardome_number, Ozone_profile, Seasonal_POD6_bespoke_DO3SE, 24h_mean_ozone_ppb, Watering_treatment, Pot_ID, Maximum_decimal_growth_stage
  - Mulika_harvest_2015.csv
    - 26 variables, 96 observations
    - Key fields: Dome_number, Ozone_profile, Target_24h_mean_O3, Measured_24h_mean_O3, AOT40_ppm, POD6_bespokeDO3SE, Watering_treatment, Pot_ID, yield and harvest metrics (e.g., Yield_kg/m2, Yield_kg/ha, Harvest_index)
  - Mulika_CCI_2015.csv
    - 11 variables, 524 observations
    - Key fields: Person_measuring, Date_of_measurement, Day_of_year, time, solardome_number, pot_ID, watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, Soil_moisture_content_%
  - Mulika_stomatal_conductance_2015.csv
    - 17 variables, 318 observations
    - Key fields: Date_of_measurement, Day_of_year, time_of_day, Solardome_number, Watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, PAR, RH, temperature, VPD
  - Note: Datasets include units and methodological notes (e.g., POD6 via DO3SE stomatal parameterisation, PLA conversions) and reflect measurements taken under varied conditions to support subsequent data analysis and modelling.