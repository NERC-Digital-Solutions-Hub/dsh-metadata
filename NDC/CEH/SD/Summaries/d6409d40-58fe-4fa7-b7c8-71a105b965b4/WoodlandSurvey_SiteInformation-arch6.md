# Woodlands Survey Site Information 1971-2001

## Overview
- A long-term ecological dataset covering 103 broadleaved woodlands in Britain, with detailed site- and plot-level data collected in 1971 and revisited in 2000s (2001-2003) using identical field methods.
- Aims to understand ecological change over time and identify principal drivers (e.g., atmospheric deposition of sulfur and nitrogen, climate, canopy changes, woodland management).
- Foundational publications: Kirkby et al. (2005) and Corney et al. (2004). Users should consult these for methods and analytical results.

## Data collected and scope
- At site level: general ecological descriptors; at 16 randomly located plots (each 200 m²) per site, detailed plot-level data.
- Measured variables include:
  - Plant species composition in the canopy and ground flora
  - Soil pH and Soil Organic Matter (SOM)
  - Habitat management and a wide range of plot- and site-level descriptors
- Field methods were standardized across time, enabling long-term change analyses.

## Survey design & methods
- Stratified sampling across the study area.
- Followed Bunce & Shaw (1973) standardized survey methods; a field handbook is available in supporting documentation.
- Re-surveyed in 2000s with the same field methods as in 1971.

## Data structure and key fields
- Core structure: Site, Plot, Code, Description, with associated descriptive fields.
- Site and plot identifiers:
  - Site: numeric code (1–103); Site_name (wood name where applicable)
  - Plot: numeric (1–16)
  - Code: numeric, with associated Description
  - Field_sheet categories include Site_header, Site_descriptions, Plot_header, Plot_descriptions
- Temporal and location data:
  - Slope71 vs Slope03; Aspect71 vs Aspect03
  - Easting/Northing (OSGB GB National Grid)
  - Year of survey for site descriptions
  - Date2003 (survey start; normalized to 2002 in practice)
- Data lineage fields:
  - Originator details (1971; 2001-3)
  - Supporting documentation notes and related datasets

## Derived indices and scoring
- Groupings to construct indices of ecological change:
  - wm: woodland management
  - r: tree/shrub regeneration
  - o: open habitats
  - l: adjacent land cover
- Scoring system for open habitat features:
  - Weighting (Score) of 1 or 5 to reflect size/extent (e.g., a 1–5 m wide path vs. a ride >5 m wide scores 5)
  - Final index represents abundance/extent of open habitats, weighted by openness
- Codes and code groups facilitate aggregation of site-level descriptors into meaningful indices

## Temporal coverage and data lineage
- 1971 baseline survey across 103 sites; follow-up surveys in 2000, 2002, and 2003 (referred to as 2001 in some contexts) using identical methods.
- The Date2003 field provides start-date reference; year standardized to 2002 for consistency.

## Related datasets and references
- Related dataset: Countryside Survey
- Earlier work: Steele (1968) National Survey of Woodlands
- Primary publications for methods and results:
  - Corney et al. (2004) on landscape-scale drivers of vegetation change
  - Kirkby et al. (2005) Measuring Long Term Ecological Change in British Woodlands (1971-2001)
- Originators in 1971 and 2001-3 are listed (names and affiliations provided)

## Access, usage notes, and data products
- Data are structured to enable self-serve analyses (e.g., dashboards, pivot tables) and the creation of site- and plot-level reports.
- Users should consult the cited publications for detailed analytical methods and interpretation of results.
- Potential data products:
  - Time-series comparisons of canopy and ground flora
  - Indices of woodland management, regeneration, open habitats, and adjacent land cover
  - Spatial analyses using slope/aspect, and geographic coordinates
- Considerations:
  - Data may include patchy or missing plots; data quality hinges on field methodology consistency across time
  - Complex descriptions require careful cross-walking of codes and field_sheet categories to ensure proper interpretation

## References
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales.
- Corney, PM et al. (2004). The effect of landscape-scale environmental drivers on vegetation composition in British woodlands. Biological Conservation.
- Haines-Young, R.H. et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
- Kirby, K.J. et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001). English Nature Research Reports.
- Kirkby, et al. (2005). See above publications for detailed methods and results.