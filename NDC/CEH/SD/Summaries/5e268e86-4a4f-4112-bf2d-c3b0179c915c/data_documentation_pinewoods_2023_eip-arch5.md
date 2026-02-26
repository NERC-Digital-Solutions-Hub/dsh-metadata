# Dataset Scottish Pinewood Survey 2018-2022: Habitat, vegetation, tree and soil data from Native Pinewoods in Scotland, 2018-2022

- A detailed ecological survey of Scotland’s native Scots pinewoods conducted between 2018 and 2022, repeating the 1971 baseline across 27 woodlands.
- Purpose: define ecological variation, enable environmental monitoring, and support conservation planning using standardized methods.

## Geographic and temporal scope

- Geographic coverage: 27 major native Scots pinewoods across Scotland (list of sites includes Glentanar, Ballochbuie, Mar Lodge, Abernethy, Rothiemurchus, Glenmore, Black Wood of Rannoch, Shieldaig, Loch Arkaig and Glen Mallie, and others).
- Time period: data collected 2018–2022; some sites contain additional plots beyond the 16 per site.
- Spatial data for sites: provided as approximate locations with OS grid references (SCOTS_PINE_2022_SITES.csv).

## Data structure and content

- Data files included (CSV format) with accompanying metadata:
  - SCOTS_PINE_2022_SITES.csv: approximate woodland locations (SITEID, SITE_NAME, OSGR, EASTING, NORTHING).
  - SCOTS_PINE_2022_SITE_INFO.csv: site-wide and plot-level descriptions, including habitat descriptions, slope, aspect, survey dates, and data categories.
  - SCOTS_PINE_2022_TREE_DATA.csv: tree-level data per plot, including SITE_NO, PLOT_NO, TREE_ID, TREE_TYPE, SPECIES, DBH, DEAD status.
  - SCOTS_PINE_2022_GROUND_FLORA.csv: ground flora records for each plot, including vascular plants and bryophytes, with species names, cover, growth form, and nest-level observations.
  - SCOTS_PINE_2022_SOIL_DATA.csv: soil data per plot, including pH (fresh and air-dried), LOI (%), and soil date.
- Sampling design:
  - In each wood: 16 randomly assigned 200 m2 quadrats (plots) surveyed, following Bunce & Shaw (1973) methods; some sites (site 4, Abernethy) include additional plots (up to 50 in some ancillary plots).
  - Vegetation categories per plot:
    - Trees, saplings, and shrubs (recorded by individual stems)
    - Vascular plants (species lists with nested quadrats: 4 m2, 25 m2, 50 m2, 100 m2, 200 m2; % cover by 5% bands and presence/absence)
    - Bryophytes (ground flora)
  - Soil data: pH and LOI measured on topsoil (0–15 cm) using a standard coring method.
  - Habitat data: predefined habitat categories with slope and aspect measurements; site-level and plot-level descriptions.

## Methodology and standards

- Original basis: 1971 survey of major native pinewoods (Steven & Carlisle 1959); 2018–2022 repeat survey using the same woods and standardized methods to enable environmental monitoring and change assessment.
- Survey methods and data documentation:
  - Field methods documented in Bunce & Shaw (1973) and Smart & Wood (2021) field handbook; nomenclature for vegetation follows Stace (1997).
  - Nested quadrat approach for vascular plants; detailed species-level recording for trees, saplings, shrubs, bryophytes, and ground flora.
  - Habitat categorization, slope, and aspect recorded with defined measurement procedures (clinometer for slope; compass for aspect).
- Data provenance:
  - Prepared by UK Centre for Ecology & Hydrology (Lancaster) with field survey team including named surveyors and associated institutions.
  - Soil analyses coordinated with UKCEEH and Lancaster laboratories; land permissions coordinated by dedicated teams.
- Data quality and reproducibility:
  - Use of standardized field sheets and codes; explicit data dictionaries in accompanying site information.
  - OSGB36 coordinates for site localization; consistent data formats across files to facilitate integration and reuse.

## Governance, access, and reuse considerations for Data Stewards

- Metadata and provenance:
  - Clear documentation linking data to original field methods, field handbook (2021), and baseline 1971 methodology.
  - Source data include multiple codified fields (CODE_GROUP, CODE, DESCRIPTION) to support interpretation and interoperability.
- Data interoperability:
  - Data are organized into cohesive, related CSV files with site-level and plot-level granularity; consistent species nomenclature (Stace 1997) and measurement units (DBH in cm, LOI in %, pH values, etc.).
  - Cross-references to related datasets (1971 baseline, standardized procedures) support longitudinal analyses.
- Scope and limitations:
  - 27 woods with 16 plots each (some sites have additional plots); spatial coverage is approximate for some sites.
  - Some site-level nuances (e.g., site 4 Abernethy additional plots) noted; codes and habitat classifications are detailed in the field handbook.
- Documentation and attribution:
  - Document version 1.1 (as of 25/8/2023); primary authors and institutional affiliations listed; field team and laboratory collaborators acknowledged.
- Usage guidance:
  - Users should consult the accompanying site information to interpret plot-level data (habitat codes, slope/aspect classifications, and data sheet descriptions).
  - Data should be analyzed in the context of the 1971 baseline for change detection and conservation planning.

## Related resources and references

- Field handbooks and methodologies:
  - Bunce, R.G.H., & Shaw, M.W. (1973). Standardized procedure for ecological survey.
  - Smart, S.M., & Wood, C.M. (2021). National Woodland Survey & Native Pine Survey Field Handbook.
  - Stace, C. (1997). New flora of the British Isles.
- Foundational studies:
  - Steven, H.M., & Carlisle, A. (1959). The Native Pinewoods of Scotland.
  - Wood, C.M., & Bunce, R.G.H. (2016). Ecological survey of the native pinewoods of Scotland 1971 (Earth Syst. Sci. Data).
- Related datasets:
  - Scottish Pinewood Survey 1971 (baseline)
  - Bunce National Woodland Survey 1971 (baseline context)
- Originators and collaborating institutions:
  - UK Centre for Ecology & Hydrology, Lancaster
  - Field surveyors and supporting teams (listed in document)