# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Baseline (VB) Dataset

## Overview
- Origin and ownership: ECN Data Centre (Centre for Ecology and Hydrology); dataset owned by a consortium of UK government departments and agencies.
- Sponsorship: Agri-Food and Biosciences Institute; BBSRC; Cyfoeth Naturiol Cymru; Defra; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- Purpose: Baseline vegetation dataset to understand environmental change causes and consequences; supports long-term monitoring and research on vegetation types and associated features.
- Usage note: Acknowledgement requested; provide one reprint of any publication citing the data.

## Data structure and access
- Storage: 12 site-specific tables in an Oracle database (D1VB_xxx and D2VB_xxx per site).
- Core data tables: D1VB_xxx with SITECODE, SYEAR, PLOTPID, PLOTTYPE, FIELDNAME, VALUE.
- Plot information: D2VB_xxx with SITECODE, PLOTPID, SDATE, FEATURES, UNSURVEYED, plus additional fields.
- Metadata: Core data reference tables (M_DESC, M_REFFIELD) and separate core metadata documentation.
- Data formats and units: Fields include SITECODE (string), SYEAR (integer), PLOTPID (integer), PLOTTYPE (S or W), FIELDNAME (species/quality code), VALUE (numeric, optional); D2VB fields include SDATE, FEATURES, UNSURVEYED.
- Outputs: Dashboards, pivot tables, reports/charts, and accompanying quality metadata to aid interpretation.

## Sampling protocol and data collection
- Sampling grid: Approximately regular grid aligned with the National Grid; ~400 sample positions per site; up to 100 infill points in under-represented vegetation types.
- Plot design: 2 m x 2 m plots centered on each grid or infill point; plots oriented to cardinal directions; permanent marking for long-term monitoring.
- Data collected per plot: Species list (presence/absence or abundance); one-off survey to generate vegetation maps and select plots for long-term monitoring.
- Data availability: Continuous monitoring data (coarse/fine-grain, woodland vegetation surveys) available via ECN Data Centre and Environmental Information Platform.
- Output emphasis: Data prepared for map creation and long-term trend analysis; quality metadata provided to aid use.

## Site codes and coverage
- 12 sites (T01–T12) with names, coordinates, and data date ranges (e.g., Drayton T01, Glensaugh T02, Hillsborough T03, Moor House - Upper Teesdale T04, North Wyke T05, Rothamsted T06, Sourhope T07, Wytham T08, Alice Holt T09, Porton Down T10, Y Wyddfa - Snowdon T11, Cairngorms T12).
- Date ranges vary by site, spanning early 1990s to around 2000.

## Data structure details and fields
- Core data (D1VB_xxx): SITECODE, SYEAR, PLOTPID, PLOTTYPE (S = standard, W = woodland), FIELDNAME (species or quality code), VALUE (numeric, optional).
- Plot information (D2VB_xxx): SITECODE, PLOTPID, SDATE, FEATURES (composite code), UNSURVEYED (percentage), plus core metadata and measurement details.
- Documentation: Site/plot details stored per site code; use the accompanying quality information when using data.

## Species and feature codes
- Features: Codes for landscape features such as P (Path), W (Wall), S (Stream), H (Hedge), D (Ditch), F (Fence), B (Bank), N (Natural boundary), X (No feature).
- Species codes: Large mappings from numeric codes to Latin names and to BRC database concepts; includes synonyms and taxonomic references.
- Data capture: FIELDNAME and VALUE convey presence/absence or abundance for species; extensive code-to-name mappings are documented within dataset documentation.

## Quality and usage
- Quality codes: ECN standard quality codes (e.g., 100–513) indicating data quality factors (no information, sample issues, partial loss, equipment and environmental effects, etc.).
- Unusual events: Code 999 used for unusual events, with explanatory text in the accompanying quality information.
- Guidance: Users should consult the quality metadata to understand data limitations, formats, and transformations.

## Access and contact
- Data Centre: ECN Data Centre (data.ecn.ac.uk)
- Support contact: ecn@ceh.ac.uk
- Platform: Oracle-based database hosting 12 site-specific tables (D1VB_xxx, D2VB_xxx) with comprehensive metadata documentation.