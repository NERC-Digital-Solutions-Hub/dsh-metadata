# Field sites and microclimate measurements

- Overview
  - Field component of a project conducted in six forest reserve stands in the Northern Boreal zone of Sweden.
  - Sites span a range of ages since last wildfire (approx. 47 to 367 years) with similar soil types and vegetation: Scots pine, Norway spruce, dwarf shrubs, and feather moss ground cover.
  - Microclimate and greenhouse gas (GHG) data were collected between June 2012 and July 2014.

- Study sites and environmental context
  - Six sites with codes: NJA (Njållatjivelg), JAR (Jarvliden), LAD (Laddok), GUO (Guorbåive), FET (Fettjärn), REV (Reivo).
  - Precise geographic coordinates provided for each site.
  - Time since last fire (years) ranged from 47 to 367.

- Data collected and sensors
  - Weather stations (where installed) measured air temperature; soil temperature at 1 cm and 5 cm depth; soil moisture; surface leaf moisture.
  - Instrument platform: Decagon Devices devices.
  - GUO site lacked a weather station, which affected some analyses.

- Plant and soil sampling
  - Post-GHG sampling: destructive harvest of all plant material within gas chamber collars; biomass dried and weighed.
  - Soil cores: one 5 cm diameter, 10 cm depth per collar; used to assess horizon depths, bulk densities, and total soil C:N.
  - Vegetation cover estimates by species and by plant functional type (PFT: shrub, graminoid, bryophyte); some plots exceeded 100% cover due to overlay.

- Soil and microbial analyses
  - June 2012: six soil cores along transects for inorganic nitrogen (NO3−, NH4+).
  - September 2013: four additional cores for pH, total phosphorus, loss on ignition (organic matter), and microbial PLFA content in the soil organic horizon.
  - Microbial biomass and fungal/bacterial ratios via a modified Bligh and Dyer lipid extraction; PLFAs identified and quantified (nmol PLFA g dry weight−1). Bacterial PLFAs highlighted by specific branched/cyclopropyl fatty acids; fungal PLFAs identified by 18:2ω6,9.

- Gas flux measurements (forest floor GHG fluxes)
  - Five permanent PVC collars (30 cm diameter, 10 cm height) per site along transects on a moss mat.
  - Collected data: June 2012 (initial), Sep 2012, Jun 2013, and Jul 2014 (subsequent campaigns).
  - Measurements: ecosystem respiration (ER) and net ecosystem exchange (NEE) over 2-minute intervals with an infrared gas analyser (PP Systems EGM4) using opaque/clear chamber lids.
  - NEE interpretation: negative means net CO2 sequestration (GPP > ER); positive means net CO2 release.
  - CH4 and N2O measured with a closed static chamber approach; 10 mL headspace samples taken every 10 minutes over 30 minutes; analyzed by GC with detectors for CH4 and N2O.
  - Data processing: convert gas concentrations to fluxes in mg CH4-C and mg N2O-N m−2 h−1; quality control to identify missing data and atmospheric contamination; drift corrections applied.

- Data processing and quality control
  - GC-based gas data corrected for instrumental drift; standard curves generated from calibrated gas standards.
  - Data transformation to flux units (mg CH4-C and mg N2O-N m−2 h−1) for analyses.
  - Quality assurance steps designed to flag gaps and contamination.

- Statistical analysis and modeling approaches
  - Objective: assess relationships among time since fire, site properties, and GHG fluxes; compare sites; identify predictors of forest floor GHG emissions.
  - Software: analyses conducted in R.
  - Methods:
    - Linear regression to explore trends in site properties and GHG fluxes with time since fire; combined data from collar cores and transects.
    - ANOVA to test discrete site differences (e.g., vegetation cover); Tukey's HSD for post-hoc comparisons.
    - Data transformations applied as needed to meet ANOVA assumptions; non-parametric Kruskal-Wallis with Dunn’s test when appropriate.
    - Linear mixed-effects models (LMEs) to identify controls on forest floor GHG fluxes.
      - Time since wildfire removed as a predictor due to lack of significant relationships; site treated as a fixed effect.
      - Collinearity checks to remove highly correlated variables (retain one of each pair with >70% correlation).
      - Random effects included to account for repeated sampling per plot and heterogeneity across sites.
      - Model selection via stepwise deletion using chi-squared likelihood ratio (LR) tests; interactions evaluated and simplified if terms non-significant.
    - Two modeling approaches due to missing weather data at GUO:
      - All Sites model (including all data, with weather data accommodated where available).
      - Including WS Data model (excluding GUO data due to lack of weather station); after removing collinear weather variables, hourly averages used: AirTemp1 (mean air temperature), mean soil moisture, and mean surface leaf moisture.
  - Plant coverage and functional groups considered in models; species with less than 5% cover in a plot excluded; correlated species removed from selection (e.g., P. schreberi and Vaccinium-related variables treated with their PFTs).

- Data management and governance considerations for data leaders
  - The study integrates multi-temporal, multi-site ecological data (microclimate, vegetation, soil properties, PLFA, and GHG fluxes) to support integrated analyses.
  - Explicit handling of missing data (GUO weather station absence) through alternative modeling strategies.
  - Clear documentation of sampling design, measurement protocols, and analytic workflows to enable reproducibility and cross-site comparability.
  - Use of standardized units, calibration and quality control steps, and transparent model selection criteria to support data reliability and discoverability.