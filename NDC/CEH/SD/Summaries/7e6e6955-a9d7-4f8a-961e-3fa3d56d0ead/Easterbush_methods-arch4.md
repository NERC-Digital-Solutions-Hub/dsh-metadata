# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

- Overview
  - A comprehensive data set from the Easter Bush field site in South East Scotland (near Edinburgh), focusing on grazed, cut, and fertilised temperate grassland.
  - Timeframe: measurements span January 2002 to May 2011 for most data; specific components have shorter windows (e.g., 2002–2003 N2O fluxes, 2006–2008 N and C leaching concentrations).
  - Location and site context: two adjacent fields (South and North); primary measurements between fields; soil type and management history described (permanent grassland with Lolium perenne, pH ~5.1, 20–26% clay; groundwater table ~0.85 m; rooting depth to ~0.31 m).

- Data collection framework and scope
  - Atmosphere–soil exchange and ecosystem fluxes
    - Net ecosystem exchange (NEE), gross primary production (GPP), and ecosystem respiration (EcoResp) via eddy covariance.
    - CO2 exchange parameters include NEE, GPP, TER; data quality controls applied (e.g., u* threshold, plausible CO2 flux ranges, LE/H flux bounds); gap-filling and partitioning performed using standard online tools.
    - Methane (CH4) and nitrous oxide (N2O) fluxes measured; CH4 via GC with flame detector; N2O via GC with ECD (EC and chamber methods used at different periods).
    - Nitrogen oxides (NOx) fluxes measured with autochamber system (2009–2010) to capture soil NOx fluxes.
    - NOx, N2O, CH4, and CO2 flux datasets include both chamber-based and eddy covariance-based measurements where applicable.
  - Meteorology and soil state
    - Meteorological and soil variables collected continuously: precipitation, air temperature, soil temperature (multiple depths), soil volumetric water content, and a tipping-bucket rain gauge.
    - Dry deposition measurements for atmospheric N species collected from a nearby Delta system field (NH3, HNO3, NH4+, NO3- concentrations).
  - Management and inputs
    - Livestock grazing (stocking density, animal numbers) and silage cuts (dates) with associated dry matter, nitrogen, and carbon removals.
    - Fertiliser inputs (ammonium nitrate and urea) and organic manure applications (slurry) with detailed application dates and representative nutrient content.
  - Soil properties and leaching
    - Leaching measurements: soil water leachates (DIC, DOC) and dissolved inorganic/organic N (DIN, DON) using suction cups at two locations (slope and hollow; only slope data retained due to water logging in hollow).
    - Leaching fluxes and concentrations derived from measured leachate concentrations, soil water model outputs, daily precipitation, and evapotranspiration estimates.
    - One-off soil sampling for total soil N and C at two time points (May 2004 and May 2011) across multiple soil depths (0–60 cm).
  - Data products and formats
    - Daily, monthly, and one-off data files with clearly defined variable lists and units.
    - File metadata included (dates, units, variable names) and blank values indicate missing measurements.
    - Key data files:
      - metdata_daily.csv: daily weather and soil moisture/temperature variables.
      - Flux_daily.csv: ecosystem gas fluxes (GPP, NPP, EcoResp, NEE; CH4, N2O; NOx; NOx; NOx; CO2 flux decomposition and NPP assumptions).
      - Livestock_yield_fertiliser_daily.csv: stocking densities, animal numbers, YIELD DM, N and C offtake, and fertiliser inputs.
      - N_C_leaching_flux_daily.csv: leaching fluxes for DIC, DOC, DON, NH4, NO3, plus modelled groundwater recharge and hydrological terms.
      - N_C_leaching_conc_sampling_period.csv: concentrations of DIC, DOC, TN, NH4, and NO3 in leachates.
      - Dry_N_conc_monthly.csv: monthly concentrations of atmospheric N species (NH3, HNO3, NH4+, NO3-).
      - Soil_C_N_oneoff.csv: soil mass, SOC, SON by depth (0–60 cm) from May 2004 and May 2011.
      - Metadata and references sections summarise methods and sources.

- Temporal coverage and spatial setup
  - South field data (the dataset includes measurements primarily from the South field; a map and figure indicate equipment locations and wind directions).
  - Measurements span 2002–2011 for most datasets; specific components have narrower ranges (e.g., N leaching data 2006–2008; NOx 2009–2010; EC-based N2O 2002–2003 and 2006–2009).

- Data quality, processing, and standards
  - Quality control and data processing
    - Eddy covariance NEE data curated with standard QC filters: minimum friction velocity, CO2 plausible range, latent/sensible heat flux bounds.
    - Gap-filling and flux partitioning conducted with established online tools (Reichstein et al., 2005).
    - NPP set as 50% of GPP based on Amthor (2000) and Zhang et al. (2009) assumptions.
    - Linear and measurement checks performed for N2O/CH4 flux measurements (detection limits and linearity assessments described; weekly or more frequent sampling during fertilisation events).
  - Data provenance and references
    - Methods and instruments cited in detail (EC, TDLS, GC with ECD, autochamber NOx system, Delta dry deposition, diffusion denuder technique for atmospheric deposition).
    - Comprehensive references provided for measurement approaches and data interpretation (e.g., Di Marco et al., Reichstein et al., Butterbach-Bahl et al., Helfter et al., etc.).
  - Metadata and discoverability
    - Each file includes explicit variable definitions and units; a dedicated “Nature and units of recorded values” section standardises naming and units across data products.
    - Blank values indicate days with no data, aiding data discovery and gap identification.

- Data governance, accessibility, and reuse
  - The dataset supports examination of the nitrogen, carbon, and greenhouse gas budget of a temperate grazed grassland, with potential cross-site comparisons and model validation.
  - Structured in a way that supports integration into broader data platforms or networks, given the explicit metadata, file-level documentation, and standard scientific references.
  - Potential data needs for data leaders: clear provenance, consistent units, documentation of data gaps, and alignment with data standards for ecosystem flux and soil chemistry data.

- Practical implications for data strategy and use
  - Strengths for data leadership
    - End-to-end data capture across multiple coupled processes (climate, soil, plant, microbial/trace gas fluxes) enabling system-level analyses.
    - Explicit QA/QC criteria and gap-filling methodology support reproducibility and reliability assessments.
    - Detailed management and input data enable scenario analysis of land-use practices and their impact on GHG budgets.
  - Considerations and challenges
    - Data are spread across multiple files with varying temporal resolutions; integration requires careful harmonization of time stamps and units.
    - Some components (e.g., NOx, certain leaching measurements) have limited time windows, potentially limiting long-term trend analyses.
    - Data gaps and missing values are indicated, requiring explicit handling in analyses and models.

- Key takeaways
  - The dataset provides a robust, multi-faceted view of carbon and nitrogen fluxes, meteorology, management inputs, and soil properties from a temperate grazed grassland site, with thorough documentation, QA, and references to established methodology.
  - It is well-suited for researchers and data leaders seeking to understand or model whole-system data flows, data quality practices, and data integration in agroecosystem contexts.