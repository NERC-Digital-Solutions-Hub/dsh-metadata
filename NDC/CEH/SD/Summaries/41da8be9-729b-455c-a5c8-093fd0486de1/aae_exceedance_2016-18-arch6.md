# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2016-18

## Overview
- Two 1x1 km grid-based data sets presenting the Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen, based on deposition exceeding habitat-specific critical loads (2016–2018).
- AAE summarizes exceedances across habitats within each grid square to enable broad-scale assessment of potential ecosystem risk.

## How AAE is calculated
- For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- AAE (keq ha-1 year-1) = total AE across habitats in a 1x1 km grid square ÷ total habitat area (ha) in that square.
- If deposition is below the critical load, AAE = 0.
- For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1). Acidity AAE remains in keq ha-1 year-1.

## Habitats included
- Acidity AAE: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen AAE: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data sources and context
- UK Methods Report (Hall et al., 2015) provides full description of methods for calculating UK critical loads and exceedances and related data.
- Critical loads and CBED deposition data available from the EIDC.
- Summary exceedance statistics by habitat and country published annually in the Trends Report (e.g., Hall et al., 2017) and in the UK Biodiversity Indicator (B5a). Freshwater exceedances (1752 sites) are reported separately and are not included in the AAE datasets because freshwater data are catchment-based, not 1x1 km grid-based.

## Use and interpretation
- Critical loads maps are based on empirical/steady-state methods; exceedance indicates potential long-term risk, not immediate damage.
- Habitat maps and areas used for critical loads/exceedances are limited to areas with data; may differ from other habitat distribution maps, affecting total habitat areas used in calculations.
- Reducing deposition below critical loads does not imply immediate ecological recovery; both chemical and biological recovery can have long time lags.

## Data structure and files
- Two data files (UK coverage differs by dataset due to habitat distributions):
  - acidity: acidhab_AAE_2016-18.csv
  - nutrient nitrogen: nutnhab_AAE_2016-18.csv
- Each file includes:
  - East_m: Easting for centre of 1x1 km square (OSGB grid, metres)
  - North_m: Northing for centre of 1x1 km square (OSGB grid, metres)
  - Unique1km: Unique identifier for 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland

## Data quality and limitations
- Based on methods agreed at UNECE CLRTAP; detailed methodology documented in Hall et al. (2015).
- Uncertainties and metadata for habitat mapping and critical loads are described in related publications and data catalog metadata.

## References
- Rowe E, Sawicka K, Mitchell Z, Smith R, Dore T, Banin LF & Levy P (2019) Trends Report 2019: Trends in critical load and critical level exceedances in the UK.
- Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK.