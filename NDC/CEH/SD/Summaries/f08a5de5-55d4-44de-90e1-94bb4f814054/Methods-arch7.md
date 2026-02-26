# Field sites and microclimate measurements

- Purpose: Document six forest reserve stands in Northern Boreal Sweden used to study field sites, microclimate, soil, plant data, and forest-floor greenhouse gas fluxes, with data to support map-based visualization and spatial analyses.

- Study site details:
  - Six sites with varying time since last wildfire (2014): NJA (47 years), JAR (53), LAD (136), GUO (183), FET (232), REV (367).
  - Locations share similar soil type and vegetation: Scots pine, Norway spruce, ground vascular plants (Vaccinium spp., Empetrum spp., Calluna spp.) and feather mosses (P. schreberi, H. splendens).
  - Some sites included weather stations measuring air and soil temperatures and related variables; GUO lacked a weather station.

- Temporal scope:
  - Microclimate and related field measurements collected between June 2012 and July 2014.

- Field measurements and sampling (plant, soil, and atmosphere):
  - Weather and microclimate: air temperature, soil temperature at 1 cm and 5 cm, soil moisture, surface leaf moisture.
  - Gas sampling plots: five permanent collars per site (30 cm diameter, 10 cm height) for greenhouse gas flux measurements; measurements taken in June 2012 and September 2012, June 2013, and July 2014.
  - Gas flux parameters: ecosystem respiration (ER), net ecosystem exchange (NEE), and, using opaque/clear chambers with PAR data, estimates of gross primary productivity (GPP). CH4 and N2O fluxes measured via closed static chamber method with headspace sampling and GC analysis.
  - Plant and soil data: destructively harvested plant material within gas collars; dry biomass measured; one soil core (5 cm diameter, 10 cm depth) for horizon depth, bulk density, and soil C:N; plant cover estimated by species and aggregated into plant functional types (PFTs: shrubs, graminoids, bryophytes).
  - Additional transect samples (June 2012 and Sept 2013): soil cores for inorganic nitrogen (NO3-, NH4+), pH, total phosphorus, loss on ignition (organic matter), microbial PLFA content.
  - Microbial analyses: PLFA extraction and analysis to determine microbial biomass and bacterial vs fungal ratios; identification of PLFAs by GC and calculation of nmol PLFA g dw-1; specific marker PLFAs for bacteria and fungi used to estimate community composition.

- Laboratory methods (PLFA and chemistry):
  - Lipid extraction using Bligh and Dyer method; phospholipids analyzed and methylated for GC analysis.
  - PLFA peaks identified via retention times and internal standards; conversion to nmol PLFA g dw-1.
  - Bacterial vs fungal PLFAs distinguished by characteristic fatty acids; total PLFAs calculated from identified peaks.

- Data processing and quality control:
  - Gas concentrations converted to fluxes (mg CH4-C or mg N2O-N m-2 h-1) using standard curves; corrections for instrumental drift.
  - QC procedures implemented to identify missing data or atmospheric contamination.

- Statistical analyses and modeling:
  - Objectives: assess how time since fire, site properties, and vegetation influence GHG fluxes; evaluate inter-site differences; identify predictors of forest-floor GHG emissions.
  - Software: R.
  - Methods:
    - Linear regressions to evaluate trends in soil properties and GHG fluxes with time since fire (using data from within collars and transects).
    - ANOVA to test discrete inter-site differences (with Tukey’s HSD for post-hoc comparisons); data transformed as needed or non-parametric tests used (Kruskal-Wallis with Dunn’s test).
    - Linear mixed-effects (LME) models to identify controls on forest-floor GHG fluxes:
      - Time since wildfire often replaced by site as a discrete factor after finding no significant continuous relationship.
      - Collinearity checks (>70% correlation) to drop one of collinear pairs.
      - Random effects included for repeated measurements and unequal variances across sites.
      - Fixed effects selected via single-term deletions and likelihood ratio tests; interactions simplified when principal terms were non-significant.
  - Special case: GUO site without a weather station led to two model sets:
    - All sites model including weather data (excluding GUO data where weather variables could not be used).
    - Model excluding GUO with weather data to maximize use of available data.
  - Fixed factors (as in Table 2) included a broad set of soil properties, moisture variables, depth to organic horizon, C:N, bulk density, plant biomass, moss/lichen cover, shrub/grass indicators, and cover percentages for key plant taxa and PFTs (with exclusions for collinear or highly correlated species).

- Data considerations for GIS applications:
  - Spatially explicit site coordinates and time-since-fire metadata enable mapping of site age, soil/vegetation properties, and GHG flux patterns.
  - Multiple, nested sampling design (collars, transects) provides spatially distributed data suitable for geospatial aggregation and scale-aware analyses.
  - Missing data at GUO due to lack of weather station is a notable data gap for spatial models incorporating weather variables.