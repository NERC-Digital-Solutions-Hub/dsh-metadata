# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

## Purpose and GIS relevance
- Provides a multi-faceted dataset for mapping and exploring spatially explicit emissions and crop performance under different irrigation and fertilization regimes.
- Suitable for creating map-based visualizations of GHG fluxes (NH3, CH4, N2O), soil properties, meteorology, and yield/NUE across plots.
- Supports data integration and comparison across variables such as irrigation regime, fertilizer type, and temporal sampling.

## Spatial and temporal coverage
- Location: Indian Agricultural Research Institute (IARI), New Delhi, India; site name IARI_ND.
- Coordinates: 28°40' N, 77°12' E; Altitude: 228 m.
- Soil: silty clay loam (Typic Ustochrept).
- Timeframe: 2016 kharif season (transplanting July 2016, harvest October 2016).
- Plot size: 6 m x 7 m; two irrigation regimes (continuous flooding CF, intermittent flooding IF) in a split-plot design with five fertilizer treatments, each with three replicates.

## Datasets and contents (files)
- irrigation.csv: measurements of water depth over time for CF and IF plots (dates; continuous vs intermittent water table heights).
- weather.csv: daily meteorological data from a nearby station (date; min/max temperature; rainfall; mean temperature; relative humidity; sunshine; evapotranspiration; wind).
- site_properties.csv: plot-level soil and management properties (irrigation type, fertilizer treatment, replicate; soil pH, total N and C, bulk density; texture components; sampling dates).
- NH3.csv: ammonia flux measurements (date; irrigation; treatment; replicate; NH3 flux in g NH3-N ha-1 d-1); values below 1 g NH3-N ha-1 d-1 treated as zero.
- N2O_CH4.csv: nitrous oxide and methane flux measurements (date; irrigation; treatment; replicate; N2O flux g N2O-N ha-1 d-1; CH4 flux g CH4-C ha-1 d-1).
- soil_NO3_NH4.csv: soil nitrate and ammonium concentrations (date; irrigation; treatment; replicate; NO3-N and NH4-N in mg N kg-1).
- crop_biomass_N.csv: biomass data (grain and straw) with corresponding nitrogen content (grain_biomass_dryweight; grain_N_conc; straw_biomass_dryweight; straw_N_conc) reported per date, irrigation regime, treatment, and replicate.
- Table references within descriptions indicate fertiliser types, N inputs, and timing of applications.

## Experimental design and management
- Flooding regimens: CF vs IF to compare emissions and nitrogen use efficiency (NUE) under contrasting water regimes.
- Fertiliser treatments (five total): CON (no N), FYM (50% N via farmyard manure and 50% via neem coated urea), LCC (Leaf Colour Chart-based NCU application), NCU (100% N via neem-coated urea), PRI (100% N via prilled urea). All treatments receive basal P, K, and Zn.
- Nitrogen input: 120 kg N ha-1 for all fertiliser-containing treatments.
- Crop: rice variety Pusa 44; transplanted 12-13 July 2016; plot-level management mirrors local regional practice.
- Measurements include gas fluxes (NH3, CH4, N2O), plant biomass and nitrogen content, soil nitrogen content, and basic soil properties.

## Data collection methods and units
- Gas fluxes: static chamber method; CH4 measured with GC-FID and N2O with GC-ECD; flux calculations use chamber volume, ground area, and concentration change over time.
- Ammonia volatilisation: measured with a separate static chamber; NH3-N quantified by titration after absorbing NH3 in boric acid; fluxes discounted below 1 g NH3-N ha-1 d-1.
- Plant and soil analyses: biomass and nitrogen content via standard Kjeldahl methods; NUE calculated relative to control within each irrigation method.
- Sampling cadence: gas and soil samples collected on specified dates; weather data and irrigation depths recorded continuously across the season.

## Data quality and considerations for GIS use
- Some site property measurements (texture) have NA values for most replicates (texture data not complete across replicates).
- Data include replicate-level observations, enabling spatial variance analysis across the 6x7 m plots.
- Measurements are localized to a single experimental site (IARI, Delhi) with a nearby meteorological station for weather data; spatial generalization beyond this site should be approached cautiously.
- Clear documentation of measurement methods, calibration standards, and data processing (e.g., NH3 flux threshold) supports reproducibility and data integration.

## Potential GIS applications and analyses
- Create layer maps of NH3, CH4, and N2O fluxes by irrigation regime and fertilizer treatment, with temporal slices.
- Overlay gas flux data with soil properties (pH, organic carbon, total N), texture, and bulk density to assess spatial drivers of emissions.
- Link flux data to crop biomass and NUE to explore spatial-temporal relationships between management, yield, and emissions.
- Integrate weather and irrigation data to model flux responses to environmental conditions.
- Use proximity to the sampling layout (plots, replicates) for spatial pattern analyses and uncertainty mapping.

## References and provenance
- Cowan et al. (2021): main study comparing CF and IF impacts on CH4, N2O, and NH3 emissions, NUE, and yield.
- Methodological references for gas flux and soil analyses provided in the document (e.g., Bremner 1965; Pathak et al. 2002–2003; Bhatia et al. 2005, 2016; Page et al. 1982).