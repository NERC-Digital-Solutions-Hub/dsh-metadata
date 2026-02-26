# Woodlands Survey Site Information 1971-2001

## Overview
- 103 broadleaved woodlands surveyed across Britain in 1971.
- Within each site, 16 randomly located 200 m² plots; data collected on canopy and ground flora, soil pH, soil organic matter, habitat management, and other site/plot descriptors.
- Re-surveyed in 2000, 2002, and 2003 (referred to as 2001) using the same field methods to assess ecological change.
- Analyses linked ecological change to drivers such as atmospheric deposition (S and N), climate, canopy structure changes, and woodland management.
- Foundational publications: Kirkby et al. (2005) and Corney et al. (2004) provide details on methods and spatial factors; users should consult these for deeper methodological context.

## Survey Design & Methods
- Stratified sampling across the study area.
- Fieldwork conducted according to Bunce & Shaw’s 1973 standardized survey methods.
- Field handbook and supporting documentation accompany the data.
- Related datasets and references include the Countryside Survey and the 1968 Steele national woodland survey.

## Data Structure and Content
- Hierarchy and identifiers:
  - Site: numeric code (1–103), with Site_name for site header context.
  - Plot: numeric (1–16) within a site (Plot header/Plot descriptions).
  - Code/Description: descriptors for site/plot characteristics (with codes and groupings).
  - Year and Field_sheet classifications indicating data collection periods and sheet types (Site header, Site descriptions, Plot header, Plot descriptions).
- Key attribute groups:
  - Indices for management (wm), tree/shrub regeneration (r), open habitats (o), and adjacent land cover (l) based on grouped site descriptors.
  - Score field used to weight open habitat features (e.g., 1 for narrow paths, 5 for wide rides) to derive an abundance index of open habitats.
- Geospatial and attribute details:
  - Slope and Aspect for 1971 and 2000s (Slope71, Slope03; Aspect71, Aspect03).
  - Easting and Northing coordinates using OSGB 1936 National Grid, expressed in kilometres (site header only).
  - Country (England, Scotland, Wales), and survey recorders (1971 and 2003).
  - Reasons for any plot not surveyed in the 2000s (Reason_for_nosurvey).
  - Dates: Date2003 (start date for 2000s survey; standardized to 2002 year in the metadata) and Date1971 (survey start).
- Data organization:
  - Supporting documentation includes a “Field_sheet” concept with: Site Header, Site Descriptions, Plot Header, Plot Descriptions.
  - Supporting documentation and field handbooks provide deeper definitions of descriptors and scoring.

## Geospatial Application Considerations for GIS
- Suitable for map-based visualization of site locations, plot distributions, and spatial trends in woodlands over time.
- Coordinates (Easting/Northing) enable GIS integration within the OSGB National Grid framework.
- Separate 1971 and 2000s descriptors allow change detection and trend analyses at site and plot scales.
- Indices for management, regeneration, open habitats, and adjacent land cover support landscape-scale assessments when combined with other spatial datasets (e.g., Countryside Survey).

## Related Datasets and Documentation
- Related dataset: Countryside Survey.
- Publications for methodology and analysis:
  - Corney et al. (2004): Landscape-scale drivers of vegetation composition.
  - Kirby et al. (2005): Measuring long-term ecological change in British woodlands (1971–2001).
- Originators and curators listed for 1971 and 2001 surveys (Bunce, Shaw, Smart, Black, Kirby, Corney, Smithers, etc.).

## Data Quality, Gaps and Considerations for Use
- Data spans multiple years with resurvey gaps and a specific reference year for the 2000s survey.
- Some plots were not surveyed in the 2000s; Reasons for nosurvey are recorded.
- Data aggregation requires careful alignment of field_sheet types and code_group classifications.
- Spatial resolution varies (site-level coordinates; plot-level descriptions exist within field sheets), necessitating careful data transformation for GIS analyses.
- Users should consult the cited publications and the field handbook for detailed methods, descriptor definitions, and coding schemes before GIS integration.

## References
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales.
- Corney, P.M., LeDuc, M.L., Smart, S.M., Kirby, K.J., Bunce, R.G.H., Marrs, R.H. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation, 115, 200-215.
- Haines-Young, R.H. et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management, 67, 267-281.
- Kirby, K.J. et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis of change based on the 103 sites in the Bunce 1971 woodland survey. English Nature Research Reports 653.