# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

## Overview
- Dataset focuses on carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland, and woodland sites in Dorset, collected in 2017–2018 as part of the Dorset Valuing Nature Project field component.
- Aims to establish baseline conditions and explore how ecosystem services change with habitat condition using map-based, geospatial data products.

## Experimental design
- Builds on a historic Dorset botanical survey by Professor Ronald Good (1931–1939); archive available via the Dorset Environmental Records Centre.
- Subsamples Good-identified calcareous grassland, heathland, and woodland sites from the 1930s to form the survey set.
- Site selection targets a gradient of habitat condition:
  - Calcareous: improved grassland; restoration; calcareous grassland (SSSI quality)
  - Heathland: coniferous plantation on heathland; gorse high heathland; heathland (SSSI quality)
  - Woodland: coniferous plantation; broadleaf woodland; ancient woodland (SSSI quality)
- 13 calcareous grassland, 13 heathland, and 12 woodland sites selected to cover this gradient; some sites linked to SSSIs and priority habitat assessments.
- Mapping of current habitat types uses multiple data sources:
  - UK Land Cover Map 2007
  - Natural England Priority Habitat Inventory (2015)
  - Sites of Special Scientific Interest (SSSIs) data (2014)
  - Horsfall (1981) and Dorset Heathland Survey (Rose et al., 2000)
  - Higher Level Stewardship schemes

## Collection methods
- Sampling grid: random 50m x 50m plots within the original Good survey area, assigned in ArcGIS prior to fieldwork.
- Soil sampling:
  - Within each plot: four 15 cm deep soil cores.
  - Cores processed as air-dried, sieved to 2 mm, ball milled; analysed by Vario EL instrument (oxidative combustion with thermal conductivity detection).
  - Calibration with standards; QA includes blanks and certified reference materials (CRMs).
  - Limits of detection: ~2.0% C, ~0.12% N.
  - Bulk density measured from two additional soil samples; cores oven-dried and used to compute density.
- Biomass sampling:
  - Five 50 cm quadrats per plot; all vegetation layers collected, identified (shrubs to species level), dried, and weighed.
  - Dried vegetation sent to UKCEH for analysis following soil methods.
- Data integrity:
  - Field data collected by experienced ecologists; consistent data entry and anomaly checks.

## Data structure and fields
- DVNP_Soil_Chemistry_data: includes site identifiers (Site_No), carbon (% C_total), nitrogen (% N_total), bulk density (Bulk_Density), and related numeric categories.
- DVNP_VegetationChemistry_data: includes Site_No, Quad_No (1–4 or Combined_all), Vegetation_type (Fresh, Litter), Vegetation_layer (Herb, Scrub), carbon (% C_total), nitrogen (% N_total), and Dry_Weight (g).
- Units:
  - Carbon and nitrogen concentrations are given as percentages.
  - Bulk density in g/cm3; Dry_Weight in grams.

## Habitat gradient lookup
- A lookup table defines the gradient category by mapping historical (1940) habitat to current (2017) habitat:
  - Examples: Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland
  - Heathland variants: Coniferous plantation on heathland, Gorse high heathland, Heathland (SSSI quality)
  - Woodland variants: Broadleaf woodland, Coniferous plantation, Ancient woodland (SSSI quality)
- This lookup enables spatially explicit gradient classification for GIS analyses.

## Data quality, provenance, and usage considerations
- Data are derived from multiple sources and historical context, integrated through a standardized sampling design (50m plots) and consistent field teams to ensure comparability.
- Some potential limitations include reliance on historic habitat classifications and the need to harmonize data from varied sources; gradient categorization helps contextualize spatial analyses.

## References
- Good, R. (1937). An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116.
- Horsfall, A. (1981). A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3. Dorset Proc 103.
- Natural England (2014). Sites of Special Scientific Interest and historical monuments.
- Natural England (2015). Priority Habitats Inventory version 2.1.
- Rose, R.J., Webb, N.R., Clarke, R.T., Traynor, C.H. (2000). Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125.