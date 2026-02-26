# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

- Purpose and approach
  - Data-driven machine learning (Self-Organising Maps) to create landscape and agricultural management archetypes at 1 km resolution.
  - Three tiers defined by adaptation opportunities:
    - Tier 1: broad, country-wide landscape differences (modifiable only over long timescales).
    - Tier 2: nuanced variations within farmland-dominated landscapes (intermediate timescales).
    - Tier 3: national England and Wales focus on socio-economic and agro-ecological farm management characteristics (shorter timescales).
  - Tier 3 archetypes for Scotland could not be generated due to missing input variables.
  - Tiers are analyzed separately, not nested (a Tier 3 archetype can occur in more than one Tier 2 archetype).

- Data structure and outputs
  - 4 multi-band raster files:
    - Tier 1 and Tier 2: one GB raster.
    - Tier 3: one England raster and one Wales raster.
  - Each raster contains:
    - Archetype ID
    - Euclidean distance (how well each cell fits its archetype)
  - 4 corresponding CSV files with:
    - Loadings of each input variable for each archetype
    - Shorthand name for each archetype

- Input variables and data processing
  - Resolution: 1 km² to reflect data availability and typical farm size in England.
  - Tier-specific variable selection to capture bio-geo-physical, land management, and socio-economic variation.
  - Data processing tools: ArcGIS v10.6 and R.
  - Variable categories and examples:
    - Land cover and geo-physical
      - Land cover percentages (nine classes), climate (temperature, precipitation), soils (pH, sands, silt, clay, organic carbon), soil moisture, relative soil dryness, elevation and slope, water courses, woody linear features, inter-field hedges.
    - Socio-economic
      - Population density, road accessibility, protected area coverage (Tier 2), high-level socio-economic indicators from the Sustainable Intensification Dynamic Typology Tool (Farm Business Survey-based).
    - Farm and field spatial characteristics
      - Farm and field sizes, farm spread, field shape, farm boundaries from stewardship schemes, interpolation to predict farm size.
    - Crop and livestock cover
      - Crops and livestock distributions (from Land Cover plus Crops and Ag census), pesticide application rates, and metrics describing spatial patterns of crops (diversity, evenness, edge contrast, subdivision, isolation) across multiple years.
  - Tier-specific variable inclusion reflects intended influence: Tier 1 for broad landscape patterns; Tier 2 for management-influenced features; Tier 3 for farm-level practices.

- Self-Organising Map (SOM) parameterisation and analysis
  - SOMs (Kohonen method) used to cluster 1 km² cells into archetype nodes.
  - Data normalised (mean-centred, unit variance); missing data allowed (cells clustered with available data).
  - Model run: parallel batch SOM, 500 presentations; grid size chosen via elbow criterion balancing accuracy and consistency.
  - Stability and certainty
    - 1000 iterations with fixed input parameters to account for stochastic initialization.
    - Hierarchical clustering (Ward’s method) on node codebooks to align iterations and identify major archetype groups.
    - 1:1 mapping across iterations; each cell assigned to the archetype it most frequently maps to (plus a distance metric for certainty).

- Archetype derivation and naming
  - Archetype centroids (codebooks) derived from aggregated iterations.
  - Names derived by concatenating the strongest negative and positive variable weightings in each archetype’s codebook; names simplified for readability. These names are for convenience and do not fully describe all archetype characteristics.
  - Outputs include per-cell archetype assignments and distance to archetype centroids to indicate fit.

- Practical implications for data use
  - Provides a set of named archetypes at three organizational scales (country, farmland, and socio-economic management).
  - Enables self-serve exploration of landscape and farming practice typologies across Great Britain (with England and Wales for Tier 3; Scotland limited by data availability).
  - Useful for policy prioritisation, scenario analysis, and targeted management strategies by linking landscape characteristics to potential adaptation opportunities.
  - The supporting information includes detailed loadings and variable contributions to each archetype, enabling researchers and practitioners to interpret and reuse the archetypes in further analyses.

- Notes and limitations
  - Tier 3 archetypes unavailable for Scotland due to missing input variables.
  - Archetype definitions are not nested across tiers; a Tier 3 archetype can appear in multiple Tier 2 archetypes.
  - Variable selection and data availability influence archetype characteristics; sensitivity analyses were conducted to assess the impact of including/excluding variables.