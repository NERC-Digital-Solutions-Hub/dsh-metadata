# Methods for the calculation of critical loads and their exceedances in the UK

## Overview
- UK critical loads are calculated using methods agreed at national and international CLRTAP meetings; [Hall et al., 2015] provides the full data and methodological description used to produce UK critical-load maps for habitats sensitive to acidification and eutrophication.

## Nature & units of recorded values
- Habitat areas: hectares (ha).
- Critical loads: kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversion: 1 keq ha-1 year-1 of nutrient nitrogen equals 14 kg N ha-1 year-1.
- Acidity critical loads represent a combined S and N effect and are expressed only as keq ha-1 year-1 (not convertible to kg S or kg N).

## Quality control and uncertainty
- Quality control: methods are those agreed under CLRTAP; a detailed transparency report is Hall et al. (2015).
- Uncertainties in habitat datasets:
  - All data sets (land cover, forest land use, species distributions, NVC classes, soils, altitude) have uncertainties.
  - Habitat critical loads are provided at 1 km resolution but combine data from 1 km and 10 km datasets; this can lead to over- or under-estimation within 1 km squares.
  - 10 km species distributions refine habitat areas but do not guarantee species presence in every 1 km cell within a 10 km square.
  - 10 km NVC maps carry similar uncertainties.
  - Habitat maps used for UK critical loads may differ from other national maps, affecting total habitat areas mapped for acidity vs nutrient nitrogen.
  - Data cover only areas with existing data; may not extrapolate to other regions.

## Use and interpretation
- Critical-load maps provide a national picture of relative sensitivity of soils, habitats, and freshwaters to acidification and/or eutrophication.
- Not intended for small-scale, site-specific risk assessments.
- Dose–response relationships are generally not developed for applying critical loads to individual species.
- Freshwater acidity loads target brown trout protection; dose–response functions are not available for most other aquatic species.
- Critical-load estimates may be revised in the future as knowledge and methods evolve.

## Details of data structure
- Data design: one file per habitat for acidity critical loads and one file per habitat for nutrient nitrogen critical loads.
- Abbreviations and habitat classes are described in Table 1; Tables 2–4 describe data columns for acidity and nutrient-nitrogen files.
- Acidity data files: Acidity_AG_Final.csv; Acidity_CA_Final.csv; Acidity_CDW_Final.csv; Acidity_CG_Final.csv; Acidity_CW_Final.csv; Acidity_DW_Final.csv; Acidity_MON_Final.csv; Acidity_POG_Final.csv.
- Nutrient nitrogen data files: NutrientN_AG_Final.csv; NutrientN_BOG_Final.csv; NutrientN_CA_Final.csv; NutrientN_CG_Final.csv; NutrientN_CW_Final.csv; NutrientN_DG_Final.csv; NutrientN_DW_Final.csv; NutrientN_FGW_Final.csv; NutrientN_MON_Final.csv; NutrientN_OAK_Final.csv; NutrientN_SM_Final.csv; NutrientN_SPW_Final.csv; NutrientN_UMW_Final.csv.
- Common data columns (examples):
  - East_m, North_m: OSGB grid coordinates for center of 1x1 km square (metres).
  - Unique1km: unique 1x1 km square identifier.
  - Area_ha: habitat area within the 1x1 km square.
  - CLmaxS, CLminN, CLmaxN (acidity): maximum acidity load (S-based), minimum nitrogen load, maximum nitrogen load (all in keq ha-1 year-1).
  - CLnutN (nutrient N): critical load of nutrient nitrogen (keq ha-1 year-1).
  - Country_ID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
  - EUNIS_class: habitat class according to EUNIS (with notes on mapping limitations for certain habitats).
- Freshwater specifics:
  - For acidity in freshwater, data come from 1752 UK sites (mostly upland lakes/streams); these are point data and cannot be extrapolated to other sites.
  - SiteCode/Naming fields included for freshwater files (e.g., Acidity_FW_Final.csv).
- Notes on habitat suffixes and peat soils:
  - Certain suffixes reflect habitat-specific conventions (e.g., _POG for bog acidity assuming peat soils).
  - Some habitats have special mappings for unmanaged woodland categories (e.g., _CDW for unmanaged coniferous/broadleaved woodland in acidity; multiple categories for nutrient N).
- Linking and data use:
  - Tables designed to be linked with a common key; Tables 1–4 provide the structure to connect across acidity and nutrient-nitrogen datasets.

## References
- Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra, Contract AQ0826. http://www.cldm.ceh.ac.uk/sites/cldm.ceh.ac.uk/files/MethodsReport_Updated_July2015_WEB.pdf