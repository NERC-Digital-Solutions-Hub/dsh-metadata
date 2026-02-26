# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

## Overview
- Dataset from Dorset Valuing Nature Project field component focusing on carbon and nitrogen content in soils and vegetation.
- Targets calcareous grassland, heathland, and woodland sites in Dorset, surveyed in 2017–2018.
- Built from a baseline comparison using historical Good (1930s) surveys to assess ecosystem services relative to habitat condition.
- Data are structured into soil chemistry and vegetation chemistry components with standardized headings and units.

## Experimental design
- Baseline site selection: use Good’s 1931–1939 Dorset survey to identify calcareous grassland, heathland, and woodland sites.
- Subsampling approach: select current habitats corresponding to Good’s 1930s classifications using multiple data sources (UK Land Cover Map 2007, Natural England Priority Habitat Inventory, SSSIs, Horsfall 1981, Dorset Heathland survey 2000, Higher Level Stewardship schemes).
- Site numbers: 13 calcareous grassland, 13 heathland, 12 woodland sites chosen to represent a degradation gradient from the original habitat.
- Gradient categories (examples): 
  - Calcareous: Improved grassland; Restoring calcareous grassland; Calcareous grassland (SSSI quality).
  - Heathland: Coniferous plantation on heathland; Gorse high heathland; Heathland (SSSI quality).
  - Woodland: Coniferous plantation; Broadleaf woodland; Ancient woodland (SSSI quality).
- Habitat gradient table: includes a lookup mapping 1940 habitat types to 2017 habitat classifications to define the gradient category for each site.

## Collection methods
- Plot design: random 50m x 50m sample squares within the original Good survey area, assigned using ArcGIS prior to field visits.
- Soil sampling:
  - Within each sample square, four 15 cm deep soil cores.
  - Two cores air-dried and sieved (2 mm) and amalgamated for analysis.
  - Analysis performed on ball-milled, air-dried samples; oven-dried prior to weighing.
  - Instrumentation: Vario EL (Elementar) with oxidation and thermal conductivity detection.
  - Calibration: Acetanilide standard (~71.1% C, ~10.4% N); blanks and three certified reference materials (CRMs) included in each batch.
  - Limits of detection: C 2.0%, N 0.12%.
  - Outputs expressed as percent C and N and mg/L of sample.
  - Bulk density: measured from two additional soil samples; cores oven-dried; density calculated from weight, volume, and content (with rock and root corrections).
- Vegetation sampling:
  - Five 50 cm quadrats per sample square; all vegetation layers sampled (herb, shrub, litter).
  - Samples dried, weighed; shrub species identified to species level.
  - Dried vegetation sent to UKCEH for analysis following the same soil methodology.
- Quality and consistency:
  - Experienced field ecologists conducted all surveys; methods applied consistently.
  - Data recorded directly in field spreadsheets and checked for anomalies.
- Data management:
  - Outputs organized into standardized data files with defined column headings and units.

## Data structure and columns

- Soil chemistry file (DVNP_Soil_Chemistry_data)
  - Site_No (1–39; CEH allocated site number)
  - C_total (percent carbon)
  - N_total (percent nitrogen)
  - Bulk_Density (g cm-3; top 15 cm soil)
- Vegetation chemistry file (DVNP_VegetationChemistry_data)
  - Site_No (1–39; CEH allocated site number)
  - Quad_No (1–4; quadrat number; Combined_all option available)
  - Vegetation_type (text; e.g., Fresh, Litter)
  - Vegetation_layer (Herb, Scrub, etc.)
  - C_total (percent carbon)
  - N_total (percent nitrogen)
  - Dry_Weight (grams)
- Notes on columns:
  - Site_No maps to field sites; consistent across soil and vegetation datasets.
  - Units: carbon and nitrogen concentrations as percentages; bulk density in g cm-3; dry weight in grams.

## Habitat gradient lookup

- A mapping table aligns historical habitat classifications (1940) with current habitat classifications (2017) to define the gradient category for each site.
- Examples of mappings:
  - 1940 Calcareous → 2017 Calcareous grassland (SSSI quality) or Improved grassland or Restoring calcareous grassland.
  - 1940 Heathland → 2017 Coniferous plantation on heathland or Gorse high heathland or Heathland (SSSI quality).
  - 1940 Woodland → 2017 Broadleaf woodland, Coniferous plantation, or Ancient woodland (SSSI quality).
- This gradient framework supports analysis of habitat condition changes over time and their relation to carbon and nitrogen content.

## References and provenance
- Good, R. (1937). An account of a botanical survey of Dorset.
- Horsfall, A. (1981). A pattern of change: observations on plant habitat change in North-East Dorset since 1931.
- Rose, R.J., Webb, N.R., Clarke, R.T., Traynor, C.H. (2000). Changes on the heathlands in Dorset, England, between 1987 and 1996.
- Natural England (2014, 2015). Sites of Special Scientific Interest and Priority Habitats Inventory.
- Data sources used for site identification and habitat classification summarized in the experimental design.