# Ozone exposure experiment on wheat (Mulika) under drought and pest pressures, CEH solardomes, 2015

- Location and setup
  - Conducted April–August 2015 at the Centre for Ecology and Hydrology (CEH) air pollution facility, Abergwyngregyn, North Wales.
  - Wheat cultivar Mulika grown in 25-liter pots with John Innes No.3 compost; inoculated with soil microbes from a neighboring wheat field.
  - Eight solardomes (ventilated glasshouses) used to impose ozone (O3) treatments; random allocation of treatments to solardomes to mitigate environmental gradients.
  - O3 delivery via controlled air with two air changes per minute; continuous monitoring of O3 (30-minute cycles) and routine weather data (temperature, PAR, RH) in one solardome.

- Experimental design and treatments
  - O3 exposure across eight profiles over 82 days, with 24-hour mean concentrations from 27 to 57 ppb.
  - Profiles split into two groups:
    - Four treatments: low background (28–32 ppb) with high midday peaks (36–115 ppb).
    - Four treatments: high background (25–59 ppb) with small daily peaks (max 32–65 ppb).
  - Drought regimes: one of three watering regimes applied to mesocosms
    - Well-watered
    - Early-season drought (10 days, pre-anthesis)
    - Late-season drought (10 days, post-anthesis)
  - Pests and fertilization: powdery mildew and aphid outbreaks; fungicide (Unix) and three insecticide applications; fertiliser after anthesis (ammonium nitrate, ~80 kg/ha).
  - Climatic/stress controls: climatic conditions across solardomes previously found not to differ significantly; environmental conditions monitored to support model parameterisation.

- Measurements and timing
  - Growth stages: assessed using the Tottman decimal code on four dates (9 Jun, 30 Jun, 14 Jul, 27 Jul); maximum growth stage per pot recorded.
  - Chlorophyll content: chlorophyll content index (CCI) measured ad-hoc on 28 days from early May to late July using CCM-200, with calibration to standardise readings.
  - Stomatal conductance: stomatal conductance to water (gsto) measured ad-hoc on 9 days (late May–late July) with a leaf porometer; paired with soil water content (SWC) and CCI readings; calibration of porometer performed daily.
  - Additional context data: meteorological conditions recorded to enable model parameterisation.

- Harvest and yield data
  - Harvest conducted 5–12 August 2015 after flag leaf senescence; all non-edge plants harvested.
  - Measurements: fresh and dry weights of straw and grains, grain weights per plant and per ear, 100-grain dry weight, grain weight per ear, ear numbers, harvest/index metrics (grain vs total aboveground biomass), and yields expressed as kg/m2 and kg/ha.
  - Data processing: weights re-weighed if anomalous values were found; data entered in Excel and checked by multiple individuals.

- Data structures and metadata
  - Mulika_growth_stage_data_2015.csv
    - 320 observations, 9 variables including Date_of_measurement, solardome_number, Ozone_profile, Growth stage (decimal), and Maximum_decimal_growth_stage (per pot).
    - Includes Day_of_year, pot_id, and related fields.
  - Mulika_harvest_2015.csv
    - 96 observations, 26 variables including Dome_number, Ozone_profile, target/measured 24h mean O3, AOT40, POD6_bespokeDO3SE, Watering_treatment, and a comprehensive set of yield and biomass metrics (e.g., Ear_number_per_m2, Harvest_index, Yield_kg/m2, Yield_kg/ha).
    - Derived fields such as ear counts, grain weights, and per-plant measurements.
  - Mulika_CCI_2015.csv
    - 524 observations, 11 variables including measurement date/time, solardome_number, pot_ID, watering_treatment, current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, and Soil_moisture_content_%.
    - Combines plant-level chlorophyll data with environmental context (soil moisture, watering status).
  - Mulika_stomatal_conductance_2015.csv
    - 318 observations, 17 variables including Date_of_measurement, solardome_number, pot_ID, watering_treatment, current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, time_canopy_computer_recording, relative_humidity, PAR, temperature, and VPD.
    - Includes adaxial/abaxial comparisons, ozone-related stomatal conductance, and concurrent meteorological data.

- Data quality, governance, and limitations
  - Data metadata provided in detail (variable names, units, descriptions, and data structure) to support reuse and reproducibility.
  - No replication across solardomes for ozone treatments due to space constraints; addressed through statistical approaches (mixed models) to mitigate pseudoreplication.
  - Random allocation of ozone treatments to solardomes and uniform environmental monitoring aimed to minimise biases and enable robust analyses.
  - Potential data governance considerations noted implicitly via openness and metadata richness (calibration standards, measurement protocols, and data-sharing readiness through detailed data dictionaries).