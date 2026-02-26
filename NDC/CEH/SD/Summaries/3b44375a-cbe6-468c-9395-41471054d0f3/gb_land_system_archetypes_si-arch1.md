# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

- Purpose: Data-driven machine learning to create landscape and agricultural management archetypes at 1 km resolution, organized into three tiers reflecting levels of adaptation opportunities and control by land managers.

- Tiers and scope:
  - Tier 1: Broad landscape differences across Great Britain (GB); changes are difficult to influence by land managers (long timeframes).
  - Tier 2: Nuanced variations within farmland-dominated GB landscapes; land manager influence possible on intermediate timescales.
  - Tier 3: National-level archetypes for England and Wales focusing on socioeconomic and agro-ecological characteristics within farmland-dominated landscapes; Scotland not included due to input gaps.

- Data structure and outputs:
  - Four multi-band raster files (GB for Tier 1 & 2; England and Wales for Tier 3) with two bands each: archetype ID and Euclidean distance to archetype.
  - Four supporting CSV files detailing input variable loadings for each archetype and shorthand archetype names.
  - Resolution and scale: all input variables processed at 1 km2; values reflect 75% land cover grid cells.

- Input variables (highlights by category):
  - Land cover and geo-physical: nine land-cover classes, soil properties (pH, sand, silt, clay, organic carbon), mean climate metrics (temperature, precipitation), soil moisture, relative dryness, elevation, slope, landscape structure metrics, water courses, woody linear features, inter-field hedges.
  - Socio-economic: population density (Tier 1), road accessibility, protected areas (natural protected areas and Scheduled Monuments), and high-level socio-economic indicators from the Sustainable Intensification Dynamic Typology Tool.
  - Farm and field spatial characteristics: farm boundaries (from stewardship schemes), field-level spatial features (size, Spread Index), field shape metrics.
  - Crop and livestock: crop and livestock cover sourced from Land Cover Plus (Crops) and Ag Census; pesticide application rates; diversity and functional-structure metrics (e.g., Simpson’s diversity, Edge Contrast Index, Subdivision Index, Isolation); patch-based metrics across five-year data windows.
  - Data sources include UKCEH, OS Open Roads, Natural England schemes, Glastir (Wales), CADW/Historic England and Scotland data, and multiple national soil and climate datasets.

- Self-Organising Map (SOM) methodology:
  - Clustering and dimensionality reduction via SOMs (Kohonen method) using normalized data.
  - Handling missing data: cells with missing data for all but one variable are still clustered; missing values do not prevent clustering.
  - SOM configuration: grid size determined by elbow method; aim to maximize accuracy (mean distance to centroids), consistency (stable node assignment), and cross-iteration stability.
  - Implementation: Kohonen R package, parallel batch, 500 presentations per run.

- Archetype generation and stability:
  - To address randomness in SOM initialization, 1000 iterations were run with fixed inputs.
  - Hierarchical clustering (Ward’s method) across node codebooks to identify consistent archetypes; each cell assigned to the archetype it most frequently mapped to across iterations.
  - Certainty metric: records consistency of a cell’s assignment across iterations.
  - Archetype naming: derived from concatenating strongest negative and positive variable loadings in each archetype’s codebook; names are simplified for readability and do not fully describe archetype characteristics.

- Processing tools and workflow:
  - Data processing: ArcGIS v10.6 and R (R Core Team 2020).
  - Variables standardized and condensed through expert judgment to capture tier-specific modifiability and timeframes (Tier 1: broad landscape differences; Tier 2: farmed landscapes; Tier 3: short-term farming decisions).
  - Sensitivity analyses: tested variable removal/addition and alternative configurations to assess impact on archetypes, clusters, and classifications.

- What the outputs enable for analysts:
  - Spatial mapping of archetypes across GB, England, and Wales, with per-cell distance to archetype centroids indicating how well each cell fits its assigned archetype.
  - Comparative analysis of landscape and farming practice archetypes to inform policy, management, and adaptation planning.
  - Transparent data provenance and reproducibility through explicit data sources, loadings, and codebooks, enabling discoverability and reuse.

- Key limitations and considerations:
  - Tier 3 archetypes unavailable for Scotland due to missing input variables.
  - Tiers are analyzed separately rather than nested; a Tier 3 archetype can exist within multiple Tier 2 archetypes.
  - Variability in input data resolution and availability across datasets; careful interpretation required when transferring archetypes between regions or scales.