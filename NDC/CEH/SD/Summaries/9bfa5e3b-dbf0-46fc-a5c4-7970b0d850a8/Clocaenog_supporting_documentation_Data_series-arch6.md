# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope
  - Documents data collected from Climoor climate-change manipulation at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
  - Data cover both abiotic and biotic responses across multiple years and measurements, with the aim of enabling data users to explore climate-perturbed ecosystem processes and generate data products.

- Site and treatments
  - Location and ecosystem: upland moorland dominated by Calluna vulgaris (heather); soil described as humo-ferric podzol.
  - Treatments: two climate manipulations (drought and warming) with three replicates each and three control plots (total n=9). Treatments arranged in blocks.
  - Drought: retractable polyethylene roofs reduce rainfall (May–Sept, historically; since 2012 April–October) by roughly 14–80% depending on year and method, with some rainfall events missed by sensor limits.
  - Warming: retractable aluminium mesh curtains reduce night-time heat loss; rain re-entry timed to minimize rainfall loss, with operation halted in high winds (>10 m s^-1).
  - Design notes: tables summarize treatment timing, block assignment, and long-term changes (e.g., drought roof refurbishment in 2016).

- Data types and data collection
  - AWS meteorological data: minute-level sensors (air temp, RH, rainfall, wind, radiation, PAR, etc.), collected continuously with daily/hourly aggregation; data quality checked visually.
  - Micro-meteorological plot data: daily soil/air temperature and soil moisture at multiple depths; evolving measurement methods over time.
  - Rainfall and rainfall chemistry: site-level storage rain gauge biweekly samples; plot-level throughfall data biweekly; chemical analyses (pH, NO3, Cl, SO4, DOC, NH4) using standard lab techniques.
  - Throughfall: plot-level rainfall fractions used to derive treatment-specific rainfall by applying percent differences to site-level rainfall data; data gaps treated with exclusions or infill when appropriate.
  - Water table depth: biweekly measurements via permeable tubes to bedrock (from 2009 onward); maximum detectable depths per plot noted.
  - Soil respiration: CO2 efflux measured with collars; method evolved from static chambers and CIRAS-2 to LI-COR systems; automated campaigns in 2013–2014; units converted to mg CO2-C m^-2 h^-1.
  - Trace gases (CH4 and N2O): measured with static chambers linked to a gas chromatograph; headspace sampling at multiple time points; legacy processing notes indicate inconsistent documentation of data processing.
  - Net ecosystem CO2 exchange (NEE): measured in 2002–2004 and 2010–2011 with different chamber systems; adjustments made for biomass differences in flux calculations.
  - Photosynthesis: ambient measurements and response curves (PAR and Ci) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; data include leaf mass/area considerations for standardization.
  - Vegetation survey (Pin-Point biomass): annual quantification (1998–2012) using pin-point hits across quadrats; conversion factors provided to translate hits into biomass; calibration via destructive sampling in 2000.
  - Canopy reflectance: NDVI and PRI indices from ground-based spectrometry (2001–2004) for plant condition assessment.
  - Vegetation phenology and pathogens: shoot elongation, budburst, leaf emergence, flowering, and pathogen signs tracked annually (1999–2009, with ongoing measurements later).
  - Vegetation chemistry: elemental composition (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) for green and litter material.
  - Litterfall: monthly collection (1999–2002), later less frequent; conversion to litter mass per area with carbon and nitrogen analyses.
  - Root biomass: cores and extraction across multiple years (2003–2011) using several methods; detailed depth-specific root processing.
  - Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012) with DOC analysis to estimate microbial biomass C.
  - Nitrogen mineralisation: incubation-core approach (1998–2004) to derive ammonium and nitrate fluxes.
  - SOM, SOC and bulk density: paired cores to determine soil organic matter, carbon content, and bulk density; results converted to g m^-2.
  - Soil solution and leachate chemistry: lysimeters and tension samplers (1998 onward); biweekly to monthly sampling for pH, NO3, Cl, SO4, DOC.

- Data processing, formats, and units
  - Standardized unit conversions across datasets (e.g., soil respiration units to mg CO2-C m^-2 h^-1; flux conversions between CIRAS-2, LICOR 8100, and other instruments using documented factors).
  - biomass adjustments: flux measurements adjusted for plot biomass differences using above-ground biomass from pin-point surveys; biomass-based calibration factors provided (Table 6).
  - Throughfall calculations: used to derive treatment-specific rainfall by applying percent reduction to site rainfall; data exclusion and occasional infilling when data gaps occurred.
  - Vegetation data: pin-hit to biomass calibrations (Table 6); pin-hit counts corrected for missing pins (e.g., 300 pins per plot) using a ratio-based adjustment.
  - Canopy reflectance: NDVI and PRI indices computed from spectral bands; standard NDVI680, NDVI570 formulas included.
  - Data quality and documentation: data processing notes acknowledge legacy practices; some datasets lack complete processing documentation; 2016 note indicates drought roofs not operated due to refurbishment.

- Data availability and contact
  - Not all data are stored in the Environmental Information Data Centre (EIDC); some datasets are stored externally or in project-specific files.
  - For access or details, contact CEH Bangor personnel (Sabine Reinsch, Bridget Emmett) named in the document.

- Appendices and site layout
  - Appendix 1–3: site and plot layouts, including quadrat arrangements and plot identifiers, aiding geospatial interpretation of measurements.

- Key limitations and considerations for data users
  - Legacy data handling: some data processing steps are not fully documented; caution advised when reusing older measurements (e.g., trace gas and NEE data).
  - Treatment data gaps: drought-roof operation paused in 2016 due to refurbishment; throughfall and rainfall treatment integrity may vary by year.
  - Data gaps and infill: treatment means sometimes calculated with fewer than the full replicates; occasional data infilling applied in cross-year analyses.

- Potential data products and uses
  - Enables cross-cutting analyses of drought and warming effects on carbon, nitrogen, water fluxes, and plant–soil–microbe interactions.
  - Supports model calibration and validation for climate-perturbed upland heath ecosystems.
  - Provides a rich baseline for temporal trends in vegetation dynamics, soil processes, and trace gas exchanges under simulated climate change.