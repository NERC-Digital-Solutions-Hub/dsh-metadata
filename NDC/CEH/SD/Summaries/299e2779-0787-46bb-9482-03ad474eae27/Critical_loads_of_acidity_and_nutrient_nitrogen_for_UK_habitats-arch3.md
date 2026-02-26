# Methods

- Purpose and scope
  - UK critical loads are calculated using methods agreed at national and international CLRTAP meetings to map habitat sensitivity to acidification and eutrophication.
  - The outputs are intended to give a national picture for policy scrutiny and future decision-making, not for site-specific risk assessment.

- Data and units
  - Habitat areas are expressed in hectares (ha).
  - Critical loads are expressed in kilo-equivalents per hectare per year (keq ha-1 year-1).
  - Nutrient nitrogen critical loads can be converted to kg N ha-1 year-1 by multiplying keq ha-1 year-1 by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity critical loads reflect a combination of sulphur and nitrogen; thus, they are presented as keq ha-1 year-1 only for most habitats.

- Data sources and coverage
  - Based on methods and data described in Hall et al. (2015) Methods for the calculation of critical loads and their exceedances in the UK.
  - Freshwater acidity critical loads are derived from 1752 UK freshwater sites sampled in the 1990s, mainly upland waters; these data cannot be extrapolated to other sites.

- Spatial data and data structure
  - Critical loads are provided as 1 km x 1 km gridded data to align with national mapping needs.
  - Two data streams:
    - Acidity critical loads (per habitat)
    - Nutrient nitrogen critical loads (per habitat)
  - Each habitat has a dedicated data file for acidity and a corresponding file for nutrient nitrogen.
  - Column structure includes: grid coordinates (East_m, North_m), Unique1km, Area_ha, CLmaxS (acidifying sulphur), CLminN (minimum N removal), CLmaxN (maximum N deposition), Country_ID (England, Wales, Scotland, Northern Ireland), and EUNIS_class (habitat classification).
  - Freshwater acidity data files include SiteCode and SiteName for site-level context.
  - File naming follows a suffix convention linked to habitat type (e.g., _AG for acidity in acid grassland; _CW for acidity in managed conifer woodland; _MON for montane, etc.).

- Use and interpretation
  - Critical load maps are intended to show relative national sensitivity of soils, broad habitats, and freshwaters to acidity and eutrophication.
  - They are not suitable for small-scale or site-specific risk assessment.
  - Dose–response relationships are generally not developed for most species, so extrapolations to individual species are limited.
  - Acidity loads for freshwaters are specifically tied to brown trout protection; dose–response data are not available for most other aquatic species.
  - The datasets and methods may be revised in light of new knowledge and methodological updates.

- Uncertainties and limitations
  - Broad uncertainties stem from input data (land cover, soils, species distributions, NVC classes, altitude) and from using multiple data sources with different resolutions (1 km, 10 km).
  - The 1 km grid is consistent for mapping but may overestimate habitat areas when refined from 10 km species distributions.
  - Some habitat classes lack data (e.g., dune grassland, saltmarsh for some measures).
  - The data reflect areas where data exist for calculation; they may differ from other national habitat maps, potentially affecting total habitat areas mapped for acidity versus nutrient nitrogen.

- Quality control and governance
  - Methods are based on established CLRTAP protocols with a detailed transparency report (Hall et al., 2015) describing data and methods used to derive UK critical loads.
  - Data handling, reporting, and potential future revisions are guided by formal methodological documentation and Defra contract work.

- Metadata and reproducibility
  - The dataset structure is explicit (distinct files per habitat and per critical load type) with clearly defined column headers and coding (e.g., country codes, habitat classifications).
  - Documentation notes the alignment with EUNIS habitat classifications and the need to reference the accompanying Methods Report for full transparency.

- Reference
  - Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra.