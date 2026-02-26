# Methods for the calculation of critical loads and their exceedances in the UK

- Purpose and scope
  - Documents UK methods for calculating critical loads and their exceedances for habitats sensitive to acidification and eutrophication, based on UNECE CLRTAP guidelines.
  - Provides a national-scale (not site-specific) picture of habitat sensitivity to acidity and nitrogen deposition.
  - Acetidity critical loads for freshwaters are derived from 1752 UK sites and are not extrapolated to other sites.

- Data and data sources
  - Methods and data are aligned with national/international CLRTAP workshops and Hall et al. (2015) Methods Report.
  - Habitat distribution data and land cover inputs contribute to 1 km grid-scale critical loads (1 km resolution for consistency with the maps).

- Data structure and files
  - Two main data families:
    - Acidity critical loads (for habitats): one file per habitat (Acidity_*_Final.csv; e.g., Acidity_AG_Final.csv).
    - Nutrient nitrogen critical loads (for habitats): one file per habitat (NutrientN_*_Final.csv; e.g., NutrientN_AG_Final.csv).
  - Freshwater acidity data: Acidity_FW_Final.csv; accompanying site-level fields for freshwater habitats.
  - Each file contains 1x1 km grid cell data with key fields.
  - Habitat abbreviations and table references:
    - Table 1 lists habitat abbreviations and corresponding file suffixes (e.g., AG for Acid Grassland, CG for Calcareous Grassland, etc.).
    - Tables 2 and 3 describe acidity data columns; Table 4 describes nutrient nitrogen columns.
  - Columns and geography
    - Spatial identifiers: East_m and North_m (OSGB grid coordinates for the center of each 1x1 km square); Unique1km identifiers.
    - Area_ha: habitat area within the 1x1 km square.
    - Critical loads:
      - CLmaxS: maximum acidity load (sulphur-based) in keq ha-1 year-1.
      - CLminN: minimum nitrogen load in keq ha-1 year-1.
      - CLmaxN: maximum nitrogen load in keq ha-1 year-1.
      - For nutrient nitrogen datasets: CLnutN representing habitat-specific nutrient nitrogen critical loads.
    - Metadata:
      - Country_ID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
      - EUNIS_class: habitat classification (where available).
      - For freshwater datasets: SiteCode, SiteName, SiteNumber to identify sites; Area_ha reflects site catchment area (without nested counts to avoid double counting).
  - File naming and suffixes
    - Acidity files use suffixes like _AG, _CG, _DW, _POG, etc., to denote habitat and acidity calculations.
    - Nutrient nitrogen files use corresponding suffixes (e.g., _AG, _CG, _DW, _POG, _FGW, _OAK, _SM, etc.) for nitrogen calculations.
    - Some habitats have no data for acidity or nitrogen in specific squares (No data).

- Habitat coverage and data limitations
  - Critical loads maps provide a national-level view of sensitivity across soils, broad habitat types, and freshwaters.
  - Not intended for small-scale or site-specific risk assessments.
  - Dose-response relationships are generally not developed for most species; freshwater acidity critical loads are specifically linked to brown trout protection.
  - Habitat distribution maps may omit very small areas; grids combine data from different resolutions (1 km for habitat areas, 10 km for species distributions), which can lead to over- or under-estimation in some cells.
  - The data cover areas with available data used for derivation; may differ from other national habitat maps, affecting total habitat area counts.

- Uncertainties and quality considerations
  - Uncertainties exist in land cover, forest data, species distributions, NVC classes, soils, and altitude inputs.
  - Resolution mismatch and use of 10 km species data to refine 1 km habitat areas introduce potential mismatches.
  - Uncertainties are acknowledged; outputs reflect national-scale patterns rather than complete local precision.

- Use and interpretation guidance
  - Outputs are intended to show relative sensitivity across the country, not to assess risk at specific local sites.
  - Most dose-response relationships for individual species are not provided; caution in applying critical loads to predict species-level effects.
  - Results may be revised as scientific knowledge and methods evolve.
  - Freshwater acidity loads focus on brown trout protection; other aquatic species lack established dose-response functions.

- Data quality control and transparency
  - Methods and data are documented in the CLRTAP-based framework; a detailed Hall et al. (2015) report provides transparency about data and methods used to derive UK critical loads.

- Reference
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra.