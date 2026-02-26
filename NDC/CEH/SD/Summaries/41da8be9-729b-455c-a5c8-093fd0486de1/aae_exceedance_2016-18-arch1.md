# AAE data for acidity and nutrient nitrogen 2016-18

## What the data are
- 1x1 km gridded datasets summarising Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2016–2018.
- AAE aggregates exceedance across habitats within each grid cell and normalises by total habitat area in the cell.
- Two separate datasets cover: (a) acidity and (b) nutrient nitrogen.

## How AAE is calculated
- For each habitat, compute Accumulated Exceedance (AE):
  - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- Sum AE across all habitats within a 1x1 km grid square.
- AAE (keq ha-1 year-1) = total AE / total habitat area in the grid square.
- Where deposition is below the critical load, AAE is set to zero.
- For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- Acidity AAE represents a mix of sulphur and nitrogen compounds and is expressed only as keq ha-1 year-1.

## Habitats included
- Acidity (AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen (AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data structure and files
- Two files (different UK coverage due to habitat distributions):
  - acidhab_AAE_2016-18.csv (acidity)
  - nutnhab_AAE_2016-18.csv (nutrient nitrogen)
- Key columns (examples):
  - East_m: Easting for centre of 1x1 km square (metres OSGB)
  - North_m: Northing for centre of 1x1 km square (metres OSGB)
  - Unique1km: unique identifier for the 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- The Unique1km code enables linking acidity and nitrogen datasets for the same grid squares.

## Data quality, interpretation, and limitations
- Basis: methods agreed under the UNECE CLRTAP; detailed methodology documented in Hall et al. (2015).
- Use of critical loads: exceedance indicates potential long-term harm under steady-state assumptions; does not imply current damage.
- Habitat maps and habitat areas used for critical loads/exceedances may differ from other habitat distribution maps, affecting total habitat areas.
- Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery can be slow.
- Freshwater data (about 1752 UK freshwater sites) are not included in the AAE calculations because they are catchment-based, not grid-based.
- Uncertainties exist in habitat mapping and underlying critical loads; see Hall et al. (2015) and related metadata for details.

## Related data, metadata, and access
- Trends in critical load and critical level exceedances in the UK (Trends Report 2019) and associated publications provide summary statistics by habitat and country.
- UK Methods Report (Hall et al., 2015) details the methods for calculating critical loads and exceedances.
- CBED deposition data and related materials are available through the Environment and Climate Change datasets (EIDC).

## Practical notes for analysts
- The two datasets can be combined via Unique1km to compare acidity and nitrogen exceedances for the same grid cells.
- Applicable to analyses linking deposition to habitat-level exceedances, with attention to the long timescales for chemical and biological recovery.
- When using, reference the underlying methodology (CLRTAP-based) and the metadata for uncertainties and data scope.