# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

- Purpose and scope
  - Data-driven machine learning to create landscape and agricultural management archetypes at 1 km resolution across Great Britain, at three tiers of analysis.
  - Tier 1: broad landscape differences (modifiable only over long timescales).
  - Tier 2: nuanced farmed-landscape differences (moderate timescale influence by land managers).
  - Tier 3: national-level socio-economic and agro-ecological characteristics within farmland-dominated landscapes (shorter-term modifiable aspects).
  - Scotland could not have Tier 3 archetypes due to missing input variables.
  - Tiers are analyzed separately (not nested) to maintain interpretability.

- Data structure and formats
  - Outputs: four multi-band raster files (two bands per file) with 1 raster for Tier 1 and 2 across Great Britain, and 1 raster each for England and Wales for Tier 3.
  - Each raster includes: archetype ID and Euclidean distance to the archetype.
  - Supporting CSV files (four) provide loadings of input variables for each archetype and enable shorthand archetype naming.
  - Data are aligned to a 1 km2 grid (standard for variable availability and farm size approximation in England).

- Input variables and tier-specific design
  - Tier 1: land cover, basic geo-physical, climate, soils, and landscape structure variables to capture broad landscape differences.
  - Tier 2: adds soil moisture, relative dryness, accessibility metrics, protected area coverage, and larger-scale socio-economic indicators.
  - Tier 3: emphasizes farm/field spatial features, crop and livestock distributions, farm economics, and more granular landscape metrics.
  - Variables are sourced from multiple datasets with defined timeframes (e.g., Land Cover Map 2015; climate 2005–2015; soils around 2013; Farm Business Survey 2016; AgCensus 2010; UKCEH LCC 2015–2020).

- Data sources and provenance
  - Land cover and soils: UKCEH/associated national soil maps; OS, UKCEH datasets.
  - Climate and hydrology: CHESS/CHESS-met, MaRIUS-G2G, hydrological and meteorological datasets.
  - Farm and socio-economic data: Farm Business Survey (England & Wales), AgCensus, Rural Designations, and Glastir scheme data (Wales).
  - Landscape structure and features: road networks, watercourses, woody linear features, hedges, and protected area designations.
  - Data processing and tools: ArcGIS v10.6 and R; SOM implementation via Kohonen package; missing-data tolerance during clustering.

- Methodology and quality assurance
  - Self-Organising Maps (SOMs) used for clustering 1 km2 cells into archetypes, with normalised input data.
  - SOM runs allow missing data for all but one variable; clustering performed with parallel batch processing (500 passes).
  - To address stochasticity, 1000 iterations were run; hierarchical clustering (Ward’s method) identified consistent archetype groupings across iterations to enable 1:1 mappings.
  - Each cell is assigned to the archetype it most frequently maps to across iterations; a certainty metric records classification stability.
  - Archetype names are derived from the strongest positive/negative variable loadings in each archetype’s codebook, then simplified for interpretability.

- Outputs and interpretation
  - Archetype centroids (codebooks) describe typical variable combinations for each archetype.
  - Per-cell assignments include archetype label and Euclidean distance to the archetype centroid, plus a certainty score.
  - Outputs are designed to be usable across stakeholders for understanding landscape and farming practice typologies, with documentation in Tables S1–S4 and accompanying supporting information.

- Data quality, uncertainty, and reproducibility
  - Balance between generalisation and specificity addressed via iterative SOM configurations and elbow-plot assessments of clustering distance.
  - Consistency across iterations checked through hierarchical clustering; mean codebooks computed across iterations to stabilise archetype definitions.
  - Sensitivity analyses conducted by adding/removing variables to evaluate effects on archetype stability and cluster consistency.
  - Missing data handled in clustering to maximise inclusion without biasing results unduly.

- Practical considerations for Data Stewards (data governance and reuse)
  - Metadata and provenance: comprehensive documentation of data sources, timeframes, scales, and processing steps is essential for reproducibility and audit trails.
  - Data formats and interoperability: maintain clear specifications for raster outputs (band structure, projections) and CSV loadings to enable reuse in GIS and analytics workflows.
  - Versioning and updates: given stochastic SOM outputs, preserve iteration metadata, archetype mappings, and certainty scores to support traceability and future re-runs.
  - Licensing and access: ensure licensing for all input datasets is respected; provide clear reuse terms for archetype outputs and any derivative analyses.
  - Data quality management: maintain data quality checks, lineage records, and change logs; document limitations (e.g., Tier 3 Scotland absence) and their implications for cross-region analyses.
  - Governance implications: establish governance for archiving, sharing, and updating archetype datasets, including procedures for handling missing variables in future updates and ensuring cross-tier compatibility where applicable.

- Limitations and caveats
  - Tier 3 archetypes unavailable for Scotland due to input-variable gaps.
  - Archetype definitions are simplified for readability and do not exhaustively describe all archetype characteristics.
  - Archetypes are non-nested across tiers; a Tier 3 archetype may appear in more than one Tier 2 archetype.