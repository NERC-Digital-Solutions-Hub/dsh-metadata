# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment using automated roof technology to simulate drought and warming scenarios expected over the next 20–30 years.
- Powered by solar and wind; established in 1998; consists of replicated drought and warming treatments with three replicate plots per treatment and three controls, totaling 9 plots.
- Location: Clocaenog Forest, North East Wales; upland moorland ecosystem dominated by Calluna vulgaris (heather) with a mix of shrub and bryophyte species.
- The documentation describes site information, climate treatment details, equipment, data processing methodologies, and a broad suite of data types collected over time.

## Climate change treatments and site layout
- Treatments and replication
  - Two climate treatments: warming (W) and drought (D), plus control (C) plots; arranged in 3 blocks with 3 plots per block (n=9 total).
- Drought treatment
  - Uses retractable polyethylene roof to exclude rainfall during the growing season; rain reduction ~20% annually, with ~80% of rain excluded during active drought periods.
  - Timing: originally May–Sept (1999–2011); since 2012, April–October; closed during high winds (>10 m/s) to prevent damage.
- Warming treatment
  - Uses retractable aluminium mesh curtains to reduce heat loss at night by reflecting infrared radiation; nightly closure triggered by light measurements and rainfall triggers to avoid rainfall loss.
  - Annual rainfall reduction ~14%; also not operated in high winds.
- Plot configuration
  - Each treatment has three replicate plots; additional scaffolding controls mirror shading effects; block design aids experimental control.

## Data types and data collection
- AWS meteorological data
  - Measurements: temperature, humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Frequency: daily; sensors sample every minute; data processed to hourly averages.
  - Data quality: basic visual QC in Excel; some limitations acknowledged (not all automated checks applied).
- Micro-meteorological plot data
  - Soil/air temperature and soil moisture measured at multiple depths; daily sampling; logging frequency transitioned (pre- and post-2016) to hourly or 0.5-hourly averages.
- Rainfall and rainfall chemistry
  - Site-level rainfall via storage rain gauge (biweekly samples preferred for robustness over logger-based data).
  - Rainfall chemistry via Warren spring collectors; analyses include pH, NO3, Cl, SO4, DOC, ammonium.
- Throughfall data
  - Plot-level rainfall collected with funnels/bottles; biweekly collection; data used to compute treatment-specific rainfall changes by applying percent differences to site-level rainfall.
- Hydrology
  - Water table depth measured with permeable tubes (since 2009); manual biweekly readings; maximum detectable depths per plot documented.
- Soil respiration and trace gases
  - Soil CO2 efflux measured fortnightly (1999 onward) with collars; measurement methods evolved (CIRAS-2, LI-COR 8100, automated systems); data converted to mg CO2-C m^-2 h^-1 using specified unit conversions.
  - CH4 and N2O fluxes measured using static chambers; sampling at 0, 15, and 30 minutes; analyzed via GC with calibration procedures noted.
- Net ecosystem CO2 exchange (NEE)
  - Measured in selected years (2002–2004, 2011) with different chamber systems; fluxes converted to mg CO2-C m^-2 h^-1; adjustments made for biomass differences using above-ground measurements within chambers.
- Photosynthesis
  - Ambient photosynthesis and response curves (PAR and Ci) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; several years (2001–2007) with fixed CO2 or PAR conditions; data captured in CIRAS and other field instruments.
- Vegetation biomass and structure
  - Pin-point vegetation surveys (1998–2012) across three quadrats per plot; 300 pin hits per plot converted to biomass using species-specific calibration factors; adjustments for missing pins applied with conversion factors.
- Canopy reflectance
  - Ground-based spectral measurements (400–950 nm) to calculate NDVI and PRI indices; measurements around solar noon on sunny days (2001–2004).
- Phenology, growth, and pathogens
  - Spring phenology and shoot elongation measurements for dominant shrubs (1999–2009, plus selected years); budburst and leaf emergence tracked for Vaccinium myrtillus and pathogen presence (rust Valdensia heterodoxa) noted.
- Vegetation chemistry
  - Green and senesced material analyzed for C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates; samples prepared from both live and litter material.
- Litterfall
  - Litter traps (12 collectors) emptied monthly (1999–2002); later frequency reduced; litter dried, weighed, and converted to g m^-2; pooled by quadrat/year for carbon and nitrogen analyses.
- Root biomass
  - Root sampling across several years (2003–2013) with soil cores; multiple methods used (manual root extraction, sieving, WinRHIZO analysis) to quantify biomass.
- Soil microbial biomass
  - Chloroform fumigation method (2000, 2001, 2012) with DOC extraction; microbial biomass carbon derived from fumigated vs. unfumigated samples.
- Nitrogen mineralisation
  - Sporadic measurements (1998–2004) using paired cores to measure ammonium and nitrate fluxes after incubation in the field and lab.
- Soil organic matter, carbon, and bulk density
  - SOM and SOC measured on paired cores; SOM% and SOC% calculated, with bulk density estimates computed to express SOM/SOC per m^2.
- Soil solution and leachate chemistry
  - Lysimeters and tension samplers installed in 1998; biweekly sampling; analysis includes pH, NO3, Cl, SO4, and DOC.

## Data processing, formatting, and quality notes
- Data processing
  - Multiple instruments and methods across years; unit conversions documented (e.g., soil respiration flux units; CO2 to CO2-C conversions; NEE flux calculations).
  - Legacy data: some processing steps and best practices not consistently documented; data entries may reflect non-standardized older workflows.
- Data integration considerations
  - Throughfall and plot-level rainfall adjustments require careful treatment of missing data and occasional infilling with year-wide averages.
  - Biomass-based flux corrections (NEE) rely on above-ground biomass measurements within chambers; spatial variability in biomass addressed during analysis.
- Data availability and access
  - Not all data are stored in the on-site Electronic Information/Data Centre (EIDC); smaller, infrequently collected, or post-2015 datasets may be outside the EIDC.
  - Primary contacts for data access and details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

## Metadata, provenance, and governance
- Documentation references
  - Data structured in a set of topic-specific RTF data inventories (e.g., SD_...rtf files) with explicit sensor types, methods, and time scales.
  - Appendix materials include site layout and quadrat configurations, providing spatial metadata for data alignment.
- Site and data provenance
  - Detailed protocols for each data stream, including instrument models, sampling frequencies, and processing equations, facilitate traceability and reproducibility.
  - Some datasets (e.g., later years or smaller, infrequent datasets) may require direct inquiry to determine availability and completeness.

## Key takeaways for data leadership
- The Climoor documentation outlines a comprehensive, multi-decadal data ecosystem combining meteorology, hydrology, soil biology, vegetation ecology, and biogeochemistry under controlled climate manipulations.
- Data management challenges stem from: long time series with evolving instrumentation; multiple data formats and storage locations; partial data availability outside central repositories; and legacy processing practices.
- For data strategy and governance, prioritize:
  - Consolidated metadata standards for cross-dataset discovery and integration.
  - Documentation of data provenance, processing steps, and unit conversions to ensure reproducibility.
  - Clear data access governance, with a centralized catalog or EIDC entry for datasets, and explicit liaison points (e.g., CEH Bangor contacts).
  - Ongoing data quality assessment, including handling of missing/infilled data and harmonization across measurement methods.
  - Security and continuity planning for field sites and automated measurement systems to minimize data gaps.