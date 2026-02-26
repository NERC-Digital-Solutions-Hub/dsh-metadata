# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2013-15

- Overview
  - Presents 1x1 km grid datasets of Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen critical loads due to acid and nitrogen deposition for 2013–2015 in the UK.
  - AAE summarizes exceedances across multiple habitats within each 1x1 km grid square.
  - UK coverage varies by habitat distribution; data are linked to habitat presence, not a blanket national coverage.

- How AAE is calculated
  - For each habitat:
    - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - In each 1x1 km grid square, AE is summed across all habitats.
  - AAE (keq ha-1 year-1) = total AE / total habitat area (ha) in that grid square.
  - If deposition is below the critical load, AAE = 0.
  - Nutrient nitrogen AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity exceedance combines sulfur and nitrogen compounds and is therefore reported as keq ha-1 year-1 (not separable into kg S or N).

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen: all acidity habitats plus unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Data files and structure
  - Two CSV files:
    - acidhab_AAE_2013-15.csv (AAE for acidity)
    - nutnhab_AAE_2013-15.csv (AAE for nutrient nitrogen)
  - Shared structure and fields (Table 1):
    - East_m: Easting for centre of 1x1 km square (OSGB grid, metres)
    - North_m: Northing for centre of 1x1 km square (OSGB grid, metres)
    - Unique1km: Unique identifier for the 1x1 km square (links acidity and nitrogen datasets)
    - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
    - CountryID: Geographic region code (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland)
  - Coverage differs between the two datasets due to habitat distributions.

- Quality control and provenance
  - Methods follow UNECE CLRTAP-aligned processes; detailed transparency provided in Hall et al. (2015) and related meta-data.
  - Summary trends and related data are published in UK reports (e.g., Hall et al. 2017) and in the UK Biodiversity Indicator.

- Use, interpretation, and caveats
  - Critical load maps are based on empirical/steady-state methods; exceedance indicates potential long-term harm, not necessarily current damage.
  - Habitat maps and mapped areas used for critical loads/exceedances may differ from other national habitat maps, affecting total habitat area totals.
  - Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery can be time-lagged and long.
  - Uncertainties and data limitations are noted in the accompanying Hall (2015) and related metadata (e.g., CBED deposition information via EIDC).

- Fieldwork and calibration
  - Not applicable (N/A) for fieldwork or instrumentation entries in this dataset.

- References
  - Hall, J., Smith, R., Dore, T. (2017). Trends Report 2017: Trends in critical load and critical level exceedances in the UK. Defra contract AQ0843.
  - Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK. Defra contract AQ0826.