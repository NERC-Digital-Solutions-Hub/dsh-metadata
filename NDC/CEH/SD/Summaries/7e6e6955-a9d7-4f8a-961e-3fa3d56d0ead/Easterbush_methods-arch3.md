# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

- Overview
  - A long-term, multi-variable dataset from Easter Bush, South East Scotland (near Edinburgh), focusing on grazed, cut and fertilised temperate grassland.
  - Measurements span 2002–2010/2011 across meteorology, eddy covariance fluxes, greenhouse gases, soil properties, and management practices.
  - Data are collected at the South field (with instrumentation between two adjacent fields) and include detailed management and environmental context.

- Data content and structure
  - metdata_daily.csv
    - Daily meteorology and soil context: date, precipitation, temperature (daily avg/min/max), soil temperature, volumetric water content.
  - Flux_daily.csv
    - Ecosystem fluxes and gas exchanges: GPP, NPP, EcoResp, NEE; CH4, N2O (chamber and EC), NOx; CO2 exchange components; quality checks noted.
  - livestock_yield_fertiliser_daily.csv
    - Grazing/management records: stocking density (LSU and head per m2), animal numbers, forage yield/offtake (DM, N, C), mineral and organic fertiliser inputs.
  - N_C_leaching_flux_daily.csv
    - Leaching fluxes: DIC/DOC/DON, NH4, NO3; modelled groundwater recharge and precipitation; actual evapotranspiration (from latent heat flux).
  - N_C_leaching_conc_sampling_period.csv
    - Leachate concentrations: DIC/DOC (mg/L), TN/NH4/NO3 (mmol/L).
  - Dry_N_conc_monthly.csv
    - Monthly dry deposition concentrations: NH3, HNO3, NH4+, NO3- (from DELTA system).
  - soil_C_N_oneoff.csv
    - Total soil N and C content from May 2004 and May 2011, with depth resolution 0–60 cm and granular soil mass data.
  - metdata_daily.csv (soil and site context legend)
    - Depth-specific soil temperature and moisture, rainfall, and air temperature context; measurement depths noted (3.5, 7.5, 15, 30 cm).
  - Additional notes on data blanks indicate no measurements or missing days.

- Site and management context
  - Location and climate
    - Easter Bush, 10 km south of Edinburgh; mean annual precipitation ~947 mm; mean temperature ~9.0 °C (2002–2010).
    - Imperfectly drained Macmerry soil (Eutric Cambisol), pH 5.1, clay 20–26%.
  - Land management
    - Permanent grassland (>99% Lolium perenne; <0.5% Trifolium repens).
    - Continuous grazing by sheep (ewes and lambs) with some cattle; silage cuts in 2002, 2003; variable stocking densities.
    - Fertilisation with ammonium nitrate/urea (3–4 times per year; ~56 kg N ha-1 per application; 2008 extra mineral N with urea).
    - Organic manure (cattle slurry) applied in 2004 and 2005; slurry N and C contents analyzed; plant N and C analysed from harvested vegetation.

- Measurement methods and instruments
  - Gas and carbon fluxes
    - CO2 and energy fluxes via eddy covariance system (fast 3D ultrasonic anemometer and LI-COR 7000 IRGA) with data at 20 Hz; QC includes u* threshold, plausible CO2 concentration ranges, and sensible/latent heat flux ranges.
    - NEE partitioning into GPP and TER using online Reichstein et al. (2005) tool; NPP assumed as 50% of GPP.
    - CH4 and N2O fluxes measured with eddy covariance (short period, 2002–2003) and closed chambers (2006–2009); chamber details include 0.4 m diameter, 0.2 m height and sampling over ~60 minutes.
    - NOx fluxes measured 2009–2010 with autochambers and NOx/ozone analyzers; multiple daily closures with control chamber accounting for in-tube reactions.
  - Soil, water, and deposition measurements
    - Soil and water gas/solution measurements using suction cups (0.5–1 µm pore size) at 30 cm and 90 cm depths for leachates; dissolved inorganic/organic C and N analysed via CFA/colorimetry; leachate fluxes derived from soil water balance.
    - DELTA denuder-based atmospheric deposition sampling for NH3, HNO3, NH4+, NO3- at a nearby location (~300 m away).
    - Dry deposition totals computed from monthly gas/particle concentrations.
    - Soil C and N content measured by dry combustion on 2004 and 2011 samples; cores collected on a regular grid (10 m spacing) with depth stratification (0–60 cm).
  - Meteorology and site monitoring
    - Continuous soil temperature and volumetric water content at multiple depths; precipitation measured by tipping-bucket; air temperature via integrated transmitter.

- Data processing, quality control, and interpretation
  - Eddy covariance data quality control
    - Exclude data when u* < 0.2 m s-1; remove implausible CO2 values (330–450 ppm) and flux ranges (-50 to 50 µmol m-2 s-1); restrict LE/H to plausible ranges (-250 to 800 W m-2).
    - Gap-filling of NEE using established online tools; partitioning into GPP and TER with temperature-based parameterisation.
  - Gas flux specifics
    - N2O and CH4 fluxes derived from chamber measurements with detection limits (N2O ~11 ng N m-2 s-1; CH4 ~17 ng CH4-C m-2 s-1) and weekly to during fertilisation periods sampling.
  - Soil and deposition data
    - Total soil C and N treated as soil organic carbon only (no inorganic carbon); multi-depth sampling; standard dry combustion analyses.
  - Data presentation
    - Daily and monthly time series with explicit date formats; units provided per variable (e.g., g C m-2 d-1 for fluxes; mg/L for concentrations).
  - Metadata and data governance
    - Data described with explicit methods, sensors, depths, sampling intervals, and data gaps; references provided for methods and prior related work.
    - Emphasis on data openness, traceability to originators, and detailed metadata to support reuse and policy-relevant interpretation.

- Temporal and spatial coverage
  - Timeframe
    - Measurements and sampling conducted from January 2002 through at least 2010–2011 (with various subsets in different datasets).
  - Scope
    - Focused on the South field of a two-field setup; site-wide context documented (soil type, rooting depth, groundwater depth, and climate).

- Relevance for monitoring frameworks
  - Provides a comprehensive, multi-domain dataset (climate, soil, management, and greenhouse gas fluxes) suitable for evaluating environmental health policies, monitoring approaches, and policy-informed decision-making.
  - Demonstrates integration of data types, metadata completeness, data quality controls, and governance practices necessary to support transparency, replication, and open data sharing.
  - Highlights common data challenges (gaps, silos, metadata gaps, and data transformation needs) and how they were addressed through standardized measurements, cross-field data linkage, and explicit documentation.