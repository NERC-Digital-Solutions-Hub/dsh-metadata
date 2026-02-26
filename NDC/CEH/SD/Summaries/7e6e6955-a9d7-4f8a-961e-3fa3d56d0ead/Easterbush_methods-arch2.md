# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

- Overview of the study site and management
  - Experimental site: Easter Bush, South East Scotland (near Edinburgh), two adjacent fields (South and North); South field data used here.
  - Mean climate (2002-2010): rainfall ~947 ± 234 mm/year; mean temperature ~9.0 ± 0.4 °C.
  - Land use: permanent grassland (>20 years) dominated by Lolium perenne (>99%), with <0.5% Trifolium repens; imperfectly drained Macmerry soil (Eutric Cambisol), pH 5.1, clay 20–26%.
  - Measurements collected between January 2002 and May 2011; main measurement equipment located between fields.
  - Groundwater and rooting zone characteristics described (water table depth ~0.85 m; rooting to ~0.31 m).

- Sampling regime and field management
  - Monitoring period: 2002–2011 (various data streams overlapped; some datasets extend beyond).
  - Management regime: continuous grazing (ewes, lambs; occasional heifers in calf); silage cuts on 1 June 2002, 8 August 2002, and 29 May 2003; ammonium nitrate or urea fertiliser 3–4 times/year (avg 56 kg N ha−1 per application); in 2008 an extra mineral N application with urea; cattle slurry applied in Sep 2004 and Mar 2005.
  - Yield and inputs: stocking densities and animal numbers tracked; plant tissue sampled for N and C analyses; slurry N and C quantified by application volume and slurry composition.

- Data streams and file coverage
  - livestock_yield_fertiliser_daily.csv (2002–2010): stock numbers, stocking density (LSU and head per field), yield offtake (DM, N, C), mineral and organic N fertiliser inputs, organic C fertiliser inputs.
  - N_C_leaching_flux_daily.csv and N_C_leaching_conc_sampling_period.csv (2006–2008): suction cup-based leaching measurements; DIC/DOC/DON/TN, NH4, NO3 fluxes and concentrations; modelled groundwater recharge and evapotranspiration.
  - Dry_N_conc_monthly.csv: monthly concentrations of atmospheric deposited N species (NH3, HNO3, NH4+, NO3−) using DELTA system at a nearby field.
  - Flux_daily.csv (2002–2010): fluxes of CO2 (NEE, GPP, TER, NPP), CH4, N2O (from chambers and EC), NOx.
  - metdata_daily.csv (2002–2010): meteorological variables and soil moisture at multiple depths, precipitation, and air temperature.
  - soil_C_N_oneoff.csv (2004 and 2011): soil total N and C by depth (0–60 cm) from a 10 m grid, with separate analyses for root- and stone-free fractions.
  - Additional referenced data fields in the Daily Flux file include metadata for quality checks and units.

- Measurement techniques and data processing
  - CO2 and energy fluxes: eddy covariance system; 2.5 m wind height; LI-COR 7000 CO2/H2O analyzer; data quality controlled (filters for turbulence, plausible CO2, and flux ranges).
  - Gap-filling and partitioning: NEE gap-filling using online tool (Reichstein et al., 2005); NEE partitioned into GPP and TER using the same tool; daytime TER extrapolated from night-time temperature parameterisations; NPP assumed as 50% of GPP (per Amthor 2000; Zhang et al. 2009).
  - N2O and CH4: measured with closed static chambers (2006–2009) and EC data (2002–2003); GC-based analysis; detection limits specified.
  - NOx: measured with an autochamber system (June 2009–Aug 2010); measurements four times daily; data corrected for chamber/ozone influences.
  - Dry deposition: nearby DELTA-based measurements for atmospheric N deposition (NH3, HNO3, NH4+, NO3−) used to contextualize inputs.
  - Leaching and soil C/N: soil cores collected in May 2004 and May 2011; soils dried and analyzed for total N and C; C and N leaching quantified via pore water suction cup data and a soil water balance model (for leachate volumes).

- Data content and units (selected highlights)
  - Metdata_daily.csv: daily precipitation (mm d−1), temperature (°C; daily avg/min/max), soil temperature, volumetric water content (% daily avg).
  - Flux_daily.csv: GPP (g C m−2 d−1), NPP (g C m−2 d−1), EcoResp (g C m−2 d−1), NEE (g C m−2 d−1), CH4 (g C-CH4 m−2 d−1), N2O (g N-N2O m−2 d−1) via chambers and EC, NOx fluxes (g N-NO m−2 d−1).
  - N_C_leaching_flux_daily.csv: DIC and DOC leaching flux (g C m−2 d−1), DON and NH4NO3 leaching flux (g N m−2 d−1), NO3 leaching flux (g N m−2 d−1), modelled groundwater recharge (mm d−1), precipitation and ET.
  - N_C_leaching_conc_sampling_period.csv: DIC, DOC (mg C L−1); TN, NH4, NO3 concentrations (mmol N L−1).
  - Dry_N_conc_monthly.csv: DELTA-based concentrations of NH3, HNO3, NH4+, NO3− (ug m−3).
  - soil_C_N_oneoff.csv: soil mass, SOC (kg C m−2), SON (kg N m−2) by depth.
  - NEE-derived products and QC: included as part of Flux_daily with flags and plausible value ranges.

- Quality, scope, and accessibility
  - Data quality controls applied to flux measurements; gap-filled NEE and partitioned GPP/TER estimates described.
  - Documentation emphasizes storage and uploading of created datasets to appropriate portals; datasets are designed for long-term environmental monitoring and cross-data integration.
  - The dataset supports analysis of carbon and nitrogen fluxes in a grazed, cut, and fertilised temperate grassland, including grazing and management effects on GHG budgets.

- References and methodological grounding
  - Methods and analytical approaches anchored to established studies and tools (e.g., Reichstein et al. 2005 for gap-filling; Amthor 2000 and Zhang et al. 2009 for NPP/GPP relationships; multiple references for flux measurement techniques and chemical analyses).

- Potential uses for environmental monitoring and policy analysis
  - Long-term carbon, nitrogen, and greenhouse gas budgeting for grazed grasslands.
  - Evaluation of management impacts (grazing intensity, cutting frequency, fertiliser and slurry applications) on GHG fluxes and soil C/N pools.
  - Integration with meteorological data to assess climate-driver relationships on ecosystem processes.
  - Data accessibility and standardization enable cross-site comparisons and portfolio-wide monitoring of environmental health and policy performance.