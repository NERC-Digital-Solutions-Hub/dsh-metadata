# Methods for the calculation of critical loads and their exceedances in the UK

- This document describes UK critical loads for habitats sensitive to acidification and eutrophication, based on methods agreed at national and international meetings under the UNECE CLRTAP.
- Full methodological detail and data provenance are provided in Hall et al. (2015) “Methods for the calculation of critical loads and their exceedances in the UK.”

## Nature, units and data records

- Habitat areas are expressed in hectares (ha).
- All critical loads are expressed in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversion guidance:
  - Nutrient nitrogen critical loads can be converted to kg N ha-1 year-1 by multiplying keq ha-1 year-1 by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity critical loads (combining sulphur and nitrogen) are expressed only as keq ha-1 year-1 and cannot be converted to kg of S or N alone.

## Quality control and methodology

- Data and methods follow the standards agreed at CLRTAP-related meetings/workshops.
- A detailed transparency-focused Methods Report is available (Hall et al., 2015) documenting the data and methods used to derive UK critical loads.

## Uncertainties in habitat distribution datasets

- Datasets carry uncertainties in land cover, forest land use, species distributions, NVC classes, soils, and elevation.
- Habitat distributions are provided at 1 km resolution, derived from multiple data sources with differing resolutions (e.g., 1 km land cover and 10 km species distributions).
- When refining from 10 km species distributions to 1 km habitats, 10 km grid squares are selected to represent broad habitat presence, which can overestimate habitat areas within some 1 km cells.
- 10 km NVC maps carry similar uncertainties.
- Habitat maps used for UK critical loads may differ from other national maps or estimates, potentially affecting total habitat area counts for acidity versus nutrient nitrogen critical loads.

## Use and interpretation

- Critical load maps aim to show national-scale sensitivity of soils, broad habitats, and freshwaters to acidification and eutrophication.
- They are not intended for small-scale or site-specific risk assessments.
- Dose-response relationships are generally not developed for applying these models to individual species.
- Freshwater acidity critical loads are based on brown trout protection; dose-response data for most other aquatic species are largely absent.
- Critical loads may be revised in the future as knowledge and methods evolve.

## Details of data structure

- Data consist of:
  - One file per habitat for acidity (Acidity_*_Final.csv, e.g., Acidity_AG_Final.csv, Acidity_CGW_Final.csv, etc.).
  - One file per habitat for nutrient nitrogen (NutrientN_*_Final.csv, e.g., NutrientN_AG_Final.csv, NutrientN_BOG_Final.csv, etc.).
- Abbreviations and habitat naming are described in Table 1 (file name suffixes indicate habitat and data type; e.g., _AG for Acid grassland, _CG for Calcareous grassland, _POG for peat bog acidity assumptions, etc.).
- Columns in acidity data files (Table 2):
  - East_m, North_m: centre coordinates in OSGB grid (metres).
  - Unique1km: unique 1 km square identifier.
  - Area_ha: habitat area within the 1 km square.
  - CLmaxS: maximum acidity load (S-only) in keq ha-1 yr-1.
  - CLminN: minimum nitrogen load in keq ha-1 yr-1 (long-term N removal processes).
  - CLmaxN: maximum nitrogen load in keq ha-1 yr-1 (N-only acidity load when S deposition is zero).
  - Country_ID: England=1, Wales=2, Scotland=3, Northern Ireland=4.
  - EUNIS_class: habitat class per European Nature Information System (when assigned).
- Columns in acidity data for freshwater habitats (Table 3):
  - Site-specific coordinates (East_m, North_m), Unique1km, Area_ha (catchment area if nested, otherwise site area).
  - CLmaxS, CLminN, CLmaxN, Country_ID, EUNIS_class, SiteCode, SiteNumber, SiteName.
- Columns in nutrient nitrogen data files (Table 4):
  - East_m, North_m, Unique1km, Area_ha.
  - CLnutN: critical load of nutrient nitrogen (empirically derived values for most habitats; mass-balance derived for CW and DW).
  - Country_ID, EUNIS_class.
- Freshwater critical loads are based on 1,752 UK freshwater sites (upland lakes/streams from the 1990s) and are provided as point data; they cannot be extrapolated to other sites or areas.
- Notes explain habitat-specific conventions (e.g., peat soil assumption for bog acidity, “within” qualifiers for unmanaged woodland categories).

## References

- Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra. http://www.cldm.ceh.ac.uk/sites/cldm.ceh.ac.uk/files/MethodsReport_Updated_July2015_WEB.pdf