# Field sites and microclimate measurements

- Purpose: Describe the field-site setup, measurements, and analyses used to study forest floor greenhouse gas fluxes and associated soil/vegetation properties across boreal forest stands with different times since last wildfire.
- Scope: Six forest reserve stands in Northern Sweden (Northern Boreal zone) with similar soil and vegetation, varying ages since last fire; microclimate and biogeochemical measurements collected from 2012–2014.

## Site characteristics and design

- Six site descriptions (time since last fire in 2014): NJA (47 years), JAR (53), LAD (136), GUO (183), FET (232), REV (367).
- Vegetation/soils: Scots pine, Norway spruce, and ground vegetation including dwarf shrubs and feather mosses; soil type and plant community chosen to be comparable across sites.
- Weather/microclimate monitoring: Weather stations installed at all sites measuring air temperature, soil temperature at 1 cm and 5 cm, soil moisture, and surface leaf moisture; GUO lacked a weather station.
- Temporal scope: Microclimate data collected over June 2012 to July 2014.

## Plant and soil sampling and analyses

- Biomass and vegetation: After the final gas sampling, gas plots were destructively harvested; plant material within gas collars dried at 60ºC and weighed for total biomass; cover estimates for individual species and aggregated into plant functional types (PFTs) such as shrubs, graminoids, and bryophytes.
- Soil sampling: 
  - June 2012: Six soil cores along transects for inorganic nitrogen (NO3-, NH4+).
  - September 2013: Four additional cores for soil properties including pH, total phosphorus, loss on ignition (organic matter), and microbial PLFA content in the soil organic horizon.
- Microbial analyses: 
  - PLFAs extracted via a modified Bligh and Dyer method; analyzed as fatty acid methyl esters (FAMEs) via GC.
  - Bacterial PLFAs identified by specific fatty acids; fungal PLFAs identified by 18:2ω6,9.
  - Total PLFA concentration calculated from identified peaks; results expressed as nmol PLFA g dry weight^-1.
- Data handling: Methods followed established protocols (referenced in the text) for lipid extraction, profiling, and identification.

## Forest floor greenhouse gas flux measurements

- Field apparatus: Five permanent PVC collars per site (30 cm diameter, 10 cm height) on a moss mat; collars installed along a transect and left for two days prior to measurements.
- Sampling schedule: June 2012 (initial), Sept 2012, June 2013, and July 2014 (two measurements per campaign).
- GHG flux measurements:
  - CO2 fluxes: Net ecosystem exchange (NEE) and ecosystem respiration (ER) measured with a portable IR gas analyzer; photosynthetically active radiation (PAR) recorded to partition GPP and ER.
  - CH4 and N2O fluxes measured with a closed static chamber (10 mL headspace samples collected every 10 minutes for 30 minutes; analyzed by GC).
  - Chamber types: Opaque and clear lids used for ER and NEE respectively.
- Data processing: Gas concentrations converted to fluxes (mg CH4-C or mg N2O-N m^-2 h^-1); quality control to identify missing values and atmospheric contamination; adjustments for instrument drift as needed.

## Laboratory analyses and quality assurance

- Gas methodology references: Ward et al. (2013) for sampling protocols and accuracy considerations.
- QC emphasis: Ongoing data quality checks to ensure reliable flux measurements across campaigns and sites.

## Statistical analysis framework

- Core aims:
  - Assess relationships among time since wildfire, site properties, and GHG fluxes.
  - Evaluate inter-site differences in properties and fluxes.
  - Identify key ecosystem properties predicting forest floor GHG emissions.
- Software and methods: Analyses performed in R.
- Approaches:
  - Linear regression to explore trends in site properties and GHG fluxes with time since fire.
  - ANOVA to test discrete site differences; Tukey’s HSD for post-hoc comparisons.
  - Data transformations or non-parametric tests (Kruskal-Wallis with Dunn’s test) to meet assumptions.
  - Linear mixed effects (LME) models to account for repeated sampling and unequal variances:
    - Initial treatment: time since wildfire (continuous) removed when not significant, replaced by site (discrete).
    - Collinearity check with correlation matrix; removal of one of highly collinear pairs (>70% correlation).
    - Random effects included for plot-level repetition and site-level variance.
    - Fixed effects selected via stepwise deletions and likelihood ratio (LR) tests; non-significant terms removed.
    - Interactions retained only if supported; if significant, related terms adjusted accordingly per LR outcomes.
- GUO-specific modeling: Because GUO lacked a weather station, two model variants were created to maximize data usage:
  - All sites model (including weather data).
  - Model excluding GUO data (Using weather-station data only).
- Predictor set and data handling:
  - For plant cover, only species with ≥5% cover in at least one plot included; highly correlated species were removed from predictor sets to reduce redundancy (e.g., P. schreberi and V. myrtillus).
  - Depth to organic horizon (OH), soil organic horizon characteristics, carbon-to-nitrogen ratios, bulk density, and plant biomass were among the soil/biotic predictors considered.

## Data limitations and adaptive considerations for monitoring

- Weather data constraints: Absence of GUO weather station necessitated alternate modeling approaches, highlighting the importance of consistent instrumentation across sites for cross-site comparability.
- Covariate handling: Collinearity led to exclusion of certain predictors; stepwise model selection guided by LR tests prioritized interpretable, non-redundant drivers.
- Temporal relationship: Time-since-fire did not remain a significant continuous predictor in the best models, prompting a shift to site-level discrete effects to capture spatial heterogeneity.

## Implications for monitoring frameworks

- Long-term, multi-site design: Demonstrates how to structure a forest-floor GHG monitoring program across sites with different disturbance histories.
- Data breadth: Combines gas flux measurements with detailed soil chemistry, microbial community indicators (PLFA), and vegetation structure to explain flux patterns.
- Data governance considerations:
  - Need for standardized metadata and data sharing to enable cross-site synthesis.
  - Importance of maintaining consistent measurement protocols and weather instrumentation to avoid data silos and gaps.
- Practical monitoring recommendations:
  - Ensure weather data coverage at all sites to maximize model applicability and comparability.
  - Include sufficient replication (collars, transects) and repeated sampling to account for temporal variability.
  - Use robust model-building approaches (LMEs with random effects, collinearity checks) to identify key drivers of GHG fluxes.
  - Document data processing steps and QC procedures to support transparency and reproducibility.

## References

- Crossman ZM, Abraham F, Evershed RP. 2004.
- de Vries FT, Manning P, et al. 2012.
- Ward SE, Ostle NJ, et al. 2013.
- Whitaker J, Ostle N, et al. 2014.
- Zuur AE, Ieno EN, et al. 2009.