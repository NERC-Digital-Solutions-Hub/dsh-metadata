# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2014-16.

## Overview
- Provides 1x1 km grid-based AAE measures for acidity and nutrient nitrogen exceedances relative to their respective critical loads (2014–2016).
- Designed to support environmental monitoring, policy evaluation, and future decision-making.

## What AAE represents and how it is calculated
- AAE is derived by aggregating exceedances across habitats within each 1x1 km grid square.
- For each habitat: AE = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- AAE = total AE across habitats in the grid square ÷ total habitat area in the grid square (keq ha-1 year-1).
- Acidity and nutrient nitrogen AAEs are expressed in keq ha-1 year-1.
- If deposition is below the critical load, AAE is set to zero.
- For nutrient nitrogen, AAE values can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- Acidity exceedance combines sulfur and nitrogen contributions and cannot be converted to kg of S or N.

## Habitats included
- Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen: acids grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data structure and files
- Two AAE data files (UK coverage differs by habitat type):
  - acidhab_AAE_2014-16.csv (AAE for acidity)
  - nutnhab_AAE_2014-16.csv (AAE for nutrient nitrogen)
- Each row includes:
  - East_m, North_m: centre coordinates in OSGB grid metres
  - Unique1km: unique 1x1 km grid square identifier
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- These grids are linked via Unique1km to allow cross-comparison where both datasets have data for the same square.
- Freshwater data (1752 sites) are not included in these AAE calculations because they are based on catchment areas, not 1x1 km grid squares, and do not represent all UK freshwaters.

## Geographic scope and data coverage
- UK-wide 1x1 km grid framework (England, Wales, Scotland, Northern Ireland).
- Habitat distributions used for calculations may differ from other national habitat maps and can affect total habitat areas mapped for acidity vs. nutrient nitrogen.

## Quality control, metadata, and data provenance
- Methods aligned with national and international practices under the UNECE CLRTAP framework.
- Detailed methodological transparency provided in Hall et al. (2015); ongoing updates and interpretation in Hall et al. (2019).
- Metadata and uncertainties documented in associated publications and data catalogues:
  - Hall et al. 2015 (Methods for calculating UK critical loads and exceedances)
  - Hall et al. 2019 (Trends Report 2018: trends in critical loads and exceedances)
  - Critical loads and CBED deposition data available via EIDC/CEH catalogues

## Use, interpretation, and caveats for monitoring
- Exceedance indicates potential for harm under long-term steady-state assumptions; current exceedance does not imply immediate damage.
- AAE maps reflect data-available areas for critical-load calculations and may not equal other habitat-area maps.
- Recovery after reducing deposition below critical loads can exhibit significant time lags, both chemically and biologically.
- Data governance considerations include data sharing and metadata availability; some barriers include data silos and the effort required to transform data into usable formats.

## Implications for monitoring frameworks
- Provides standardized, spatially explicit indicators of acidification and eutrophication pressure across the UK to inform policy review, trend analysis, and decision-making.
- Supports reporting obligations (e.g., UK Trends Reports and biodiversity indicators) and can be integrated into dashboards and governance processes.
- Highlights data quality/availability challenges common to environmental monitoring, emphasizing need for consistent metadata, data sharing, and open access where appropriate.

## References
- Hall, J.; Rowe, E.; Smith, R.; Dore, T.; Banin, L.F.; Levy, P.; Sawicka, K. 2019. Trends Report 2018: Trends in critical load and critical level exceedances in the UK. Report to Defra under Contract AQ0843, CEH Project NEC05708.
- Hall, J.; Curtis, C.; Dore, T.; Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra, Contract AQ0826.