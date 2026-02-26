# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation site using automated roof technology to simulate drought and warming for upland moorland habitats over the next 20–30 years.
- Located in Clocaenog Forest, North East Wales; established 1998; features replicated drought and warming treatments plus controls.
- Comprehensive data catalogue spanning meteorology, plot-scale processes, vegetation, soils, and biogeochemical signals collected over multiple years using a combination of on-site sensors, chamber methods, and laboratory analyses.
- Data governance notes: not all data are stored in the EIDC; contact CEH Bangor for access to legacy or infrequent datasets and metadata details.

## 1.0 Site information

- Habitat and location: upland west Atlantic moorland with Calluna vulgaris as the dominant plant; other species present include Vaccinium myrtillus and Empetrum nigrum.
- Soil: humo-ferric podzol with variable horizons; eluvial (E) and illuvial (Bh) horizons not always visible; typical E horizon depth ~6–17 cm.
- Climate baseline: site-specific climate data collected since 1997–2014; mean conditions include shifts in temperature, rainfall, and N deposition patterns.
- Experimental design: replicated climate treatments across plots within the Clocaenog field site.

## 2.0 Climate change treatment information

- Treatments and replication: two climate treatments (drought and warming) with three replicates each, plus three control plots; total n = 9 plots.
- Drought treatment: May–Sept (1999–2011) and Apr–Oct (since 2012); uses retractable polyethylene roof to exclude rainfall, reducing annual rainfall by ~20% and excluding ~80% of rainfall during the drought window; curtains inhibited in high winds.
- Warming treatment: night-time warming via retractable aluminum curtains; curtains reflect infrared radiation; roof retraction when rainfall detected to preserve rainfall; average annual rainfall reduction ~14%.
- Experimental layout: plots organized into blocks; specific treatment-block assignments provided; some shading controls mimic structural effects on treatment plots.
- Data caveat: operational details and timing vary across years; high-level treatment intent remains consistent.

## 3.0 Equipment, protocols and data processing methodology

- Data types and datasets: extensive suite of abiotic and biotic measurements collected with AWS and plot-scale instruments; Table 3 summarizes data types and collection protocols.
- Data accessibility: on-site AWS and plot data are supplemented by various datasets; not all data stored in the EIDC; contact CEH Bangor for details.

### 3.1 AWS meteorological data

- Dataset: Daily automated weather station data (1999–2015 in Clocaenog).
- Sensors and measures: temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
- Data cadence: hourly averages; measurements every minute with QC via visual checks.
- Setup notes: AWS mounted on secured mast at 4 m after 2007 due to theft; quality control tripwires described.

### 3.2 Micro-meteorological plot data

- Dataset: Daily micromet data (1998–2015).
- Measures: plot-level soil and air temperature, soil moisture, etc.; soil temperatures at multiple depths; soil moisture via TDR or prior theta probes.
- Cadence: hourly averages; data quality checked visually.
- Notes: micromet data complemented by earlier methods; ongoing daily/weekly campaigns.

### 3.3 Storage rain gauge data and rainfall chemistry

- Dataset: Rainfall_Clocaenog.csv; rainfall chemistry via biweekly samples.
- Method: ground-level storage rain gauge (funnel 12.7 cm) with biweekly collection; rainfall samples stored at 4°C for lab analyses.
- Analyses: pH, nitrate, chloride, sulfate, DOC, ammonium via standard lab instruments (ion chromatography, TOC, colorimetric assays).
- Data considerations: storage gauge preference due to robustness; occasional holiday-derived sampling gaps.

### 3.4 Throughfall data (plot-level rainfall)

- Dataset: Throughfall_Clocaenog.csv; biweekly collection via plot-level funnels.
- Processing: used to estimate plot-level rainfall by calculating percent change relative to site-level rainfall; data gaps due to equipment loss or damage are excluded from treatment means; some infilling with yearly averages when appropriate.

### 3.5 Water table depth data

- Dataset: Water table depth_Clocaenog.csv; measured from 2009 onward with permeable tubes to bedrock.
- Cadence: biweekly manual measurements; maximum detectable depths per plot documented.

### 3.6 Soil respiration data

- Datasets: Fortnightly soil respiration_Clocaenog.csv and Automated soil respiration_Clocaenog.csv.
- Method history: measurements using three collars per plot; early methods used CIRAS-2 with static chambers, later switched to LI-COR 8100 system and automated chambers (2013–2014); one collar sometimes altered for automation, with observed soil drying effects.
- Data processing: CO2 flux converted to mg CO2-C m^-2 h^-1; Rs estimated by linear regression after acclimation period; biomass effects accounted for in NEE calculations.

### 3.7 Trace gas (CH4 and N2O) measurement

- Dataset: Trace gases_Clocaenog.csv; static chamber method on the same collars as soil respiration.
- Sampling: three time points (0, 15, 30 minutes); samples stored in glass vessels and analysed by gas chromatography.
- Calibration: regular calibration with standards; note that legacy practices mean some documentation may not reflect current standards.

### 3.8 Net ecosystem CO2 exchange (NEE)

- Dataset: Net ecosystem exchange_Clocaenog.csv; measurements in 2002–2004 and 2011.
- Method: Perspex chamber linked to IR gas analyser; different systems used in different years; adjustments made for biomass differences using above-ground biomass measurements.
- Conversions: raw units converted to mg CO2-C m^-2 h^-1; adjustments for biomass to standardize flux across plots.

### 3.9 Photosynthesis data

- Dataset: Photosynthesis_Clocaenog.csv; infrequent measurements (2001–2003 for C. vulgaris and V. myrtillus; 2001 for E. nigrum).
- Method: leaf cuvette with light source and CIRAS-2; standardized for leaf area by leaf mass since leaves are three-dimensional.

### 3.10 Vegetation survey data (Pin Point analysis)

- Dataset: Vegetation survey_Clocaenog.csv; pin-point biomass estimates using a 0.5 m grid across three quadrats per plot.
- Method: 300 pins per plot; conversion factors derived from destructive sampling (2000) to biomass (g m^-2); annual surveys conducted in multiple years (1998–2012 with gaps).
- Coding: detailed pin-hit codes for species and life forms; cross-checked by double-entry and consistency checks; pins adjusted for missing data.

### 3.11 Canopy reflectance

- Dataset: Canopy reflectance_Clocaenog.csv; spectral reflectance (400–950 nm) collected in 2001–2004.
- Method: ground-based spectrometer; NDVI and PRI indices calculated (NDVI680, NDVI570, PRI) using targeted wavelength bands.

### 3.12 Vegetation phenology, annual growth and pathogen assessment

- Dataset: Phenology Growth Pathogens_Clocaenog.csv; phenophase and growth measures for C. vulgaris, V. myrtillus, E. nigrum.
- Method: annual shoot elongation and phenophase scoring from April to September; species-specific metrics documented (budburst, leaf emergence, flowering, herbivory, rust infection).

### 3.13 Vegetation chemistry

- Dataset: Vegetation chemistry_Clocaenog.csv; analyses on green (current year) and senesced material.
- Determinants: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; samples prepared and sent to CEH Lancaster.

### 3.14 Litterfall

- Dataset: Litterfall.csv; collectors collected monthly (1999–2002) and less frequently thereafter.
- Processing: litter dried and weighed; conversion to g litter m^-2; subsamples analysed for C and N.

### 3.15 Root biomass

- Dataset: Root biomass.csv; root biomass measured in multiple years (2003, 2004, 2008, 2011) using soil cores and varied extraction methods.
- Processing: roots separated by soil horizon, dried, and weighed; WinRHIZO used for some analyses.

### 3.16 Soil microbial biomass

- Dataset: Soil microbial biomass.csv; chloroform fumigation method (2000, 2001, 2012).
- Processing: difference in DOC between fumigated and unfumigated samples, corrected to microbial biomass carbon per g soil organic matter.

### 3.17 Nitrogen mineralisation

- Dataset: Nitrogen mineralisation.csv; measurements between 1998–2004.
- Method: paired soil cores; initial and final cores analysed for NH4+ and NO3- via colorimetric methods; net mineralisation calculated.

### 3.18 SOM, SOC and bulk density

- Dataset: Soil organic matter carbon density.csv; SOM and SOC contents from cores; bulk density calculations and g m^-2 conversions provided.

### 3.19 Soil solution and leachate chemistry

- Dataset: Water chemistry.csv; soil solution collected from lysimeters (zero-tension and tensioned samplers) installed in 1998.
- Analyses: pH, NO3-, Cl-, SO4^2-, DOC, NH4+; samples filtered and stored before lab analyses.

## Appendix references

- Appendix 1: Site layout for the experimental site.
- Appendix 2: Quadrat layout and measurement areas.
- Appendix 3: Plot layout with quadrats and measurement areas, including lysing/planting markers.

## Data governance and contact

- Caveat: some datasets are legacy or infrequently collected; documentation of data processing may not meet current best practices.
- Contacts for data access and further details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

- Overall: the document details a rich, multi-decadal data ecosystem encompassing climatic treatments, micro- and macro-ecological measurements, vegetation dynamics, and soil processes, with explicit methods, units, and data processing notes, plus important considerations for data accessibility and quality control.