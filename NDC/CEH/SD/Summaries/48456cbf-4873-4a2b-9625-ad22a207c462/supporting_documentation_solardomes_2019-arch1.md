# Ozone and Meteorology 2019 Dataset from Solardomes Experiment

- Location and setup
  - Rural site in North Wales, UK, part of Bangor University farm; near the sea at 53°14'N, 4°01'W, 15 m ASL.
  - Eight solardomes (hemi-spherical glasshouses) used in 2019; ozone is computer-controlled and logged hourly.
  - Three solardomes were heated by +7°C to simulate tropical/subtropical conditions; plant biomass/physiology data available only for these three heated domes.
  - Ozone exposure follows a weekly cycle with night and day additions.

- Experimental design
  - Four replicate pots per species/cultivar grown from seed and exposed to ozone in the solardomes.
  - Continuous hourly logging of ozone and meteorological conditions; ad-hoc plant measurements (stomatal conductance, soil moisture, chlorophyll content).
  - Exposure length varied by species/cultivar; end-of-study biomass/yield measured for all.
  - Species included sweet potato (physiology data available) and several beans (yield data).

- Treatments
  - Low ozone, heated: target peak ~35 ppb, ambient temp +7°C
  - Medium ozone, heated: target peak ~80 ppb, ambient temp +7°C
  - High ozone, heated: target peak ~115 ppb, ambient temp +7°C

- Data collection and instrumentation
  - Ozone and meteorology logged with LabView software; QA to ensure plausible ranges; gap-filled as needed.
  - Plant physiology: stomatal conductance (AP4 porometer), soil moisture (theta probe), chlorophyll content index (CCM-200).
  - Biomass/yield measured at end of exposure.

- Calibration and quality control
  - AP4 porometer calibrated daily per manufacturer instructions.
  - Ozone analysers calibrated externally.
  - CCM-200 autocalibration during use.
  - QA checks for data range, plausibility of outliers, and gap filling where necessary.

- Data resources (files and contents)
  - Biomass_and_Yield_2019.csv: 63 rows, 11 columns; includes plant species, treatment, pot/pod metrics, pod/bean weights, bean counts, and tuber yield for sweet potato.
  - Ozone_and_meteorology_2019.csv: 10,008 rows, 11 columns; hourly ozone, meteorology (including Day_of_Year, Date, Hour_of_Day, temperature, humidity, wind, pressure, etc.); includes fixed values for wind and a dummy 1 mm/hour precipitation to enable DO3SE model runs.
  - Plant_Physiology_2019.csv: 692 rows, 12 columns; plant physiology data (only for sweet potato); contains blank cells where readings were not taken.
  - Notes: Some segments may have missing readings; data gaps are documented and subject to gap-filling procedures described below.

- Gap filling and data correction protocol
  - Maintain an original and an amended copy; all changes logged.
  - Ensure 24 hourly entries per day; gaps ≤5 hours filled by average of surrounding values.
  - Larger gaps: use values from the previous and next day, adjusted to preserve patterns; if the system was off, fill with a 5 ppb dummy value.
  - Identify and flag anomalous values (e.g., <0 ppb) and replace using neighboring values to maintain plausibility.

- Data resource structure and notes
  - Plant_Physiology_2019.csv: 12 columns, 692 rows; readings may be unavailable (blanks); data available only for sweet potato.
  - Ozone_and_meteorology_2019.csv: 11 columns, 10008 rows; contains hourly DO3SE-relevant parameters; constant air pressure and wind for dome conditions.
  - Biomass_and_Yield_2019.csv: 11 columns, 63 rows; yield metrics per pot; notes indicate zero indicates no pods for beans; tuber yield reported for sweet potato only.
  - Blank cells indicate readings not taken or unavailable.

- Miscellaneous and access
  - Further information on the experimental facility available at: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system

- Relevance for data-driven analysis
  - Rich hourly ozone and meteorological time series enabling correlation and model-based analyses of ozone effects on plant physiology and yield.
  - Multi-species design with replicated pots and gradient ozone exposure, including a tropical/heated treatment.
  - Data are accompanied by QA, calibration details, and explicit gap-filling procedures to support reproducibility and transparent analyses.
  - Limitations: plant physiology data limited to sweet potato; some readings missing; DO3SE model inputs rely on fixed values for certain variables (e.g., wind, precipitation) due to experimental setup.