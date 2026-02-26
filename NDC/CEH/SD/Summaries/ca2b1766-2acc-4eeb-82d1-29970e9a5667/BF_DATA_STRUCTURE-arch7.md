# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview
- Phenology-based dataset focused on spawning of the Common Frog as an indicator of frog population health.
- Data collected via ECN protocol with both field observations (egg masses) and laboratory analyses of pond water.
- Managed by ECN Data Centre; dataset owners are the UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.
- Acknowledgement and publication requirements: acknowledge data use and send one reprint of any publication citing the data.

## Data structure and storage
- Data are stored in Oracle databases as two main data domains:
  - D1BF_xxx: Field/phenology data (spawning observations) for site xxx
  - D2BF_xxx: Laboratory analyses related to the same site
- Site-centric organization:
  - There are 10 site-level tables for each domain (one table per site), identified by site codes (e.g., T01, T02, ..., T11).
  - Site codes include site name, location coordinates, and dataset date range (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon).
- Core metadata and field structure:
  - Core metadata tables described in accompanying metadata documentation.
  - Field fields cover sampling dates, site codes, location codes, and a wide range of measured variables.
  - Example data fields span water chemistry, spawning indicators, and related observations (see “Fieldnames” for representative variables below).
- Typical workflow for GIS use:
  - Join per-site field data (D1BF_xxx) with per-site lab data (D2BF_xxx) on site code and sampling date.
  - Use site location coordinates to map spatial patterns of spawning events and water-quality metrics over time.

## Protocol and data content
- Data collection method:
  - Spawning observed in selected pools/ditches; eggs (egg masses) counted as an indicator of health.
  - Laboratory analyses performed on water samples from observed pools.
- Field and lab data are complemented by quality information that accompanies the dataset.
- Core variables (representative examples from Fieldnames):
  - Water chemistry: alkalinity (ALKY), aluminium (ALUMINIUM), calcium (CALCIUM), chloride (CHLORIDE), conductivity (CONDY), color (COLOUR), dissolved organic carbon (DOC), ammonium (NH4N), nitrate (NO3N), phosphate (PO4P), potassium (POTASSIUM), sodium (SODIUM), sulphate (SO4S), various metals (e.g., IRON, MAGNESIUM, etc.).
  - Spawning indicators: CONGDATE (date frogs first seen congregating), NEWMASS (new spawn masses), SPAWNDATE (date of first spawning observed), SURFAREA (area covered by spawn), PERCDEAD (percentage of dead/diseased eggs), SPWAN-related dates (HATCHDATE, LEAVEDATE, etc.).
  - Physical/biological context: DEPTH, MAXTMP, MINTMP, various pH measurements (PH, PH1–PH3, PHAQCS, PHAQCU), sample volumes, filtration dates, etc.
- Quality codes:
  - ECN standard quality codes (e.g., 100–199 and 200s–239s range) indicating data issues such as no information, sample loss, partial loss, contamination, equipment failure, or field/laboratory issues.
  - A long list includes codes for hazards or anomalies (e.g., 999 for unusual events with accompanying text). Quality codes are attached per measurement or data point to document data quality.

## Site details (examples)
- T01 Drayton
  - Location: 52°11'37.95"N, 1°45'51.95"W
  - Date range in dataset: 01-JAN-1994 to 22-FEB-2012
- T02 Glensaugh
  - Location: 56°54'33.36"N, 2°33'12.14"W
  - Date range in dataset: 01-JAN-1994 to 19-JUN-2012
- T03 Hillsborough
  - Location: 54°27'12.24"N, 6° 4'41.26"W
  - Date range in dataset: 01-JAN-1994 to 25-FEB-2011
- T04 Moor House - Upper Teesdale
  - Location: 54°41'42.15"N, 2°23'16.26"W
  - Date range in dataset: 01-JAN-1994 to 10-OCT-2012
- T05 North Wyke
  - Location: 50°46'54.96"N, 3°55'4.10"W
  - Date range in dataset: 05-JAN-1994 to 28-MAR-2012
- T06 Rothamsted
  - Location: 51°48'12.33"N, 0°22'21.66"W
  - Date range in dataset: 17-FEB-1994 to 14-JUL-2010
- T08 Wytham
  - Location: 51°46'52.86"N, 1°20'9.81"W
  - Date range in dataset: 01-JAN-1994 to 17-JUN-1994
- T09 Alice Holt
  - Location: 51° 9'16.46"N, 0°51'47.58"W
  - Date range in dataset: 28-FEB-1995 to 14-MAR-2001
- T10 Porton Down
  - Location: 51° 7'37.83"N, 1°38'23.46"W
  - Date range in dataset: 14-FEB-2001 to 07-APR-2010
- T11 Y Wyddfa - Snowdon
  - Location: 53° 4'28.38"N, 4° 2'0.64"W
  - Date range in dataset: 31-DEC-1995 to 30-MAY-2012

## Data quality and provenance
- Quality assurance: site managers assign ECN quality codes to reflect data quality factors; if an issue is not covered by codes, a textual note is attached (code 999 with accompanying text).
- The accompanying quality information should be reviewed alongside data usage.

## Access, usage, and documentation
- Data origin and contact:
  - Dataset originator: ECN Data Centre
  - Data centre: ECN data portal (http://data.ecn.ac.uk)
  - Primary contact: ecn@ceh.ac.uk
- Dataset owners and sponsorship: ECN programme funded by a consortium of UK government departments and agencies (list includes Defra, Natural England, Environment Agency, Scottish Government, etc.).
- Protocol reference:
  - Terrestrial measurements: http://www.ecn.ac.uk/measurements/terrestrial/b/bf
- Usage acknowledgment:
  - Please acknowledge ECN data use and send one reprint of any publication citing the data.
- Metadata and structure:
  - Core metadata tables and additional metadata documentation exist to describe the overall dataset structure and fields.

## GIS-specific considerations
- The dataset is designed for map-based data products, enabling visualization of frog spawning events and associated water-quality variables across multiple sites and over time.
- Suggested GIS workflow:
  - Build a spatial layer using site coordinates (from site metadata).
  - Join field data (D1BF_xxx) and lab data (D2BF_xxx) by SITECODE and sampling date (SDATE) to create enriched records for mapping.
  - Use quality codes to filter or annotate data quality in spatial visualizations.
- Data preparation notes:
  - Be aware of date formats (dd-mmm-yyyy) and ensure consistent temporal alignment when combining datasets.
  - Consider resampling or aggregating cross-site data where necessary to support comparative mapping across years or sites.

## Key takeaways for GIS usage
- Rich, site-level, time-series data on frog spawning and pond water chemistry, organized per site with clear coordinates and date ranges.
- Two linked data domains (field observations and lab analyses) provide a comprehensive basis for spatial-temporal mapping of environmental change signals related to amphibian populations.
- A robust quality-coding system helps assess and annotate data reliability for mapping outputs.