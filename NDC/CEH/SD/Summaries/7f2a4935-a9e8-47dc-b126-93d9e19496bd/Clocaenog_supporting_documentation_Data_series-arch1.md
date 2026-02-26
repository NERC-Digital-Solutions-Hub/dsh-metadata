# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog Forest, North East Wales.
- Uses automated roof technology and warming curtains to simulate drought and warming treatments over the next 20–30 years.
- Established in 1998 on upland moorland dominated by Calluna vulgaris (heather); solar and wind power powered systems.

## Location and site characteristics
- Location: Clocaenog Forest, North East Wales (approximate coordinates 53.055 N, -3.465 W).
- Ecosystem: Wet upland heath/moorland with Calluna vulgaris as the dominant vegetation; bryophytes and two minor shrub species present.
- Soil: Humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; parent material Ordovician/Silurian shale or mudstone.
- Climate context (from site table): mean air temperature around 8.0°C; mean control soil temperature ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha⁻¹ yr⁻¹; soil chemical and physical properties provided (CEC, base saturation, C:N ratios, etc.).

## Climate change treatments
- Treatments and replication: Two treatments (drought and warming) with three replicated plots each, plus three control plots (n = 9 plots total).
- Drought:
  - Timing: May–September annually 1999–2011; since 2012, April–October.
  - Method: Retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% and excludes ~80% of individual rain events during drought periods.
  - Wind sensitivity: Curtains do not operate in winds >10 m s⁻¹ to prevent damage.
- Warming:
  - Method: Retractable aluminium mesh curtains that reflect infrared radiation, reducing night-time heat loss.
  - Rain interaction: Roofs retract during rain to mitigate rainfall loss; average annual rainfall reduction ~14%.
  - Wind sensitivity: Curtains also avoided in high winds.
- Control plots mimic shading from the experimental structure to decouple shading effects from treatment effects.

## Experimental design and plot layout
- Plot size: 4 m × 5 m per plot.
- Plot arrangement: 3 warming (W), 3 drought (D), and 3 control (C) plots arranged in blocks to manage spatial variability.
- Appendix provides site and quadrat layouts, including lysimeters, pin quadrats, and quadrat grids for consistent sampling.

## Data collection and processing overview
- A wide range of abiotic and biotic data collected through an automated weather station (AWS) and plot-level sensors, plus periodic destructive and non-destructive measurements.
- Data processing and QA: Data quality control described; legacy data noted with variable documentation of processing steps; some datasets require transformations or careful interpretation when combining sources.

## Datasets and data collection details
- AWS meteorological data
  - Dataset: Daily automated weather station data_1999to2015_Clocaenog.csv
  - Sensors: Temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Time scale: Daily (1999–current day)
- Micro-meteorological plot data
  - Dataset: Daily micromet data_1998to2015_Clocaenog.csv
  - Metrics: Plot-level soil/air temperature, soil moisture
  - Time scale: Daily
- Rainfall data (site level rainfall and rainfall chemistry)
  - Dataset: Rainfall_Clocaenog.csv
  - Methods: Storage rain gauge (biweekly rainfall sums); rainfall chemistry via Warren spring collectors; analyses for pH, NO3, Cl, SO4, DOC, NH4
- Throughfall data (plot-level rainfall)
  - Dataset: Throughfall_Clocaenog.csv
  - Method: Plot-level throughfall collectors; data used to derive plot-level rainfall by applying treatment-specific percent changes
- Water table depth
  - Dataset: Water table depth_Clocaenog.csv
  - Method: Permeable tubes down to bedrock; manual biweekly measurements (2009–current day)
- Soil respiration
  - Datasets: Fortnightly soil respiration_Clocaenog.csv; Automated soil respiration_Clocaenog.csv
  - Method: Collars installed in plots; measurements across multiple years with different instrumentation (CIRAS-2, LI-COR 8100, automated systems); unit conversions provided
- Trace gases (CH4 and N2O)
  - Dataset: Trace gases_Clocaenog.csv
  - Method: Static chamber technique with gas chromatography; three time-point sampling per measurement
- Net ecosystem CO2 exchange (NEE)
  - Dataset: Net ecosystem exchange_Clocaenog.csv
  - Methods: Various chamber setups (2002–2004 with CIRAS-2; 2010–2011 with LI-COR) plus adjustments for biomass differences in flux calculations
  - Conversion factors between measurement units documented
- Photosynthesis
  - Dataset: Photosynthesis_Clocaenog.csv
  - Method: Leaf-level measurements using a cuvette and CIRAS-2; limited to specific years/species
- Vegetation biomass (Pin-point biomass methodology)
  - Dataset: Vegetation survey_Clocaenog.csv
  - Method: Pin-point quadrats within plots (1998–2012, and ongoing); conversion from pin hits to species biomass using species-specific calibration factors
  - Table 5 and Table 6 outline coding schemes and pin-to-biomass calibration
- Canopy reflectance
  - Dataset: Canopy reflectance_Clocaenog.csv
  - Method: Ground-based spectrometer measurements; NDVI and PRI indices calculated
- Vegetation phenology, annual growth, and pathogens
  - Dataset: Phenology Growth Pathogens_Clocaenog.csv
  - Method: Monitoring shoot elongation and phenophases for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; yearly sampling
- Vegetation chemistry
  - Dataset: Vegetation chemistry_Clocaenog.csv
  - Determinants: Carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates
- Litterfall
  - Dataset: Litterfall.csv
  - Method: Litterfall collectors; monthly collection 1999–2002; later collection intervals varied; samples analyzed for C and N
- Root biomass
  - Dataset: Root biomass.csv
  - Methods: Soil coring and root extraction; multiple years (2003–2013) with different core sizes and extraction protocols
- Soil microbial biomass
  - Dataset: Soil microbial biomass.csv
  - Method: Chloroform fumigation technique; calculation of microbial biomass carbon
- Nitrogen mineralisation
  - Dataset: Nitrogen mineralisation.csv
  - Method: Paired cores with KCl extractant to determine ammonium and nitrate; rates calculated from initial and final cores
- SOM, SOC and bulk density
  - Dataset: Soil organic matter carbon density.csv
  - Method: SOM/SOC analysis from paired cores; bulk density calculations
- Soil solution and leachate chemistry
  - Dataset: Water chemistry.csv
  - Method: Lysimeters and tensioned samplers; analysis for pH, NO3, Cl, SO4, DOC, NH4
- Data access
  - Data stored on the EIDC portal; not all data are kept there; contact CEH Bangor staff (Sabine Reinsch, Bridget Emmett) for details

## Data quality, limitations, and notes
- Some datasets are legacy with variable documentation of data processing steps.
- Throughfall data may require exclusions or infilling when samples are compromised; percent changes applied to site-level rainfall data to estimate plot-level rainfall.
- Automated vs. manual measurement methods evolved over time; unit conversions and calibration factors are provided for context.
- Data gaps exist for certain years or measurements due to equipment issues or protocol changes.
- Appendix includes detailed site layout and quadrat layouts for reproducibility.

## Data access and contacts
- Primary contact: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Data availability and specifics are described in the provided documentation and dataset notes; some data may not be stored in the EIDC portal.