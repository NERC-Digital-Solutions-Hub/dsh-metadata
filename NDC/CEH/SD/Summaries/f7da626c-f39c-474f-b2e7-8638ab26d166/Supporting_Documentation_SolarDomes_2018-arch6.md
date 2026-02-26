# Summary Description of experiment location - Rural site in North Wales, UK.

- Overview of the experimental site
  - Rural site in North Wales, UK; part of Bangor University farm; near the sea
  - Coordinates: 53°14'N, 4°01'W; elevation 15 m
  - Eight solardomes used in 2018; three heated to ~+7°C to mimic tropical/subtropical conditions
  - Ozone is added following a set weekly profile, controlled by LabView; ozone applied at night and day
  - Plants watered as required during ozone exposure; exposure ends at different times for different species

- Experimental design and treatments
  - Four replicate pots per species/cultivar; grown from seed and exposed to ozone
  - Continuous hourly sampling of ozone and meteorological conditions
  - Ad-hoc measurements of stomatal conductance with soil moisture and chlorophyll content index; biomass/yield measured at harvest
  - Species/cultivar measurements include multiple beans, cowpeas, amaranth, and sorghum varieties with start and end exposure dates
  - Treatment categories (combinations of ozone level and temperature regime) described to cover low/medium/high ozone and ambient vs elevated temperatures

- Data collected and instruments
  - Ozone and meteorology: hourly logged, QA checks for range, plausibility, and gap-filling
  - Plant physiology: ad-hoc measurements (stomatal conductance, soil moisture, chlorophyll content index)
  - Biomass and yield: end-of-experiment measurements; species-specific notes on what was measured (e.g., seed heads for amaranth)
  - Instruments and methods:
    - Ozone exposure system controlled by LabView
    - AP4 porometer for stomatal conductance
    - Theta probe for soil moisture
    - CCM-200 for chlorophyll content index

- Data files and structure
  - Biomass_and_Yield_2018.csv
    - 14 columns; including species, treatment, pot, pod/bean counts and weights, total biomass, seed head data, and derived averages
    - Indicates some measurements not taken for certain crops (e.g., seed in amaranth)
  - Ozone_and_meteorology_2018.csv
    - 11 columns; includes Treatment, DOY/Date/Hour, hourly ozone, and meteorological variables (Light, Temperature, VPD, Pressure, Windspeed, Precipitation)
    - Gaps filled via internal protocol; windspeed constant due to dome fans; air pressure and precipitation provided as constants for DO3SE modeling
  - Plant_Physiology_2018.csv
    - 12 columns; includes Treatment, species, replicate, date/time, relative humidity, stomatal conductance, light, temperature, soil moisture, chlorophyll index, etc.
    - Blank cells indicate readings not taken; some readings missing due to instrument issues

- Data quality control and processing
  - QA procedures:
    - Ozone/met data: range checks, plausibility checks, gap filling
    - Plant physiology: plausibility checks; ad-hoc data reviewed
    - Biomass/yield: range checks; plausibility checks
  - Data processing notes:
    - Three primary CSV files plus a structured QA history; original data preserved alongside amended versions
    - Appendix 1 describes gap-filling methodology to maintain hourly DO3SE compatibility

- Gap filling and data correction (Appendix 1)
  - Identify daily hourly data gaps; ensure 24 hourly records per day
  - For gaps ≤ 5 consecutive hours: fill with average of surrounding values
  - For larger gaps: consult lab book; fill using previous/next day values, adjusted to preserve patterns
  - When ozone system not running: fill with a dummy value (5 ppb)
  - Outliers and unrealistic values flagged and corrected using surrounding data
  - All modifications saved as a separate “filled and corrected” dataset; originals preserved with change logs

- Calibration and instrumentation details
  - AP4 Porometer: daily calibration per manufacturer instructions
  - Ozone analysers: calibrated by external supplier
  - CCM-200: autocalibration step in startup
  - DO3SE model inputs rely on constant air pressure, wind speed, and precip values in the dataset

- Metadata and accessibility
  - Experimental facility description available at CEH: solardomes and ozone field release system
  - Data resources include explicit file names, column counts, and notes on missing data
  - Blank cells indicate missing readings; minor data gaps acknowledged and documented with gap-filling procedures

- Information for data reuse
  - Clear delineation of data files and their contents facilitates cross-file joins (treatment, date/time, species, measurements)
  - Detailed gap-filling appendix supports reproducibility and traceability of data adjustments
  - Notes on measurement limitations (e.g., certain crops not yielding, missing photometric readings) help contextualize analyses

- Practical notes for data users
  - DO3SE requires hourly time-step data and consistent auxiliary variables (air pressure, wind, precip)
  - Some columns have placeholders or constant values to support modeling and data integrity
  - Users should reference the gap-filling procedures and data QA sections when interpreting filled data vs. raw data

- Additional resources
  - Related data and facility information: link to the CEH solardomes and ozone field release system page
  - Appendix 1 provides explicit gap-filling procedures and data handling steps used in this dataset