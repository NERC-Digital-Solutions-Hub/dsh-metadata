# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2013-15

- Purpose and scope
  - Provide 1x1 km grid datasets of AAE for acidity and nutrient nitrogen critical loads due to deposition, covering 2013–2015.
  - AAE summarises exceedances across multiple habitats within each grid square.

- How AAE is calculated
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - Sum AE across all habitats within a 1x1 km grid square.
  - AAE (keq ha-1 year-1) = total AE / total habitat area (ha) in the grid square.

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various woodland types (productive and unmanaged).
  - Nutrient nitrogen: same acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, plus a range of woodland types and additional habitats (beach and dune-related habitats, saltmarsh, etc.).

- Data files and structure
  - acidhab_AAE_2013-15.csv: AAE for acidity.
  - nutnhab_AAE_2013-15.csv: AAE for nutrient nitrogen.
  - Each file includes: East_m, North_m (OSGB grid coordinates for the grid square center); Unique1km (unique 1x1 km square identifier); AAE_keq (AAE value); CountryID (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland).
  - Unique1km enables linking acidity and nutrient nitrogen data across squares where both exist.

- Units and interpretation
  - AAE values are in keq ha-1 year-1.
  - If deposition is below the critical load, AAE is set to zero.
  - Conversion: for nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity exceedance combines sulphur and nitrogen components and cannot be separated into S or N units.

- Quality control and provenance
  - Methods are aligned with national/international guidelines from CLRTAP (UNECE).
  - Detailed methodological transparency is provided in Hall et al. (2015); meta-data available for critical loads data.
  - CBED deposition data referenced via the EIDC.

- Use, interpretation, and caveats
  - UK critical loads maps are based on empirical/steady-state methods; exceedance indicates potential long-term harm but not immediate damage.
  - Habitat maps/areas for critical loads/exceedances reflect data-available areas and may differ from other habitat maps; totals may vary accordingly.
  - Reducing deposition below critical loads does not imply immediate ecological recovery; chemical and biological recovery can have long time lags.
  - Uncertainties exist in habitat mapping and critical loads; refer to Hall et al. (2015) and associated metadata for details.

- Data coverage and special notes
  - Data cover the UK, with differences in coverage due to habitat distribution; freshwater data (1752 sites) are not included in AAE calculations since they are catchment-based, not 1x1 km grid-based.

- References
  - Hall, J., Smith, R., Dore, T. 2017. Trends Report 2017: Trends in critical load and critical level exceedances in the UK.
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK.
  - Additional data access: Critical Loads data (EIDC) and related metadata.