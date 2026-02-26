# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

## Overview
- Purpose: Provide dataset linked to the Dorset Valuing Nature Project focusing on carbon and nitrogen content in soils and vegetation across calcareous grassland, heathland, and woodland in Dorset (2017–2018).
- Basis: Builds on a baseline from Good's botanical survey of Dorset (1931–1939) to examine how ecosystem services change with habitat condition.
- Site selection: 13 calcareous grassland, 13 heathland, and 12 woodland sites chosen along a condition gradient representing degradation or restoration status.
- Data sources used for site identification and classification: Good (1930s), UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), Sites of Special Scientific Interest (SSSIs, 2014), Horsfall 1981, Dorset Heathland survey (Rose et al., 2000), and Higher Level Stewardship schemes.

## Experimental design and gradient mapping
- Gradient concept: Each habitat type is represented along a degradation/restoration gradient.
  - Calcareous grassland: categories include Improved grassland (loss of calcareous), Restoring calcareous grassland, Calcareous grassland (SSSI quality) with ties to Priority Habitats and maintenance/restoration statuses.
  - Heathland: categories include Coniferous plantation on heathland, Gorse high heathland, Heathland (SSSI quality).
  - Woodland: categories include Coniferous plantation, Broadleaf woodland, Ancient woodland (SSSI quality).
- Selection constraint: Ancient woodland plantations were explicitly excluded from site selection.
- Gradient mapping: A lookup aligns historical habitat (1940) with current habitat (2017) to define the gradient category for each site.

## Sampling methods
- Field layout: Within the Good survey area, sample squares (50 m × 50 m) were randomly assigned using ArcGIS prior to visiting.
- Soil sampling: Within each square, four 15 cm deep soil cores were collected; two were air dried and sieved (2 mm), then combined and analyzed.
  - Laboratory procedures: Ball milling of dried samples; analysis by Vario EL instrument after oxidative combustion; calibration with Acetanilide standards.
  - Quality assurance: blanks and standards run with each batch; three CRMs used at defined intervals.
  - Reporting: Carbon and nitrogen content reported as both percent (% C, % N) and mg/L of sample.
  - Bulk density: Measured in two additional soil samples; cores oven-dried at ~110°C for 48 hours; density calculated from oven-dry weight, core volume, rock fragments, etc.
- Vegetation sampling: Five 50 cm quadrats per square; all vegetation layers (herb, shrub, litter) collected and dried; shrub species identified to species level; samples analyzed as for soil.
- Data collection: Executed by experienced field ecologists; consistent data collection and QA with anomaly checks.

## Data structure and fields

- DVNP_Soil_Chemistry_data
  - Site identifiers: Site_No (CEH allocated site number; range 1–39)
  - Measurements: C_total (%), N_total (%), Bulk_Density (g cm-3)
  - Data handling: Numeric categories used for data quality checks; values correspond to top 15 cm soil samples

- DVNP_VegetationChemistry_data
  - Site and quadrat identifiers: Site_No, Quad_No (1–4, with Combined_all option)
  - Vegetation descriptors: Vegetation_type (Fresh, Litter), Vegetation_layer (Herb, Scrub)
  - Measurements: C_total (%), N_total (%), Dry_Weight (g)
  - Notes: Includes per-quadrat and combined (all quadrats) data

- Data column headings and units (summary)
  - Soil: C (%), N (%), Bulk_Density (g cm-3)
  - Vegetation: C (%), N (%), Dry_Weight (g)
  - Site/quad identifiers: Site_No, Quad_No
  - Additional descriptors: Vegetation_type, Vegetation_layer

## Habitat gradient lookup table
- Purpose: Defines the mapping from 1940 habitat classifications to 2017 habitat classifications to establish the gradient category.
- Examples of mappings:
  - Calcareous (1940) → Calcareous grassland (SSSI quality) or Improved grassland or Restoring calcareous grassland
  - Heathland (1940) → Coniferous plantation on heathland or Gorse high heathland or Heathland (SSSI quality)
  - Woodland (1940) → Broadleaf woodland, Coniferous plantation, Ancient woodland (SSSI quality)
- Utilization: Used to assign the appropriate gradient category to each site based on historical vs. current habitat.

## Data provenance, quality and access
- Provenance: Data collected in a consistent, controlled field program with a documented linkage to historical Dorset surveys.
- QA: Field ecologists performed uniform sampling; data checked for anomalies; laboratory QA with blanks, standards, and CRMs.
- Accessibility: The Good archive (historic Dorset botanical survey) is publicly accessible via the Dorset Environmental Records Centre; data collection relied on multiple established data sources (land cover, habitat inventories, and historical surveys).

## References
- Good, R. (1937). An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981). A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3. Dorset Proc 103
- Natural England (2014). Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015). Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000). Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125