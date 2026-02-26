# AAE data for acidity and nutrient nitrogen, 2014-16

## Overview
- Two data files (one for acidity, one for nutrient nitrogen) covering 1x1 km grid squares across the UK.
- Values represent Average Accumulated Exceedance (AAE) of critical loads due to acid and nitrogen deposition for 2014–2016.
- AAE is expressed in keq ha-1 year-1; below-CRL values are set to zero.
- For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 y-1 = 14 kg N ha-1 y-1).
- Data are aligned with habitat data and are based on methods under the UNECE CLRTAP framework; not all freshwater data are included in these AAE datasets.

## What AAE measures and how it is calculated
- AE (exceedance) for each habitat: AE = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- AAE per grid cell: sum AE for all habitats within the 1x1 km square, divided by total habitat area in that square.
- Acidity exceedance combines sulfur and nitrogen contributions; reported as keq ha-1 year-1 only.
- If a grid square’s deposition is below the critical load, the AAE is zero for that square.

## Habitats included
- Acidity (for AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen (for AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data structure and files
- acidhab_AAE_2014-16.csv: AAE for acidity.
- nutnhab_AAE_2014-16.csv: AAE for nutrient nitrogen.
- Grid reference: OSGB 1x1 km grid with:
  - East_m: Easting for centre of the square (metres)
  - North_m: Northing for centre of the square (metres)
  - Unique1km: unique identifier for each 1x1 km square (linking datasets)
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland

## Quality control, uncertainties, and interpretation
- Data are produced using methods agreed at national/international CLRTAP workshops; transparency is documented in Hall et al. (2015).
- Detailed uncertainty and metadata are available alongside the critical loads data (Hall et al., 2015) and via the CEH data catalog.
- Summary exceedance statistics by habitat and country are published annually in the Trends Report (e.g., Hall et al., 2017) and as UK Biodiversity Indicator B5a; these statistics are based on 1752 UK freshwater sites but are not included in the AAE datasets here because freshwater data are catchment-based, not grid-based.
- Habitat maps and areas used for critical loads/exceedances may differ from other national habitat distributions, potentially affecting total habitat areas mapped for acidity and nitrogen.

## Use and interpretation guidance
- Critical loads/maps reflect long-term steady-state assumptions; exceeding a critical load indicates potential for harmful effects, not immediate damage.
- The habitat distribution maps used for critical loads/exceedances reflect only areas with available data for calculation; they may differ from other habitat distributions.
- Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery can have long time lags.
- Outputs are suitable for linking with other datasets via the Unique1km key to enable cross-dataset analyses at 1x1 km resolution.

## Access, references, and related information
- UK Trends Report 2018 and related methods: Hall et al. 2019; Trends in critical load and exceedances in the UK.
- Methods for calculating critical loads: Hall et al. 2015.
- Additional data and deposition information: CBED deposition (EIDC) and associated metadata.
- Tables and file structures are described in the data documentation; Unit conversions and interpretation notes are included within the dataset description.