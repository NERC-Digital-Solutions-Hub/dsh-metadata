# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose: A climate change manipulation experiment using automated roof technology to simulate drought and warming conditions predicted for the next 20–30 years in upland moorland.
- Location and habitat: Clocaenog Forest, North East Wales (53°03'19"N, 3°27'55"W); upland west-atlantic moorland dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum; soil is humo-ferric podzol.
- Site history and layout: Established in 1998; replicated drought and warming treatments across 9 plots (3 per treatment + 3 controls) arranged in blocks.
- Treatments:
  - Drought (D): Retractable polyethylene roof over each plot to reduce rainfall; targeted ~20% annual rainfall reduction; May–Sept operation 1999–2011, April–October since 2012; curtains disabled in high winds (>10 m/s).
  - Warming (W): Retractable aluminium mesh curtains to reduce nighttime heat loss; canopy cooling reduces infrared loss; rain retraction mechanism reopens after rainfall to limit rainfall exclusion; ~14% annual rainfall reduction; curtains disabled in high winds.
  - Controls (C): Scaffolding to mirror shading from treatment structures; 3 controls per block to match local shading.
- Climate context: Site mean annual temp ~8.0°C; mean control soil temperature ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha⁻¹ yr⁻¹; soil horizon structure and horizon depths vary across the site.
- Data scope and purpose for analysts: A comprehensive, long-term, multi-parameter data suite (abiotic and biotic) to analyse climate manipulation effects on ecosystem processes and productivity; datasets span meteorology, soil respiration, trace gases, net CO2 exchange, vegetation dynamics, litter, roots, soils, and chemistry.

## 1.0 Site information highlights

- Automated climate manipulation site designed for sensitivity to upland moorland responses and powered by solar and wind.
- Plot design: 4 m x 5 m plots; 3 replicates per treatment (D, W, C) totaling 9 plots; treatment schedule and block design described.
- Biophysical setting: Heather-dominated vegetation with bryophytes and several vascular plants; E and Bh soil horizons variably visible; soil type and parent material detailed.

## 2.0 Climate change treatment information highlights

- Drought treatment details:
  - Timing: May–Sept (1999–2011), April–October since 2012.
  - Mechanism: Retractable roof that excludes rainfall; approximate annual rainfall reduction ~20%, with larger fraction of smaller events excluded (~80% of rain excluded during drought periods).
  - Wind considerations: Curtains paused in winds >10 m s⁻¹.
- Warming treatment details:
  - Mechanism: Retractable aluminium mesh curtains reflecting infrared radiation; night-time warming with minimized heat loss.
  - Rain interaction: Roof retraction occurs after rain to minimize rainfall exclusion; approximate annual rainfall reduction ~14%.
  - Wind considerations: Curtains paused in winds >10 m s⁻¹.
- Data on climate metrics (Tables 1 and 2): Site climate parameters across years (mean air/soil temps, rainfall, N deposition) and warming GDD changes documented; some years lack complete data (NA entries noted).

## 3.0 Equipment, protocols and data processing methodology highlights

- Data infrastructure:
  - On-site Automated Weather Station (AWS) for meteorological data (daily, hourly-derived data since 1999–present).
  - Micro-meteorological plots for soil and air temperatures and soil moisture (daily, from 1998–present with updates to instrumentation).
  - Ground-level rainfall gauges and rainfall chemistry collectors (biweekly to monthly data; site-level rainfall used to scale plot-level throughfall data).
  - Throughfall collectors (plot-level rainfall, biweekly); data are used to estimate plot rainfall changes relative to site rainfall.
  - Lysimeters and tensioned samplers for soil solution and leachate chemistry (biweekly sampling; 1998–present for various components).
- Data types and datasets (examples):
  - AWS meteorological data (Daily automated weather station data_1999to2015_Clocaenog.csv) with multiple sensors (temperature, humidity, rainfall, solar and net radiation, PAR, wind).
  - Micro-meteorological plot data (Daily micromet data_1998to2015_Clocaenog.csv).
  - Rainfall and rainfall chemistry (Rainfall_Clocaenog.csv) and Throughfall_Clocaenog.csv.
  - Water table depth (Water table depth_Clocaenog.csv).
  - Soil processes: Fortnightly soil respiration_Clocaenog.csv, Automated soil respiration_Clocaenog.csv; Trace gases (Trace gases_Clocaenog.csv); Net ecosystem exchange (Net ecosystem exchange_Clocaenog.csv); Photosynthesis (Photosynthesis_Clocaenog.csv).
  - Vegetation and soils: Vegetation survey_Clocaenog.csv (Pin-point biomass via quadrats), Canopy reflectance_Clocaenog.csv, Phenology Growth Pathogens_Clocaenog.csv, Vegetation chemistry_Clocaenog.csv, Litterfall_Clocaenog.csv, Root biomass_Clocaenog.csv, Soil microbial biomass_Clocaenog.csv, Nitrogen mineralisation_Clocaenog.csv, SOM/SOC and bulk density, Soil organic matter carbon density_Clocaenog.csv, Water chemistry_Clocaenog.csv.
- Measurement methods and frequency (highlights):
  - AWS sensors: Temperature, humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind; hourly daily time scale; data quality checked visually.
  - Micro-met: Soil temperatures at multiple depths; soil moisture via TDR and previously theta probes; daily sampling.
  - Gas fluxes: Soil respiration and trace gases using chamber methods (static/open systems) and IRGA/Li-COR analyzers; varying historical instrumentation (CIRAS-2, LICOR 8100, automated LI-COR 8100) with detailed unit conversions.
  - NEE and photosynthesis: Chamber-based CO2 flux measurements with biomass normalization (above-ground biomass from pin-point data and calibration from destructive sampling).
  - Vegetation: Pin-point biomass surveys (1998–2012, and ongoing); species-level calibration (Table 6) translating pin hits to biomass (g m⁻²).
  - Canopy reflectance: Ground-based spectrometer measurements for NDVI and PRI indices (2001–2004; 2000–2004 windows).
  - Phenology and pathogens: Shoot elongation and phenophase tracking for C. vulgaris, V. myrtillus, E. nigrum.
  - Litter and soils: Litterfall collection and chemical analyses; root biomass from multiple years using varied core methods; soil microbial biomass via chloroform fumigation; nitrogen mineralisation via KCl extraction and NO3/NH4 analyses.
  - Soil chemistry and SOM: Lysimeter and tensioned sampler analyses; pH, nitrate, chloride, sulfate, DOC, ammonium; SOM and SOC content with bulk density calculations.
- Data processing notes:
  - Legacy data exist; some documentation of data processing may not reflect current best practices.
  - Data are transformed to consistent CO2 flux units (mg CO2-C m⁻² h⁻¹) with unit conversion factors described.
  - Throughfall data require adjustments to represent plot-level rainfall via percent-change application to site rainfall; data gaps are handled by exclusion or infilling using mean reductions.
- Data access and contacts:
  - Primary data storage and access through CEH Bangor; contact Sabine Reinsch (sabrei@ceh.ac.uk) or Bridget Emmett (bae@ceh.ac.uk) for details.
  - Some datasets not stored in the EIDC; metadata and supporting documentation accompany each dataset.

## Key datasets and documentation

- Datasets mentioned include: AWS meteorological data, daily micromet data, Rainfall_Clocaenog.csv, Throughfall_Clocaenog.csv, Water table depth_Clocaenog.csv, Fortnightly soil respiration_Clocaenog.csv, Automated soil respiration_Clocaenog.csv, Trace gases_Clocaenog.csv, Net ecosystem exchange_Clocaenog.csv, Photosynthesis_Clocaenog.csv, Vegetation survey_Clocaenog.csv, Canopy reflectance_Clocaenog.csv, Phenology Growth Pathogens_Clocaenog.csv, Vegetation chemistry_Clocaenog.csv, Litterfall_Clocaenog.csv, Root biomass_Clocaenog.csv, Soil microbial biomass_Clocaenog.csv, Nitrogen mineralisation_Clocaenog.csv, Soil organic matter carbon density_Clocaenog.csv, Water chemistry_Clocaenog.csv.
- Supporting documentation files (RTF) accompany each dataset, providing methods and processing details.

## Appendices and site layout

- Appendix 1: Site layout and plot references.
- Appendix 2: Quadrat layout and quadrat codes; plot identifiers (LYS, PQ, SS).
- Appendix 3: Plot layout with quadrats and measurement areas.

- Note: The Climoor site data enable cross-cutting analyses of drought and warming effects on ecosystem processes, but users should account for legacy data practices and incomplete years when integrating across datasets.