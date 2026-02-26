# Average Accumulated Exceedance (AAE) data sets for acidity and nutrient nitrogen, 2013-15

## Overview
- 1x1 km gridded data sets that summarize exceedances of acid and nitrogen deposition above their respective critical loads for multiple habitats.
- Covers AAE for acidity and for nutrient nitrogen across the UK for the years 2013–2015.
- Aimed at informing monitoring, assessment, and decision-making on environmental health and policy effectiveness.

## What the data represent
- AAE is derived from:
  - Exceedance (keq ha-1 year-1) for each habitat
  - Exceeded habitat area (ha)
  - Total habitat area within each 1x1 km grid square
- Calculation sequence:
  - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
  - AAE (keq ha-1 year-1) = total AE across habitats in the grid square / total habitat area in the grid square
- Habitats included:
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous and broadleaved woodland
  - Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh
- Species and freshwater data:
  - The 1752 freshwater data (based on catchments) are not included in these AAE calculations, as they use different geographic units (catchments) and data do not cover all UK freshwaters in the grid-based AAE.

## Calculation details and units
- Units: AAE values are expressed in keq ha-1 year-1. When converting to kilograms of nitrogen, multiply by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1). Acidity exceedance combines sulfur and nitrogen compounds and cannot be split into S or N.
- Zeros: If deposition is below the critical load, AAE is set to zero.
- Data provenance and methods: Based on methods agreed at national/international meetings under the UNECE CLRTAP; detailed methodological transparency is provided in Hall et al. (2015) and related documents.

## Data structure and access
- Two separate files:
  - acidhab_AAE_2013-15.csv for acidity
  - nutnhab_AAE_2013-15.csv for nutrient nitrogen
- Common fields and grid linkage:
  - East_m: Easting for centre of the 1x1 km square (OSGB grid, metres)
  - North_m: Northing for centre of the 1x1 km square (OSGB grid, metres)
  - Unique1km: Unique identifier for each 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Linking capability: Unique1km enables linking acidity and nutrient nitrogen data for the same grid squares where applicable.

## Quality control, provenance and uncertainty
- Methods and data follow internationally agreed guidelines (CLRTAP).
- Hall et al. (2015) provides a detailed Methods Report for calculating UK critical loads and exceedances; Hall et al. (2017) provides Trends Report updates.
- Metadata and uncertainties are documented in the accompanying meta-data for Critical Loads data and related references.
- Data users should be aware that habitat maps and areas may differ from other national maps, potentially affecting total habitat areas across acidity and nutrient nitrogen datasets.

## Use and interpretation for monitoring frameworks
- Exceedance indicates potential for harmful effects under long-term steady-state assumptions; observed exceedances do not imply immediate damage.
- Recovery after reducing deposition below the critical load may involve long chemical and biological lag times, especially for sensitive ecosystems.
- The datasets support national monitoring and trend reporting but should be interpreted with awareness of:
  - Differences between grid-based habitat areas and other habitat distribution maps
  - Data availability limited to areas with data for critical loads calculation
  - Exclusion of freshwater data in these AAE calculations
- Outputs are suitable for integration into dashboards, reports, and governance processes that require spatially explicit monitoring indicators of acidification and eutrophication pressures.

## References
- Hall, J., Smith, R., Dore, T. (2017). Trends Report 2017: Trends in critical load and critical level exceedances in the UK. Report to Defra.
- Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra.
- Additional information on CBED deposition and critical loads data available from the EIDC and related metadata.