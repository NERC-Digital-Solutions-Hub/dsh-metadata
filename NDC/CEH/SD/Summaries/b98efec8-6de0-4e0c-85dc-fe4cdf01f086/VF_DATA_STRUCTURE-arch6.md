# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Data from the UK Environmental Change Network (ECN) programme to understand environmental change via standardized site monitoring.
- Dataset includes species presence data on plots within sites across years, with site and cell metadata.

## Data Ownership and Acknowledgement
- Owners: ECN programme, supported by a consortium of UK government departments and agencies.
- Usage: Acknowledge ECN data and provide one reprint of any publication citing the data.

## Protocol and Quality
- Standard operating procedures ensure site comparability; protocol documentation outlines data collection methods.
- Observations carry quality codes; detailed quality context provided in accompanying documentation.

## Sampling Design and Usage Notes
- Design: At least two 10m x 10m plots per NVC type at a site; species presence recorded in 40cm x 40cm cells within plots.
- Frequency: Surveys every three years; some sites conduct annual surveys with fewer plots for temporal resolution.
- Quality: Analyze using accompanying quality information.

## Data Downloads and Structure
- Core data fields: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME (VEG_SPEC for species codes or Q for quality codes), VALUE (species or quality code).
- Supporting Documentation:
  - ECN_VF2.csv: Site/Plot metadata (SITECODE, SYEAR, PLOTPID, SDATE, PEDATE, LANDUSE, SLOPE, SLOPEFORM, NVCCLASS).
  - ECN_VF3.csv: Cell-level information (SITECODE, SYEAR, PLOTPID, CELLID, FEATURE).
  - ECN_VF_qtext.csv: Quality text explanations (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).
- Site Codes: T01–T12 with site names and coordinates (e.g., Drayton, Glensaugh, Hillsborough, etc.).
- Explanatory Metadata:
  - Land Use (Hodgson codes) with descriptions (e.g., Ley grassland, Cereals, Deciduous woodland).
  - Slope Form codes (Convex, Straight, Concave); Features (Path, Wall, Stream, Hedge, etc.).
  - Species codes: ECN uses VESPAN with cross-reference to other codes and Latin names; extensive mapping provided.

## Data Quality and Use Considerations
- Observations include quality indicators; quality context is available in ECN_VF_qtext.csv (e.g., 999 for unusual events).
- For analysis, join the main data with ECN_VF2 (plot metadata), ECN_VF3 (cell features), and ECN_VF_qtext (quality context) to interpret data quality and context.
- Cross-site comparability relies on the standard protocols and accompanying metadata.

## Practical Data Support Guidance
- Data Integration:
  - Link observations by SITECODE, SYEAR, PLOTPID, and CELLID to site/plot metadata and cell features.
- Data Cleaning and QC:
  - Filter or flag records with quality codes (Q1–Q3) and review 999 unusual events via ECN_VF_qtext.csv.
  - Normalize land use and slope form categories using Hodgson codes and provided descriptions.
- Analysis-ready Outputs:
  - Site-level summaries: species richness, presence/absence by year, plot-level variability.
  - Temporal analyses: inter-annual variability (annual subsets vs. 3-year cycles).
  - Spatial context: map sites with coordinates; link to land use and slope characteristics.
- Dashboard/Product Ideas:
  - Self-serve dashboards: species presence by site/year/plot; plot-level cell data; quality-flagged records.
  - Dashboards to compare NVCCLASS (NVC class) distribution across sites and years.
- Governance and Reuse:
  - Acknowledge ECN data; consider sending a reprint for publications using the data.

## Access and Contact
- Data provided in structured CSV formats with accompanying documentation; join keys include site, year, plot, and cell identifiers.
- For questions or assistance, consult ECN Data Centre contact details in the dataset header.

## Explanatory Information: Species codes (highlights)
- The dataset includes extensive species code mappings (e.g., Rumex obtusifolius variants, Scapania degenii mappings, Sorbus aucuparia variants) linking common names to multiple code references.
- Many-to-many and cross-referenced mappings exist to accommodate synonyms and taxonomy variants; use the provided mappings to translate codes to species names.

## Explanatory Information: Quality Codes (highlights)
- Quality codes span broad categories, including:
  - 100: No information available
  - 101–139, 140s, 160s–230s: various in-field and laboratory context issues (sampling, contamination, disturbance, equipment, etc.)
  - 501–507: laboratory-related notes
  - 999: Unusual event (see quality text)
- A detailed mapping accompanies the dataset to interpret each code in context during data cleaning and analysis.