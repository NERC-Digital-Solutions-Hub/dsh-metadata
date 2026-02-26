# Climoor field site in Clocaenog forest Supporting documentation for data

- This document describes the Climoor climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming treatments projected for the next 20–30 years.
- Established in 1998 in upland moorland, the site comprises replicated drought and warming treatments and control plots, with extensive abiotic and biotic data collection over multiple years.
- The site is dominated by Calluna vulgaris (heather) with a plant assemblage including Vaccinium myrtillus, Empetrum nigrum, and others, on humo-ferric podzol soil.

## Site information and context

- Location: Clocaenog Forest, North East Wales; coordinates SJ019519 (53.055 N, 3.465 W).
- Ecosystem: Wet upland heath moorland; typical growing season June–August; dormancy in November–February.
- Dominant vegetation and soil horizons: Heather-dominated plant biomass (>60%), with E and Bh horizons variably visible; soil type is humo-ferric podzol with variable depth to horizons.
- Site layout appendix: detailed plot arrangement and quadrat layout provided.

## Climate change treatments and experimental design

- Treatments and replication:
  - Drought: 3 replicated plots + 3 control plots (total n=9). Type: drought-roof system that excludes rainfall on treatment plots during the growing season.
  - Warming: 3 replicated plots + 3 control plots. Type: retractable aluminium mesh curtains that reduce nighttime heat loss; rainfall exclusion occurs indirectly due to timing of roof retraction after rain events.
- Treatment timings and duration:
  - Drought: implemented annually May–Sept (1999–2011); since 2012, April–October. Rain exclusion reduces annual rainfall by ~20% and growing-season rainfall by ~79% in some years.
  - Warming: implemented year-round at night; rainfall reduction from warming is ~14% on average due to rain retraction lag.
- Environmental constraints: curtains not operated in high winds (>10 m s-1) to prevent damage.

## Data collection, equipment, and data types

- On-site observing and instrumentation:
  - Automated Weather Station (AWS) for daily meteorological data (1999–present); mast height at 4 m after 2007.
  - Micro-meteorological plots for soil and air temperature, soil moisture (1998–present with changes in method timing and sensors).
  - Rainfall collection: storage rain gauge (biweekly), plus rain chemistry sampling; throughfall collectors (plot-level, biweekly) to derive plot-level rainfall relative to site rainfall.
  - Water table depth: measured from bedrock via permeable tubes (since 2009), biweekly.
  - Soil respiration: fortnightly measurements using collars; later automated measurements (2013–2014) with LI-COR equipment; multiple methods over time.
  - Trace gases (CH4 and N2O): measured using the same collars with static chambers and gas chromatography; sampling at multiple time points.
  - Net ecosystem CO2 exchange (NEE): measured in select years (2002–2004, 2009–2011) with Perspex and LI-COR systems; adjustments for biomass were applied.
  - Photosynthesis: infrequent measurements (2001–2003) using leaf cuvettes and CIRAS-2 analyzer for standardization.
  - Vegetation biomass and structure: Pin-point vegetation surveys conducted in 1998–2012 (with yearly or near-yearly sampling in several years); conversion from pin hits to biomass using species-specific calibration.
  - Canopy reflectance: ground-based spectral measurements (NDVI and PRI indices) in 2001–2004.
  - Phenology, growth, pathogens: budburst, shoot elongation, and phenophase assessments for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum (various years 1999–2009); herbivory and disease observations.
  - Vegetation chemistry: elemental analysis (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) on green and litter material (1998 onward).
  - Litterfall: collectors deployed; monthly to yearly collection patterns (1999–2002); later years with less frequent collection.
  - Root biomass: multiple sampling campaigns (2003–2013) using soil cores with varied extraction methods; depth- and horizon-specific root quantification.
  - Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012).
  - Nitrogen mineralisation: incubation-based measures (1998–2004) with ammonium and nitrate analyses.
  - SOM, SOC, and bulk density: soil core analyses on paired samples (1999–2004, 2013).
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers to 30 cm depth; biweekly sampling (1998–2008).
- Data handling and formats:
  - Datasets named for each measurement type (examples: AWS daily data, Fortnightly soil respiration, Canopy reflectance, Litterfall, etc.).
  - Units and conversion guidelines provided (e.g., soil respiration units and conversions to mg CO2-C m-2 h-1; NEE conversions between g CO2 m-2 h-1 and mg CO2-C m-2 h-1).
  - Legacy data present where documentation may be incomplete or non-standard by current best practices; cautious interpretation advised.

## Data processing, quality, and accessibility

- Quality control:
  - Basic data quality checks described (visual QC with Excel; manual verification; consistency checks for pin-hit to biomass calibrations).
  - Throughfall treatment data occasionally excluded plots in which data were compromised (e.g., funnel loss); occasional infilling with average reductions across years.
  - Biomass adjustments in NEE to account for plot biomass differences using above-ground biomass measurements.
- Data management notes:
  - Some data stored outside of the EIDC; high-level data summaries and supporting documentation retained.
  - Datasets may be stored with accompanying R/Python processing scripts or metadata; not all processing steps are fully documented for legacy data.
- Access and contact for data:
  - Primary contacts: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
  - Data availability statement notes that not all datasets are stored in the EIDC and to contact CEH for details.

## Datasets overview (examples of data categories and methods)

- AWS meteorological data: daily measurements (temperature, humidity, rainfall, solar radiation, PAR, net radiation, pressure, wind) from 1999–present.
- Micro-meteorological plot data: daily soil/air temperature and soil moisture (1998–present).
- Rainfall and rainfall chemistry: site-level rainfall (biweekly) and plot-level rainfall throughfall (biweekly); chemistry includes pH, nitrate, chloride, sulfate, ammonium, DOC.
- Water table depth: biweekly measurements from 2009–present.
- Soil respiration: fortnightly and automated campaigns; multiple instrument generations (CIRAS-2, LI-COR systems) with unit conversions.
- Trace gases: CH4 and N2O fluxes via static chambers and GC analysis (sampling at 0.25, 15, and 30 minutes).
- Net ecosystem exchange: NEE fluxes with adjustments for biomass; data from early 2000s to 2011.
- Photosynthesis: infrequent leaf-level measurements under standardized light conditions.
- Vegetation biomass and structure: Pin-point biomass estimates with species-level calibration; annual or multi-year sampling across plot quadrats.
- Canopy reflectance: NDVI and PRI indices from ground-based spectroscopy.
- Phenology and growth: budburst, shoot elongation, leaf counts, and pathogen observations across several species.
- Vegetation chemistry and litter: carbon, nitrogen, phosphorus, minerals, lignin, tannin, alpha-cellulose, carbohydrates; litterfall mass and composition.
- Root biomass: multiple campaigns across 2003–2013 using cores and extraction methods.
- Soil microbial biomass, nitrogen mineralisation, SOM/SOC and bulk density, soil solution chemistry: multi-year campaigns with standard soil and water chemistry methods.

## Appendix and site documentation

- Appendix 1: Site layout (grid references, plot numbering).
- Appendix 2: Quadrat layout and plot quadrats (D3, E4, E7, etc.).
- Appendix 3: Plot layout with quadrats and measurement areas; 2012 Climoor plot layout annotations (LYS, PQ, SS).
- Plot-specific details include the grid reference SJ019519 and coordinates for precise localization.

- Note: The document emphasizes that the Climoor site provides a rich, multi-decadal data resource for climate change manipulation experiments, including drought and warming treatments, with extensive meteorological, biogeochemical, and ecological measurements, alongside detailed documentation of methods and calibration across time.