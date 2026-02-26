# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment using automated roof technology to simulate drought and warming effects over the next 20–30 years.
- Located in Clocaenog Forest, North East Wales; upland moorland ecosystem dominated by Calluna vulgaris (heather) with a mix of Vaccinium myrtillus, Empetrum nigrum, and other species.
- Established in 1998; measurements span abiotic and biotic variables across multiple data streams and years.

## Climate change treatments and experimental design

- Treatments: drought and warming, each with three replicated plots plus three controls to mirror shading (total of 9 plots in the layout; organized into blocks).
- Drought treatment: running May–Sept (1999–2011), later Apr–Oct (since 2012), achieved with retractable polyethylene roofs that exclude rainfall, reducing site rainfall by about 20% and growing-season rainfall by up to ~80% during drought periods.
- Warming treatment: night-time warming via retractable aluminium mesh curtains that reflect infrared radiation; roofs retract during rain to preserve rainfall, causing some rainfall exclusion (annual rainfall reduction ~14% on average); operation constrained by wind (>10 m/s) restrictions.
- Site characteristics: humo-ferri c podzol soil; variable horizons (E and Bh not always visible); diverse plant assemblage with bryophytes indicated in Table notes.
- Data collection spans a broad suite of abiotic and biotic measurements across the plots, with AWS and plot-level sensors integrated into the study.

## Data and datasets collected (high-level categories)

- AWS meteorological data (daily): temperature, humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
- Micro-meteorological plot data (daily): soil and air temperature, soil moisture at several depths.
- Rainfall data (site level): storage rain gauge with biweekly collection; rainfall chemistry from warren spring collectors (pH, NO3-, Cl-, SO4, DOC, ammonium).
- Throughfall data (plot level): plot-level rainfall collected biweekly; used to scale to treatment-level rainfall.
- Water table depth (biweekly to current): permeable tubes to bedrock.
- Soil respiration (fortnightly to high-resolution): CO2 efflux measured with closed-system chambers; multiple measurement approaches over time (CIRAS-2, LI-COR 8100, later automated systems).
- Trace gases (CH4 and N2O) (periodic): static chamber approach with GC analysis.
- Net ecosystem CO2 exchange (NEE) (2002–2004, 2011): chamber-based CO2 flux measurements; biomass-adjusted for plot differences.
- Photosynthesis (ambient and response curves): measurements on Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum using CIRAS-2 and fixed PAR/CO2 levels; leaf-level and species-specific data.
- Vegetation survey data (plant biomass) via pin-point method: multi-year, three quadrats per plot; biomass conversion factors established (Table 6) to convert pin hits to g/m2; includes bryophytes pooled.
- Canopy reflectance: ground-based spectrometer measurements (NDVI, PRI) for several plots and species, 2001–2004 with targeted sampling near solar noon.
- Vegetation phenology, annual growth and pathogen assessment: shoot elongation, budburst, leaf counts, and signs of herbivory/pathogen infection for C. vulgaris, V. myrtillus, E. nigrum; measurements across multiple years.
- Vegetation chemistry: chemical composition (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) for green and senesced material.
- Litterfall: monthly to yearly collections (1999–2002, then less frequent); litter dried and weighed; carbon and nitrogen analysis.
- Root biomass: sampling across several years (2003–2013) using soil cores and destructive extraction; detailed stratified methods for organic/inorganic horizons.
- Soil microbial biomass: chloroform fumigation technique (2000, 2001, 2012) with DOC extraction and correction factor to obtain microbial biomass carbon.
- Nitrogen mineralisation: soil-core incubation studies (1998–2004) with NH4+/NO3- analysis to calculate net mineralisation and ammonification rates.
- SOM, SOC and bulk density: analysis on paired cores from mineral/organic horizons; SOM via weight loss, SOC via SOM×0.55, bulk density calculations and extrapolation to g/m2.
- Soil solution and leachate chemistry: lysimeters and tensioned soil water samplers (biweekly); pH, NO3-, Cl-, SO4, DOC, ammonium analyses.

- Note on data storage: Not all data are stored within the EIDC; smaller/less-frequent datasets and post-June 2015 data may be stored elsewhere. For details or access, contact project contacts.

## Data collection, equipment, and data processing

- On-site instrumentation:
  - AWS met data: uses HMP sensors, pyranometers, PAR sensors, barometer, tipping bucket rain gauge; data logged hourly; minute-level sampling with hourly averages; quality control via visual inspection.
  - Micro-met data: soil temperature at 5/10/20 cm, soil moisture via TDR or earlier methods; hourly averages; daily to hourly time scales.
- Data processing and units:
  - CO2 flux conversions across instruments (g CO2 m-2 h-1 and µmol m-2 s-1) to mg CO2-C m-2 h-1 using standard conversion factors.
  - NEE and photosynthesis calculations adjusted for biomass using above-ground biomass measurements from chamber bases and pin-point biomass calibrations.
  - Soil respiration data integrated across varying measurement systems (CIRAS-2, LICOR 8100, automated systems) with documented conversion factors.
- Quality and provenance:
  - Legacy data note: documentation of data processing steps may be incomplete; best practic es for some datasets may be lacking due to historical practices.
  - Throughfall and rainfall data handling involves substitution rules when data are lost or compromised; some years require data infill with average reductions.
  - Plot-level adjustments (e.g., biomass-based normalization) rely on species-specific calibration factors and pin-hit to biomass conversions (see Table 6).

## Data governance, availability, and access

- Data governance and stewardship considerations:
  - Large, multi-method dataset with many data streams; data come from multiple instruments and analysis approaches over many years.
  - Not all data are stored in a central repository (EIDC) and some legacy datasets may reside elsewhere; contact project leads for access.
  - Documentation exists (supporting documentation files) but some data processing steps are not comprehensively documented due to legacy practices.
  - Key contacts for data details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Data discovery and use:
  - Datasets are named and described in supporting documentation; care required when combining legacy data with more recent measurements due to methodological changes over time.
  - Potential use includes climate-impacts analyses, vegetation dynamics under drought and warming, soil carbon and nitrogen cycling, and ecosystem gas flux studies.

## Particular challenges and considerations for Data Stewards

- Incomplete or evolving understanding of user needs and priorities for long-term data use.
- Timely access to data from ongoing field campaigns and integration of replicated treatments across plots.
- Ensuring data creators' metadata, format, and standards meet governance needs; alignment with current data portals and catalog schemas.
- Interoperability across many data types (from AWS to soil chemistry) and handling of large, heterogeneous datasets.
- Managing updates to datasets (e.g., throughfall adjustments, biomass normalization) and documenting data lineage.
- Dealing with legacy data gaps in documentation and achieving consistent, transparent data provenance.

## Appendix and site layout

- Appendix 1: Site layout and plot arrangement.
- Appendix 2: Quadrat layout showing measurement areas within plots.
- Appendix 3: Plot Layouts and labeling conventions for legacy site data (e.g., LYS, PQ, SS codes).

- Grid reference for the Clocaenog site: SJ019519; latitude/longitude 53.055N, -3.465W.