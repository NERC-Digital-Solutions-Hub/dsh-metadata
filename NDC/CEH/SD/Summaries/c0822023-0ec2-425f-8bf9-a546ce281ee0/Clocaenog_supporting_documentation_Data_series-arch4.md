# Climoor field site in Clocaenog forest Supporting documentation for data

- Overview
  - Climate change manipulation experiment at Clocaenog Field Site (upland moorland in North East Wales), established in 1998.
  - Automated roof technology creates drought and warming treatments to reflect 20–30 year climate projections.
  - Treatments: drought, warming, and controls (replicated across plots); site-powered by solar and wind.
  - Diverse data types collected across physical, chemical, and biological domains to study ecosystem responses.

- Data assets and structure (datasets and scope)
  - AWS meteorological data (daily; 1999–current but with document up to 2015) and micro-meteorological plot data (daily; 1998–current).
  - Rainfall and rainfall chemistry at site level (storage rain gauge; monthly/biweekly) and plot-level throughfall data (biweekly; 1999–current).
  - Hydrology: water table depth (2009–current) via permeable tubes.
  - Biogeochemistry and soil processes: soil respiration (fortnightly and automated), trace gases CH4 and N2O (via static chambers), net ecosystem CO2 exchange (NEE; 2002–2004, 2009–2011), nitrogen mineralisation, soil solution and leachate chemistry.
  - Plant and vegetation data: photosynthesis (infrequent; early 2000s), vegetation survey data (pin-point biomass; 1998–2012 with ongoing post-2012 data), canopy reflectance (NDVI/PRI indices; 2000–2004), vegetation phenology, annual growth, pathogen assessment, vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates).
  - Litter and roots: litterfall (1999–2002; then irregular), root biomass (various years/ methods), soil microbial biomass (chloroform fumigation), SOM/SOC/bulk density (soil cores), soil solution chemistry (lysimeters and tension lysimeters).
  - Appendix data: site layout and quadrat geometry for spatial context.
  - Data hosting: not all data stored in a single portal; some datasets stored outside the primary portal (EIDC); contact points below for access.

- Data collection, methods, and processing (highlights relevant to governance)
  - Equipment and sensing
    - AWS met data: multiple sensors (temperature, humidity, rainfall, pressure, net radiation, PAR, wind); data logged hourly; originally at 1 m but moved to 4 m mast after 2007 due to theft.
    - Micro-mete plots: soil temperature at multiple depths; soil moisture via TDR or earlier methods; hourly averages.
  - Data processing and units
    - Fluxes: soil respiration and NEEs converted to mg CO2-C m-2 h-1; documented unit conversions (e.g., g CO2 m-2 h-1 and µmol m-2 s-1 to mg CO2-C m-2 h-1).
    - Pin-point vegetation data: pin hits converted to biomass via species-specific calibration factors; normalisation to 300 pins per plot; 1998–2012 datasets with calibration updates.
    - Litterfall: collected, dried, weighed; converted to g m-2; carbon and nitrogen analyses in CEH Lancaster.
  - Data quality and legacy notes
    - Data quality control relied on manual quality checks; some legacy data lack complete documentation of processing steps.
    - Some datasets (e.g., early trace gas/NEE methods) have multiple instrument changes; cross-dataset conversion requires careful provenance.
  - Data gaps and irregularities
    - Throughfall data may exclude certain plots when samplers fail; occasional infilling with year-wide averages; some replicates may be omitted in treatment means.
    - Not all datasets are continuously updated in the central data portal; some data remain outside the main repository.

- Data governance, access, and metadata
  - Data stewardship
    - Data described with dataset-specific supporting documentation (rtsf files) detailing sensors, time scales, and methods.
    - Summary tables exist for major datasets; cross-year methodological changes documented in the text.
  - Access and discovery
    - Some datasets stored within CEH data hubs; not all are in the EIDC; contact points provided for data access and clarifications.
    - Primary contacts for data provisioning: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk).
  - Documentation and provenance
    - Dataset documentation exists but processing provenance for legacy datasets is sometimes incomplete.
    - Appendix materials provide site layout and quadrat arrangements to support spatial analyses.
  - Data scope and maturity
    - Long-running, multi-disciplinary dataset with multi-method changes over time; useful for integrated ecosystem analyses but requires careful harmonisation and provenance tracing for cross-study synthesis.

- Practical implications for data leaders (takeaways and recommendations)
  - Centralise metadata and data dictionaries
    - Create a unified metadata schema across all datasets (sensor specs, time scales, units, calibration factors, and data processing steps).
  - Standardise units and provenance
    - Maintain consistent flux units and document all conversions; preserve instrument-specific calibration details and version histories.
  - Ensure data discoverability and access
    - Integrate legacy datasets into the central data portal with clear access instructions and contact points; ensure DOIs or persistent identifiers where possible.
  - Strengthen data quality controls and documentation
    - Capture processing workflows, quality checks, and data quality flags; document gaps, assumptions, and infilling procedures.
  - Encourage data stewardship and co-ownership
    - Engage the wider data community and partner networks to steward datasets, ensure interoperability, and reduce duplication of effort.

- Contact and references
  - Authors: Alwyn Sowerby (original author); edited by Sabine Reinsch.
  - For data access or details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
  - Supporting documentation references: data-specific RTFs and dataset descriptions accompany each dataset.