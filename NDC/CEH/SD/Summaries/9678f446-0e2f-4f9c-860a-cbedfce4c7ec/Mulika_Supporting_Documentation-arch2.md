# Materials and Methods

- Aim and context
  - Conduct an ozone (O3) exposure experiment to understand how wheat responds to realistic and projected O3 concentrations.
  - Generate structured datasets suitable for monitoring environmental health and policy performance over time.

- Experimental setup
  - Location: Centre for Ecology and Hydrology (CEH) air pollution facility, Abergwyngregyn, North Wales (53.2°N, 4.0°W).
  - Organism and cultivation: Wheat seeds (Triticum aestivum L., cv. Mulika) in 25 L pots with John Innes No.3 compost; seed density ~260 seedlings/m²; pots inoculated with soil microbial communities from a nearby wheat field.
  - Ozone exposure: Eight ventilated hemispherical solardomes (O3 exposure), from 15 May to 82 days.
  - O3 profiles: Four treatments with low background but high midday peaks (36–115 ppb max) and four with high background but small daily peaks (max 32–65 ppb). 24-hour mean O3 concentrations ranged 27–57 ppb.
  - Replication and randomization: No true treatment replication due to limited solardomes; addressed with mixed-model analysis to mitigate pseudoreplication. Ozone treatments were randomly allocated to solardomes; climatic conditions were monitored to ensure no significant inter-dome variation.
  - Environment control: Solardomes ventilated at 2 air changes per minute with charcoal-filtered air and added O3 from oxygen. Temperature, PAR, and relative humidity monitored in one solardome; O3 concentrations monitored every 30 minutes with matched-calibration analyzers.

- Treatments and management
  - Watering regimes: well-watered, early-season drought (10 days, pre-anthesis), late-season drought (10 days, post-anthesis).
  - Pest and fertiliser: outbreaks of powdery mildew and aphids controlled with a fungicide and three insecticide applications; fertiliser (ammonium nitrate, ~80 kg/ha) applied after anthesis.

- Measurements and timing
  - Growth stages: Assessed using the Tottman system on four dates (9 June, 30 June, 14 July, 27 July); four pots per ozone and drought treatment evaluated.
  - Chlorophyll content index (CCI): 523 measurements across 28 days (late spring to mid-summer) using CCM-200 meters; two meters used with calibration to standardise readings.
  - Stomatal conductance to water: 318 measurements across 9 days (27 May–22 July) using AP4 porometer; measurements on randomly selected non-edge leaves (flag leaf from 28 May); soil water content measured concurrently.
  - Data quality: Porometer calibrated daily; measurements taken under diverse meteorological conditions to support later model parameterisation.

- Harvest and yield
  - Harvest: 5–12 August, non-edge plants harvested; biomass separated into straw and ears; grains threshed and weighed (fresh and after 1 week drying at 65°C); data checked for anomalies and re-weighed as needed.

- Data structures and datasets
  - Mulika_growth_stage_data_2015.csv
    - 9 variables, 320 observations
    - Key fields: Date_of_measurement, Day_of_year, solardome_number, Ozone_profile, Seasonal POD6 (POD6_bespoke_DO3SE), 24h_mean_ozone_ppb, Watering_treatment, Pot_ID, Maximum_decimal_growth_stage.
  - Mulika_harvest_2015.csv
    - 26 variables, 96 observations
    - Key fields: Dome_number, Ozone_profile, Target_24h_mean_O3, Measured_24h_mean_O3, AOT40_ppm, POD6_bespokeDO3SE, Watering_treatment, aphid presence, ear counts and weights, grain and straw weights, harvest indices, yield (kg/m² and kg/ha), and related calculations.
  - Mulika_CCI_2015.csv
    - 11 variables, 524 observations
    - Key fields: Person_measuring, Date_of_measurement, solardome_number, pot_ID, watering_treatment, current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, Soil_moisture_content_%.
  - Mulika_stomatal_conductance_2015.csv
    - 17 variables, 318 observations
    - Key fields: Date_of_measurement, Day_of_year, time_of_day, solardome_number, Watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, PAR, humidity, temperature, VPD, and related canopy monitoring data.

- Data handling and monitoring significance
  - POD6 (phytotoxic ozone dose) computed using the DO3SE model with wheat cultivar parameterisation to reflect stomatal ozone flux.
  - Data capture designed to enable model parameterisation and integration with environmental monitoring datasets.
  - Data are prepared for storage and sharing via appropriate data portals, supporting broader access and re-use for environmental health and policy evaluation.