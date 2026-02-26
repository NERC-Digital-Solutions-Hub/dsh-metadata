# Methods

- Purpose: 1x1 km data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen deposition relative to habitat-specific critical loads, covering 2016–2018. Two files exist: AAE for acidity and AAE for nutrient nitrogen, with different UK coverage based on habitat distributions.
- Data products: 
  - acidhab_AAE_2016-18.csv (AAE for acidity)
  - nutnhab_AAE_2016-18.csv (AAE for nutrient nitrogen)
  - Each row corresponds to a 1x1 km grid square with a Unique1km code enabling linkage between the two datasets where applicable.

- How AAE is calculated:
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
  - AAE (keq ha-1 year-1) = total AE ÷ total habitat area (ha) within the 1x1 km grid square
  - If deposition is below the critical load, AAE is set to zero
  - For nutrient nitrogen, AAE values can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1)
  - Acidity AAE represents a mix of sulphur and nitrogen compounds and cannot be separated into S or N

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland
  - Nutrient nitrogen: the same habitats as acidity plus unmanaged beech, unmanaged oak, unmanaged Scots pine woodlands, other unmanaged woodland, dune grassland, saltmarsh

- Data sources, standards, and quality
  - Methodology aligned with UK CLRTAP processes; referenced in Hall et al. (2015) and summarized in subsequent reports (e.g., Hall et al., 2017; Rowe et al., 2019)
  - Critical loads and CBED deposition data available from the EIDC
  - Quality control relies on methods agreed at national/international meetings under CLRTAP; detailed methodology in Hall et al. (2015)

- Usage and interpretation guidance
  - Critical loads maps use empirical/steady-state methods; exceedance indicates potential long-term harm but not immediate damage
  - Habitat distribution maps for critical loads/exceedances may differ from other national habitat maps, affecting total habitat areas
  - Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery may have long time lags
  - Uncertainties exist in habitat mapping and critical-load derivation; refer to Hall et al. (2015) and dataset metadata for details

- Data structure and technical details
  - Files include: East_m (metres, OSGB grid), North_m (metres, OSGB grid), Unique1km (grid identifier), AAE_keq (keq ha-1 year-1), CountryID (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland)
  - AAE values are provided per 1x1 km square and can be linked between acidity and nitrogen datasets via Unique1km

- Accessibility and additional information
  - For UK critical loads/exceedances data and metadata, consult the UK Trends Reports and CEH references
  - Freshwater exceedance statistics (1752 sites) are reported separately and not included in the AAE calculation for these datasets

- References
  - Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK.
  - Rowe E, Sawicka K, Mitchell Z, et al. (2019). Trends Report 2019: Trends in critical load and critical level exceedances in the UK.
  - EIDC and related metadata for CBED deposition data