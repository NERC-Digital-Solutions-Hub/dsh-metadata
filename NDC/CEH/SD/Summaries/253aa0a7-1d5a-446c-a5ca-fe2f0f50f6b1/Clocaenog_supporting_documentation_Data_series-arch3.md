# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope
  - Documenting a climate change manipulation experiment (drought and warming) at the Clocaenog upland moorland site.
  - Automated roof technology creates drought and warming treatments to reflect 20–30 year climate predictions.
  - Nine plots arranged as three warming, three drought, and three control (three replicates per treatment) across blocks; includes scaffolding controls to mirror shading.

- Site and experimental design
  - Location: Clocaenog Forest, North East Wales; upland west-atlantic moorland ecosystem.
  - Dominant vegetation: Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum; soil: humo-ferric podzol.
  - Established: 1998; remote, solar/wind powered, automated measurements and treatments.
  - Treatments: 
    - Drought (D): retractable polyethylene roof to exclude rainfall; ~20% reduction in annual rainfall; variable reduction of growing-season rain (up to ~80% during drought periods); operated May–Sept (1999–2011) and Apr–Oct (since 2012); curtailed in high winds (>10 m/s).
    - Warming (W): retractable aluminium curtains to reduce nighttime heat loss; limits rainfall within warming due to rain-triggered retraction; ~14% annual rainfall reduction on average.
  - Layout: 9 plots total, organized in blocks with specific mappings of treatment and block assignments.

- Climate change treatment details
  - Drought: timing and extent documented year-by-year (1997–2014 data provided); varying annual and growing-season rainfall reductions; operational constraints in some years.
  - Warming: growing degree days (GDD) changes recorded; year-by-year changes in warming effect; some years NA due to missing data.

- Data streams and collection (data catalog)
  - AWS meteorological data: daily, 1999–current; measurements include air temp, relative humidity, rainfall, air pressure, net and solar radiation, PAR, wind speed/direction.
  - Micro-meteorological plot data: daily; soil and air temperatures at 5, 10, 20 cm; soil moisture via TDR and prior methods.
  - Storage rain gauge data and rainfall chemistry: biweekly collection; site-level rainfall (robust gauge) and plot-level throughfall; chemical analyses of rainfall (pH, NO3-, Cl-, SO4-, DOC, NH4+).
  - Throughfall data (plot level rainfall): biweekly; used to derive plot-level rainfall by applying percent changes relative to site-level rainfall.
  - Water table depth data: biweekly since 2009; measures depth via permeable tubes (maximum detectable depths per plot specified).
  - Soil respiration data: fortnightly; multiple instruments over time (CIRAS-2, LI-COR 8100, automated systems); includes soil collars; flux expressed as mg CO2-C m-2 hr-1; both heterotrophic and autotrophic respiration included.
  - Trace gases (CH4 and N2O): measured with static chambers on the same collars; gas chromatography analyses; sampling at 0.25, 15, and 30 minutes; legacy data with notes on processing gaps.
  - Net ecosystem CO2 exchange (NEE): 2002–2004 and 2009–2011; two instrument systems used; flux units converted to mg CO2-C m-2 hr-1; adjustments for biomass where applicable.
  - Photosynthesis: ambient measurements and response curves (2001–2007 for various species); leaf-level measurements with CIRAS; includes leaf mass/area calibrations for standardization.
  - Vegetation survey data (Pin-point biomass): years 1998–2012; three quadrats per plot; 300 pins per plot; conversion from pin hits to biomass via species-specific calibration; includes procedures to adjust for missing pins.
  - Canopy reflectance: 2001–2004; NDVI and PRI indices from ground-based spectrometer measurements.
  - Vegetation phenology, annual growth, and pathogens: 1998–2009+; shoot elongation, budburst, leaves formed, herbivory and fungal infection records; species-specific phenophase scales.
  - Vegetation chemistry: 1998–ongoing; elemental analysis (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) from green and senesced material.
  - Litterfall: 1999–2002 monthly; after 2002 less frequent; litter collected, dried, weighed, and converted to g m-2; pooled per year for chemical analyses.
  - Root biomass: 2003–2004 soil cores; 2008 and 2011 multi-year core analyses; methods range from manual root extraction to WinRHIZO analyses.
  - Soil microbial biomass: chloroform fumigation methods (2000, 2001, 2012); DOC difference used to estimate microbial biomass carbon.
  - Nitrogen mineralisation: 1998–2004; paired cores with NO3- and NH4+ analyses after KCl extraction; mineralisation rates calculated from initial/final cores.
  - SOM, SOC and bulk density: cores from mineral/organic horizons; standard SOM and SOC determinations; bulk density calculated from core volume.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; monthly to biweekly samples; pH, NO3-, Cl-, SO4-, DOC, NH4+ analyses.

- Data processing, units, and methodological notes
  - Data processing across eras often used different equipment; unit conversions documented for CO2 flux (e.g., g CO2 m-2 hr-1 to mg CO2-C m-2 hr-1; µmol m-2 s-1 to mg CO2-C m-2 hr-1).
  - Early datasets include legacy processing notes; some methods evolved (e.g., soil respiration instrumentation) with explicit conversion factors and acclimation periods.
  - Throughfall processing relies on applying plot-level percent reductions derived from throughfall measurements to site-level rainfall data; data gaps lead to exclusion or infilling with year-average reductions.
  - Pin-point biomass calibration based on destructive sampling and species-specific conversion factors; QA includes cross-checks for pin counts (e.g., 300 pins per plot) and ratio corrections when pins are missing.
  - Canopy reflectance indices calculated (NDVI680, NDVI570, PRI) from spectral data; measurements taken in narrow time windows around solar noon.

- Data management, access, and governance
  - Central data storage and metadata: not all data stored in a single repository (EIDC); smaller or infrequently collected datasets may reside elsewhere; contact CEH Bangor for details.
  - Data quality and provenance: QC performed primarily through visual inspection and basic checks; some legacy data processing steps acknowledged as not fully documented.
  - Data sharing considerations: publicly sharing datasets can be a barrier for some data types; legacy datasets include notes about processing and data handling that may affect re-use.
  - Primary contacts for data queries: Sabine Reinsch and Bridget Emmett (CEH Bangor); original author: Alwyn Sowerby (edited by Sabine Reinsch).

- Practical caveats and challenges for monitoring frameworks
  - Data gaps and variable metadata quality across decades of measurement.
  - Silos and scattered storage locations complicating data discovery and integration.
  - Public data-sharing requirements potentially inhibiting access to raw datasets.
  - Data transformation needs (unit conversions, method changes, biomass adjustments) to enable cross-variable analyses.
  - Maintaining up-to-date metadata and provenance for diverse measurements (biogeochemical, acoustic, spectral, and demographic data).

- Appendix and supporting information
  - Site layout, quadrat layout, and plot identifiers included to facilitate spatial data interpretation and replication of analyses.