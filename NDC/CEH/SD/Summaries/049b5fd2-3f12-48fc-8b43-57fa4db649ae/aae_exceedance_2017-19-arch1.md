# 1x1 km AAE data sets for acidity and nutrient nitrogen critical loads, 2017-19

- The data provide 1x1 km grid summaries of Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen, reflecting critical-load exceedances due to acid and nitrogen deposition for 2017–2019.
- AAE is a grid-level summary across habitats within each 1x1 km cell, enabling comparison across space and linking acidity and nitrogen contexts.

## How AAE is calculated

- For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- AAE (keq ha-1 year-1) = total AE across habitats in the 1x1 km grid square ÷ total habitat area (ha) in that grid.
- Units: AAE is expressed in keq ha-1 year-1.
- Conversion: for nutrient nitrogen, 1 keq ha-1 year-1 = 14 kg N ha-1 year. Acidity AAE remains in keq ha-1 year-1 and cannot be split into S or N components.

## Habitats included

- Acidity (for AAE_acidity): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen (for AAE_nitrogen): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.
- Note: Freshwater data (1752 sites) are not included in the AAE calculations because they are catchment-based and use different area definitions.

## Data quality and interpretation

- Methods are aligned with UNECE CLRTAP agreement; detailed transparency in Hall et al. (2015) and related documentation.
- Summary data and trends are also published in UK Trends Reports and biodiversity indicators; freshwater data are reported separately from the grid-based AAE.
- Exceedance above the critical load indicates potential for harm at steady-state or long-term, not necessarily immediate damage.
- Habitat distribution maps used for critical loads/exceedances may differ from other habitat maps; calculated habitat areas are restricted to areas with data to derive critical loads.
- Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery can have long time lags.

## Data structure

- Two files exist: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen). The UK coverage differs due to habitat distributions.
- Key fields:
  - East_m, North_m: Easting/Northing for the centre of the 1x1 km square (OSGB grid, metres).
  - Unique1km: Unique identifier for each 1x1 km square, enabling linkage between acidity and nitrogen datasets.
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1).
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
- The 1x1 km grid allows cross-dataset linking for squares with data in both acidity and nitrogen files.