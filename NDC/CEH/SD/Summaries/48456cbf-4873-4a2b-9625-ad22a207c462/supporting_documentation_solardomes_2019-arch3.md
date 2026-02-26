# Summary

- Objective and scope
  - Document describes a controlled ozone exposure experiment at a rural North Wales site ( Bangor University farm) using eight solardomes to study plant responses to ozone under different temperature regimes.
  - Focus on generating datasets (ozone, meteorology, plant physiology, biomass/yield) to inform environmental health assessments and policy decisions.

- Experimental setup
  - Four replicate pots per species/cultivar grown from seed and exposed to ozone in solardomes.
  - Continuous hourly monitoring of ozone and meteorological conditions; stomatal conductance, soil moisture, and chlorophyll index measured ad-hoc during exposure.
  - Three heated domes (+7°C above ambient) to mimic tropical/subtropical conditions; biomass/physiology data available only for these heated domes.
  - Ozone exposure follows a weekly repeating profile with day and night application; exposure length varied by species due to growing season differences.
  - End-of-experiment biomass or yield measured for all species/cultivars.

- Treatments
  - Low ozone, heated: target peak 35 ppb, ambient temp +7°C
  - Medium ozone, heated: target peak 80 ppb, ambient temp +7°C
  - High ozone, heated: target peak 115 ppb, ambient temp +7°C

- Data collection and instrumentation
  - Ozone and meteorological data logged automatically by PC with hourly values; quality checks and gap-filling as needed.
  - Plant physiology data collected as available; QA checks applied.
  - Instruments:
    - LabView-controlled ozone exposure system
    - AP4 porometer for stomatal conductance
    - Theta probe for soil moisture
    - CCM-200 for chlorophyll content index

- Calibration and data quality
  - AP4 porometer calibrated daily per manufacturer guidelines.
  - Ozone analyzers calibrated by an external provider.
  - CCM-200 autocalibration step required during use.
  - QA processes applied to ensure data plausibility and to identify outliers.

- Data resources and structure
  - Three CSV data files:
    - Biomass_and_Yield_2019.csv: includes plant species/variety, treatment, pot and pod counts, pod and bean weights, average pod/bean weights, beans per pod, total tuber weight (for sweet potato, tuber yield only).
    - Ozone_and_meteorology_2019.csv: includes treatment, day of year, date, hour, hourly ozone ppb, light irradiance (PAR) in dome 7, temperature, vapour pressure deficit, air pressure (constant placeholder for model), wind speed (constant in domes), and precipitation (dummy value to sustain model runs).
    - Plant_Physiology_2019.csv: includes plant physiology measurements (12 columns; 692 rows), with data only for sweet potato.
  - Data gaps noted; blank cells indicate missing readings.
  - Metadata and data structure described; notes on each file’s columns and data completeness.

- Data processing, transformation and gap filling
  - Gap filling protocol to handle missing data while preserving data provenance:
    - Ensure 24 hourly rows exist for each day; gaps up to five consecutive hours filled by averaging adjacent values.
    - Larger gaps investigated via lab book; fill using same time on adjacent days or adjusted values to reflect patterns.
    - If ozone system was off, fill with a dummy value (5 ppb) to reflect no ozone addition.
  - Original datasets preserved separately from filled/corrected versions; changes logged with separate files/workbooks.

- Miscellaneous and accessibility
  - Facility description and further information available at the CEH website: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system
  - Data management and governance considerations include transparency of data processing steps, calibration, QA, and gap-filling procedures to support reproducibility and policy-relevant analysis.

- Relevance to monitoring frameworks
  - Demonstrates end-to-end data governance: clear experimental design, standardized instrumentation, calibration protocols, continuous and ad-hoc measurements, and rigorous QA.
  - Addresses typical monitoring framework challenges: structured data collection, metadata availability (column descriptions and units), handling data gaps with documented procedures, and maintaining originals alongside corrected datasets.
  - Highlights barriers and considerations for policy-oriented monitoring: data accessibility, metadata completeness, data transformation needs (e.g., model inputs like DO3SE), and the necessity of data provenance and transparent gap-handling practices.