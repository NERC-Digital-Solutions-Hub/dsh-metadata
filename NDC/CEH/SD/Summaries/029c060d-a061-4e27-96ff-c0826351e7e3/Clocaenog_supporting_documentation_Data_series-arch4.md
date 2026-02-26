# Climoor field site in Clocaenog forest Supporting documentation for data

- Overview: A climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming treatments for upland moorland over the coming decades. Site established in 1998; solar/wind powered; replicated drought and warming treatments across plots with controls.
- Scope: Comprehensive dataset collection spanning abiotic and biotic measurements from 1998–2015 (with some variables extending earlier/later); data are documented with dataset names, methods, and storage guidance.

## Data assets and datasets (high-level)

- AWS meteorological data: Daily automated weather station data (e.g., Daily automated weather station data_1999to2015_Clocaenog.csv)
- Micro-meteorological data: Plot-level daily micro-met data (e.g., Daily micromet data_1998to2015_Clocaenog.csv)
- Rainfall and chemistry: Storage rain gauge data (Rainfall_Clocaenog.csv) and rainfall chemistry; Throughfall data (Throughfall_Clocaenog.csv)
- Hydrology: Water table depth (Water table depth_Clocaenog.csv)
- Soil respiration and trace gases: Fortnightly and Automated soil respiration (Fortnightly soil respiration_Clocaenog.csv; Automated soil respiration_Clocaenog.csv), Trace gases (Trace gases_Clocaenog.csv)
- Ecosystem fluxes: Net ecosystem exchange (Net ecosystem exchange_Clocaenog.csv)
- Plant physiology and productivity: Photosynthesis (Photosynthesis_Clocaenog.csv); Vegetation biomass (Vegetation survey_Clocaenog.csv)
- Canopy and phenology: Canopy reflectance (Canopy reflectance_Clocaenog.csv); Phenology, growth and pathogens (Phenology Growth Pathogens_Clocaenog.csv)
- Vegetation chemistry and litter: Vegetation chemistry (Vegetation chemistry_Clocaenog.csv); Litterfall (Litterfall.csv)
- Root and soil biology: Root biomass (Root biomass.csv); Soil microbial biomass (Soil microbial biomass.csv); Nitrogen mineralisation (Nitrogen mineralisation.csv); SOM/SOC and bulk density (Soil organic matter carbon density_Clocaenog.csv)
- Soil solution: Soil solution and leachate chemistry (Water chemistry.csv)
- Appendix: Site layout and quadrat layout (Appendix 1–3)

## Data collection and measurement methods (key points)

- Environment and treatments
  - Two climate treatments: drought and warming, each with three replicated plots; three control plots with shading scaffolding (n=9 total per table layout).
  - Drought: rain shielding via retractable polyethylene roof during May–Sept (1999–2011; since 2012 Apr–Oct); ~20% annual rainfall reduction; sometimes misses small events; high-wind exceptions.
  - Warming: retractable aluminium mesh curtains at night to reduce heat loss; retraction during rain to maintain rainfall; overall ~14% annual rainfall reduction; wind-exclusion rules.
- Site and data context
  - Location: Clocaenog Forest, Wales; upland moorland with dominant Calluna vulgaris; soil: humo-ferric podzol; site layout and plots described in appendices.
  - Measurements span both abiotic and biotic domains, with multiple decades of data and evolving instrumentation.
- Data collection infrastructure
  - AWS meteorological station: minute-scale measurements, hourly averages; sensors for temperature, humidity, rainfall, solar radiation, PAR, net radiation, wind, pressure; data quality checked visually.
  - Micro-meteorological plots: soil/air temperature, soil moisture (TDR) at multiple depths; daily to hourly logging.
  - Rainfall: storage rain gauge (biweekly sampling) and biweekly rainfall chemistry samples (pH, NO3, Cl, SO4, DOC, NH4) via ion chromatography and TOC analyses.
  - Throughfall: plot-level rainfall collected via collectors; seasonal/annual adjustments to match plot rainfall; data gaps infilled or plots excluded when data compromised.
  - Hydrology: water table depth via permeable tubes (biweekly readings); maximum detectable depths per plot recorded.
  - Soil respiration: multiple methods over time; collars installed; 1999–2000 gas analyzers; 2001–2008 CIRAS-2; 2013– onwards LI-COR automated systems; standard 40–120s measurement windows; Rs converted to mg CO2-C m-2 h-1.
  - Trace gases: CH4 and N2O via static chambers; three time-point sampling per event; GC analysis; legacy data note on processing.
  - Net ecosystem exchange (NEE): 2002–2004 and 2011 using CIRAS-2 and LI-6400; biomass adjustments applied to fluxes.
  - Photosynthesis: infrequent measurements (2001–2003) with leaf cuvette and CIRAS; biomass-normalization considerations.
  - Vegetation biomass and structure: Pin-point quadrat surveys across years (1998–2012); conversion from pin hits to biomass using calibration data; plant-by-species and life form classifications.
  - Canopy reflectance: ground-based spectrometry (NDVI and PRI calculations) on selected plots (2001–2004); background measurements outside plots for calibration.
  - Phenology and growth: shoot elongation, budburst, leaf number, and growth-stage scoring for C. vulgaris, V. myrtillus, and E. nigrum across multiple years.
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; analyses on green and litter material.
  - Litterfall: collectors deployed; monthly collection 1999–2002; later collection frequency reduced; biomass and C/N analyses.
  - Root biomass: multiple years and methods (soil cores, sieving, WinRHIZO analyses); depth-specific measurements.
  - Soil microbial biomass: chloroform fumigation method (2000–2001, 2012).
  - Nitrogen mineralisation: paired soil cores, KCl extraction, NH4+/NO3 analysis; comparison of initial/final cores.
  - SOM, SOC and bulk density: core-based measurements with drying and ignition/fixed-temperature protocols; photos and area-based conversions.
  - Soil solution and leachate chemistry: lysimeters and tension lysimeters; pH and ion analyses; DOC determinations.
- Data processing and unit standardization
  - Clear conversion frameworks for converting raw CO2 flux measurements to mg CO2-C m-2 h-1 across different instruments; biomass adjustments for NEE based on above-ground biomass measurements.
  - Pin-hit to biomass calibration tables used for converting vegetation survey data to biomass (g m-2).
  - Throughfall-derived treatment adjustments and data quality controls when data are missing or compromised.

## Data availability and storage

- Primary sources: On-site AWS and plot sensors; various datasets stored and catalogued with dataset names and supporting documentation.
- Data accessibility: Not all data are stored in the European Open Data Infrastructure (EIDC) beyond June 2015; contact points for data access and details:
  - Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) for information on data stored beyond central repositories.
- Documentation: Each dataset linked to supporting documentation (rtf files) detailing methods, data processing steps, and quality notes.

## Key data quality notes and caveats

- Throughfall data: data gaps due to equipment loss or measurement issues; occasionally infilled with yearly average reductions.
- Trace gas and soil respiration data: legacy processing practices; some documentation on data processing may not reflect current best practices.
- Drought treatment data: occasional non-operation during high winds; rain reduction estimates vary by year and treatment.
- Data accessibility: some datasets may not be present in the central data hub after 2015; verify with project contacts for complete temporal coverage.

## Appendix references

- Appendix 1: Site layout with plot coordinates.
- Appendix 2: Quadrat layout and plot quadrats for vegetation sampling.
- Appendix 3: Plot layout with quadrats and measurement areas. Includes LYS (Lysimeters), PQ (Point quadrats), SS (Soil suction samplers).