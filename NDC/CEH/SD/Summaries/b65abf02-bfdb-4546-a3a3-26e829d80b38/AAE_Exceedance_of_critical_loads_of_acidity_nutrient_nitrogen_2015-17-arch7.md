# Methods:

- What it is
  - 1x1 km data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen critical loads due to deposition, covering 2015–2017.
  - AAE summarises exceedances across multiple habitats within each grid cell.

- How AAE is calculated
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AAE (keq ha-1 year-1) = total AE across habitats in a 1x1 km grid square ÷ total habitat area in that grid square.
  - If deposition is below the critical load, AAE is set to zero.
  - For nutrient nitrogen, AAE values can be converted to kg N ha-1 year by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year).
  - Acidity exceedance combines sulphur and nitrogen contributions and is reported as keq ha-1 year-1.

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various managed/unmanaged woodlands (coniferous and broadleaved).
  - Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, various managed/unmanaged woodlands, beech, oak, Scots pine, other woodland, dune grassland, and saltmarsh.

- Data provenance and quality
  - Methods aligned with UNECE CLRTAP processes; provenance documented in UK reports.
  - UK Methods Report (Hall et al., 2015) describes data/methods for calculating UK critical loads and exceedances.
  - Summary exceedance statistics published in Trends Reports (e.g., Hall et al., 2017) and as a UK Biodiversity Indicator (B5a).
  - Uncertainties in habitat mapping and critical loads discussed in Hall et al. 2015 and related meta-data.

- Use and interpretation
  - National critical loads maps are based on empirical/steady-state methods; exceedance indicates potential long-term harm, not immediate damage.
  - Habitat distribution maps for CL may differ from other habitat maps; total mapped habitat areas may vary between acidity and nitrogen datasets.
  - Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery can have long time lags.

- Data structure and files
  - Two files: acidhab_AAE_2015-17.csv (acidity) and nutnhab_AAE_2015-17.csv (nutrient nitrogen).
  - Coverage differs by dataset due to habitat distributions.
  - Unique1km field provides a unique identifier for each 1x1 km grid square to link acidity and nitrogen data when available.
  - Table fields include:
    - East_m, North_m (centre coordinates in OSGB grid)
    - Unique1km (grid identifier)
    - AAE_keq (Average Accumulated Exceedance)
    - CountryID (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland)

- References and access
  - Rowe, Sawicka, Mitchell, Smith, Dore, Banin, & Levy (2019) Trends Report 2019.
  - Hall, Curtis, Dore, Smith (2015) Methods for calculation of critical loads and their exceedances in the UK.
  - Data and metadata available via the UK environmental data portals (EIDC) and related CLRTAP documentation.