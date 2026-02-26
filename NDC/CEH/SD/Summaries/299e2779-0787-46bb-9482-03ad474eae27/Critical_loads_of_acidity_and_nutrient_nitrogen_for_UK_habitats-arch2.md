# Methods for the calculation of critical loads and their exceedances in the UK

## Overview and aim
- Establishes UK critical loads for habitats sensitive to acidification and eutrophication based on methods agreed at national and international CLRTAP meetings.
- Provides a transparent, standardised methodology and data framework to produce national maps of habitat sensitivity to acidity and nitrogen deposition.
- References the UK Methods Report (Hall et al, 2015) for full data and methods details.

## Data and units
- Habitat areas are expressed in hectares (ha).
- Critical loads are expressed in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Nitrogen critical loads can be converted to kg N ha-1 year-1 by multiplying keq ha-1 year-1 by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- Acidity critical loads combine sulfur and nitrogen and can only be expressed as keq ha-1 year-1 (not convertible to S or N separately).

## Methods and quality control
- Methods derived from CLRTAP, with full methodological detail in Hall et al. 2015 (Methods Report).
- No fieldwork or lab instrumentation is described for this document (N/A).
- Quality control relies on established national/international protocols; a detailed transparency-focused report is available (Hall et al., 2015).

## Uncertainties and data quality
- Datasets are based on the best available data and expert agreement, but do not capture every small local habitat.
- Spatial resolution is 1 km for critical loads, created by integrating data from multiple resolutions (e.g., 1 km land cover with 10 km species distributions).
- The use of 10 km species distribution maps to refine 1 km habitat areas can overestimate habitat extent within some 1 km cells.
- 10 km NVC maps carry similar uncertainties.
- Habitat distribution maps for UK critical loads (acidity and N) may differ from other national maps; totals may vary accordingly.
- Data cover only areas with data available for critical loads calculations; extrapolation beyond those areas is not performed.

## Use and interpretation
- Critical load maps provide a national perspective on relative sensitivity of soils, broad habitats, and freshwaters to acidification and eutrophication.
- They are not intended for fine-scale local or site-specific risk assessments.
- Dose–response relationships are generally not developed for applying these models to individual species in the UK.
- Freshwater acidity critical loads are tied to brown trout protection; dose–response functions exist for few other aquatic species.
- Critical loads may be revised in the future as knowledge and methods evolve.

## Data structure and content
- The dataset comprises:
  - One file per habitat for acidity critical loads.
  - One file per habitat for nutrient nitrogen critical loads.
- Habitats and abbreviations are described in Table 1 (habitat naming conventions linked to EUNIS classifications).
- Tables 2 and 3 detail columns for acidity critical loads data files (Acidity_AG_Final.csv, Acidity_CA_Final.csv, Acidity_CDW_Final.csv, Acidity_CG_Final.csv, Acidity_CW_Final.csv, Acidity_DW_Final.csv, Acidity_MON_Final.csv, Acidity_POG_Final.csv) and Tables 3 for freshwater habitats (Acidity_FW_Final.csv).
  - Common columns include: East_m, North_m (OSGB grid coordinates for 1 km square centers); Unique1km; Area_ha; CLmaxS (maximum acidity load in S terms); CLminN, CLmaxN (nitrogen-related loads); Country_ID; EUNIS_class.
- Table 1: Abbreviations for file naming (e.g., AG for Acid grassland, CG for Calcareous grassland, FW for Freshwater, POG for peat bog acidity, etc.).
- Table 2: Column descriptions for acidity data files (including grid coordinates, area, critical load values, country, and habitat classification).
- Table 3: Column descriptions for acidity data in freshwater habitats (site-based data with site codes and names).
- Table 4: Column descriptions for nutrient nitrogen data files (N_* prefixes, CLnutN, site and habitat metadata, and linking identifiers).
- Freshwater acidity loads are calculated from chemistry data across 1752 UK freshwater sites (1990s), primarily upland lakes/streams; extrapolation to other sites is not possible.

## References
- Hall, J., Curtis, C., Dore, T., Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK. Report to Defra, contract AQ0826. http://www.cldm.ceh.ac.uk/sites/cldm.ceh.ac.uk/files/MethodsReport_Updated_July2015_WEB.pdf