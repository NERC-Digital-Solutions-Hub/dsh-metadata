# Bunce Woodland Survey of Great Britain 2020-2022

## Aim and Coverage
- Repeat survey of broadleaved woodlands across Britain conducted 2020–2022.
- 97 woodland sites surveyed (Great Britain) using the same field methods as earlier surveys (1971; 2000–2003; referred to as ‘2001’).
- Data collected at site level and in detail from 16 randomly located 200 m² plots per site.
- Purpose: enable analyses of ecological change since the 2000–2002 survey; supports long-term ecological change assessment.

## Data Components and Content
- Data categories and corresponding datasets (CSV format):
  - WOODLANDS_SURVEY_SITES_2022.csv: Approximate locations of surveyed woodlands; SITE_NUMBER (1–103), SITE_NAME, OSGB36 coordinates; note that 97 sites were accessible (some not granted access).
  - WOODLANDS_SURVEY_SITE_INFORMATION_2022.csv: Descriptions of surveyed sites and plots, including habitat descriptions, slope, aspect, locations, survey dates, and grouping codes.
  - WOODLANDS_SURVEY_TREE_DATA_2022.csv: Tree data per plot, including SITE_NO, SITE, PLOT_NO, QUARTER, TREE_TYPE, DBH, species (SP_CODE, SPECIES), and related fields.
  - WOODLANDS_SURVEY_GROUND_FLORA_2022.csv: Ground flora records for plots (vascular plants, bryophytes, lichens), including species codes, cover values, growth forms, and related metadata.
  - WOODLANDS_SURVEY_SOIL_DATA_2022.csv: Plot soil analyses (pH, LOI, soil type/date, codes for missing data, notes); includes MISSING_CODE and S_SAMPLE_NOTES.
- Data scale and structure:
  - 97 sites with multiple plots per site (16 plots per site) and site-level descriptors.
  - Standard nomenclature and coding referenced to field handbook and taxonomic references (e.g., Stace 1997).

## Methods, Provenance and Related Datasets
- Survey design and methods:
  - Stratified sampling across the study area.
  - Field methods aligned with Bunce & Shaw (1973) standardized ecological survey procedures.
  - Field handbook: Smart, S. M. and Wood, C. M. (2021) National Woodland Survey & Native Pine Survey Field Handbook.
- Originators and field team:
  - Originators: S.M. Smart, C.M. Wood, F. M. Seaton (UK Centre for Ecology & Hydrology, Lancaster).
  - Field surveyors include multiple named individuals; soil analyses by C. Benskin and team.
- Relationship to earlier work:
  - Built as a repeat of the 1971 Bunce survey, with subsequent repeats 2000–2003 (2001) and now 2020–2022.
  - Enables comparisons with Bunce 1971, Bunce 2000–2003, Countryside Survey, and Scottish Pinewood Survey baselines.
- Related datasets and publications:
  - Bunce National Woodland Survey 1971 (and 2000–2003).
  - Countryside Survey; Scottish Pinewood Survey 1971 (and 2018–2022).
  - References include field methods and prior analyses (e.g., Bunce & Shaw 1973; Smart & Wood 2021; Stace 1997).

## Access, Documentation and Data Governance
- Access notes:
  - Some sites were not granted access in the 2020–2022 survey (indicated by asterisks in the site list).
- Data documentation:
  - Descriptions provided for each dataset, including field codes, groupings, and data sheet origins.
  - Coordinates provided in OSGB36 (BNG) for site locations.
- Data versioning:
  - Document version: 1.1 (August 2023) prepared by UKCEH Lancaster.

## Data Quality, Limitations and Metadata
- Data quality and QC:
  - Metadata includes quality control notes; MISSING_CODE fields capture missing data.
  - Some issues noted: 7 samples with missing plot numbers; certain codes not applicable to particular groupings.
- Data limitations:
  - Incomplete site access limiting the full 103-site potential; 97 sites included.
  - Variability in data completeness across plots (e.g., soil sampling date availability, missing soil numbers).
- Nomenclature and standards:
  - Plant identifications aligned with Stace (1997).
  - Species and codes use Biological Records Centre (BRC) coding scheme where applicable.
  - Data sheets and coding conventions linked to the 2021 field handbook.

## Practical Use and Governance Implications for Data Stewards
- Governance and stewardship:
  - Clear provenance, versioning, and method documentation support data curation and reuse.
  - Five integrated datasets enable cross-cutting analyses (site, plot, tree, ground flora, soil) with consistent identifiers (SITE_NO, SITE_NAME, PLOT_NO).
- Interoperability considerations:
  - Standardized field methods and taxonomic references support cross-dataset analyses and linkage with earlier Bunce surveys.
  - Data stored as CSV with explicit field definitions, codes, and notes facilitating ingestion into data portals and catalogues.
- Reuse and attribution:
  - Primary sources: Smart, Wood, and colleagues; field handbook (2021) and foundational Bunce surveys.
  - Useful for longitudinal woodland ecology studies, climate/management impact assessments, and national woodland inventories.
- Future updates:
  - Repeats and ongoing monitoring could be integrated with this framework to maintain longitudinal continuity.

## References and Further Reading
- Bunce R.G.H. & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey.
- Smart, S.M. and Wood, C.M. (2021). National Woodland Survey & Native Pine Survey Field Handbook.
- Stace, C. (1997). New flora of the British Isles.
- Additional readings on long-term ecological change and related woodland surveys listed in the document.