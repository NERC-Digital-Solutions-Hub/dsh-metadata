# Methods

- These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2015-17.

- AAE summarises exceedances across multiple habitats within a grid square by combining habitat-specific exceedance, exceeded habitat area, and total habitat area in the square.

- Calculation steps:
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
  - AAE (keq ha-1 year-1) = total AE across habitats in the square ÷ total habitat area (ha) in that square
  - For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1)
  - Acidity exceedance represents a combination of sulphur and nitrogen compounds and is expressed only as keq ha-1 year-1

## Habitats included

- Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland

- Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh

## Data sources and references

- UK Methods Report and CLRTAP-aligned methodologies underpinning the data (Hall et al., 2015; Rowe et al., 2019 Trends Report)

- Summary exceedance statistics and UK Biodiversity Indicator information available from national sources; freshwater data excluded from the AAE calculation due to different spatial foundations

## Data structure and files

- Files:
  - acidhab_AAE_2015-17.csv (AAE for acidity)
  - nutnhab_AAE_2015-17.csv (AAE for nutrient nitrogen)

- Shared data fields:
  - East_m, North_m: centre coordinates of the 1x1 km grid square (OSGB grid)
  - Unique1km: unique identifier for each 1x1 km square (enables linking acidity and nitrogen datasets)
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland

- Differences in UK coverage between acidity and nitrogen reflect habitat distributions

## Quality control and uncertainty

- Methods agreed at national/international meetings under CLRTAP; QA detailed in Hall et al. (2015)

- Uncertainties and habitat mapping considerations described in Hall et al. (2015) and dataset metadata

## Use and interpretation

- Exceedance indicates potential long-term harm under steady-state assumptions; current damage may not be present

- Habitat maps used for CRL can differ from other habitat maps, affecting total habitat areas used in calculations

- Reducing deposition below the critical load may not yield immediate ecological recovery; chemical and biological recovery can take long

- CBED deposition and related data are described by EIDC

## Additional notes

- 2015-17 coverage; fieldwork/lab instrumentation and calibration steps are not applicable to these data

- For more information on CBED deposition and data provenance, refer to EIDC and associated metadata