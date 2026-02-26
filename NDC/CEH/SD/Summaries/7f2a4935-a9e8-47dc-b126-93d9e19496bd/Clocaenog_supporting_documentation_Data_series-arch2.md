# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose: Document the Climoor climate change manipulation experiment and the wide range of abiotic and biotic data collected for environmental health and policy monitoring over time.

## 1.0 Site information
- Location: Clocaenog Forest, North East Wales (56-year climate data context), upland moorland habitat.
- Ecosystem: Wet upland heath dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum; diverse bryophytes and mosses.
- Soils: Humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; typical E horizon at 6–17 cm depth.
- Climate and context: Remote, sensitive upland environment with a growing season roughly June–August; winter dormancy November–February.
- Layout: Replicated climate manipulation plots across three treatments (warming, drought) and three controls; appendix includes site and quadrat layouts.

## 2.0 Climate change treatment information
- Treatments and replication:
  - Drought: three replicate drought plots and three controls.
  - Warming: three replicate warming plots and three controls.
  - Plot size: 4 m x 5 m; treatments organized in blocks.
- Drought implementation:
  - Annual May–September drought (1999–2011; extended to April–October since 2012).
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor, excluding about 80% of rain during drought periods; reduces annual rainfall by ~20% on site.
  - Rainfall timing and limits vary by year.
- Warming implementation:
  - Night-time warming via retractable aluminum mesh curtains that reflect infrared radiation, reducing heat loss.
  - Curtains retract automatically after detection of rain to preserve rainfall input; average annual rainfall reduction ~14%.
  - Wind threshold (>10 m/s) prevents curtain operation to avoid damage.
- Treatment timing and data references:
  - Table-based details per year on drought dates, percent rainfall reduction, and warming degree-day changes; site-specific climate data align with ongoing monitoring.

## 3.0 Equipment, protocols and data processing methodology
- Overall setup:
  - On-site automated weather station (AWS) plus plot-level micro-meteorological sensors.
  - Data coverage spans multiple decades with varying instrumentation updates.
  - Quality control: basic graphic checks in Excel; detailed data processing notes included for each dataset.
- 3.1 AWS meteorological data
  - Dataset: Daily automated weather station data (1999–2015).
  - Sensors: air temperature, relative humidity, rainfall, wind speed/direction, solar radiation, net radiation, PAR, barometric pressure.
  - Height now 4 m due to thefts; data logged hourly from 1999–present.
  - Data handling: minute-level measurements averaged to hourly; QC performed visually.
- 3.2 Micro-meteorological data
  - Dataset: Daily micro-met data (1998–2015).
  - Measurements: soil temperature at depths (5, 10, 20 cm); soil moisture via TDR or theta probes (with earlier methods used 1997–2008).
  - Frequency: minute-level data averaged to daily/hourly; QC via visual checks.
- 3.3 Storage rain gauge data and rainfall chemistry
  - Dataset: Rainfall_Clocaenog.csv; storage rain gauge (biweekly collection).
  - Chemistry: rain samples for pH, nitrate, chloride, sulfate, ammonium, dissolved organic carbon (DOC) analyzed via standard lab methods.
  - Storage gauge preferred for robustness over AWS data; rainfall chemistry collected biweekly.
- 3.4 Throughfall data (plot level rainfall)
  - Dataset: Throughfall_Clocaenog.csv; biweekly collection per plot.
  - Method: plot-level rainfall collection with funnels; data used to compute percent change relative to site rainfall; noisy periods excluded; occasional data infill with average reductions.
  - Purpose: derive plot-level rainfall for treatment comparisons.
- 3.5 Water table depth data
  - Dataset: Water table depth_Clocaenog.csv; measured with perforated tubes to bedrock (installed 2009).
  - Frequency: biweekly field measurements; maximum detectable depths per plot documented.
- 3.6 Soil respiration data
  - Datasets: Fortnightly soil respiration_Clocaenog.csv and Automated soil respiration_Clocaenog.csv.
  - Method: soil collars (20 cm diameter) with static chambers; switch from manual methods (1999–2000) to infrared gas analyser and LI-COR systems; automated 2013–2014 measurements added.
  - Processing: Rs computed from CO2 efflux; unit conversions detailed to mg CO2-C m^-2 h^-1; acclimation period applied; data quality and site disturbance notes included.
- 3.7 Trace gas (CH4 and N2O) measurement
  - Dataset: Trace gases_Clocaenog.csv; same collars as soil respiration.
  - Method: static chamber with gas-tight caps; samples collected at 0, 15, and 30 minutes; analyzed by gas chromatography; calibration and QA notes included.
- 3.8 Net ecosystem CO2 exchange (NEE)
  - Dataset: Net ecosystem exchange_Clocaenog.csv; measurements in 2002–2004 and 2011, using CIRAS-2 and LI-COR systems.
  - Processing: raw data converted to mg CO2-C m^-2 h^-1; biomass adjustments applied to account for plot variation in NEE and photosynthesis estimates.
- 3.9 Photosynthesis
  - Dataset: Photosynthesis_Clocaenog.csv; infrequent measurements (2001–2003 for C. vulgaris and V. myrtillus; 2001 for E. nigrum).
  - Method: leaf cuvette and CIRAS-2 IRGA; standardization across species via leaf area proxies and leaf mass data.
- 3.10 Vegetation survey data (plant biomass) – Pin Point analysis
  - Dataset: Vegetation survey_Clocaenog.csv; years 1998–2012 with additional years onward.
  - Method: pin-point technique across three fixed quadrats per plot; 300 pins per plot; taxon-specific calibration factors to convert pin-hits to biomass (g m^-2); notes on data cleaning and missing-pin adjustment.
  - Codes and species list provided (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, mosses, bryophytes, etc.).
- 3.11 Canopy reflectance
  - Dataset: Canopy reflectance_Clocaenog.csv; 2001–2004 (and 2000–2001) using a ground-based spectrometer; NDVI and PRI indices calculated from reflectance bands.
- 3.12 Vegetation phenology, annual growth and pathogen assessment
  - Dataset: Phenology Growth Pathogens_Clocaenog.csv; spring phenology measured for C. vulgaris, V. myrtillus, E. nigrum in select years; shoot elongation, phenophase stages, and flowering/leaves variables recorded.
- 3.13 Vegetation chemistry
  - Dataset: Vegetation chemistry_Clocaenog.csv; chemical analyses of green and senesced material for C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates.
- 3.14 Litterfall
  - Dataset: Litterfall.csv; collected 1999–2002 monthly; later samples pooled annually; litter ground to biomass; carbon and nitrogen analyses performed on litter.
- 3.15 Root biomass
  - Dataset: Root biomass.csv; roots sampled 2003, 2004, 2008, 2011 with various core methods and size; extraction and biomass determination described.
- 3.16 Soil microbial biomass
  - Dataset: Soil microbial biomass.csv; chloroform fumigation method used in 2000, 2001, 2012; microbial biomass carbon derived from difference in DOC between fumigated and unfumigated samples.
- 3.17 Nitrogen mineralisation
  - Dataset: Nitrogen mineralisation.csv; sporadic measurements 1998–2004; paired cores used to estimate net mineralisation and ammonification via KCl extraction and subsequent analyses.
- 3.18 SOM, SOC and bulk density
  - Dataset: Soil organic matter carbon density.csv; SOM and SOC measured on cores from N-mineralisation study; bulk density and g m^-2 conversions computed.
- 3.19 Soil solution and leachate chemistry
  - Dataset: Water chemistry.csv; lysimeters and tensioned soil water samplers installed (1998); lab analyses for pH, NO3, Cl, SO4, DOC, ammonium; samples processed within 4 hours of sampling.

## Data management, accessibility and notes for analysts
- Data storage and portals:
  - Primary data stored in the Environmental Information Data Centre (EIDC) or CEH Bangor systems; some smaller or post-2015 data may not be stored in the EIDC.
  - For missing datasets or access, contact project leads (e.g., Sabine Reinsch, Bridget Emmett) for details.
- Data quality and processing notes:
  - Multiple datasets note legacy processing practices; where applicable, unit conversions and calibration details are documented to enable re-analysis.
  - Data processing includes treatment-specific adjustments (e.g., NEE adjustments for biomass differences in plots; pin-hits conversions to biomass; throughfall treatment mean calculations with data-loss handling).
- Appendix resources:
  - Appendix 1: Site layout
  - Appendix 2: Quadrat layout with measurement areas
  - 2012 Climoor plot layout and measurement abbreviations (LYS, PQ, SS) for reference

- Key takeaway for analysts:
  - The Climoor site provides a long-term, multi-variable dataset combining abiotic forcing (drought and warming) with a broad suite of ecological response metrics (phenology, biomass, chemistry, carbon/nitrogen fluxes, and soil processes) suitable for monitoring environment health and policy performance over time. Data come in standardized formats but include legacy aspects; careful alignment of time scales, units, and biomass adjustments is essential for cross-dataset analyses.