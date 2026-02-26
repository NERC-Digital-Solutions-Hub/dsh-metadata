# Methods:

- This document describes 1x1 km data sets for Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2016–2018.
- AAE summarizes exceedances across multiple habitats within each grid square, accounting for exceedance amount, habitat area exceeded, and total acid- or nitrogen-sensitive habitat area.

## How AAE is calculated
- For each habitat: AE_keq year-1 = exceedance_keq ha-1 year-1 × exceeded habitat area (ha).
- Sum AE across all habitats in a 1x1 km grid square.
- AAE_keq ha-1 year-1 = total AE / total habitat area (ha) in the grid square.
- If deposition is below the critical load, AAE is set to zero.

## Habitats included
- Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed coniferous woodland, managed broadleaved woodland, unmanaged coniferous and broadleaved woodland.
- Nutrient nitrogen: the above habitats plus unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data provenance and references
- UK Methods Report (Hall et al, 2015) provides full description of methods for UK critical loads and exceedances.
- Critical loads and CBED deposition data available from the EIDC.
- Summary exceedance statistics published annually in the Trends Report (e.g., Hall et al., 2017) and as a UK Biodiversity Indicator (B5a).
- Freshwater exceedance data (1752 sites) are not included in the AAE calculations since they are catchment-based, not 1x1 km grid-based.

## Units and conversion
- AAE values are in keq ha-1 year-1.
- If deposition is below the critical load, AAE = 0.
- Nutrient nitrogen AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year).
- Acidity exceedance combines sulphur and nitrogen contributions and cannot be expressed in kg of S or N.

## Quality control and standards
- Data are based on methods agreed at national/international meetings under the UNECE CLRTAP.
- A detailed methods report (Hall et al., 2015) documents transparency of methods and data.

## Use, interpretation, and caveats
- National critical load maps are based on empirical/steady-state approaches; exceedance indicates potential long-term harm but not immediate damage.
- Habitat maps for acidity and nutrient nitrogen CLs may differ from other national habitat maps, affecting total mapped habitat areas.
- Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery can be slow and time-delayed.
- For uncertainties about habitat mapping and critical loads, refer to Hall et al. (2015) and the meta-data for the Critical Loads data.

## Data structure and access
- Two data files: acidhab_AAE_2016-18.csv (acidity) and nutnhab_AAE_2016-18.csv (nutrient nitrogen).
- Files cover different UK areas due to habitat distributions.
- Each record includes:
  - East_m, North_m: centre coordinates in OSGB metres.
  - Unique1km: unique 1x1 km grid square identifier (links acidity and nitrogen datasets where square data exist in both).
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1).
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
- Table 1 (in the document) describes the exact structure of the files.

## Notable sources and metadata
- Rowe et al. (2019) Trends Report 2019: trends in critical load and exceedances (Defra contract).
- Hall et al. (2015) Methods for calculation of critical loads and exceedances in the UK.
- Methods and data transparency linked to CEH/CLDM resources and EIDC catalog entries.