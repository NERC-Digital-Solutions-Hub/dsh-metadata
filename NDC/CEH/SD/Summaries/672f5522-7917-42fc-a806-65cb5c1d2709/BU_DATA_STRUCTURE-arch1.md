# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU)

## Overview
- A dataset collection from the UK Environmental Change Network (ECN) focusing on rabbits, deer, and related transect observations across multiple sites.
- Data are intended to support understanding of environmental change effects via relative abundance indices rather than direct population counts.

## Provenance and access
- Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset Owners: A consortium of UK government departments and agencies (e.g., DEFRA, Natural England, Environment Agency, NERC councils, Welsh and Scottish administrations, etc.).
- Usage acknowledgement: ECN requests acknowledgement of data use and one reprint of any publication citing the data.

## Protocol and study design
- Sampling frequency: Dropping counts recorded on a transect twice yearly (late March and late September).
- Abundance estimation: Direct population size cannot be measured; uses an index based on droppings as a relative abundance proxy.
- Moor House method: The same methodology applied to estimate relative grouse abundance at Moor House.
- Quality information: Always use accompanying quality metadata when using the data.

## Data structure and schema
- Core organization: Data stored in 9 site-specific tables across three dataset types (per site):
  - D1BU_xxx: Survey data
    - Key fields: SITECODE, LCODE, SDATE, PLOTID, FIELDNAME, VALUE
  - D2BU_xxx: Droppings data
    - Key fields: SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY
  - D3BU_xxx: Transects data
    - Key fields: SITECODE, LCODE, PLOTID, LENGTH, HABDESC
- Site codes and scope: Data cover 10 sites (T01–T10), each with site-specific code and metadata.

## Site codes and temporal coverage
- T01 Drayton: 01-APR-1993 to 11-OCT-2006
- T03 Hillsborough: 07-JUN-1995 to 02-MAY-2012
- T04 Moor House - Upper Teesdale: 14-MAY-1993 to 10-OCT-2012
- T05 North Wyke: 23-MAR-1993 to 28-SEP-2012
- T06 Rothamsted: 11-APR-1994 to 18-OCT-2010
- T07 Sourhope: 12-MAY-1993 to 28-SEP-1993
- T08 Wytham: 06-MAY-1993 to 01-OCT-2012
- T09 Alice Holt: 10-OCT-1994 to 10-NOV-2006
- T10 Porton Down: 22-APR-1994 to 17-APR-2012

## Field definitions (measurement data)
- D: Count of deer droppings (units: count)
- G: Count of grouse droppings (units: count)
- R: Count of rabbit droppings (units: count)
- S: Count of sheep droppings (units: count)
- Q1–Q8: Quality codes (each with a quality code and a corresponding value/description)

## Quality codes and interpretation
- ECN quality codes indicate data quality factors; codes cover common issues (e.g., no information, sample loss, debris in funnel, environmental disturbances, instrument problems, etc.).
- 999: Unusual event – additional explanatory text may accompany the dataset.
- The list includes hundreds of specific codes (e.g., 100 No information available; 101 No sample/reading taken; 140 Debris in funnel = Chemicals applied; 141–176 various grazing and environmental/disturbance factors; 501–512 laboratory and analytical issues; 999 unusual event, etc.).
- Site managers assign multiple applicable codes per field; when needed, free-text quality notes accompany the codes.

## Usage notes and caveats
- Population estimates are indices (relative abundance) rather than absolute counts.
- Data quality is annotated with a structured quality code system; users should consult quality codes and associated text before analysis.
- Data come from multiple sites with varying date ranges, requiring careful alignment when combining site data for analyses.

## Metadata and contact
- Core metadata structure is documented separately; see ECN metadata documentation for full schema.
- Data availability and contact: ECN Data Centre (ecn@ceh.ac.uk); data usage should follow the protocol and acknowledgment guidelines.