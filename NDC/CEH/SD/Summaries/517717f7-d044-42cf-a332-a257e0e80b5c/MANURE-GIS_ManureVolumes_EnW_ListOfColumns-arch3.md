# Manure volumes by livestock type and land use for England and Wales

- Overview: A shapefile-based dataset that stores manure volumes by livestock type and land use across England and Wales. File name: MANURE-GIS_ManureVolumes_EnW.shp. Columns have name, description, and unit as described in the accompanying table.

- Data structure and scheme:
  - Uses prefixes to denote livestock sectors and manure type sources:
    - Beef (B_), Dairy (D_), Layers (L_), Pigs (P_), Sheep (S_), Broilers (Bro_)
  - Manure sources include Farmyard manure, Slurry, Direct excreta (and combinations thereof).
  - Destination land use types cover Grass, Arable Winter, Arable Spring, Arable (unspecified "-"), and others as indicated.
  - Units are either kilograms or litres; some fields designate a dash/presented as "-".

- Representative field patterns:
  - Beef: B_FYM_Gras, B_FYM_AraW, B_FYM_AraS, B_Slu_Gras, B_Slu_AraS, B_Slu_AraW, B_Grazing
  - Dairy: D_FYM_Gras, D_FYM_AraW, D_FYM_AraS, D_Slu_Gras, D_Slu_AraS, D_Slu_AraW, D_Grazing
  - Layers: L_FYM_Gras, L_FYM_AraW, L_FYM_AraS, L_FrRngGra
  - Broilers: Bro_FYM_Gras, Bro_FYM_AraW, Bro_FYM_AraS, Bro_FYM__1
  - Pigs: P_OutGrazi, P_FYM_Gras, P_FYM_AraW, P_FYM_AraS, P_Slu_Gras, P_Slu_AraS, P_Slu_AraW
  - Slurry-focused entries across multiple sectors: Slu_Gras, Slu_AraS, Slu_AraW
  - Sheep: S_FYM_Gras, S_FYM_AraW, S_FYM_AraS, S_Grazing
  - Special note for sheep grazing: S_Grazing (*) includes only the proportion of excreta deposited at grazing on managed grass; does not include rough grazing.

- Notable caveat:
  - S_Grazing field (*) excludes excreta deposited on rough grazing; the grazing data reflect only managed grassland deposition.

- Purpose and use for monitoring and policy:
  - Enables estimation of manure volumes by livestock type and land use, supporting environmental health monitoring, policy scrutiny, and decision-making.
  - Facilitates analysis of manure management practices and their environmental implications (e.g., nutrient flows, emissions, water quality).

- Metadata and governance considerations:
  - Metadata for each column (name, description, unit) is provided in the accompanying table, aiding data verification, transformation, and interpretation.
  - As with many datasets of this type, careful attention to data source provenance, transformation, and unit consistency is important for robust monitoring outputs.