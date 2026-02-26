# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2015-17.

- Overview
  - AAE summarizes exceedances across multiple habitats within each 1x1 km grid square.
  - AE for a habitat = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AAE = sum of AE across habitats in the grid square divided by the total habitat area in that grid square.
  - AAEs are expressed in keq ha-1 year-1; where deposition is below the critical load, AAE is set to zero.
  - For nutrient nitrogen, AAE values can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year).

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Data sources and methods
  - UK methods based on long-standing empirical/steady-state mass balance approaches for critical loads and their exceedances (Hall et al., 2015).
  - CBED deposition data available from the EIDC.
  - Summary exceedance statistics by habitat and country published annually in Trends Report (e.g., Hall et al., 2017) and as UK Biodiversity Indicator B5a.

- Data structure and coverage
  - Two files: acidhab_AAE_2015-17.csv (acidity) and nutnhab_AAE_2015-17.csv (nutrient nitrogen).
  - Coverage differs by habitat distribution for acidity vs. nitrogen.
  - Each record includes:
    - East_m, North_m: centre coordinates (OSGB grid, metres).
    - Unique1km: unique 1x1 km grid square identifier (links acidity and nitrogen data where available).
    - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1).
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.

- Interpretation and limitations
  - Exceedance indicates potential for harmful effects under steady-state or long-term conditions; a current exceedance does not imply immediate damage.
  - Habitat distribution and total habitat areas used for AAE may differ from other habitat maps, potentially affecting total habitat area calculations.
  - Reducing deposition below the critical load does not guarantee rapid ecological recovery; chemical and biological recovery may have long timescales.
  - Uncertainties are documented in Hall et al. (2015) and related metadata; freshwater (1752 sites) data are not included in AAE because they are catchment-based, not grid-based.

- Quality control
  - Methods agreed at national/international meetings under CLRTAP.
  - Detailed methodology and transparency provided in Hall et al. (2015); uncertainties described in accompanying metadata.

- Additional information and references
  - Trends Report 2019 (Rowe et al.) and related outputs.
  - Hall, Curtis, Dore, Smith (2015) Methods for the calculation of critical loads and their exceedances in the UK.
  - CBED deposition and related data accessible via EIDC.