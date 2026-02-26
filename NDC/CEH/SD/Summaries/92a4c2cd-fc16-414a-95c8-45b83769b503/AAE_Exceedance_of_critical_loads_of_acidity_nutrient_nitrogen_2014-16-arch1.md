# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2014-16.

## Overview of AAE data sets
- 1x1 km grid-based data for Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads from deposition (2014–2016).
- AAE summarizes exceedances across habitats within each grid cell.
- Calculation steps:
  - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha) for each habitat.
  - AAE (keq ha-1 year-1) = total AE across habitats in cell ÷ total habitat area in the cell.
- Units:
  - AAE values are in keq ha-1 year-1.
  - For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity exceedance expresses as keq ha-1 year-1 (not separable into S or N).

## Habitats included
- Acidity (a): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
- Nutrient nitrogen (b): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech, unmanaged oak, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data sources and references
- UK Methods Report (Hall et al., 2015) provides full description of data and methods for UK critical loads and exceedances.
- Critical loads and CBED deposition data available from the EIDC.
- Summary exceedance statistics by habitat and country published annually in the Trends Report and UK Biodiversity Indicator (B5a), noting freshwater data are not included in these AAE datasets.

## Data structure and access
- Two data files:
  - acidhab_AAE_2014-16.csv (acidity)
  - nutnhab_AAE_2014-16.csv (nutrient nitrogen)
- Common fields:
  - East_m, North_m: centre coordinates of the 1x1 km square (OSGB grid, metres).
  - Unique1km: unique 1x1 km square identifier (linking acidity and nitrogen datasets where applicable).
  - AAE_keq: Average Accumulated Exceedance value (keq ha-1 year-1).
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
- Note: The two files have different UK coverage due to habitat distributions.

## Use and interpretation notes
- Critical loads maps are based on empirical/steady-state methods; exceedance indicates potential long-term harm, not necessarily current damage.
- Habitat distribution maps used for critical loads/exceedances may differ from other habitat maps, affecting total mapped habitat areas for acidity versus nitrogen.
- Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery may be very slow.
- For uncertainties in habitat mapping and critical loads, refer to Hall et al. (2015) and the metadata for the Critical Loads data; CBED deposition details available from EIDC.

## Quality control
- Data reflect methods agreed at national/international meetings under the UNECE CLRTAP.
- A detailed transparency-focused report is Hall et al. (2015).

## Related information and access
- 1752 freshwater exceedance statistics exist (upland lakes/streams); not included in the AAE datasets because freshwater data use catchment areas, not 1x1 km grid squares.
- For more information on CBED deposition and metadata, see the EIDC and associated references.
- Summary and metadata available via linked references (Hall et al. 2015; Hall et al. 2019 Trends Report).