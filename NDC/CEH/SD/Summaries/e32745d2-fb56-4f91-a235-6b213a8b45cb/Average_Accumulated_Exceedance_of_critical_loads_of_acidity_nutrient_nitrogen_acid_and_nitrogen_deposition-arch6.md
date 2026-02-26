# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2013-15.

- Purpose: Document and describe the 1x1 km AAE data sets for acidity and nutrient nitrogen critical loads, used to assess long-term potential impacts of deposition across the UK.

## Scope and what the data represent
- AAE data summarize exceedances across habitats within each 1x1 km grid square.
- AE is calculated per habitat as exceedance (keq ha-1 year-1) times exceeded habitat area (ha); AAE is the sum of AE divided by total habitat area in the grid square.
- Year set: 2013–2015.
- Units: AAE values are in keq ha-1 year-1. For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- Acidity exceedance combines sulphur and nitrogen contributions and cannot be separated into S vs N.

## Habitats included
- Acidity (AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed (productive) coniferous woodland; managed (productive) broadleaved woodland; unmanaged coniferous woodland; unmanaged broadleaved woodland.
- Nutrient nitrogen (AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed (productive) coniferous woodland; managed (productive) broadleaved woodland; unmanaged beech woodland; unmanaged oak woodland; unmanaged Scots pine woodland; other unmanaged woodland; dune grassland; saltmarsh.

## Data structure and file details
- Two files due to different habitat distributions:
  - acidhab_AAE_2013-15.csv (AAE for acidity)
  - nutnhab_AAE_2013-15.csv (AAE for nutrient nitrogen)
- Common fields in both:
  - East_m: Easting for the centre of the 1x1 km grid square (OSGB grid metres)
  - North_m: Northing for the centre of the 1x1 km grid square (OSGB grid metres)
  - Unique1km: Unique identifier for the 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Data coverage differs between acidity and nutrient nitrogen according to habitat distributions.
- Geography links: Unique1km allows matching acidity and nitrogen data for the same squares.

## Data quality, interpretation, and caveats
- Quality control: Methods based on international CLRTAP practices; detailed Hall et al. (2015) Methods Report provides transparency.
- Use and interpretation:
  - Exceedance indicates potential for harmful effects at steady-state or long-term, not immediate damage.
  - Habitat maps and areas used for critical loads may differ from other national maps; total habitat areas may not be identical across acidity and nitrogen datasets.
  - Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery can have long time lags.
- Uncertainty: Refer to Hall et al. (2015) and related metadata for uncertainties in habitat mapping and critical loads.

## Related outputs and metadata
- Summary exceedance statistics by habitat and country are published annually in the Trends Report (e.g., Hall et al., 2017) and as the UK Biodiversity Indicator B5a.
- Freshwater data (1752 records) with acidity exceedance statistics exist but are not included in the AAE calculations; freshwater data are catchment-based and not 1x1 km grid-based.
- Additional information on CBED deposition available from the EIDC.
- References:
  - Hall, J., Smith, R., Dore, T. (2017). Trends Report 2017: Trends in critical load and critical level exceedances in the UK.
  - Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK.