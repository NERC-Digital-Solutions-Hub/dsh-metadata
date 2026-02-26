# Data access

## Overview
- ECN Data Centre dataset documenting counts of animal droppings (deer, grouse, rabbit, sheep) across multiple UK environmental sites.
- Uses an index method (droppings counts) to estimate relative abundance; transect-based data collected twice yearly (late March and late September).
- Data are organized for GIS-friendly mapping and multi-site comparison; standard operating procedures ensure cross-site comparability.

## Data provenance and ownership
- Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Data owners: UK Environmental Change Network (ECN) sponsors, with multiple government departments and agencies listed.
- Usage acknowledgement requested; authors also ask for one reprint of any publication citing the data.

## Access and identifiers
- Data accessible at: https://doi.org/10.5285/0be0aed3-f205-4f1f-a65d-84f8cfd8d50f
- Supporting information and catalogues available via ECN and CEH links provided in the document.

## Data structure and downloads
- Main data schema uses the following fields:
  - SITECODE: Unique code for each ECN site
  - LCODE: Location ID (unique within site)
  - SDATE: Sampling date
  - PLOTID: Transect section
  - FIELDNAME: Variable measured (D, G, R, S, or quality fields Q1–Q8)
  - VALUE: Measured value
- Supporting documentation files:
  - ECN_BU2.csv: Survey information (SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY)
  - ECN_BU3.csv: Transect information (SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC)
  - ECN_BU_qtext.csv: Quality text and codes (SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION)
- Quality information:
  - ECN quality codes are extensive (examples: 100–999), with detailed meanings for data quality issues and field operating conditions.
  - A separate quality text file (ECN_BU_qtext.csv) provides descriptive context for non-standard or ongoing quality concerns.

## Site codes and locations (Explanatory Information)
- T01 Drayton: 52°11'37.95"N 1°45'51.95"W
- T03 Hillsborough: 54°27'12.24"N 6° 4'41.26"W
- T04 Moor House - Upper Teesdale: 54°41'42.15"N 2°23'16.26"W
- T05 North Wyke: 50°46'54.96"N 3°55'4.10"W
- T06 Rothamsted: 51°48'12.33"N 0°22'21.66"W
- T07 Sourhope: 55°29'23.47"N 2°12'43.32"W
- T08 Wytham: 51°46'52.86"N 1°20'9.81"W
- T09 Alice Holt: 51° 9'16.46"N 0°51'47.58"W
- T10 Porton Down: 51° 7'37.83"N 1°38'23.46"W
- Explanatory information and site catalogues are available at CEH and ECN portals.

## Variables and measurements
- FIELDNAME options:
  - D: Count of deer droppings (units: count)
  - G: Count of grouse droppings (units: count)
  - R: Count of rabbit droppings (units: count)
  - S: Count of sheep droppings (units: count)
  - Q1–Q8: Quality codes (integer units) describing data quality factors
- The accompanying quality code descriptions cover a wide range of potential data issues (e.g., sample loss, equipment problems, environmental disturbances).

## Quality assurance and usage notes
- Use accompanying quality information when analyzing data.
- Quality codes provide context for data reliability; 999 indicates an unusual event requiring narrative in ECN_BU_qtext.csv.
- Some datasets/fields may have non-standard sampling dates/times or non-standard procedures; consult ECN_qtext for details.
- Index-based abundance estimates mean results are relative, not absolute population counts.

## Usage guidance for GIS specialists
- Data are suitable for map-based visualization of site-level abundance trends and transect-level comparisons.
- Integrate site coordinates with SITECODEs to plot site locations; use LCODE and PLOTID to display transects.
- Leverage quality codes to layer data reliability, enabling users to filter or flag uncertain observations.
- Use supporting CSVs (ECN_BU2, ECN_BU3, ECN_BU_qtext) to enrich GIS datasets with survey dates, transect extents, and quality context.

## Related resources
- Explanatory site information: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27
- ECN site catalogue and further information available via ECN/CEH portals.