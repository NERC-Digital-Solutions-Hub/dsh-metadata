# Methods for the calculation of critical loads and their exceedances in the UK

- Purpose and scope
  - Describes UK critical loads for habitats sensitive to acidification and eutrophication, based on methods agreed at national and international CLRTAP meetings.
  - UK Methods Report (Hall et al., 2015) provides full data and methods for producing UK critical-load maps.

- Data and units
  - Habitat areas are expressed in hectares (ha).
  - Critical loads are expressed as keq ha-1 year-1.
  - Nitrogen critical loads can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity critical loads are a combination of sulfur and nitrogen and are expressed only as keq ha-1 year-1 (not convertible to S or N alone).

- Data structure and files
  - One file per habitat for acidity critical loads and one file per habitat for nutrient nitrogen critical loads.
  - Freshwater acidity data are based on 1752 sites; freshwater data are provided as point data and cannot be extrapolated to other sites.
  - Spatial resolution and linkage
    - Critical loads are produced on a 1 km x 1 km grid, with data tied to habitat areas within each square.
    - Data include Easting/Northing in OSGB grid, Unique1km identifiers, area in ha, and several load values.
  - Key columns (examples)
    - East_m, North_m: centre coordinates for 1x1 km square.
    - Unique1km: unique 1x1 km identifier.
    - Area_ha: habitat area within the 1x1 km square.
    - CLmaxS: maximum acidity load (sulfur-related).
    - CLminN / CLmaxN: minimum and maximum nitrogen loads.
    - Country_ID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
    - EUNIS_class: habitat class per European Nature Information System.
  - Table-linked datasets
    - Table 1: file-name suffix mappings by habitat (e.g., acidity vs nutrient nitrogen) and habitat type.
    - Table 2: columns in Acidity_AG_Final.csv, Acidity_CA_Final.csv, etc.
    - Table 3: columns in Acidity_FW_Final.csv (freshwater habitats).
    - Table 4: columns in NutrientN_AG_Final.csv, NutrientN_BOG_Final.csv, etc.
  - Notes on data scope
    - Some habitat squares may have incomplete sub-divisions due to ancillary data limitations.
    - 10 km datasets are used to refine habitat distributions within 1 km cells; this can lead to overestimation within some 1 km squares.

- Use and interpretation
  - Provides a national-level view of relative sensitivity of soils, broad habitat types, and freshwaters to acidification and eutrophication.
  - Not intended for small-scale, site-specific risk assessments.
  - Dose-response relationships for individual species are generally not developed; for freshwater acidity, brown trout protection is explicitly modeled, with limited or no dose-response for most other species.
  - Critical loads may be revised as methods and knowledge evolve.

- Uncertainties and limitations
  - Uncertainties inherent in underlying data (land cover, forest land use, species distributions, NVC classes, soils, altitude).
  - 1 km resolution datasets based on combining data at different resolutions (e.g., 1 km and 10 km), which can cause habitat area over- or under-estimation within 10 km blocks.
  - Habitat distribution maps used here may differ from other national maps, affecting total habitat areas mapped for acidity vs. nutrient nitrogen.

- Quality control and provenance
  - Methods and data follow internationally agreed CLRTAP approaches.
  - A detailed Methods Report (Hall et al., 2015) provides transparency on data and calculations used to derive UK critical loads and their exceedances.

- Data sources and reference
  - Hall, J.; Curtis, C.; Dore, T.; Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra.
  - Main dataset reference: UK critical loads maps and accompanying data for habitats sensitive to acidification and eutrophication.