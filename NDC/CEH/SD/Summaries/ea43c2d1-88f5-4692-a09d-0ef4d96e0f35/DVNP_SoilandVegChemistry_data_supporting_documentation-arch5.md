# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

## Overview
- Dataset from the Dorset Valuing Nature Project field component focusing on carbon (C) and nitrogen (N) content in soils and vegetation across calcareous grassland, heathland, and woodland sites in Dorset, collected in 2017–2018.
- Built on a baseline from Ronald Good’s historic Dorset botanical survey (1931–1939) to select sites and assess ecosystem-service changes with habitat condition.
- Site selection represents a gradient of habitat condition using multiple data sources (Land Cover Map 2007, Natural England inventories, SSSIs, Horsfall 1981, Dorset Heathland survey 2000s, Higher Level Stewardship schemes).

## Experimental design
- Baseline framework: Good’s 1930s survey area used to identify calcareous grassland, heathland, and woodland sites; gradient categories reflect degradation or restoration status.
- Site set: 13 calcareous grassland, 13 heathland, 12 woodland selected to span a condition gradient.
- Gradient categories (example mappings):
  - Calcareous: from improved grassland to restoring calcareous grassland to SSSI-quality calcareous grasslands
  - Heathland: from coniferous plantation on heathland to gorse-high heathland to heathland (SSSI quality)
  - Woodland: from coniferous plantation to broadleaf woodland to ancient woodland (SSSI quality)
- Habitat gradient mappings link 1940 habitat classifications to 2017 habitat classifications (Calcareous, Heathland, Woodland).

## Collection methods
- Plot design: Sample squares of 50 m × 50 m randomly assigned within the Good survey area (via ArcGIS) prior to fieldwork.
- Soil sampling:
  - Within each square, four 15 cm deep soil cores collected.
  - Two cores air-dried, sieved (2 mm), amalgamated and analysed by Lancaster Laboratories/UKCEH.
  - Analysis: ball-milled soil, oxidative combustion with thermal conductivity detection (Vario EL); calibration with acetanilide standards (approx. 71.1% C and 10.4% N).
  - QA: blanks and standards per batch; three certified reference materials (CRMs) used in runs (beginning, every 10 samples, end).
  - Limits of detection (LOD): C 2.0%, N 0.12%.
  - Outputs: C and N concentrations (%), plus results in mg/L.
  - Bulk density: assessed using two additional soil samples; cores oven-dried; density calculated through a defined equation.
- Biomass/vegetation sampling:
  - Five 50 cm quadrats per sample square; all vegetation layers collected (herb, shrub, litter).
  - Samples dried, weighed; shrub species identified to species level.
  - Analysis performed by UKCEH following soil methods.
  - Data collected by experienced field ecologists; units and field records checked for anomalies.
- Data management: field data entered into spreadsheets with consistent recording and QA checks.

## Data structure and fields
- Soil chemistry data (DVNP_Soil_Chemistry_data)
  - Site_No (CEH site number; range 1–39)
  - C_total (carbon concentration as %)
  - N_total (nitrogen concentration as %)
  - Bulk_Density (g cm-3; bulk density of top 15 cm)
- Vegetation chemistry data (DVNP_VegetationChemistry_data)
  - Site_No (CEH site number)
  - Quad_No (1–4, with Combined_all option)
  - Vegetation_type (e.g., Fresh vegetation, Litter)
  - Vegetation_layer (Herb, Scrub)
  - C_total (carbon concentration as %)
  - N_total (nitrogen concentration as %)
  - Dry_Weight (g; weight of dried vegetation sample)
- Data provenance: two linked datasets cover soil chemistry and vegetation chemistry, both anchored to Site_No and, for vegetation, Quad_No to relate quadrats within each site.

## Habitat gradient and lookup
- A dedicated lookup table maps historical (1940) habitats to contemporary (2017) habitat classifications to define the proposed gradient categories. Examples:
  - Calcareous 1940 → Calcareous grassland (SSSI quality) 2017
  - Calcareous 1940 → Improved grassland 2017
  - Heathland 1940 → Coniferous plantation on heathland 2017
  - Heathland 1940 → Gorse high heathland 2017
  - Woodland 1940 → Broadleaf woodland 2017
  - Woodland 1940 → Ancient woodland (SSSI quality) 2017
- This lookup supports consistent gradient classification across habitat types and time periods.

## Quality assurance and data governance
- Consistent data collection by the same field ecologists to ensure reliability.
- Data checks performed for anomalies; standard QA procedures for soil analyses include blanks and standards; CRMs used to ensure analytical accuracy.
- Clear documentation of methods, units, and data column definitions to support reproducibility and reuse.
- Data provenance rooted in established archives:
  - Archival basis linked to the Dorset Environmental Records Centre (DERC) and the Good archive for baseline habitat information.
  - References to foundational sources (Good 1937; Horsfall 1981; Natural England inventories; Rose et al. 2000) to support habitat classification and gradient definitions.

## Data storage, access, and provenance
- Data are organized into two primary datasets with explicit field definitions, units, and site/quadrat identifiers.
- Provenance derives from a combination of historical baselines (Good) and contemporary field data collected in 2017–2018, stored with clear linkage to habitat gradients and site coordinates.
- Primary data sources and methodological details are documented, including laboratory analyses, QA practices, and data handling steps, to facilitate future data curation, discovery, and reuse.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125