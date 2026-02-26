# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope
  - Climoor is a climate change manipulation experiment using automated roof technology to simulate drought and warming for upland moorland, reflecting climate predictions for the next 20–30 years.
  - Document provides supporting data and methodologies for environmental monitoring and analysis.

- Site description
  - Location: Clocaenog Forest, North East Wales (53°03'19"N, 3°27'55"W).
  - Habitat: upland west-atlantic moorland dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum present.
  - Soils: humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; site established in 1998.
  - Plot layout: replicated drought (D) and warming (W) treatments with three replicates each, plus three control plots (n=9 total). Scaffolding mirrors shading effects on treatment plots.

- Climate change treatments and implementation
  - Drought treatment
    - Method: retractable polyethylene roof over 4 m x 5 m plots triggered by tipping bucket rainfall sensors; reduces annual rainfall by ~20% and excludes ~80% of rain during drought period.
    - Timing: operated May–Sept (1999–2011); since 2012, April–October.
    - Wind constraint: curtains do not operate in winds >10 m/s.
  - Warming treatment
    - Method: retractable aluminum mesh curtains covering warming plots; reflects 96–97% of infrared radiation, reducing night heat loss by ~64%.
    - Rainfall interaction: roof retracts during rain to minimize rainfall exclusion; timing linked to light/dark thresholds.
    - Wind constraint: curtains not operated in high winds.
  - Experimental design and timing
    - Treatments organized into 9 plots across blocks; each treatment replicated in several blocks.
    - Historical data span 1997–2016; 2016 drought roofs were not in operation due to refurbishment.
  - Data provided on treatment performance
    - Drought: annual and growing-season rainfall reductions reported by year (example reductions from 1997–2014, with detailed yearly figures available).
    - Warming: growing degree days (GDD) changes reported by year, illustrating warming effect magnitude.

- Data collection, protocols and data types
  - Data governance and data availability
    - On-site automated weather station (AWS) and plot-level sensors; broader abiotic and biotic datasets collected.
    - Not all data stored in the central EIDC repository; contact CEH Bangor for access details (Sabine Reinsch, Bridget Emmett).
  - Equipment and data catalog (examples)
    - AWS meteorological data: daily/hourly measurements (temperature, humidity, rainfall, pressure, net/radiation, PAR, wind).
    - Micro-meteorological plot data: soil and air temperature, soil moisture (various methods), plotted daily.
    - Rainfall data: site-level storage rain gauge (biweekly sampling) plus rainfall chemistry (pH, NO3, Cl, SO4, DOC, ammonium).
    - Throughfall data: plot-level rainfall collected biweekly; data gaps addressed by applying percent reductions to site rainfall data.
    - Hydrology: water table depth via permeable tubes (biweekly).
    - Soil respiration: CO2 efflux measured with collars; methods evolved (CIRAS-2, LICOR 8100, automated systems); hourly or daily campaigns; units converted to mg CO2-C m-2 h-1.
    - Trace gases: CH4 and N2O measured with static chambers; gas samples analyzed by GC.
    - Net ecosystem CO2 exchange (NEE): measured in select years (2002–2004, 2011) with different chamber systems; respiration and photosynthesis estimated using biomass corrections.
    - Photosynthesis: ambient and response-curve measurements across several years; PAR and Ci vary; leaf-area considerations for averageization.
    - Vegetation biomass (Pin-Point), canopy reflectance, phenology and growth, pathogen assessments, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC/bulk density, soil solution and leachate chemistry.
  - Data processing notes and quality
    - Data processing spans multiple instrument generations; unit conversions documented (e.g., soil respiration: g CO2 m-2 h-1 to mg CO2-C m-2 h-1; CH4/N2O flux estimation from chamber data).
    - Legacy data: some processing steps not aligned with current best practices; data quality control often performed via manual/visual checks rather than automated constraints.
    - Data handling for throughfall and rainfall: data gaps due to equipment or field issues are sometimes infilled using year-average reductions; corresponding caveats apply.
  - Data structure and documentation
    - Each data type has dedicated datasets/files with measurement methods, frequency, time scales, and documentation pointers.
    - Appendix contains site layout and quadrat configurations; detailed codes for vegetation pin-point data and biomass conversions.

- Data quality, gaps and governance challenges
  - Key challenges aligned with monitoring frameworks
    - Data gaps and incomplete time series due to equipment downtime and refurbishment.
    - Access barriers and metadata gaps in some datasets; older data parts may lack comprehensive documentation.
    - Siloing across datasets and evolving methodologies complicate integration; legacy formats require careful interpretation.
    - Public sharing of underlying data and metadata may be constrained; data governance and openness need clear standards.
  - Data provenance and transparency
    - Detailed equipment histories, measurement procedures, and unit conversions are provided, with explicit notes on legacy practices and adjustments.
    - Researchers are encouraged to contact CEH Bangor for data details and access.

- Appendices and site context
  - Appendix 1–3: site layout, quadrat layouts, and plot configurations; additional materials document LYS/PQ/SS identifiers and broader plot mapping.
  - The document includes a comprehensive table of climate treatment timings, annual rainfall reductions, and warming-degree changes by year.

- Key takeaways for monitoring framework authors
  - Climoor provides a long-running, multifaceted environmental monitoring dataset with drought and warming treatments, offering rich temporal and spatial resolution across meteorological, hydrological, physiological, chemical, and biodiversity dimensions.
  - The documentation demonstrates the importance of: detailed treatment prescriptions; robust metadata; data provenance across instrument generations; transparent data processing notes; and governance for data access and sharing.
  - Practical challenges highlighted include data gaps, interoperability of legacy data, and barriers to data openness—areas that monitoring frameworks should explicitly address through standardized data schemas, versioning, and accessible metadata.