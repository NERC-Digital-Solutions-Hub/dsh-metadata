# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment in Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
- The site operates since 1998 with replicated drought and warming treatments plus control plots, designed for upland moorland vegetation dominated by Calluna vulgaris (heather) with additional vascular and bryophyte species.
- Data cover a wide range of abiotic and biotic measurements collected across multiple years, with emphasis on enabling analysis of treatment effects and ecosystem processes.
- The documentation lists data types, collection methods, data processing steps, units, quality considerations, and data access notes (some data not stored in the on-site data repository post-2015).

## Data sources and datasets
- AWS meteorological data (daily, 1999–present)
  - Dataset: Daily automated weather station data_1999to2015_Clocaenog.csv
  - Sensors: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Setup: initial 1 m height, moved to 4 m mast after 2007 due to theft; data quality controlled visually; hourly averages from minute samples
- Micro-meteorological plot data (daily)
  - Dataset: Daily micromet data_1998to2015_Clocaenog.csv
  - Measurements: plot-level soil/air temperature, soil moisture (multiprotocol over years), high-frequency sampling with daily averages
- Rainfall and rainfall chemistry (site-level)
  - Dataset: Rainfall_Clocaenog.csv
  - Methods: ground-level storage rain gauge (biweekly sampling) and Warren spring collectors for chemistry (pH, NO3, Cl, SO4, DOC, ammonium)
- Throughfall (plot-level rainfall)
  - Dataset: Throughfall_Clocaenog.csv
  - Method: plot-level rainfall collectors; used to compute percent treatment differences and apply to site-level rainfall to estimate plot rainfall
  - Note: data quality varies due to logistical issues; some plots omitted or infilled as needed
- Water table depth
  - Dataset: Water table depth_Clocaenog.csv
  - Method: permeable tubes installed 2009; bi-weekly manual depth measurements; maximum detectable depths per plot specified
- Soil respiration
  - Datasets: Fortnightly soil respiration_Clocaenog.csv; Automated soil respiration_Clocaenog.csv
  - Methods: CO2 efflux measured with collars; various instruments over time (CIRAS-2, LICOR 8100, automated LI-COR system); 40–120 s chamber contacts; conversion factors provided to mg CO2-C m^-2 h^-1
  - Note: plant/vegetation interactions with collars documented; some site-specific drying observed with automated collars
- Trace gas fluxes (CH4 and N2O)
  - Dataset: Trace gases_Clocaenog.csv
  - Method: static chambers with gas sampling at 0.25, 15, and 30 minutes; analysis by gas chromatography; legacy data with documentation caveats
- Net ecosystem exchange (NEE)
  - Dataset: Net ecosystem exchange_Clocaenog.csv
  - Years: 2002–2004 and 2011; methods varied (CIRAS-2 and LICOR-based systems); adjustments made for biomass differences in flux calculations
  - Unit conversions provided to align with CO2 flux units
- Photosynthesis
  - Dataset: Photosynthesis_Clocaenog.csv
  - Method: infrequent leaf-level measurements using a leaf cuvette and CIRAS-2; standardization against leaf area/mass for comparisons
- Vegetation biomass (Pin-point method)
  - Dataset: Vegetation survey_Clocaenog.csv
  - Method: pin-point canopy pin hits in three quadrats per plot across multiple years (1998–2012); conversion from pin hits to biomass using species-specific calibration (Table 6); checks for missing pins and corrections to 300 pins per plot
  - Codes provided for numerous species and growth forms
- Canopy reflectance
  - Dataset: Canopy reflectance_Clocaenog.csv
  - Method: ground-based spectrometry (NDVI from 680/570 nm; PRI) over plots in 2001–2004; spectrum 400–950 nm; calibration with a grey standard
- Vegetation phenology, annual growth, and pathogens
  - Dataset: Phenology Growth Pathogens_Clocaenog.csv
  - Method: monitoring leading shoot elongation and phenophases for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; growth measurements from April to September; V. myrtillus budburst and leaf development tracked; herbivory and disease observations
- Vegetation chemistry
  - Dataset: Vegetation chemistry_Clocaenog.csv
  - Analytes: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; samples from green and senesced material
- Litterfall
  - Dataset: Litterfall.csv
  - Method: 12 litterfall collectors per plot; monthly collection 1999–2002; later intervals less frequent; samples dried and weighed; carbon and nitrogen analysis on pooled yearly samples
- Root biomass
  - Dataset: Root biomass.csv
  - Methods: 2003–2004 soil cores with manual root extraction; 2008 soil cores with sieving and imaging/analysis; 2011 stratified cores under C. vulgaris; different core sizes and analysis approaches across years
- Soil microbial biomass
  - Dataset: Soil microbial biomass.csv
  - Method: chloroform fumigation technique (2000, 2001, 2012); DOC analysis to estimate microbial biomass carbon
- Nitrogen mineralisation
  - Dataset: Nitrogen mineralisation.csv
  - Method: paired cores with initial and final incubations; ammonium and nitrate measured; used to derive net mineralisation and ammonification rates
- SOM, SOC, and bulk density
  - Dataset: Soil organic matter carbon density.csv
  - Method: analyses on paired cores from nitrogen mineralisation studies; SOM and SOC via loss-on-ignition and combustion; bulk density calculations; results converted to g m^-2
- Soil solution and leachate chemistry
  - Dataset: Water chemistry.csv
  - Method: lysimeters (zero-tension) and tensioned samplers installed 1998; biweekly sampling; analyses include pH, NO3, Cl, SO4, DOC; documentation notes on sample handling and analysis

## Data processing, quality, and format
- Data processing notes
  - Early data relied on manual QC in Excel; data processing documented but some legacy practices predate current standards
  - Different instruments and protocols used over time; conversions provided to harmonize units (e.g., soil respiration, NEE)
  - Plot- and plot-replication adjustments (e.g., throughfall-based scaling to site rainfall; biomass adjustments for NEE)
- Data formats and access
  - Primary data files are CSVs; methodology and supporting details are provided in accompanying RTF documentation
  - Some data and infrequent measurements may not be stored in the CEH-owned EIDC (Environmental Data Information Center) post-2015; contact points provided for specifics
- Data management notes
  - 9 plots with 3 replicate treatments; drought treatment timing and warming treatment specifics summarized
  - Outputs used for evaluating climate manipulation effects on upland moorland ecology; potential for dashboard-style self-service analyses using the various time-series datasets

## Access, contacts, and usage notes
- Primary contacts for data details and access: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor
- Access considerations
  - Some data may not be stored in the central data repository; verify availability and format with the above contacts
  - Documentation emphasizes data provenance, measurement methods, unit conversions, and dataset-specific quality notes to support proper re-use

## Relevance for Data Support archetype
- Comprehensive, multi-year, multi-method dataset suitable for building data products (dashboards, self-service querying, cross-dataset analyses) across meteorology, ecosystem fluxes, plant-themes, and soil processes
- Highlights practical data support challenges:
  - Underlying asks include integrating disparate formats and instruments, handling patchy time series, and promoting data reuse
  - Data quality considerations include legacy methods, changes in instrumentation, and data gaps due to field challenges
- Provides a robust example of data governance, provenance, and cross-domain integration needed for policy-relevant or management-facing data products in environmental contexts