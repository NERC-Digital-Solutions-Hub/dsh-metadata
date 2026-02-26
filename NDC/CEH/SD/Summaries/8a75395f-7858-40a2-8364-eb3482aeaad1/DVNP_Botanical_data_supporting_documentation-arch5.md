# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

## Aim and context
- Builds on Ronald Good’s 1931–1939 Dorset botanical survey; archive is public via the Dorset Environmental Records Centre (DERC) and serves as a baseline for site selection and assessing how ecosystem services change with habitat condition.
- Subsamples sites identified by Good as calcareous grassland, heathland, or woodland from the 1930s to create survey sites representing a degradation gradient.
- Integrates multiple data sources to identify current habitat types, including UK Land Cover Map 2007, Natural England Priority Habitats Inventory (2015), SSSIs (2014), Horsfall (1981), Dorset Heathland Survey (Rose et al., 2000), and Higher Level Stewardship data.

## Experimental design
- Site numbers: 13 calcareous grassland, 13 heathland, and 12 woodland sites selected to cover a range of habitat types along a condition/degradation gradient.
- Gradient definitions:
  - Calcareous: from original Good 1930s calcareous grasslands to improved grassland, and to calcareous grassland (SSSI quality) or restoring calcareous grassland.
  - Heathland: from Good 1930s heath to coniferous plantation on heathland, to high-gorse heath and heathland (SSSI quality).
  - Woodland: from Good 1930s wood to coniferous plantation, broadleaf woodland, and ancient woodland (SSSI quality).
- Some sites overlap with SSSI status and are aligned with Priority Habitats Inventory classifications.

## Collection methods
- Sampling frame: 50 m × 50 m plots were randomly assigned within the original Good survey area using ArcGIS.
- Heathland and calcareous grassland:
  - Five 1 m quadrats per site; record percentage cover for all plant species (to species level where possible, genus if not).
  - Record bare ground and litter cover.
  - Sward height measured directly at five points per quadrat; average taken as site-level sward height.
- Woodland:
  - Five 10 m × 10 m quadrats for canopy/tree/shrub assessment laid in a cross across the 50 m × 50 m area (one in each corner and one at the center).
  - Center quadrat (5 m × 5 m) records understory components (shrubs, understory trees, saplings).
  - A 2 m × 2 m quadrat records ground-level herbaceous species and saplings; capture tree seedling cover as appropriate.
  - Detailed schema records canopy, understory, and ground-layer data, with explicit differentiation of canopy categories and growth forms.

## Quality control
- Field data collected by experienced ecologists; the same team collected all surveys to ensure consistency.
- Data entered directly from field sheets and checked for anomalies.
- Data structure and metadata:
  - DVNP_Botanical_Data_Groundcover: includes Site_No, Date_of_Survey, Surveyor, Habitat (1940 classification), Grid_ref (10 km resolution), Quad_No (1–5), Quad_size, Sward_Ht, Species_name (species or genus when necessary), %_cover, Vegetation_Layer (Ground, Canopy, etc.).
  - DVNP_Botanical_Data_WoodlandCanopy: includes Site_No, Date_of_Survey, Surveyor, Quad_No, Quadrant details, Species_name, Tree_type, Cover_type, Measurement_unit, Value.
- A habitat lookup table maps 1940 habitat categories to 2017 habitat classifications (calcareous/woodland/heathland categories and their gradient states), used to define the proposed gradient category for analyses.

## Data structure and provenance
- Two main data components:
  - Groundcover botanical data for heathland and calcareous grassland (species-level as available, with percentage cover and vegetation layer).
  - Woodland canopy data capturing canopy, understorey, and ground-level components across multiple nested quadrats.
- 10 km grid references accompany site identifiers to facilitate integration with other spatial datasets.
- 2017 habitat gradient mapping provides a standardized framework for cross-temporal comparison (1940 vs 2017 classifications).
- References informing methodology: Good (1937), Horsfall (1981), Natural England sources (2014, 2015), Rose et al. (2000).

## References and data sources
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116.
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931.
- Natural England (2014) Sites of Special Scientific Interest and historic monuments.
- Natural England (2015) Priority Habitats Inventory version 2.1.
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996.

## Data availability and governance for Data Stewards
- Public archival access through Dorset Environmental Records Centre; ensure ongoing accessibility and proper citation of Good (1937) and subsequent sources.
- Data are organized with explicit field definitions, units, and lookup mappings to support interoperability and reuse across platforms.
- Maintain provenance by preserving original field sheets, documenting any data transformations (e.g., genus-level identifications, gradient category derivations).
- Version control and metadata updates should accompany any future reprocessing or expanded datasets, particularly when aligning historical (1940) and contemporary (2017) habitat classifications.
- Considerations for data sharing limits: ensure alignment with any embargoes or usage restrictions from partner sources; clearly document data sources and lineage in metadata.

## Key considerations for alignment with Data Stewards’ aims and challenges
- Data governance: maintain standard vocabulary, consistent units, and clear metadata to support discovery and reuse.
- Interoperability: harmonize with other Dorset vegetation datasets via the 1940/2017 habitat gradient mapping and standardized grid references.
- Data quality: retain the same field collection protocols (same ecologists where possible) and rigorous anomaly checking to ensure reliability across the full dataset.
- Accessibility and updates: provide clear documentation of collection methods and gradient definitions to facilitate updates and potential expansion of sampling in future work.