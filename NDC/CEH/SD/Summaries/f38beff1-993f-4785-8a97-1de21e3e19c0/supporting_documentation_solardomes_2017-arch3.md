# Summary

- Location and facility
  - Rural site in North Wales, UK, part of Bangor University farm near the sea.
  - Eight solardomes used for experiments in 2017; ozone added to filtered air; three domes heated by +7°C to simulate tropical/subtropical conditions.
  - Ozone exposure followed a weekly, computer-controlled profile (LabView); additions occur day and night; plants watered as needed; exposure ends at different times per species.

- Experimental design
  - Four replicate pots per species/cultivar.
  - Continuous hourly sampling of ozone and meteorological conditions in the solardomes.
  - Ad-hoc stomatal conductance measurements with accompanying soil moisture and chlorophyll content index data.
  - End-of-experiment biomass and yield measurements.

- Treatments
  - Six treatments: Low, Medium, High ozone with unheated (ambient temperature) or heated (+7°C).
  - Ozone target peak heights: 35 ppb (low), 80 ppb (medium), 115 ppb (high).

- Data collection and instrumentation
  - Ozone and meteorology logged by PC with QA; gap filling when necessary.
  - Plant physiology data collected ad hoc with QA for range and plausibility.
  - Biomass and yield measured at the end; QA checks applied.

  - Instruments:
    - LabView-controlled solardome ozone/exposure system.
    - AP4 porometer for stomatal conductance.
    - Delta-T theta probe for soil moisture.
    - CCM-200 Chlorophyll Content Index meter.

- Data files and structure
  - Biomass_and_Yield_2017.csv: Yields, pod/bean metrics, weights, pod counts, and derived averages per pot/bean.
  - Ozone_and_meteorology_2017.csv: Treatment, Day of Year, Date, Hour, Ozone_ppb, PAR, temperature, VPD, Air_pressure, Windspeed (dummy), precipitation (dummy).
  - Plant_Physiology_2017.csv: Treatment, Plant_Species, Pot_Number, Date/Time, Leaf_side, stomatal_conductance, PAR, Leaf_Temperature, Soil_Moisture, Chlorophyll_Content_Index.
  - Three CSV files in total; some blank cells indicate missing readings.

- Quality control and calibration
  - Ozone and meteorology data QA for plausible ranges; gap filling as needed.
  - Plant physiology data QA for range and plausibility.
  - Calibration of AP4 porometer (daily), ozone analyzers (external calibration), and CCM-200 autocalibration.

- Data processing and gap filling
  - Gap filling protocol documented with preservation of original data.
  - Ensure 24 hourly rows per day; gaps ≤5 hours filled by averaging surrounding values.
  - Larger gaps reviewed against lab notes; where appropriate, values from previous/next day used to fill, maintaining data patterns.
  - Non-operational periods filled with a dummy 5 ppb ozone value for model runs; amended data saved separately as filled/corrected datasets with a record of changes.

- Metadata and governance
  - Data organized with clear column headings and units; explicit documentation of data collection, QA, calibration, and gap filling.
  - Separate amended datasets maintained to preserve original data; references to model inputs (e.g., DO3SE) and the need for constant wind and air pressure values for modelling.

- Miscellaneous
  - Facility information page: CEH Solardomes and ozone field release system (URL provided in the document).