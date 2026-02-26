# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Aims for GIS specialists: create map-based data products that reveal spatial patterns of vegetation across ECN sites and years, enabling analysis and exploration by policy colleagues, clients, or the public.
- Audience and workflow: data analysts in GIS collaborate with end users, verify and clean data, transform and merge datasets, and iteratively test prototypes with feedback.

## What the dataset covers

- Site coverage: vegetation data collected across ECN sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
- Spatial granularity:
  - Plot level: 10 m x 10 m plots within each NVC type.
  - Cell level: 40 cm x 40 cm cells within each plot.
- Temporal aspect:
  - Core surveys every three years.
  - Some sites conduct annual surveys for higher temporal resolution with smaller plot counts.
- Attribution and usage: ECN data usage should be acknowledged; one reprint of any publication citing ECN data.

## How the data are structured (GIS-ready)

- Main data file fields: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE.
  - FIELDNAME distinguishes data type (VEG_SPEC for species code or Q1/Q2/Q3 for quality codes).
- Plot metadata (ECN_VF2.csv):
  - SITECODE, SYEAR, PLOTPID, SDATE, PEDATE, LANDUSE, SLOPE, ASPECT, SLOPEFORM, NVCCLASS.
- Cell metadata (ECN_VF3.csv):
  - SITECODE, SYEAR, PLOTPID, CELLID, FEATURE.
- Quality metadata (ECN_VF_qtext.csv):
  - SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
- Quality codes: Q1–Q3 with textual descriptions; 999 indicates an unusual event (accompanied by descriptive text in ECN_VF_qtext.csv).

## Data standards and coding schemes (GIS context)

- Site codes: T01, T02, …, T12 with site names and coordinates.
- Land use codes: Hodgon/Hoddsdon codes describing land use (e.g., grassland, cereals, woodland, etc.).
- Slope form: Convex, Straight, Concave (Hodgson codes).
- Features: Path, Wall, Stream, Hedge, Ditch, Fence, Bank, Natural boundary, No feature.
- Species codes: ECN/VESPAN codes cross-referenced to Biological Records Centre (BRC) concepts; extensive cross-references for names, codes, and BRC concepts.
- Data structure supports joining site-level metadata (ECN_VF2.csv) with cell-level data (main file) using SITECODE, SYEAR, PLOTPID, and CELLID.

## GIS workflows and practical use

- Build a site-by-year grid of 40 cm cells with species presence as attributes.
- Join attributes across files using SITECODE, SYEAR, PLOTPID, and CELLID (and related site metadata).
- Attribute interpretation:
  - VEG_SPEC entries map to species presence (ECN/VESPAN) or to quality indicators (Q1–Q3).
  - QUALITY notes provided in ECN_VF_qtext.csv give context for data quality.
- Contextualization: incorporate LANDUSE, SLOPE, ASPECT, SLOPEFORM, and NVCCLASS to analyse patterns in vegetation presence.
- Quality control: use Q1–Q3 with accompanying textual descriptions; 999 indicates unusual events requiring special handling.
- Practical outputs: rasterized or vector vegetation maps by year, with per-cell species presence and quality annotations.

## Explanatory information: species and quality codes

- Species codes:
  - Extensive mappings between ECN/VESPAN codes and other taxonomic concepts (e.g., Rumex obtusifolius linked to multiple synonyms and related taxa).
  - The Explanatory Information section provides detailed pairings for many species-name mappings to support accurate interpretation in GIS analyses.
- Quality codes:
  - Range from 100–188, 200–299, 501–513, up to 999 (Unusual event).
  - Descriptions cover information loss, sampling issues, environmental influences, and laboratory/field data complications.
  - The 999 code denotes an unusual event and is described in the accompanying quality text file.

## Attribution, publication notes, and contact

- Originator and contact: ECN Data Centre, Centre for Ecology and Hydrology (data@ecn.ac.uk).
- Ownership and sponsorship: UK Environmental Change Network (ECN) programme, funded by government departments and agencies.
- Attribution requirements: acknowledge ECN data; provide one reprint of publications citing ECN data.

## Quick-reference data items (summary)

- Main data file structure: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE.
- Plot metadata: SDATE, PEDATE, LANDUSE, SLOPE, ASPECT, SLOPEFORM, NVCCLASS.
- Cell metadata: SITECODE, SYEAR, PLOTPID, CELLID, FEATURE.
- Quality metadata: SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
- Species and codes: ECN/VESPAN codes cross-referenced to BRC concepts.

- Note: The dataset provides a comprehensive, codified framework for mapping and analyzing ECN vegetation data across multiple sites and years, suitable for GIS-based visualization and analysis.