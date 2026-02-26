# Methods for the calculation of critical loads and their exceedances in the UK

- Purpose and scope
  - Presents UK approaches for calculating critical loads and their exceedances for habitats sensitive to acidification and eutrophication.
  - Based on methods agreed at national and international CLRTAP meetings; detailed description referenced in Hall et al. (2015) Methods Report.
  - Data are intended to provide a national picture, not site-specific risk assessments.

- Data and methods (key points)
  - Acidity and nutrient nitrogen critical loads derived using established CLRTAP-aligned methods.
  - Freshwater acidity critical loads are calculated from water chemistry data collected at 1752 UK sites in the 1990s (mostly upland lakes/streams); these data are not extrapolated to other sites.
  - Nitrogen critical loads are derived using appropriate empirical or mass-balance approaches per habitat.
  - Data sources include multiple data layers (land cover, soils, species distributions, NVC classes) and combine data at different resolutions.
  - Acknowledges potential future revisions as methods and knowledge evolve.

- Units and conversions
  - Habitat areas are expressed in hectares (ha).
  - Critical loads are expressed as kilo-equivalents per hectare per year (keq ha-1 yr-1).
  - For nutrient nitrogen, keq ha-1 yr-1 can be converted to kg N ha-1 yr-1 by multiplying by 14 (1 keq ha-1 yr-1 = 14 kg N ha-1 yr-1).
  - Acidity critical loads reflect a combination of sulfur and nitrogen and cannot be separated into kg S or kg N.

- Data structure and files
  - One file per habitat for acidity critical loads and one file per habitat for nutrient nitrogen critical loads.
  - File naming uses abbreviations described in Table 1; data organization includes:
    - For acidity: columns such as East_m, North_m, Unique1km, Area_ha, CLmaxS, CLminN, CLmaxN, Country_ID, EUNIS_class (where applicable).
    - For freshwater acidity files: site-level fields include SiteCode, SiteName, Area_ha, CLmaxS, CLminN, CLmaxN, Country_ID, EUNIS_class.
    - For nutrient nitrogen: similar spatial and attribute columns with CLnutN instead of CLmaxN.
  - 1x1 km grid units (Unique1km) underpin habitat-area calculations; some data (e.g., 10 km species distributions) are used to inform 1 km habitat boundaries.
  - Tables detailed in the document (Tables 2–4) define the specific column structure for acidity and nutrient nitrogen files.
  - Table 1 maps habitat abbreviations to file suffixes (e.g., AG for acidity in acid grassland, CG for calcareous grassland, etc.).

- Uncertainties and limitations
  - Uncertainties exist across all input datasets (land cover, forest land use, species distributions, NVC classes, soils, altitude).
  - Spatial resolution differences (1 km for habitat grids vs. coarser data used to derive inputs) can affect accuracy.
  - 10 km species distribution maps used to refine some habitat areas may not reflect within-10 km heterogeneity, risking overestimation of habitat areas in some 1 km cells.
  - Habitat distribution maps used for UK critical loads may differ from other national maps, leading to potential total-area differences.
  - Freshwater data are point-based and cannot be extrapolated to other sites or regions.

- Use and interpretation guidance
  - Critical load maps show relative sensitivity of soils, broad habitat types, and freshwater to acidification and eutrophication at a national level.
  - Not suitable for small-scale or site-specific risk assessments.
  - Dose-response relationships are generally not developed for applying these models to individual species (except where specifically noted for freshwater brown trout protection).
  - Critical loads may be revised in the future as methods and knowledge evolve.

- Quality control and provenance
  - Data and methods follow CLRTAP-aligned procedures; a detailed transparency-focused methods report is available (Hall et al., 2015).
  - The document emphasizes transparency of data and methods used to derive UK critical loads and their exceedances.

- Reference
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra.