# Summary

## Experimental Context and Location
- Rural site in North Wales, UK, part of Bangor University farm; near the sea.
- Eight solardomes (hemispherical glasshouses) used in 2017 experiments; three heated to +7°C to mimic tropical/subtropical conditions; ozone added per a set weekly profile and controlled by LabView.
- Ozone exposure occurred day and night; plants were watered as needed; ozone exposure ended at different times for different species.
- Site coordinates: 53°14'N, 4°01'W; elevation 15 m.

## Experimental Design and Treatments
- Four replicate pots per species/cultivar grown from seed and exposed to ozone in the solardomes.
- Treatments:
  - Low ozone, unheated (35 ppb peak)
  - Medium ozone, unheated (80 ppb peak)
  - High ozone, unheated (115 ppb peak)
  - Low ozone, heated (35 ppb peak, ambient +7°C)
  - Medium ozone, heated (80 ppb peak, ambient +7°C)
  - High ozone, heated (115 ppb peak, ambient +7°C)
- Species include multiple wheat cultivars, pearl millet, beans/cowpeas, finger millet, etc., with start and end dates spanning 18/05/2017 to 25/07/2017 for most entries; some pearl millet and other species had staggered end dates.

## Data Collected and Variables
- Ozone exposure and meteorology logged continuously with hourly resolution.
- Plant measurements included stomatal conductance, soil moisture, chlorophyll content index, yield, and biomass; stomatal conductance measured ad-hoc during exposure.
- Data files include:
  - Ozone and meteorology (hourly, 2017)
  - Plant physiology (per-plant measurements, intermittent)
  - Biomass and yield (end-of-experiment yield per plant/pot)

## Data Files and Schema
- Biomass_and_Yield_2017.csv (17 columns): species/variety, treatment, pot/replicate info, pod/seed metrics, biomass/yield indicators, and derived averages (e.g., pod weight, beans per pod, total grains per pot, 100-grain weight).
- Ozone_and_meteorology_2017.csv (11 columns): treatment, day-of-year, date, hour, hourly ozone (ppb), light, temperature, vapor pressure deficit, air pressure, windspeed, precipitation.
- Plant_Physiology_2017.csv (11 columns): treatment, plant species, pot, date/time, leaf side, stomatal conductance, PAR, leaf temperature, soil moisture, chlorophyll content index.
- Columns include flags for missing readings; some data gaps due to faults are noted.

## Data Collection Methods and Instrumentation
- Ozone and meteorology: automated logging via LabView; QA checks for range validity, plausibility, and gap filling as needed.
- Plant physiology: ad-hoc measurements with QA checks.
- Instruments:
  - LabView-controlled ozone/meteorology system (solardomes)
  - AP4 porometer for stomatal conductance
  - Delta-T theta probe for soil moisture
  - CCM-200 for chlorophyll content index

## Calibration and Quality Control
- Ozone analysers calibrated by external company (Air Monitors Ltd).
- AP4 porometer calibrated daily per manufacturer guidance.
- CCM-200 autocalibration as part of startup procedure.
- Data QA includes plausibility checks and range validation; missing values noted and addressed during gap filling.

## Gap Filling, Data Processing and Provenance
- Gap filling protocol documented and original data preserved separately as filled and corrected copies.
- Gaps identified to ensure 24 hourly data per day; small gaps (≤5 hours) filled by averaging adjacent values.
- Larger gaps resolved by consulting lab notes; values from previous/next day used to fill, aiming to preserve daily patterns; if the system was off, gaps filled with a 5 ppb dummy value.
- Anomalous readings (e.g., implausible spikes) corrected using surrounding values to maintain data integrity.
- When data are altered, changes are stored in separate worksheets/files labeled as filled and corrected.

## Data Availability, Structure and Documentation
- Three CSV data files comprising 11–17 columns each; some readings missing (blank cells) due to measurement gaps or faults.
- Documentation notes on data structure, unit conventions, and the specific meaning of each column header (e.g., treatment abbreviations, date/time formats, measured variables).
- Gap filling and QA procedures are documented (including Appendix 1 reference) to support traceability and reproducibility.

## Additional Resources and Notes
- Facility overview available at: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-field-releasesystem
- Analytical methods not applied to these data within this record; focus is on data collection, QA, and gap management to support future analyses.