# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2015-17

## Overview
- Datasets quantify exceedances of UK critical loads for acidity and nutrient nitrogen using Average Accumulated Exceedance (AAE) across 1x1 km grid squares for 2015–2017.
- AAE summarises exceedances by habitat, grid square area, and total habitat area within each grid square.
- AAE is expressed in keq ha^-1 year^-1; for nutrient nitrogen, AAE can be converted to kg N ha^-1 year^-1 (×14).

## Data content and scope
- Two separate files:
  - acidhab_AAE_2015-17.csv (AAE for acidity)
  - nutnhab_AAE_2015-17.csv (AAE for nutrient nitrogen)
- Habitat lists differ between acidity and nitrogen datasets.
- Coverage is 1x1 km grid squares; includes a Unique1km identifier to link acidity and nitrogen data where both exist.
- Country coding included (CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland).

## Data structure and fields (Table 1 structure described)
- East_m: Easting (metres, OSGB grid) for the centre of the 1x1 km square
- North_m: Northing (metres, OSGB grid) for the centre of the 1x1 km square
- Unique1km: Unique identifier for the 1x1 km square
- AAE_keq: Average Accumulated Exceedance (keq ha^-1 year^-1)
- CountryID: Geographic grouping (England, Wales, Scotland, Northern Ireland)

## Calculation method (how AAE is derived)
- Calculate Accumulated Exceedance (AE) for each habitat:
  AE (keq year^-1) = exceedance (keq ha^-1 year^-1) × exceeded habitat area (ha)
- Sum AE across all habitats within a grid square
- AAE = total AE / total habitat area in the grid square
- Note: An AAE value of zero is used when deposition is below the critical load (i.e., no exceedance)
- For nitrogen: AAE can be converted to kg N ha^-1 year^-1 by multiplying by 14 (1 keq ha^-1 year^-1 = 14 kg N ha^-1 year)

## Habitats included
- Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland
- Nutrient nitrogen: same as acidity plus unmanaged beech, unmanaged oak, unmanaged Scots pine woodlands, other unmanaged woodland, dune grassland, saltmarsh

## Quality control and provenance
- Methods anchored in UNECE CLRTAP processes; transparency provided via detailed reporting
- Key references: Hall et al. 2015 (Methods for calculation of critical loads and their exceedances in the UK) and the 2019 Trends Report
- Data provenance and uncertainties addressed in the linked metadata and CLRTAP documentation
- Freshwater data (1752 sites) are not included in the AAE calculations since they are based on catchments, not 1x1 km grid squares

## Use, interpretation, and caveats
- Critical load exceedance indicates potential long-term harm under steady-state assumptions; it does not imply immediate damage
- Habitat distribution maps and calculation areas reflect data availability and may differ from other habitat maps
- Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery can be slow
- Uncertainties and methodological specifics are documented in Hall et al. (2015) and accompanying meta-data

## Access and references
- Trends reports and related documentation:
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK
  - Rowe et al. 2019. Trends Report 2019: Trends in critical load and critical level exceedances in the UK
- Data availability and deposition details:
  - UK critical loads, CBED deposition data (EIDC)
- For metadata and data structure details, see the accompanying data catalog entries and the referenced publications

## Data governance considerations for Data Stewards
- Ensure complete, standardized metadata (habitat definitions, grid alignment, units, calculation steps)
- Maintain data provenance links to CLRTAP methods and UK reports; clearly document any processing or transformations
- Manage data sharing, access controls, and versioning; note any embargoes or licensing constraints
- Plan for updates or reprocessing as new CLRTAP methods or UK datasets are released; document changes and maintain linkage via Unique1km identifiers
- Include clear usage notes about interpretation, uncertainties, and alignment with other habitat maps to support proper discovery and reuse