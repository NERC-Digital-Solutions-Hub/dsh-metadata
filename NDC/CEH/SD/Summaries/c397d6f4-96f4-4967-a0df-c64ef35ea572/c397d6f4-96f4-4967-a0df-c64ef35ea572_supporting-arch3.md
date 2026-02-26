# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

## Overview
- The dataset reports soil respiration (Rs) measurements under a seven-year-old Miscanthus x giganteus stand and adjacent April-sown spring barley in the east of the United Kingdom, collected from May to August 2013.
- Measurements used automated chambers and infrared gas analysers (IRGA, LI-8100-101A) with multiplexers to compare Rs between the perennial bioenergy crop and the adjacent cereal crop.
- The study provides detailed data structures, measurement protocols, and data processing steps to support secondary analyses and policy-relevant monitoring.

## Study site and experimental design
- Field setup: comparisons between Miscanthus x giganteus and adjacent barley crops on a farm in eastern UK; full site description referenced to Drewer et al. (2012).
- Replication and placement: six chambers randomly placed within separate plots for each crop, at least 1.5 m apart; chambers mounted on PVC collars inserted ~2 cm into soil.
- Measurement protocol: chambers closed for two minutes per measurement cycle with a 30-second dead band; measurements conducted with no above-ground vegetation included in the flux calculations; collars left in place throughout the study.
- Temporal and environmental context: soil temperature and moisture recorded at 5 cm depth near each collar every 15 minutes; hourly meteorological data (solar radiation, air temperature) collected onsite.

## Data collection and processing
- Flux calculation: Rs fluxes computed as linear regressions of CO2 concentration against time and corrected for chamber volume and temperature using the manufacturer’s software; subsequent analyses performed in SAS 9.3.
- Datasets provided:
  - Dataset 1. Flux_and_soil_data
    - Variables include: DATE, CROP (ARAB = barley, MISC = Miscanthus), DTHOUR, DTQUART, TIME, Rs_Umol (µmol m^-2 s^-1), Rs_mg (mg m^-2 h^-1), Rs_r2, CHAMBERTEMP (°C), AREA (cm^2), ST_C (soil temp at 5 cm, °C), SM_M3M3 (volumetric soil moisture, m3/m3), among others.
    - Additional data fields: CHANNEL (chamber number), Rs_cv, and descriptive metadata about measurement timing and quality indicators.
  - Dataset 2. Met_data
    - Variables include: Datetime, AIRTEMP_C (air temperature, °C), RAD_WMSQ (solar radiation, W/m^2).
- Data organization details: timestamps include Datetime to hourly or 15-minute resolution; explicit units and data formats are documented in the dataset descriptions.

## Data quality, metadata and governance
- Metadata and data dictionaries are included to support reproducibility and verification, including field descriptions, units, and data formats.
- Quality aspects: Rs_r2 provides a measure of fit for each flux calculation; calibration and processing are aligned with manufacturer guidance and documented in the data description (and linked at the data provider's site).
- Governance and openness: dataset is documented with a formal citation and DOI and is associated with the NERC Environmental Information Data Centre, supporting data sharing and reuse. The documentation acknowledges typical monitoring framework challenges such as data gaps, metadata completeness, and the need for clear data governance.

## Accessibility and citations
- Data citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572
- Site and methodological references include:
  - Drewer, J.; Finch, J. W.; Lloyd, C. R.; Baggs, E. M.; Skiba, U. (2012). How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops? Global Change Biology Bioenergy, 4, 408-419.
  - Heinemeyer, A.; Di Bene, C.; Lloyd, A. R.; Tortorella, D.; Baxter, R.; Huntley, B.; Gelsomino, A.; Ineson, P. (2011). Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems, European Journal of Soil Science, 62, 82-94.

## References
- Drewer, J.; Finch, J. W.; Lloyd, C. R.; Baggs, E. M.; Skiba, U. (2012). How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops? Global Change Biology Bioenergy, 4, 408-419.
- Heinemeyer, A.; Di Bene, C.; Lloyd, A. R.; Tortorella, D.; Baxter, R.; Huntley, B.; Gelsomino, A.; Ineson, P. (2011). Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems, European Journal of Soil Science, 62, 82-94.