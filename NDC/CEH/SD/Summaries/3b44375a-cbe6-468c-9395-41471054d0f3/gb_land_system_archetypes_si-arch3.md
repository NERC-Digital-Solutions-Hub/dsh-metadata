# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

## Aim and scope
- Employ data-driven machine learning to create landscape and agricultural management archetypes at 1 km resolution, across three tiers defined by opportunities for adaptation.
- Tier 1: broad, country-wide landscape differences in soil, land cover, and population (long-term influence).
- Tier 2: nuanced variations within farmland-dominated landscapes (intermediate timescales, landowner influence).
- Tier 3: national-level England and Wales focusing on socioeconomic and agro-ecological farm management characteristics (shorter-term variation).
- Scotland Tier 3 not produced due to input variable gaps.
- Outputs designed to aid interpretation across tiers and support policy-oriented monitoring and decision-making.

## Data structure and outputs
- Outputs include:
  - Four multi-band rasters (two bands for Tier 1/2 across Great Britain; one raster per country for Tier 3 in England and Wales).
  - Each raster contains archetype ID and Euclidean distance to the archetype centroid.
  - Four accompanying CSV files detailing loadings of input variables for each archetype and shorthand archetype names.
- Spatial resolution: 1 km2, aligned to Ordnance Survey grid cells with >75% terrestrial land cover.
- Data processing and analyses performed in ArcGIS v10.6 and R.

## Input variables and data sources
- Tier-specific variable selection guided by expert judgement to capture:
  - Tier 1: broad landscape character across the country (long-term modifiability).
  - Tier 2: farmed landscape variation with intermediate-time influence.
  - Tier 3: farm-manageable elements and short-term variations.
- Land cover and geo-physical factors:
  - Land Cover Map 2015 (nine aggregate classes), climate variables (temperature, precipitation 2006–2015), soils (pH, sand, silt, clay, soil organic carbon), soil moisture and relative dryness (G2G hydrological model), elevation, slope, watercourses, woody linear features, inter-field hedges.
- Socio-economic factors:
  - Population density (2011 census-based), road accessibility, protected area designations (natural areas, Scheduled Monuments).
  - Derived from Sustainable Intensification Dynamic Typology Tool and Farm Business Survey data (England & Wales), resampled to 1 km2 for comparability.
- Farm and field characteristics:
  - Farm boundaries (England: Countryside Stewardship, Environmental Stewardship, Organic Farming Scheme; Wales: Glastir schemes), interpolated farm sizes via ordinary Kriging, Spread Index, field shape metrics (edge:length, etc.).
- Crop and livestock data:
  - Crop and livestock cover from Land Cover plus Crops (LCC) and Agricultural Census; crop diversity and connectivity metrics (Simpson's diversity/evenness, Edge Contrast Index), Patch Subdivision, Patch Isolation, Crop patch dynamics over multiple years.
- Data processing and transformation:
  - Data resampled/interpolated to 1 km2 where needed; multiple years integrated for certain metrics; module-specific scaling to relative measures for comparability.

## Self-Organising Map (SOM) methodology
- Clustering and dimensionality reduction via Self-Organising Maps (SOMs) to identify archetype centroids.
- SOM setup:
  - Input: normalized, mean-centered and unit-variance data; grid-based NxN nodes; capacity to handle cells with missing data (missing up to all but one variable).
  - Training: parallel batch method, 500 presentations.
- Robustness and reproducibility:
  - 1000 iterations with fixed input parameters to account for stochastic initialization.
  - Hierarchical clustering (Ward’s method) across iteration-derived node codebooks to align nodes into major archetype groups.
  - 1:1 mapping across iterations to derive stable archetypes; each cell assigned based on the most frequent archetype across iterations.
  - Certainty metric recorded to reflect classification stability for each cell.
- Archetype naming:
  - Names derived from the strongest positive/negative variable loadings in each archetype codebook, concatenated and simplified for readability.
  - Names are for convenience and do not exhaustively describe archetype characteristics.

## Output interpretation and monitoring relevance
- Archetypes are non-nested across tiers; a Tier 3 archetype can occur within multiple Tier 2 archetypes.
- Outputs provide a standardized, data-driven basis to monitor landscape and farming conditions, support scenario analysis, and inform policy targeting and evaluation.
- Distance to archetype and assignment certainty support assessments of data confidence and spatial coverage.

## Key methodological and governance considerations
- Data quality and availability are central: reliance on diverse national datasets with varying resolutions, update frequencies, and metadata availability.
- Metadata challenges:
  - Some datasets require careful provenance tracking and may limit sharing or reuse due to privacy or licensing.
  - Transformation and integration steps can be non-trivial, highlighting the need for transparent data governance and open reporting of methods.
- Reproducibility and transparency:
  - Extensive documentation of input variables, sources, and processing steps.
  - Provision of supporting CSVs with loadings to enable independent verification and reuse.
- Limitations:
  - Scotland Tier 3 not developed due to unavailability of certain input variables at required resolutions.
  - Handling of missing data in SOM and stability considerations addressed through iterative clustering and consistency checks.

## Practitioner takeaway for monitoring frameworks
- Tiered archetyping provides a scalable framework to categorize landscapes and farming contexts for policy assessment and monitoring.
- Data governance implications:
  - Emphasizes need for open metadata, data provenance, and clear sharing terms to enable reuse in monitoring frameworks.
  - Highlights importance of ensuring data are updated and harmonized across tiers to support timely decision-making.
- Practical use:
  - Archetypes can underpin targeted monitoring indicators, influence prioritization of sustainable intensification strategies, and support evaluation of management interventions at multiple scales and timeframes.