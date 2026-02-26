# DATA STRUCTURE

## Overview
- A shapefile containing manure volumes by livestock type and land use for England and Wales.
- File name: MANURE-GIS_ManureVolumes_EnW.shp.
- Columns encode: livestock sector, manure housing type, destination land-use type, and measurement units.

## File details and field structure
- The dataset includes fields prefixed by livestock sector and housing type, e.g.:
  - Beef: B_FYM_Gras, B_FYM_AraW, B_FYM_AraS, B_Slu_Gras, B_Slu_AraS, B_Slu_AraW, B_Grazing.
  - Dairy: D_FYM_Gras, D_FYM_AraW, D_FYM_AraS, D_Slu_Gras, D_Slu_AraS, D_Slu_AraW, D_Grazing.
  - Pigs: P_OutGrazi, P_FYM_Gras, P_FYM_AraW, P_FYM_AraS, P_Slu_Gras, P_Slu_AraS, P_Slu_AraW.
  - Sheep: S_FYM_Gras, S_FYM_AraW, S_FYM_AraS, S_Grazing (*).
  - Layers: L_FYM_Gras, L_FYM_AraW, L_FYM_AraS, L_FrRngGra.
  - Broilers (Bro_): Bro_FYM_Gras, Bro_FYM_AraW, Bro_FYM_AraS, Bro_FYM__1.
- Each field maps:
  - Source livestock sector
  - Manure/housing type (Farmyard manure, Slurry, Direct excreta)
  - Destination land-use type (Grass, Arable Winter, Arable Spring, etc.; some fields use "-")
  - Units (kilograms for solids; litres for liquids)

## Field naming conventions and examples
- Beef: B_FYM_Gras (Beef, Farmyard manure, Grass, kg); B_Slu_Gras (Beef, Slurry, Grass, litres); B_Grazing (Beef, Direct excreta, -, kg).
- Dairy: D_FYM_Gras, D_Slu_AraW, D_Grazing, etc.
- Pigs: P_FYM_Gras, P_Slu_AraW, P_OutGrazi, etc.
- Sheep: S_FYM_Gras, S_FYM_AraW, S_Grazing (*) — note on grazing data below.
- Layers: L_FYM_Gras, L_FYM_AraW, L_FrRngGra, etc.
- Broilers: Bro_FYM_Gras, Bro_FYM_AraW, Bro_FYM_AraS, Bro_FYM__1, etc.

## Special notes
- S_Grazing (*) indicates that only the proportion of sheep excreta deposited at grazing on managed grassland is included; excreta on rough grazing is not included.

## Data usage and GIS considerations
- The dataset is designed for map-based visualization of manure volumes by livestock type and land use.
- May require data cleaning or standardization due to numerous fields, varying land-use categories, and mixed units.
- Pay attention to unit consistency (kg for solids vs. litres for liquids) and to fields where destination land use is "-".