# AAE data sets for acidity and nutrient nitrogen critical loads (2015-17)

- Purpose and scope
  - Provide 1x1 km grid-based averages of Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen deposition, covering 2015–2017.
  - AAE summarises exceedances across multiple habitats within each grid square, indicating potential long-term harm rather than immediate damage.

- Methodology
  - Calculations:
    - AE (keq year-1) for each habitat = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
    - AAE (keq ha-1 year-1) = total AE across habitats in a grid square / total habitat area in that grid square.
  - Habitats included:
    - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various productive/unproductive woodlands.
    - Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, various woodlands, dune grassland, and saltmarsh.
  - Units and conversions:
    - AAE values are in keq ha-1 year-1.
    - For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Notes:
    - Acidity AAE represents a combination of sulfur and nitrogen compounds and cannot be separated into S or N.

- Data structure and content
  - Two files: acidhab_AAE_2015-17.csv (acidity) and nutnhab_AAE_2015-17.csv (nutrient nitrogen).
  - Common structure elements:
    - East_m and North_m: centre coordinates (OSGB grid, metres).
    - Unique1km: unique 1x1 km grid square identifier.
    - AAE_keq: Average Accumulated Exceedance value.
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
  - Coverage:
    - Separate files reflect different habitat distributions for acidity and nitrogen; not all squares are present in both datasets.

- Quality control and transparency
  - Methods are based on established national/international processes under the UNECE CLRTAP.
  - Detailed methodology documented in Hall et al. 2015; transparency on data and methods provided in referenced reports.

- Use, interpretation, and caveats
  - Exceedance signals potential for harm under steady-state/long-term conditions; not an immediate damage diagnosis.
  - Habitat distribution maps and areas used for critical loads/exceedances may differ from other habitat maps, affecting total habitat areas per category.
  - Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery can be slow, with long time lags.
  - Freshwater data (1752 features) are not included in the AAE calculations because they are catchment-based rather than 1x1 km grid-based.

- Metadata and references
  - Related publications:
    - Hall et al. 2015. Methods for calculation of critical loads and their exceedances in the UK.
    - Rowe et al. 2019. Trends Report 2019: Trends in critical load and critical level exceedances in the UK.
  - Additional information:
    - Trends and summary statistics are published in the UK Trends Report and UK Biodiversity Indicator (B5a), with datasets available via CEH/CLDM resources.
  - Data provenance for CBED deposition and critical loads data available from the EIDC and CEH catalogue.