# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment at Clocaenog Forest (upland moorland) using automated roof technology to simulate drought and warming over the next 20–30 years.
- Site established in 1998; conditions reflect typical upland west-atlantic moorland with Calluna vulgaris and other species; soil is humo-ferric podzol; coordinates: 53°03'19"N, -3°27'55"W.

## Objectives and scope for data users

- Documented multi-parameter datasets spanning meteorology, hydrology, soil–plant processes, and vegetation responses.
- Data intended to support exploration of climate-treatments effects on ecosystem structure and function, with potential for cross-disciplinary analysis (abiotic, biotic, chemical, and flux data).
- Datasets are stored in the CEH data ecosystem (EIDC) with emphasis on long-term records; note that not all data collected since 2015 may be stored there.

## Climate change treatments and experimental design

- Treatments: drought and warming, each with three replicates, plus three control plots (total n = 9 plots).
- Drought: operational May–Sept (1999–2011); extended to Apr–Oct since 2012. Implemented with retractable polyethylene roofs that exclude rainfall, reducing annual rainfall by ~20% and growing-season rainfall by up to ~80% in affected periods.
- Warming: nighttime warming via retractable aluminum curtains that reflect infrared radiation; rainfall avoidance logic retracted curtains during rain to maintain rainfall patterns. Curtains not operated in winds >10 m s-1.
- Experimental layout uses blocks to mirror shading effects; treatments designed to capture warming and drought effects with replicates and controls.

## Data streams and representative datasets

- AWS meteorological data: daily measurements (air temperature, relative humidity, rainfall, barometric pressure, net radiation, solar radiation, PAR, wind).
  - Dataset: Daily automated weather station data_1999to2015_Clocaenog.csv
- Micro-meteorological plot data: plot-scale soil and air temperature, soil moisture; daily resolution.
  - Dataset: Daily micromet data_1998to2015_Clocaenog.csv
- Rainfall and rainfall chemistry: site-level rainfall from storage gauge with biweekly samples for chemistry (pH, NO3, Cl, SO4, DOC, NH4, etc.); throughfall data for plot-level rainfall.
  - Datasets: Rainfall_Clocaenog.csv; Throughfall_Clocaenog.csv
- Hydrology: water table depth from permeable tubes (biweekly measurements since 2009; max detectable depths per plot varied).
  - Dataset: Water table depth_Clocaenog.csv
- Soil respiration: soil CO2 efflux measured with collars; multiple measurement systems over time (CIRAS-2, LI-COR 8100, automated systems); 1999–present with varying collar configurations.
  - Datasets: Fortnightly soil respiration_Clocaenog.csv; High_resolution_soil respiration_Clocaenog.csv
- Trace gases: CH4 and N2O fluxes using the same collars with static chambers and GC analysis.
  - Dataset: Trace gases_Clocaenog.csv
- Net ecosystem CO2 exchange (NEE): chamber-based flux measurements in several years using CIRAS-2 or LI-COR systems; includes adjustments for biomass.
  - Dataset: Net ecosystem exchange_Clocaenog.csv
- Photosynthesis: ambient measurements and response curves (PAR and Ci) for dominant species; several years and conditions (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum).
  - Datasets: Photosynthesis_Clocaenog.csv; Photosynthesis_response_Clocaenog.csv
- Vegetation biomass and structure: Pin-point vegetation survey across multiple years; biomass conversions from pin hits; detailed species-code system.
  - Dataset: Vegetation survey_Clocaenog.csv
- Canopy reflectance: ground-based spectral measurements (NDVI and PRI indices) from 2001–2004 with calibration against bare ground.
  - Dataset: Canopy reflectance_Clocaenog.csv
- Phenology, annual growth, and pathogens: shoot elongation and phenophase assessments for C. vulgaris, V. myrtillus, and E. nigrum; annual growth metrics collected periodically.
  - Dataset: Phenology Growth Pathogens_Clocaenog.csv
- Vegetation chemistry: elemental analyses (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) on green and litter material.
  - Dataset: Vegetation chemistry_Clocaenog.csv
- Litterfall: monthly collections (1999–2002); later collections less frequent; conversion to g m-2 and subsequent chemical analyses.
  - Dataset: Litterfall.csv
- Root biomass: soil core-based root extraction across multiple years and methods (2003–2013); depth-stratified analysis.
  - Dataset: Root biomass.csv
- Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012) with DOC-based biomass estimation.
  - Dataset: Soil microbial biomass.csv
- Nitrogen mineralisation and SOM/SOC: paired core method to estimate net mineralisation; SOM/SOC content and bulk density derived from cores; 1998–2004 and 2013+ datasets.
  - Datasets: Nitrogen mineralisation.csv; Soil organic matter carbon density.csv
- Soil solution and leachate chemistry: lysimeter and tensioned suction samplers (biweekly); pH, nitrate, chloride, sulfate, DOC, ammonium analyses.
  - Dataset: Water chemistry.csv

## Data collection, processing, and quality controls

- Instruments and procedures vary over time; e.g., AWS moved from 1 m to 4 m height after 2007 due to theft; plot-level sensors for micro-meteorology introduced from 1998 onward.
- Data collection frequency: daily (weather), daily to fortnightly (soil and plot measurements), monthly to yearly for some soil and vegetation measurements; many datasets are infrequent or irregular in early years.
- Data processing notes:
  - Unit conversions provided for CO2 flux (g m-2 h-1 and µmol m-2 s-1 to mg C m-2 h-1) and for deriving biomass-adjusted fluxes.
  - Pin-point biomass: conversion factors from pin-hits to biomass established via destructive calibration; annual updates and quality checks performed.
  - NEE and photosynthesis calculations adjust for biomass differences among chambers.
  - Litterfall data pooled by quadrats and years; conversion to g m-2 with subsequent chemical analyses.
- Data quality and limitations:
  - Early data processing described as legacy; best-practice documentation may be incomplete for some datasets.
  - Throughfall calculations rely on site-scale rainfall and may exclude plot-level measurements when data gaps occur; occasional data infilling used for treatment means.
  - Some datasets stored outside the main data hub after 2015; contact CEH Bangor for details.

## Access, contact, and metadata notes

- Primary data management and documentation lead: Sabine Reinsch and Bridget Emmett (CEH Bangor).
- The data are primarily stored in the EIDC; some smaller or post-2015 datasets may reside outside this repository.
- For additional details, data provenance, or specific methodological notes, contact the listed authors.

## Appendix and site layout references

- Appendix 1: Site layout and plot layout (quadrats, LYS, PQ, SS identifiers).
- Appendix 3: Plot layout with quadrats and measurement areas.
- Geographic and soil context: green shrub-dominated heath, bryophyte-rich understory, heterogenous horizon development (Eg, Bh horizons) in humo-ferric podzol soils; Ordovician–Silurian geology background.