# Climoor field site in Clocaenog forest Supporting documentation for data

- Climate change manipulation experiment using automated roof technology to simulate drought and warming over the next 20–30 years
- Site: Clocaenog Forest, North East Wales; upland moorland ecosystem dominated by Calluna vulgaris (heather); solar and wind powered; established 1998
- Treatments: three warming plots, three drought plots, and three control plots (with scaffolding mirrors for shading); replicated within blocks
- Data scope: extensive multi-disciplinary data collection across abiotic and biotic variables, spanning 1997–present in various formats and cadences

## Data assets and datasets

- AWS meteorological data (daily, minute-level sensors; daily averages; 1999–current)
- Micro-meteorological plot data (soil temperature, soil moisture; daily)
- Rainfall data
  - Site-level storage rain gauge (biweekly; rainfall chemistry)
  - Throughfall data (plot-level rainfall; biweekly; used to derive plot-specific rainfall changes)
- Water table depth data (biweekly; 2009–present)
- Soil respiration data (multiple methods; 1998–present; collars installed; flux calculations to mg CO2-C m⁻² h⁻¹)
- Trace gas measurements (CH4 and N2O; 1999–2000; 2007–2009)
- Net ecosystem CO2 exchange (NEE) and respiration components (2002–2004; 2009–2011; separate systems used across years)
- Photosynthesis data (ambient and response curves; 2001–2003; several later measurements with varying conditions)
- Vegetation survey data (pin-point biomass measurements; 1998–2012 and beyond)
- Canopy reflectance (NDVI and PRI indices; 2000–2004 with some earlier measurements)
- Vegetation phenology, annual growth and pathogen assessment (1998–present)
- Vegetation chemistry (green and senesced material; carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates)
- Litterfall (1999–2002; monthly; later years less frequent)
- Root biomass (2003–2013; varying methods; multiple data points per plot)
- Soil microbial biomass (chloroform fumigation; 2000, 2001, 2012)
- Nitrogen mineralisation (1998–2004)
- SOM, SOC and bulk density (paired cores linked to mineralisation studies)
- Soil solution and leachate chemistry (lysimeters and tensioned samplers; biweekly to monthly; 1998–2008)
- Appendix materials: site layout and quadrat/plot mappings

## Data collection, instruments, and methodologies

- Automated Weather Station (AWS)
  - Sensors: temperature, humidity, rainfall, wind, solar radiation, PAR, net radiation, pressure
  - Height: initially 1 m, relocated to 4 m due to thefts
  - Cadence: minutely measurements; hourly/daily averages; quality checks via visual QC
- Micro-meteorological data
  - Soil temperature (5, 10, 20 cm); soil moisture (TDR sensors since 2008; earlier methods noted)
  - Data logged: minutes to half-hourly averages
- Rainfall and rainfall chemistry
  - Ground-level storage rain gauge (biweekly sampling; robust against logger power loss)
  - Warren spring collectors for chemistry (pH, NO3, Cl, SO4, DOC, NH4)
- Throughfall data
  - Plot-level rainfall collectors; data used to compute treatment-specific rainfall reductions; data completeness affects treatment means
- Water table depth
  - Permeable tubes to bedrock; biweekly measurements; maximum detectable depths per plot recorded
- Soil respiration and trace gases
  - Soil collars (20 cm diameter) for Rs; multiple measurement systems over time (CIRAS-2, LICOR 8100, automated LI-COR 8100 with chambers)
  - Flux calculations via linear regression of CO2 concentration over time; various unit conversions applied
  - CH4 and N2O measured with closed chambers and gas chromatography; sampling at 0, 15, 30 minutes
- Net ecosystem CO2 exchange (NEE)
  - Chambers with PAR and temperature sensors; flux conversions to mg CO2-C m⁻² h⁻¹; biomass-based adjustments to account for plot heterogeneity
- Photosynthesis
  - Ambient and fixed Ci/PAR measurements; leaf-level measurements on Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; curves and static measurements
- Vegetation and canopy metrics
  - Pin-point biomass surveys (1998–2012+); 3 quadrats per plot; 100 pins per quadrat; conversion to g m⁻² using species-specific calibration
  - Canopy reflectance (NDVI and PRI) via ground-based spectrometer
  - Phenology and growth observations; herbivory and disease notes
  - Vegetation chemistry analyses on green and senesced material
- Litterfall and roots
  - Litter traps (monthly collection 1999–2002; later less frequent); drying and weighting; conversion to g m⁻²
  - Root biomass: multiple methods across years (soil cores, washing, WinRHIZO analyses)
- Soil biology and chemistry
  - Soil microbial biomass via chloroform fumigation method
  - Nitrogen mineralisation via paired cores; ammonium and nitrate analyses
  - SOM/SOC and bulk density from paired cores; conversions to g m⁻²
  - Soil solution and leachate chemistry: NO3, Cl, SO4, pH, DOC; monthly monitoring

## Data processing, quality, and standardization

- Unit conversions and calibrations
  - Rs and NEE flux units require specific conversions (g CO2 m⁻² h⁻¹ to mg CO2-C m⁻² h⁻¹; µmol m⁻² s⁻¹ to mg CO2-C m⁻² h⁻¹)
  - Biomass-adjusted fluxes in NEE using above-ground biomass measurements
- Legacy data and documentation
  - Not all processing steps align with current best practices; some historical documentation exists in field sheets and R packages
- Data completeness and gaps
  - Throughfall and plot-level data can be incomplete; occasional infilling with average reductions; some datasets with infrequent measurements
  - After June 2015, some smaller/less-frequently collected datasets may not be stored in the main repository
- Data storage and discovery
  - Not all datasets are stored in the Environmental Information Data Centre (EIDC); consult contacts for access
  - Data files are labeled with “SD_…” conventions and include detailed methodological notes

## Data access, governance, and contacts

- Data availability
  - Some data stored externally or as field/lab analysis records; access via project contacts
  - Not all data are in EIDC; request details and access through listed contacts
- Key contacts for data access and governance
  - Sabine Reinsch (sabrei@ceh.ac.uk)
  - Bridget Emmett (bae@ceh.ac.uk)
- Appendix resources
  - Appendix 1: site layout
  - Appendix 2: quadrat layout and plot mappings
  - Appendix 3: plot layout with quadrats and measurement areas

## Practical implications for data leaders

- Comprehensive, multi-decadal, multi-discipline data landscape requiring robust metadata
- Critical need for consistent metadata on sensors, calibration, time scales, units, and data processing steps
- Cross-dataset integration demands careful harmonization of measurement methods and conversion factors
- Data governance should address scattering of datasets (some outside central repositories) and legacy documentation gaps
- Plan for ongoing data quality checks, data provenance, and clear access procedures to support reuse and cross-network collaboration