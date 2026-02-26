# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

## Aim and scope
- Establish a baseline and monitor changes in ecosystem services by comparing current habitat conditions to a historic baseline from Good’s 1931–1939 Dorset botanical survey.
- Select sites across a condition gradient (degradation from original habitat) to study how ecosystem services vary with habitat condition.
- Use multiple data sources to identify current habitat types and ensure representation across calcareous grassland, heathland, and woodland.

## Experimental design
- Base: Good, R. 1937; public archive at Dorset Environmental Records Centre (DERC).
- Subsampling strategy: Use Good’s 1930s calcareous grassland, heathland, and woodland sites; identify current habitat types with UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), SSSIs (2014), Horsfall (1981), Dorset Heathland Survey (Rose et al., 2000), and Higher Level Stewardship data.
- Site selection: 13 calcareous grassland, 13 heathland, and 12 woodland sites; chosen to represent a range of new habitat types across a progression of degradation from the original habitat.
- Gradient definitions (examples):
  - Calcareous: improved grassland; restoring calcareous grassland; calcareous grassland (SSSI quality).
  - Heathland: coniferous plantation on heathland; high-gorse heathland; heathland (SSSI quality).
  - Woodland: coniferous plantation; broadleaf woodland; ancient woodland (SSSI quality).
- Note: Ancient woodland plantations to be excluded where relevant; all gradient classifications cross-validated with multiple data layers and SSSI status where applicable.

## Collection methods
- Plot layout: Randomly assign 50 m × 50 m sample squares within the Good survey area using ArcGIS.
- Heathland and calcareous grassland:
  - Five 1 m × 1 m quadrats per site to record percent cover of vascular plants (species or genus where needed), bare ground, and litter.
  - Sward height measured directly (five points per quadrat) and averaged.
- Woodland:
  - Five 10 m × 10 m quadrats arranged in a cross across the 50 m × 50 m area to capture canopy data.
  - Within each 10 m × 10 m quadrat: record canopy cover and presence of tree species.
  - Center 5 m × 5 m quadrat for understory: canopy cover, shrubs and understory trees, and saplings.
  - Within each 5 m × 5 m quadrat: 2 m × 2 m quadrat for ground-level herbaceous species and tree seedlings; record trunk data if needed.
- Documentation: Data recorded with explicit quadrat identifiers, species names (or genus when necessary), and vegetation layer classifications.

## Quality control
- Fieldwork conducted by experienced ecologists; the same team carried out all surveys to ensure consistency.
- In-field checks for anomalies; standardized data entry into DVNP botanical spreadsheets.
- Detailed data columns described for two datasets:
  - DVNP_Botanical_Data_Groundcover
  - DVNP_Botanical_Data_WoodlandCanopy
- Metadata fields include site numbers, dates, surveyors, habitat history (1940 baseline per Good), grid references, quadrat details, sward height, species, cover percentages, vegetation layers, and woodland-specific metrics (tree type, cover type, abundance, etc.).

## Data structure, variables, and gradient definitions
- Groundcover dataset fields include: Site_No, Date_of_Survey, Surveyor, Habitat (1940 and 2017), Grid_ref, Quad_No, Quad_size, Sward_Ht, Species_name, %_cover, Vegetation_Layer.
- Woodland canopy dataset fields include: Site_No, Date_of_Survey, Surveyor, Quad_No, Quadrat_size, Species_name, Tree_type, Cover_type, Measurement_unit, Value, Abundance.
- Lookup: Habitat1940-to-Habitat2017 gradient mapping defines proposed gradient categories (Calcareous, Heathland, Woodland) across 1940 vs 2017 statuses, including Calcareous grassland (SSSI quality), Improved/restoring calcareous grassland, Coniferous/broadleaf/ancient woodland, Gorse high heathland, and related SSSI status considerations.
- Gradient categories are designed to enable monitoring of habitat change over time and its relation to ecosystem services, with emphasis on SSSI status and habitat preservation/restoration.

## Data governance, sharing, and metadata
- Emphasis on data openness: underlying data and the methods are documented to facilitate verification and reuse.
- Metadata considerations highlighted, including the need to publically share datasets and ensure data quality and management standards at the source.
- Data provenance relies on publicly accessible historic records (Good, Horsfall, Dorset Heathland surveys, Natural England inventories, and SSSI records), enabling transparent linkage between baseline and current conditions.

## Practical relevance for monitoring and policy
- Provides a structured, multiclass habitat gradient framework to assess how ecosystem services respond to habitat condition, enabling policy evaluation and decision-making for Dorset Valuing Nature.
- Combines historic baselines with contemporary field data to quantify degradation or restoration trajectories.
- Data collection and governance align with common monitoring framework expectations: clear methods, consistent sampling, metadata-rich datasets, and openness to facilitate future analyses and accountability.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125