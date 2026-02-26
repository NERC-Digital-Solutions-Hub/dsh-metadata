# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

- Objective: Develop data-driven landscape and agricultural management archetypes (1 km resolution) across Great Britain to support monitoring of environmental health and policy performance over time, using standardized outputs for scrutiny and comparison.

- Tier structure and purpose
  - Tier 1: Quantifies broad, long-term landscape differences in soil, land cover, and population; largely not directly influenced by land managers (10–100 year timescales).
  - Tier 2: Captures nuanced variations within farmland-dominated areas; reflects features that land managers can influence on intermediate timescales (1–10 years).
  - Tier 3: National-level (England and Wales) focus on socioeconomic and agro-ecological farm-management characteristics; aims to describe how farming practices differ and may adapt.
  - Scotland: Tier 3 archetypes not generated due to unavailable input variables for agricultural management.
  - Tiers are analyzed separately (non-nested); a Tier 3 archetype can appear in multiple Tier 2 archetypes.

- Data structure and outputs
  - Spatial resolution: 1 km2 cells.
  - Outputs per tier: 4 multi-band rasters (two bands per raster) plus 4 CSV files with variable loadings and shorthand archetype names.
  - Rasters contain: archetype ID and Euclidean distance (fit quality) per cell.
  - Tier 1 & 2 rasters cover Great Britain; Tier 3 rasters cover England and Wales; no Scotland Tier 3 due to data gaps.
  - Supporting data: loadings tables and shorthand names to interpret archetypes.

- Input variables and data sources
  - Land cover and geo-physical: Land Cover Map 2015 (nine classes), mean temperature and precipitation (2006–2015), soil properties (pH, sand, silt, clay, organic carbon), soil moisture and relative dryness (2005–2015), elevation and slope, watercourses, woody linear features, inter-field hedges.
  - Socio-economic: 2011 population density; accessibility to major/minor roads; protected area data (Tier 2); high-level variables from the Sustainable Intensification Dynamic Typology Tool (Farm Business Survey-based).
  - Farm and field characteristics: farm boundaries and attributes from stewardship schemes; interpolated farm size and spread index; field shape metrics.
  - Crop and livestock: Land Cover plus Crops (2015–2019), agricultural census data (2010), pesticide application rates (2012–2016); diversity and fragmentation metrics for crops and grassland.
  - Scale rationale: Variables were chosen to represent broad landscape, management, and socio-economic variation appropriate to each tier; Tier 1 emphasizes broad physical differences, Tier 2 emphasizes modifiable landscape features, Tier 3 emphasizes farm-level management and economics.

- Methodology: Self-Organising Maps (SOM) and archetype derivation
  - Clustering method: Self-Organising Maps (SOMs) using Kohonen framework; implemented in R (kohonen package) with normalised inputs (mean-centred, unit-variance).
  - Handling missing data: Cells with missing values for most variables can still be clustered if only one variable is missing.
  - Model configuration: Parallel batch SOM, grid trained over 500 passes.
  - Determining archetypes: Iterative approach with 1000 runs of the same configuration to assess stability; to align outputs across runs, hierarchical clustering (Ward’s method) on node codebooks identified consistent archetype groupings; a 1:1 mapping of iterations to archetypes established.
  - Certainty: For each cell, assignment frequency to archetypes across iterations provides a certainty score.
  - Archetype naming: Based on strongest positive/negative weights in the archetype codebooks; names are concise shorthand for interpretation, not a full description.

- Tier-specific design details
  - Tier 1: Emphasizes broad landscape differences across GB; uses elevation, temperature, precipitation, soil and land-cover variables, population density, road distance, and large-scale land-form attributes.
  - Tier 2: Focuses on farmland-dominated landscapes; adds land-designation coverage (protected areas, scheduled monuments), landscape structure metrics (aggregation index), inter-field hedges, watercourses and woody features, and soil moisture context.
  - Tier 3: England and Wales; includes farm-level spatial features (farm/field size, spreading index, field shape), crop and livestock metrics (diversity, patch metrics, Edge Contrast Index, Isolation, Subdivision), and economic variables (farm costs, AES income, economy reliance, employment), derived from farm surveys and census data.
  - Scotland limitations: Tier 3 not produced due to missing input variables for agricultural management.

- Outputs and accessibility
  - Data products are designed for monitoring workflows: easily interpretable archetypes, associated loadings, and location-specific distance to archetype centroids.
  - Outputs enable tracking of environmental health indicators and policy performance through standardized, comparable units over time.
  - The methodology includes documentation for reproducibility (data processing via ArcGIS v10.6 and R, 1000 iterations, sensitivity analyses).

- Key methodological considerations and challenges
  - Balancing generalisation versus specificity of archetypes; multiple candidate SOM configurations assessed via elbow method and criteria for accuracy and consistency.
  - Ensuring cross-iteration stability through clustering of codebooks and recording a certainty metric for each cell.
  - Non-nested tier design aids interpretability and cross-tier comparability of archetypes.

- Relevance for Analysts Monitoring the Environment
  - Provides a standardized, data-driven framework to classify landscapes and farming practices into archetypes that are interpretable and comparable over time.
  - Facilitates integration of diverse environmental and socio-economic data into a common monitoring framework.
  - Supports evaluation of adaptation opportunities and policy impacts by linking landscape and management archetypes with environmental and agricultural outcomes.