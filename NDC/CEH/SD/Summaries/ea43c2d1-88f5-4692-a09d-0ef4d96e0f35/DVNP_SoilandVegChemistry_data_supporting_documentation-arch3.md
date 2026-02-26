# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

- Purpose and scope
  - Document describing a field dataset on soil carbon and nitrogen content and vegetation chemistry from calcareous grassland, heathland, and woodland in Dorset (2017–2018).
  - Builds a baseline, using Good’s 1930s Dorset survey to assess how ecosystem services change with habitat condition.
  - Subsamples Good-identified sites and integrates multiple data sources to characterize current habitat types and degradation gradients.

- Experimental design
  - Based on historical survey by Professor Ronald Good (1931–1939); archive publicly available via Dorset Environmental Records Centre.
  - Site selection uses Good’s calcareous grassland, heathland, and woodland categories, updated with UK Land Cover Map 2007, Natural England Priority Habitat Inventory, SSSIs, Horsfall (1981), Dorset Heathland survey (2000), and Higher Level Stewardship data.
  - For each habitat type, sites are chosen across a degradation gradient:
    - Calcareous grassland: improving grassland, restoring grassland, and SSSI-quality grassland (with related designations like HK7, HK6, etc.).
    - Heathland: coniferous plantation on heathland, high-gorse heathland, and SSSI-quality heathland.
    - Woodland: coniferous plantation, broadleaf woodland, ancient woodland (SSSI quality).
  - Gradient categories aligned with historical reference (1940) to contemporary (2017) habitat classifications.

- Site selection and gradient categories
  - Thirteen calcareous grassland, thirteen heathland, and twelve woodland sites (total 39) chosen to span the condition gradient from degraded to preserved/restored.
  - Gradient assignments link historical habitat status (1940) to 2017 habitat status, including SSSI quality, restoration, and maintenance designations.

- Collection methods
  - Sampling design: random 50 m x 50 m plots (sample squares) within the Good-area, assigned pre-visit via ArcGIS.
  - Soil sampling:
    - Within each plot, four 15 cm deep soil cores collected.
    - Samples air-dried, sieved (2 mm), ball-milled, then analysed by Vario EL CN analyzer after calibration with standards (Acetanilide; ~71.1% C, 10.4% N).
    - Quality assurance: blanks and certified reference materials (CRMs) included in each run (beginning, every 10 samples, and end).
    - Detection limits: C 2.0%, N 0.12%.
    - Bulk density: two extra samples collected; cores oven-dried, volume measured, and density calculated with rock/root corrections.
  - Vegetation sampling:
    - Five 50 cm quadrats per plot; all layers (herb, shrub, litter) sampled.
    - Species in shrub layer identified to species level.
    - Dried vegetation analysed at UKCEH like soil samples (carbon and nitrogen content, dry weight).

- Data collection and quality control
  - Experienced field ecologists conducted all surveys; two layers of checks included.
  - Data recorded in field spreadsheet; checked for anomalies to ensure consistency and reliability.

- Data structure and column headings
  - DVNP_Soil_Chemistry_data:
    - Site_No (1-39; CEH site identifier)
    - C_total (carbon concentration %)
    - N_total (nitrogen concentration %)
    - Bulk_Density (soil bulk density in g/cm^3)
  - DVNP_VegetationChemistry_data:
    - Site_No (1-39)
    - Quad_No (1-4; quadrat number; combined_all option available)
    - Vegetation_type (e.g., Fresh vegetation, Litter)
    - Vegetation_layer (Herb, Scrub)
    - C_total (carbon concentration %)
    - N_total (nitrogen concentration %)
    - Dry_Weight (g)
  - Field notes: data collected by consistent team; materials transformed and stored with clear documentation.

- Habitat gradient mapping
  - Look-up table aligns 1940 habitat labels with 2017 habitat categories to define a gradient (e.g., Calcareous → Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland, Heathland → Coniferous plantation on heathland, Gorse high heathland, Heathland (SSSI quality), Woodland → Broadleaf or Coniferous plantation, Ancient woodland (SSSI quality), etc.).

- Data provenance, accessibility, and governance
  - Archive and dataset are publicly accessible via Dorset Environmental Records Centre.
  - Metadata and data management practices underpin data quality, transformation steps, and clear presentation of findings (via reports or dashboards).
  - Data sources integrated to support transparency, comparability, and potential replication.

- References
  - Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
  - Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
  - Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
  - Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
  - Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125