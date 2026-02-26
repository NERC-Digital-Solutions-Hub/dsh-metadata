# Climoor field site in Clocaenog forest Supporting documentation for data

- Overview: Climoor is a climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years. The site (established 1998) is remote, powered by solar and wind, and features replicated drought and warming treatments with control plots.

- Experimental design and treatments:
  - Nine plots total: 3 warming (W), 3 drought (D), 3 control (C) across 4 m x 5 m plots.
  - Treatments are arranged in blocks to mirror shading effects from the experimental structures.
  - Drought treatment reduces growing-season rainfall (and annual rainfall) via retractable polyethylene roofs triggered by tipping-bucket sensors; periodically adjusted during years (May–Sept originally, since 2012 Apr–Oct).
  - Warming treatment uses retractable aluminium mesh curtains to reduce infrared loss; roofs retract during rainfall to preserve rainfall, with wind thresholds for curtain operation (>10 m/s).
  - Data availability spans 1997–present for many datasets; the drought and warming timing and reductions vary by year.

- Site and ecology (key context):
  - Upland moorland ecosystem dominated by Calluna vulgaris (heather), with Vaccinium myrtillus and Empetrum nigrum present.
  - Humo-ferric podzol soil; site characteristics (soil horizons, depth, N deposition, etc.) described in tables.

- Data types and time ranges (dataset catalogue):
  - AWS meteorological data: daily measurements from on-site automated weather station (AWS); 1999–present.
  - Micro-meteorological plot data: daily measurements of plot soil/air temperature and soil moisture; 1998–present.
  - Rainfall data: site-level storage rainfall gauge (biweekly sampling) and rainfall chemistry (pH, NO3, Cl, SO4, DOC, ammonium) collected biweekly; 1998–present.
  - Throughfall data: plot-level rainfall collected biweekly; used to compute plot rainfall as percent change relative to site rainfall; 1999–present.
  - Water table depth data: measured from 2009 onward using permeable tubes; biweekly to periodic measurements.
  - Soil respiration data: CO2 efflux measured with collars; 1999–present with multiple measurement systems (CIRAS-2, LI-COR 8100, automated systems); site-wide daily–weekly campaigns in 2013–2014.
  - Trace gases (CH4 and N2O): measurements using closed chambers; 1999–2000 and 2007–2009.
  - Net ecosystem CO2 exchange (NEE): measurements in 2002–2004 and 2011; includes respiration adjustments and biomass normalization.
  - Photosynthesis data: ambient measurements and response curves; 2001–2003 and additional fixed-Ci PAR measurements in 2001–2007.
  - Vegetation survey data (plant biomass) – Pin Point analysis: annual surveys (1998–2012) across three quadrats per plot; pin hits converted to biomass using species-specific calibration; includes bryophytes pooled.
  - Canopy reflectance: spectral reflectance (NDVI and PRI) measured in 2000–2004.
  - Vegetation phenology, annual growth and pathogen assessment: spring phenophases and growth metrics for C. vulgaris, V. myrtillus, E. nigrum; 1998–2009 (extended beyond to present for phenology).
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; green and senesced material; collected 1998–present.
  - Litterfall: monthly sampling 1999–2002; pooled yearly data for litter mass and C/N analyses; continued sporadically afterward (post-2002).
  - Root biomass: multiple methods across 2003–2013 (soil cores, washing, WinRHIZO analysis) to quantify fine/root biomass.
  - Soil microbial biomass: chloroform fumigation method; 2000–2001 and 2012.
  - Nitrogen mineralisation: soil core incubations; 1998–2004.
  - SOM, SOC and bulk density: derived from soil cores linked to N mineralisation studies; 1999–2004 and 2013; calculations include SOM, SOC (as ~55% of SOM) and bulk density for g m-2 conversions.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; 1998–2008; pH, NO3, Cl, SO4, DOC, NH4 analyzed.
  - Appendix data: site layout and quadrat arrangement provided.

- Data collection methods and units (highlights):
  - Data collected with a range of sensors and methods; detailed sensor specs, depths, and instruments provided for each dataset.
  - Data are stored in various formats (RTF, CSV/Excel-derived files; some legacy notes indicate non-uniform documentation).
  - Data quality control primarily through manual visual checks in Excel; some newer datasets employ standardized processing (e.g., HMR package in R for soil respiration).
  - Unit conversions and cross-dataset harmonization are documented (e.g., converting CIRAS/Li-COR units to mg CO2-C m-2 h-1; applying conversion factors for NEE and respiration).

- Data processing notes and caveats:
  - Legacy data: some datasets (notably trace gases and NEE) acknowledge less rigorous documentation of data processing steps.
  - Throughfall data handling: plotting and exclusion rules for missing/corrupted data; occasionally infilled with year-average reductions.
  - Automated vs. manual measurements: changes in instrumentation over time; some datasets involve different measurement systems (e.g., soil respiration methodologies pre- and post-2008).
  - 2016 drought roofs: not in operation due to refurbishment; noted as a data-era caveat for that year.

- Data access and contact:
  - Not all data are stored within the Edward (EIDC) repository; contact details provided for further details.
  - Primary contact points: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

- Appendix and site context:
  - Appendix 1–3 include site layout, quadrat configuration, and plot arrangement for reference and reproducibility.

- Practical applications for data support:
  - Comprehensive, multi-year climate manipulation dataset suitable for cross-plot and cross-dataset analyses of warming and drought effects on upland moorland ecology.
  - Enables integration of meteorology, hydrology, soil biology, vegetation dynamics, and biogeochemistry to study ecosystem responses to climate change.