# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19

## Overview
- Two 1x1 km data sets quantify AAE of acidity and nutrient nitrogen critical loads due to deposition for 2017–2019.
- AAE summarises exceedances across multiple habitats within each grid square, enabling cross-habitat and spatial comparison.

## How AAE is calculated
- For each habitat: AE (keq year^-1) = exceedance (keq ha^-1 year^-1) × exceeded habitat area (ha).
- AAE (keq ha^-1 year^-1) = total AE ÷ total habitat area (ha) within the 1x1 km grid square.
- Habitats included:
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen: the above plus unmanaged beech, unmanaged oak, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data products and structure
- Files:
  - acidhab_AAE_2017-19.csv (acidity)
  - nutnhab_AAE_2017-19.csv (nutrient nitrogen)
- Common fields:
  - East_m: Easting of the grid square centre (OSGB metres)
  - North_m: Northing of the grid square centre (OSGB metres)
  - Unique1km: Unique identifier for the 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha^-1 year^-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Coverage differences reflect habitat distributions for acidity vs nitrogen.

## Units, conversion, and interpretation
- AAE units: keq ha^-1 year^-1.
- If deposition is below the critical load, AAE is set to zero.
- Nutrient nitrogen interpretation: 1 keq ha^-1 year^-1 = 14 kg N ha^-1 year^-1.
- Acidity AAE cannot be converted to kilograms of sulfur or nitrogen; it represents combined acidity load.

## Data quality, provenance, and references
- Methods align with UNECE CLRTAP processes; detailed documentation in Hall et al. (2015).
- Summary and trends context available in Rowe et al. (2019) Trends Report; UK Biodiversity Indicators (pollution pressure) reference.
- Uncertainty information available in the associated metadata and the Critical Loads data metadata.
- CBED deposition data referenced via the EIDC.

## Use, interpretation, and cautions
- Critical loads indicate long-term potential for harm under steady-state assumptions; exceedance does not imply immediate damage.
- Habitat distribution maps used for UK critical loads/exceedances may differ from other maps, affecting total habitat areas in acidity vs nitrogen calculations.
- Recovery after reducing deposition may involve long time lags for both chemical and biological recovery.
- Freshwater data (1752 sites) are not included in these AAE calculations because they are catchment-based, not grid-based.

## Practical notes for data integration and usage
- The Unique1km field enables linking acidity and nitrogen data for the same grid squares across the two files.
- Data suitable for cross-habitat impact analyses, spatial prioritisation, and benchmarking against national deployment of deposition controls.
- For further information, refer to the associated methods reports and data portals:
  - Hall et al. 2015 Methods for calculating critical loads and their exceedances in the UK
  - Trends Report 2019
  - EIDC and related CBED deposition data