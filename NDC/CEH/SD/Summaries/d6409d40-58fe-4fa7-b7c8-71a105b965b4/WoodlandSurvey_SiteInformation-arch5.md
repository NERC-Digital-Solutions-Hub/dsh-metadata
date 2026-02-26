# Woodlands Survey Site Information 1971-2001

## Overview
- Nation-wide ecological survey of 103 broadleaved woodlands in Britain (begun 1971; re-surveyed 2000s).
- Data collected at site level and within 16 randomly selected 200 m² plots per site.
- Field measurements include plant species composition (canopy and ground flora), soil pH, soil organic matter, habitat management, and a broad set of site/plot descriptors.
- Repeated surveys used identical methods to assess ecological change and identify drivers (e.g., atmospheric deposition of sulphur and nitrogen, climate, canopy changes, management).
- Results linked to published analyses (Kirkby et al. 2005; Corney et al. 2004); users are advised to consult those publications for methods and findings.

## Data Content
- Site-level and plot-level data across two survey periods (1971 and 2000s/2001 reference).
- 103 sites with 16 plots each; data include:
  - Site: code (1–103), name, country, easting/northing, slope and aspect (1971 vs 2000s), site usage, survey dates, and recorder initials.
  - Plot: plot number (1–16), plot descriptors, and site/plot description codes.
  - Descriptive fields: textual descriptions, notes, codes and groupings for site descriptions (e.g., management, regeneration, open habitats, adjacent land cover) with weighted scores for open habitat features.
  - Measurements and indices: soil pH, soil organic matter, vegetation composition (canopy and ground flora), as well as derived indices related to habitat openness.
- Data structure uses numeric, text, and date formats; coordinates are OSGB GB National Grid in kilometres; 2003 survey date is standardized to 2002 in the dataset.

## Data Structure and Metadata
- Detailed data dictionary with field names, formats, and descriptions (Site, Plot, Code, Description, Notes, Code_group, Code_group_dsc, Score, Year, Field_sheet, etc.).
- Groupings allow construction of indices for woodland management (wm), regeneration (r), open habitats (o), and adjacent land cover (l).
- Special weighting applied to open habitat features (e.g., paths vs rides) to reflect size.
- Documentation notes:
  - 2003 date standardized to 2002 for consistency.
  - Supporting documentation clarifies year of survey for certain records.
  - Field handbook and standardized survey methods (Bunce & Shaw 1973) used; original field sheets include site and plot sections (Site header, Site descriptions, Plot header, Plot descriptions).

## Provenance and Data Quality
- Originators and collaborators by era:
  - 1971: Bunce and Shaw (Nature Conservancy) with Woodland Ecology Section, Merlewood.
  - 2001–2003: Smart, Black (CEH Lancaster); Kirby (English Nature); Corney (Liverpool) and colleagues.
- Methods and data collection aligned to standard field procedures; identical methods reused across years to enable reliable change detection.
- Supporting documentation exists to aid interpretation of field data and methodological context.
- Original analyses (e.g., spatial drivers, drivers of change) are documented in associated publications; raw data and metadata support reproducibility and re-use.

## Access, Sharing, and Use
- Dataset designed to support long-term ecological analyses and assessment of drivers of woodland change.
- Rich metadata and field documentation facilitate reuse by data managers and researchers.
- Related datasets and publications referenced (e.g., Countryside Survey; English Nature reports; related bibliographic sources) to enable broader integration.
- Data sharing practices are supported by persistent identifiers and documented provenance; users are directed to consult primary publications for analytical context.

## Related Datasets and Publications
- Related dataset: Countryside Survey; other historical woodland surveys (e.g., Steele 1968).
- Publications detailing methods and findings:
  - Kirby et al. (2005): Measuring Long Term Ecological Change in British woodlands (1971–2001).
  - Corney et al. (2004): Landscape-scale drivers of vegetation composition.
  - Supporting literature on soil classification and vegetation management.

## Challenges and Considerations for Data Stewards
- Ensuring a complete picture of user needs and the intended analyses for long-term woodland data.
- Timely acquisition of data from site surveyors and collaborators; maintaining consistency across years.
- Achieving and preserving metadata standards (codes, groups, weights) across multiple survey periods and field sheets.
- Interoperability across various data descriptors, formats, and field sheets (Site Header, Site Descriptions, Plot Headers, Plot Descriptions).
- Handling large, longitudinal datasets with consistent spatial references (OSGB coordinates) and standardized date conventions.
- Documenting and updating data provenance, including changes in survey methods, personnel, and date standardizations, to support transparent re-use.