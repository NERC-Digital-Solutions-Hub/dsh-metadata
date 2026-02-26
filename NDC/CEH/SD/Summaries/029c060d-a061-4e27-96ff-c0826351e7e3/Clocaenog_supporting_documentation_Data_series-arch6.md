# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climate change manipulation site at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over 20–30 years.
- Established in 1998; features replicated drought and warming treatments plus controls.
- Extensive, long-running dataset covering meteorology, soil/plant processes, and ecosystem exchanges.
- Data are primarily stored as CSV files with accompanying documentation in .rtf; not all data are stored in a single data portal (EIDC).

## Data sources and datasets
- AWS meteorological data
  - Daily automated weather station data (Daily automated weather station data_1999to2015_Clocaenog.csv)
  - Micro-meteorological plot data (Daily micromet data_1998to2015_Clocaenog.csv)
- Rainfall and rainfall chemistry
  - Rainfall at site (Rainfall_Clocaenog.csv)
  - Throughfall data by plot (Throughfall_Clocaenog.csv)
  - Rainfall chemistry (in Rainfall_Clocaenog.csv; sampling and analysis described)
- Hydrology
  - Water table depth (Water table depth_Clocaenog.csv)
- Ecosystem and soil processes
  - Soil respiration (Fortnightly soil respiration_Clocaenog.csv; Automated soil respiration_Clocaenog.csv)
  - Trace gases CH4 and N2O (Trace gases_Clocaenog.csv)
  - Net ecosystem CO2 exchange (Net ecosystem exchange_Clocaenog.csv)
  - Photosynthesis (Photosynthesis_Clocaenog.csv)
  - Vegetation biomass surveys (Vegetation survey_Clocaenog.csv; Pin-point method; biomass calibration)
  - Canopy reflectance (Canopy reflectance_Clocaenog.csv)
  - Vegetation phenology, annual growth and pathogen assessment (Phenology Growth Pathogens_Clocaenog.csv)
  - Vegetation chemistry (Vegetation chemistry_Clocaenog.csv)
  - Litterfall (Litterfall.csv)
  - Root biomass (Root biomass.csv)
  - Soil microbial biomass (Soil microbial biomass.csv)
  - Nitrogen mineralisation (Nitrogen mineralisation.csv)
  - Soil organic matter and carbon data (Soil organic matter carbon density.csv; SOC and bulk density conversions)
  - Soil solution and leachate chemistry (Water chemistry.csv)
- Documentation and codes
  - Supporting documentation files (.rtf) accompany each dataset
  - Appendix 1–3 include site layout and quadrat details

## Measurements, timeframes and methods (highlights)
- Time span: data spanning late 1990s to around 2015+ for many datasets; ongoing updates noted in documentation.
- Frequencies: daily (weather and micro-meteorology), fortnights to monthly (soil respiration, rainfall throughfall, lysimeters), annual to multi-year (vegetation surveys, chemistry, litterfall, biomass).
- Methods overview:
  - AWS sensors at ~4 m height; hourly averages from 1999–present with quality checks.
  - Micro-met plots track soil temperature, moisture; daily data collection.
  - Drought treatment uses retractable roof to reduce rainfall; warming uses night-time infrared-reflective curtains, with rain-triggered retraction.
  - Throughfall and rainfall data adjusted to estimate plot-level rainfall relative to site-level rainfall.
  - Soil respiration and trace gases collected with closed-chamber methods; various instrument transitions over time (CIRAS-2, LICOR LI-8100, automated systems).
  - Net ecosystem exchange and photosynthesis computed with adjustments for biomass and calibration.
  - Pin-point vegetation surveys convert hits to biomass using species-specific calibration; yearly, with pre-1998 baseline and later years.
  - Canopy reflectance and phenology – spectral indices (NDVI, PRI) and phenological stages documented.
  - Soil chemistry and biogeochemistry (SOM, SOC, nutrients, pH, leachates) collected via lysimeters and soil cores; multiple lab analyses described.
- Data processing notes:
  - Legacy data; some processing steps not documented with modern best practices.
  - Unit conversions provided for CO2 flux (g CO2 m-2 h-1 and µmol m-2 s-1 to mg CO2-C m-2 h-1) and biomass adjustments for NEE.
  - Data quality controlled via basic visual/Excel checks; data gaps excluded from treatment means when data are missing or compromised.

## Climate change treatments (experimental design)
- Drought (D): retractable polyethylene roof reduces rainfall; timing typically May–September (1999–2011) and April–October since 2012; ~20% reduction in annual rainfall, excluding large events depending on sensor limits; curtains do not operate in high winds (>10 m s-1).
- Warming (W): retractable aluminum mesh curtains that reflect infrared radiation, reducing heat loss at night; rain-triggered retraction to preserve rainfall; average annual rainfall reduction ~14%; operation timing tied to night-time conditions and weather.

## Site and ecosystem context
- Location: Clocaenog Forest, North East Wales; upland moorland dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum.
- Soil: humo-ferric podzol with variable eluvial/illuvial horizons.
- Experiment scale: 9 plots total (3 warming, 3 drought, 3 controls) arranged in blocks; plots sized 4 m x 5 m.
- Appendix resources: site layout and quadrat layouts provided to map measurement points.

## Data access, quality, and contacts
- Not all datasets are stored in a single repository (EIDC); several smaller or post-2015 datasets may reside elsewhere.
- Primary data producers/curators: Alwyn Sowerby (author) and Sabine Reinsch; continuing contact for data specifics via CEH Bangor.
- Key contact for data details and access: Sabine Reinsch (sabrei@ceh.ac.uk) or Bridget Emmett (bae@ceh.ac.uk).
- Note: Where data are incomplete or data collection varied (e.g., throughfall gaps, plot exclusions due to data loss), these limitations are described in the dataset documentation.

## Practical implications for data support and reuse
- Rich, multi-taxa, multi-method time-series suitable for cross-dataset dashboards and integrative analyses (e.g., NEE, GPP, respiration, moisture, nutrients, litter).
- Requires careful handling of heterogeneous data formats, units, and legacy processing steps; rely on the provided dataset-specific metadata and conversion notes.
- Use throughfall-adjusted rainfall and site-level rainfall foundations to estimate plot-level hydrology metrics.
- For completeness and reproducibility, coordinate with CEH Bangor maintainers for access to updated or non-public datasets and to obtain any missing data or clarifications.