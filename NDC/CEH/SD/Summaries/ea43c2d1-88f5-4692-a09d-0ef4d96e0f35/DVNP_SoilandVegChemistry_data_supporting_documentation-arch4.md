# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

## Purpose and context
- Documents the dataset from the Dorset Valuing Nature Project field component, measuring soil carbon (C) and nitrogen (N) content and vegetation chemistry across calcareous grassland, heathland, and woodland sites in Dorset during 2017–2018.
- Builds a baseline using Good’s historical Dorset botanical survey (1931–1939) to compare ecosystem services against habitat condition.
- Integrates multiple data sources to identify current habitat types and select survey sites across a condition gradient.

## Experimental design
- Good, a renowned Dorset botanist, provided a historical baseline; his site identifications (calcareous grassland, heathland, woodland) are used to guide current sampling.
- Subsampling of Good’s 1930s sites employed various data sources to identify current habitat types: UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), SSSIs (2014), Horsfall (1981), Dorset Heathland survey (Rose et al., 2000), and Higher Level Stewardship data.
- Site selection: 13 calcareous grassland, 13 heathland, 12 woodland sites, chosen to represent a gradient of degradation/condition.
- Gradient categories tie 1940 habitat classifications to 2017 habitat outcomes, including transitions such as improved grassland, restoring calcareous grassland, coniferous plantations on heathland, gorse-dominated heath, ancient woodland, and SSSI-quality designations.
- Note: some 1940 woodland categories map to 2017 broadleaf or coniferous plantations; ancient woodland mappings are included where applicable.

## Collection methods
- Plots: 50 m x 50 m sample squares randomly assigned within the original Good survey area using ArcGIS.
- Soil samples: four 15 cm deep cores per square; two air-dried and sieved (2 mm), then ball-milled and analyzed by Vario EL; dried and combusted with oxidative method; calibration with standards and CRMs; QA includes blanks and multiple CRM concentrations; LOD: 2.0% C, 0.12% N; results expressed as percent and mg/L.
- Bulk density: measured from two additional soil samples; cores oven-dried (110°C, 48 h); density calculated from weight, volume, and rock/plant material exclusions using a specified formula.
- Biomass samples: vegetation collected from five 50 cm quadrats per square, across all layers; samples dried and weighed; shrub layer identified to species; analysis performed by UK CEH/Lancaster Laboratories following soil procedures; field ecologists conduct data collection consistently; data checked for anomalies.

## Data structure and metadata
- DVNP_Soil_Chemistry_data
  - Site_No (CEH site identifier, 1–39)
  - C_total (carbon concentration %, numeric category)
  - N_total (nitrogen concentration %, numeric category)
  - Bulk_Density (soil bulk density, g cm-3)
- DVNP_VegetationChemistry_data
  - Site_No (CEH site number)
  - Quad_No (1–4; with Additional_all option)
  - Vegetation_type (text; e.g., Fresh vegetation, Litter)
  - Vegetation_layer (Herb, Scrub, etc.)
  - C_total (carbon concentration %, numeric)
  - N_total (nitrogen concentration %, numeric)
  - Dry_Weight (weight of dried vegetation sample, g)
- Data are organized to support cross-site comparisons and gradient analyses across soil and vegetation chemistry.

## Habitat gradient mapping
- A lookup table translates 1940 habitat classifications to 2017 habitat categories to define gradient categories. Examples include:
  - Calcareous 1940 → Calcareous grassland (SSSI quality) 2017
  - Heathland 1940 → Coniferous plantation on heathland 2017
  - Woodland 1940 → Broadleaf woodland or Ancient woodland (SSSI quality) 2017
- The table links historical habitat identity with current habitat status to enable gradient-based analyses of ecosystem change.

## Data quality, provenance and governance
- Consistent data collection by the same experienced field ecologists across sites to ensure reliability.
- Rigorous QA processes: blanks, standards, CRMs, and calibration checks for soil chemistry analyses; LODs documented.
- Data lineage documented from original Good survey baseline through contemporary fieldwork (2017–2018) and the integration of multiple historical and contemporary data sources.
- Metadata includes definitions of units, data columns, and gradient categorizations to support reuse and interoperability.

## Access and references
- The Dorset Environmental Records Centre hosts the archive of the Good survey data and related materials.
- References include Good (1937), Horsfall (1981), Natural England (2014, 2015), and Rose et al. (2000), detailing historical context, habitat inventories, and change in heathlands and woodlands.