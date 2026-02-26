# AAE 2016-18: Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads

- Objective
  - Provide 1x1 km grid-based AAE measures for acidity and nutrient nitrogen to scrutinise and inform policy decisions on environmental health and inform future monitoring efforts.

- What the data represent
  - AAE is the sum of exceedances across habitats within a 1x1 km grid square, normalized by total habitat area in that square.
  - Two datasets:
    - Acidity AAE (acidhab_AAE_2016-18.csv)
    - Nutrient nitrogen AAE (nutnhab_AAE_2016-18.csv)
  - Exceedance components:
    - AE for each habitat = exceedance (keq ha^-1 year^-1) × exceeded habitat area (ha)
    - AAE = total AE across habitats in the grid square ÷ total habitat area (ha)
  - Acidity AAE uses habitats sensitive to acidification; nutrient nitrogen AAE uses habitats sensitive to eutrophication.

- Habitats included
  - Acidity (acidic deposition): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various productive/unproductive coniferous and broadleaved woodlands.
  - Nutrient nitrogen (nitrogen deposition): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, various woodlands, dune grassland, and saltmarsh.

- Units and conversions
  - AAE units: keq ha^-1 year^-1
  - If deposition is below a critical load, AAE = 0
  - For nutrient nitrogen, AAE can be converted to kg N ha^-1 year by multiplying by 14 (1 keq ha^-1 year^-1 = 14 kg N ha^-1 year)
  - Acidity AAE represents a mix of sulphur and nitrogen contributions and cannot be split into S or N kg terms

- Data structure and linkage
  - Two files with the same grid framework but different habitat distributions:
    - acidhab_AAE_2016-18.csv (acidity)
    - nutnhab_AAE_2016-18.csv (nutrient nitrogen)
  - Each row includes:
    - East_m, North_m: grid square centre coordinates in OSGB (metres)
    - Unique1km: unique grid square identifier
    - AAE_keq: the AAE value for the grid square
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
  - The Unique1km code allows linking acidity and nitrogen data where both exist for the same square

- Data quality and provenance
  - Methods aligned with national/international guidelines under CLRTAP
  - Hall et al. (2015) provides a full methods description; Trends Report 2019 and the UK Biodiversity Indicator provide context
  - Metadata and uncertainties documented in referenced reports and CEH/EIDC catalogues

- Use and interpretation notes
  - Critical loads and exceedances reflect long-term steady-state assumptions; exceedance indicates potential for harm under steady-state conditions, not necessarily immediate damage
  - Habitat maps and habitat-area calculations may differ from other maps, affecting total habitat areas used in calculations
  - Time lags exist between deposition reductions and chemical/biological recovery; recovery can be long, especially for sensitive ecosystems

- References
  - Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK. CEH/Defra contract report.
  - Rowe et al. (2019). Trends Report 2019: Trends in critical load and critical level exceedances in the UK.
  - EIDC and related metadata/catalogue entries for CBED deposition data