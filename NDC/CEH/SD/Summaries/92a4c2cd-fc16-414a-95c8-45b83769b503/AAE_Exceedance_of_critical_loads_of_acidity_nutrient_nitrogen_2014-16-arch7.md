# Average Accumulated Exceedance (AAE) data for acidity and nutrient nitrogen, 2014–16 (1x1 km grids)

## Overview
- Dedicated 1x1 km grid datasets representing the Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2014–16.
- AAE summarizes exceedances across habitats within each grid square, enabling spatial visualization of potential exceedance pressures.

## How AAE is calculated
- For each habitat:
  - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
- For each 1x1 km grid square:
  - AAE (keq ha-1 year-1) = total AE across habitats / total habitat area in the grid square
- Resulting AAE values are expressed as keq ha-1 year-1
- Nutrient nitrogen AAE values can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1)
- Acidity exceedance represents a combination of sulfur and nitrogen compounds and is reported in keq ha-1 year-1 only

## Habitats included
- Acidity (AAE data):
  - Acid grassland
  - Calcareous grassland
  - Dwarf shrub heath
  - Bog
  - Montane
  - Managed (productive) coniferous woodland
  - Managed (productive) broadleaved woodland
  - Unmanaged coniferous and broadleaved woodland
- Nutrient nitrogen (AAE data):
  - All acidity habitats listed above
  - Unmanaged beech woodland
  - Unmanaged oak woodland
  - Unmanaged Scots pine woodland
  - Other unmanaged woodland
  - Dune grassland
  - Saltmarsh

## Units and interpretation
- AAE units: keq ha-1 year-1
- If deposition is below the critical load, AAE is set to zero
- Important interpretation notes:
  - Exceedance indicates potential for harmful effects under long-term or steady-state assumptions; current exceedance does not imply immediate damage
  - Habitat distribution maps used for critical loads/exceedances may differ from other national habitat maps
  - Recovery after reducing deposition below the critical load can be slow (chemical and biological recovery timescales may be long)

## Data structure and files
- Two separate files (UK coverage differs by habitat distribution):
  - acidhab_AAE_2014-16.csv (AAE for acidity)
  - nutnhab_AAE_2014-16.csv (AAE for nutrient nitrogen)
- Common fields:
  - East_m: Easting of the grid square centre in OSGB grid metres
  - North_m: Northing of the grid square centre in OSGB grid metres
  - Unique1km: Unique identifier for each 1x1 km square (used to link acidity and nutrient nitrogen datasets when data exist for the same squares)
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: Geographic scope (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland)

## Coverage and data quality
- Data are based on methods agreed under the UNECE CLRTAP framework
- Comprehensive documentation exists (Hall et al. 2015; Hall et al. 2019) detailing methods, uncertainties, and data provenance
- Summary exceedance statistics and trends are published separately (e.g., Trends Report and UK Biodiversity Indicator)

## Use and interpretation for GIS specialists
- Use AAE values to map and compare spatial patterns of acidity and nitrogen exceedances across the UK at 1x1 km resolution
- Leverage the Unique1km field to join acidity and nitrogen layers where applicable
- Be mindful of potential mismatches with other habitat maps and the time-lag in ecological recovery
- When integrating with other datasets, account for differences in coverage and grid definitions

## References
- Hall, J.; Rowe, E.; Smith, R.; Dore, T.; Banin, L.F.; Levy, P.; Sawicka, K. 2019. Trends Report 2018: Trends in critical load and critical level exceedances in the UK. CEH report to Defra.
- Hall, J.; Curtis, C.; Dore, T.; Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. CEH report to Defra.