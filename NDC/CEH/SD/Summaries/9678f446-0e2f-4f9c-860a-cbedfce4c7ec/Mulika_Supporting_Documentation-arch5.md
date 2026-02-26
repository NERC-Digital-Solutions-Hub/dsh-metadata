# Materials and Methods

- Study setting and organism
  - Ozone exposure experiment conducted April–August 2015 at the Centre for Ecology and Hydrology (CEH) air pollution facility in Abergwyngregyn, North Wales (53.2°N, 4.0°W).
  - Plant material: Wheat seeds Triticum aestivum L., cv. Mulika, grown in 25-L pots with John Innes No.3 compost.
  - Seeds sown in rows 7 cm apart (40 seeds per pot) to achieve ~260 seedlings/m2; pots inoculated with soil microbial communities from a nearby wheat field.

- Experimental design
  - Eight ozone (O3) exposure solardomes (ventilated hemispherical glasshouses) with varying O3 profiles.
  - Treatments spanned 82 days with 24-h mean O3 from 27 to 57 ppb; four treatments had low background with high midday peaks; four had high background with small daily peaks.
  - No replication of treatment within the experiment due to limited solardomes; pseudoreplication addressed statistically via mixed models.
  - Random allocation of ozone treatments to solardomes to minimize environmental gradient effects; prior assessment suggested little climatic variation between solardomes.
  - Environmental controls: two air changes per minute with charcoal-filtered air; controlled O3 added from oxygen source; continuous monitoring of temperature, PAR, and relative humidity in one solardome; O3 monitored every 30 minutes in all solardomes with matched calibrations.

- Water and pest/dertilization treatments
  - Mesocosms subjected to three watering regimes: well-watered, early-season drought, or late-season drought.
  - Drought events lasted 10 days with a mid-drought watering pulse to prevent total desiccation.
  - Early drought occurred pre-anthesis (booting to flag leaf sheath extension); late drought occurred post-anthesis (late milk to early dough).
  - Pest management: one fungicide application and three insecticide applications as needed; fertilizer (ammonium nitrate, ~80 kg/ha) applied after anthesis.

- Measurements and data collection
  - Growth stages: assessed using the Tottman decimal growth stage system on four occasions (9 Jun, 30 Jun, 14 Jul, 27 Jul) across four pots per ozone/drought treatment.
  - Chlorophyll content index (CCI): 523 measurements across 28 days (May–July) on the most recently fully expanded leaf; two chlorophyll meters used with calibration line standardization.
  - Stomatal conductance to water: 318 measurements across 9 days (27 May–22 Jul) on the flag leaf; measured with AP4 leaf porometer; concurrently measured soil water content (SWC).
  - Calibration and measurement practices: porometer calibrated daily; measurements taken under physiologically active daytime conditions (10:00–16:00) and across varied meteorological conditions to support model parameterization.
  - Canopy and microclimate data: temperature, PAR, relative humidity monitored; meteorological data linked to observations.

- Harvest and yield data
  - Harvest window: 5–12 August 2015 after flag leaf senescence and grain drying onset.
  - Procedure: non-edge plants harvested; straw separated from ears; grains threshing by hand; fresh and dry weights recorded (drying at 65°C for one week); data quality checks and re-weighing where needed.
  - Post-harvest processing ensured data consistency and recalibration of scales as necessary.

- Data structure and content (files)
  - Mulika_growth_stage_data_2015.csv
    - 320 observations, 9 variables
    - Key fields: Date_of_measurement, Day_of_year, solardome_number, Ozone_profile, Seasonal_POD6_bespoke_DO3SE, 24h_mean_ozone_ppb, Watering treatment, Pot_ID, Maximum_decimal_growth_stage.
  - Mulika_harvest_2015.csv
    - 96 observations, 26 variables
    - Key fields: Dome_number, Ozone_profile, Target_24h_mean_O3, Measured_24h_mean_O3, AOT40_ppm, POD6_bespokeDO3SE, Watering_treatment, Pot_ID, presence_of_aphids, various yield and biomass metrics (e.g., Ear_weight_in_sample_g, Grain metrics, Harvest_index, Yield_kg/m2, Yield_kg/ha).
  - Mulika_CCI_2015.csv
    - 524 observations, 11 variables
    - Key fields: Person_measuring, Date_of_measurement, Day_of_year, solardome_number, pot_ID, watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, Chlorophyll_content_index, Soil_moisture_content_%, time_canopy_record, PAR and temperature context fields.
  - Mulika_stomatal_conductance_2015.csv
    - 318 observations, 17 variables
    - Key fields: Date_of_measurement, Day_of_year, time_of_day, Solardome_number, Watering_treatment, Current_watering_status, stomatal_cond_adaxial_water, stomatal_cond_abaxial_water, stomatal_cond_adaxial_ozone, stomatal_cond_PLA_ozone, Soil_moisture_content_%, Time_canopy_computer_recording, Relative_humidity_in_dome7, PAR_in_dome7, corrected_dome_7_temperature, corrected_dome_7_VPD.

- Data provenance, references, and methodological context
  - References to related work and background on ozone exposure, climate context, and measurement methodologies (e.g., Mills et al. 2009; Hayes et al. 2015; Tottman 1987; IPCC 2013; DO3SE modeling for POD6).
  - Data descriptions include explicit units, measurement definitions, and calculation notes (e.g., POD6 calculated with wheat cultivar parameterization, PLA conversions for stomatal conductance, and area-based scaling for yield estimates).

- Data governance and stewardship considerations
  - The dataset is organized into clearly defined files with explicit variable names, definitions, units, and measurement contexts to facilitate discovery, reuse, and interoperability.
  - Documentation notes include calibration procedures, measurement timing, randomization, and statistical handling of limitations (notably lack of replication; addressed via mixed-model analysis).
  - Key challenges highlighted include incomplete alignment with user needs, timely data acquisition, diverse systems/formats, large data volumes, and legacy or bespoke instrumentation; these are mitigated by comprehensive metadata and standardized data structures in the provided files.