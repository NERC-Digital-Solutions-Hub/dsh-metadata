# Field sites and microclimate measurements

- Study location and design
  - Six forest reserve stands in the Northern Boreal zone of Sweden, varying in time since last wildfire (47–367 years as of 2014).
  - Sites chosen with similar soil type and vegetation: Scots pine, Norway spruce, and ground vegetation dominated by dwarf shrubs and feather mosses.
  - Coordinates and time-since-fire data provided for each site (NJA, JAR, LAD, GUO, FET, REV).

- Microclimate measurements
  - Weather stations installed at all sites except GUO, recording air temperature, soil temperature at 1 cm and 5 cm, soil moisture, and surface leaf moisture.
  - Data collection period for microclimate data: June 2012 to July 2014.

- Field data collection and plant/soil sampling
  - Gas sampling plots: gas-chamber collars installed at each site to host habitat for measurements.
  - Destructive harvest of plant material within gas chamber collars for dry biomass.
  - Soil core (5 cm diameter, 10 cm depth) taken from collar centers for horizon depth, bulk density, and total soil C:N.
  - Vegetation cover estimated per species and grouped into plant functional types (PFTs: shrubs, graminoids, bryophytes); total cover summed per type.
  - June 2012: six soil cores along transects for inorganic nitrogen (NO3-, NH4+).
  - September 2013: four additional cores for soil properties including pH, total phosphorus, loss on ignition (organic matter), and microbial PLFA content in the soil organic horizon.

- Microbial and PLFA analyses
  - Microbial biomass and fungal/bacterial ratios derived from a modified Bligh and Dyer lipid extraction, followed by PLFA analysis.
  - Phospholipid fatty acids (PLFAs) identified for bacterial (e.g., 15:0i, 15:0a, 16:0i, etc.) and fungal groups (18:2ω6,9).
  - Total PLFA concentration calculated from identified peaks and converted to nmol PLFA g dw^-1.

- Greenhouse gas (GHG) flux measurements on the forest floor
  - Five permanent PVC collars per site along a transect (10–20 m apart), placed on a moss mat (P. schreberi).
  - Collars left in place for two days before initial measurements; sampling occurred: June 2012 (first set) and September 2012, June 2013, and July 2014 (subsequent campaigns).
  - GHG fluxes measured as:
    - Ecosystem respiration (ER) and net ecosystem exchange (NEE) using an infrared gas analyzer with opaque or clear chambers; PAR measured with a light sensor for NEE.
    - NEE interpreted as negative when photosynthesis GPP > ER; positive when ER > GPP.
    - Methane (CH4) and nitrous oxide (N2O) measured with a closed static chamber approach; headspace samples taken every 10 minutes for 30 minutes and analyzed by gas chromatography.
  - Concentrations converted from ppm to fluxes in mg CH4-C or mg N2O-N per m^2 per hour; quality control implemented to identify data gaps or atmospheric contamination.

- Data processing and quality control
  - Gas concentration data corrected for instrumental drift as needed.
  - Standardized conversion of gas concentration to flux, with procedures aligned to Ward et al. (2013).
  - Ensured data integrity across multiple campaigns and sites, including handling of missing values.

- Statistical analysis and modelling approach
  - Objectives:
    - a) Determine relationships between time since fire, site properties, and GHG fluxes.
    - b) Assess inter-site differences in properties and GHG fluxes.
    - c) Identify ecosystem properties that predict forest floor GHG emissions.
  - Software and methods:
    - Analyses conducted in R; linear regressions for trends with time since fire.
    - ANOVA to test discrete site differences; Tukey’s HSD for post-hoc when significant.
    - Data transformations applied as needed; non-parametric Kruskal-Wallis with Dunn’s test when assumptions violated.
  - Linear mixed effects (LME) modelling
    - Time since wildfire (continuous) initially not significantly related to soil properties or GHG emissions, so replaced by site (discrete) in models.
    - Collinearity check: removed one of highly correlated variable pairs (>70% correlation).
    - Random effects included to account for repeated sampling per plot and unequal site variances.
    - Fixed effects selected via single-term deletion and likelihood ratio (LR) tests; non-significant terms removed.
    - Interaction terms interpreted; if significant interactions contained single terms, the interaction was retained but components removed as needed for LR testing.
  - Modelling with and without the GUO site
    - GUO lacked a weather station, so two modelling datasets were created:
      - All Sites (including weather data, with GUO data used where possible).
      - Including WS Data but without GUO data (to maximize comparability across weather-station sites).
    - Weather variables considered after removing collinear terms:
      - AirTemp1 (hourly-averaged air temperature before sampling), mean soil moisture, mean surface leaf moisture.
    - Additional covariates in the models included cover by key species and plant functional types, with adjustments for collinearity (e.g., removal of certain moss/shrub indicators tied to total moss/shrub cover).
  - Model specifics
    - Dataset variants labeled as All Sites (with GUO) and Including WS Data (GUO excluded).
    - DepthOH refers to soil organic horizon depth; BDOH to bulk density of organic horizon; C:NOH to carbon:nitrogen ratio of the organic horizon.
  - Documentation and replication
    - Factors included in initial models summarized (see Table 2 for fixed factors).
    - OH = soil organic horizon; "AirTemp1" denotes hourly-averaged air temperature used in certain model sets.

- Practical implications for environmental monitoring
  - Demonstrates integration of multi-mocha data (microclimate, soil chemistry, microbial community structure, and GHG fluxes) across multiple sites and years.
  - Highlights data-handling considerations when stations are missing (e.g., GUO) and how to construct alternative modelling frameworks to maximize available data.
  - Illustrates standardised sampling and analysis pipelines suitable for long-term environmental monitoring and policy-performance assessment.