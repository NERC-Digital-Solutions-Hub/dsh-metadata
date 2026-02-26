# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2014-16

## Overview
- Presents 1x1 km grid-based AAE data for acidity and nutrient nitrogen across the UK for 2014–2016.
- AAE summarises exceedances of habitat-specific critical loads due to deposition, enabling comparison across grid squares and habitats.
- Covers selected habitats sensitive to acidification (acidity AAE) and eutrophication (nitrogen AAE).

## How AAE is calculated
- For each habitat within a grid square:
  - AE (keq year^-1) = exceedance (keq ha^-1 year^-1) × exceeded habitat area (ha).
- AAE for a grid square = total AE across habitats ÷ total habitat area in the square.
- Values are expressed in keq ha^-1 year^-1.
- If deposition is below the critical load, AAE is set to zero.
- For nutrient nitrogen, AAE can be converted to kg N ha^-1 year^-1 by multiplying by 14 (1 keq ha^-1 year^-1 = 14 kg N ha^-1 year).
- Acidity exceedance represents a combination of sulphur and nitrogen compounds and is reported as keq ha^-1 year^-1 only.

## Habitats included
- Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen: same habitats plus unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, and saltmarsh.

## Data structure and accessibility
- Two separate files:
  - acidhab_AAE_2014-16.csv (AAE for acidity)
  - nutnhab_AAE_2014-16.csv (AAE for nutrient nitrogen)
- Common fields:
  - East_m and North_m: centre coordinates in OSGB grid metres
  - Unique1km: unique 1x1 km square identifier (enables linking across the two datasets)
  - AAE_keq: Average Accumulated Exceedance (keq ha^-1 year^-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Coverage differs between datasets due to habitat distributions.

## Data quality, provenance, and uncertainty
- Based on methods agreed at national/international levels under the UNECE CLRTAP; transparent methodology documented.
- Detailed method description available in Hall et al. 2015; meta-data for critical loads data available via CEH catalog.
- Summary exceedance statistics by habitat and country published annually (e.g., Hall et al., 2017) and in UK Biodiversity Indicators.
- Freshwater data (1752 sites) are not included in these AAE calculations because they are based on catchment areas, not 1x1 km grid squares, and do not represent all UK freshwaters.
- Acknowledges uncertainties in habitat mapping and critical loads; see Hall et al. 2015 and linked metadata.

## Use, interpretation, and caveats for decision-making
- Critical loads reflect long-term, steady-state conditions; exceedance indicates potential for harmful effects but does not imply immediate damage.
- Habitat distribution maps used for critical loads/exceedances may differ from other habitat maps, potentially affecting total habitat areas in acidity vs. nitrogen datasets.
- Rebound or recovery after reducing deposition below critical loads may take long; chemical and biological recovery can lag.
- Users should consult the cited methods reports and metadata for uncertainty considerations.

## Related data and references
- Data derived under UK CLRTAP framework; linked to CBED deposition data (EIDC).
- References:
  - Hall, J., Rowe, E., Smith, R., Dore, T., Banin, L.F., Levy, P., Sawicka, K. 2019. Trends Report 2018: Trends in critical load and critical level exceedances in the UK.
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK.
- Data location and further metadata:
  - UK Methods Report and trends data: CEH and Defra-supported portals
  - Critical loads metadata: CEH catalog (e.g., metadata documents and data provenance)