# Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads by acid and nitrogen deposition for 2013-15

## Overview
- Presents 1x1 km gridded datasets of AAE for acidity and nutrient nitrogen critical loads due to deposition for 2013–2015.
- AAE summarizes exceedances across multiple habitats within each grid cell to indicate potential long-term environmental risk.
- Data are tied to UK habitat types and are used to assess policy relevance and environmental health over time.

## Data and Methods
- AAE is derived from AE for each habitat, where AE = exceedance (keq ha⁻¹ year⁻¹) × exceeded habitat area (ha).
- AAE per grid cell = total AE from all habitats / total habitat area in the 1x1 km cell.
- Grid reference: 1x1 km cells using OSGB coordinates (Easting/Northing in metres); each cell has a Unique1km identifier for linking acidity and nitrogen datasets.
- Two separate datasets:
  - Acidity (acidic habitats)
  - Nutrient nitrogen (nitrogen-sensitive habitats)

## Habitats Included
- Acidity AAE habitats:
  - Acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen AAE habitats:
  - All acidity habitats plus: unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Calculation Details
- AE (keq year⁻¹) = exceedance (keq ha⁻¹ year⁻¹) × habitat area exceeded (ha).
- AAE (keq ha⁻¹ year⁻¹) = total AE across habitats in a grid cell / total habitat area in that grid cell.
- Values below the critical load (no exceedance) are set to zero.
- For nutrient nitrogen, AAE can be converted to kg N ha⁻¹ year⁻¹ by multiplying by 14 (1 keq ha⁻¹ year⁻¹ = 14 kg N ha⁻¹ year⁻¹).
- Acidity exceedance reflects a combination of sulfur and nitrogen compounds and cannot be expressed as kg of S or N.

## Quality Control and Data Provenance
- Methods are based on national/international procedures from CLRTAP (UNECE).
- Detailed transparency reports exist (Hall et al. 2015) describing methods and data.
- Summary statistics and trend reporting are published (e.g., Hall et al. 2017) through the UK Trends Report and related biodiversity indicators.
- CBED deposition data are available from the Environmental Information Data Centre (EIDC).

## Use and Interpretation
- UK critical loads represent long-term steady-state thresholds; exceedance indicates potential long-term harm, not immediate damage.
- Habitat distribution maps used for critical loads/exceedances may differ from other habitat maps; data represent areas with available calculation data.
- Reducing deposition below critical loads does not guarantee immediate ecological recovery; chemical and biological recovery can have long time lags.
- Users should consult Hall et al. (2015) and related metadata for uncertainties and mapping caveats.

## Data Structure and Files
- Two files corresponding to each dataset:
  - acidhab_AAE_2013-15.csv (Acidity)
  - nutnhab_AAE_2013-15.csv (Nutrient nitrogen)
- Common fields:
  - East_m: Easting center of 1x1 km grid (OSGB metres)
  - North_m: Northing center of 1x1 km grid (OSGB metres)
  - Unique1km: Unique grid cell identifier
  - AAE_keq: Average Accumulated Exceedance (keq ha⁻¹ year⁻¹)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Note: Coverage differs between acidity and nitrogen datasets due to habitat distributions.

## References
- Hall, J., Smith, R., Dore, T. (2017). Trends Report 2017: Trends in critical load and critical level exceedances in the UK.
- Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK.