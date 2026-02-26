# Dataset Originator

- A data resource originating from the ECN Data Centre (Centre for Ecology and Hydrology) with the ECN program coordinated across UK partner organisations.
- Data providers include a consortium of UK government departments and agencies funding site monitoring or network coordination (e.g., Defra, Natural England, Environment Agency, Forestry Commission, Natural Resources Wales, Scottish Government agencies, NERC, etc.).
- Acknowledgement: ECN requests acknowledgement of data use and a reprint of any publication citing ECN data.

## Visualisation and GIS context

- The dataset is designed for cross-site comparability and integration into GIS-based analyses and visualisations for environmental monitoring and change research.

## Protocol and Data Quality

- Standard operating procedures are used to ensure data comparability across ECN sites; a separate document (wc.pdf) explains data collection methods.
- Usage notes emphasize data quality controls, including:
  - Weekly dip sampling for stream water chemistry.
  - Quality control (QC) solution analyses run in parallel with field samples.
  - Quality information accompanying the dataset should be used for proper interpretation.

## Data Structure and Download Format

- Core fields in the main data download:
  - SITECODE: Unique ECN site code.
  - LCODE: Location ID (unique within the site).
  - SDATE: Sampling date.
  - FIELDNAME: Variable measured.
  - VALUE: Measured value.
- Supporting documentation files (with additional metadata):
  - ECN_WC2.csv: Lab analysis metadata (lab NID, dates, pH measurement times, etc.).
  - ECN_WC_qtext.csv: Quality text for site managers’ quality codes (SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).
  - ECN_QC1.csv: QC field, including SITECODE, SDATE, FIELDNAME, VALUE.
  - ECN_QC2.csv: Additional lab analysis QC details (dates, times, LAB_NID, pH times, filtration dates, analysis completion).
- Quality codes (Q-codes) are included to describe data quality issues or unusual events; 999 indicates an unusual event with text available in ECN_WC_qtext.csv.

## Site Codes and Locations

- Site code and location mapping (examples):
  - T02: Glensaugh – coordinates 56° 54' 33.36" N, 2° 33' 12.14"W
  - T04: Moor House - Upper Teesdale – 54° 41' 42.15" N, 2° 23' 16.26"W
  - T05: North Wyke – 50° 46' 54.96" N, 3° 55' 4.10"W
  - T06: Rothamsted – 51° 48' 12.33" N, 0° 22' 21.66"W
  - T07: Sourhope – 55° 29' 23.47" N, 2° 12' 43.32"W
  - T08: Wytham – 51° 46' 52.86" N, 1° 20' 9.81"W
  - T11: Snowdon (YWyddfa) – 53° 4' 28.38" N, 4° 2' 0.64"W
  - T12: Cairngorms – 57° 6' 58.84" N, 3° 49' 46.98"W
- This location data supports GIS integration and mapping of site-specific observations.

## Variables Measured

- A wide range of water chemistry and related measurements, including:
  - Alkalinity (ALKY)
  - Aluminium
  - Calcium
  - Chloride
  - Colour (absorbance)
  - Conductivity (CONDY)
  - Dissolved Organic Carbon (DOC)
  - Iron
  - Magnesium
  - Ammonium (NH4N)
  - Nitrate-N (NO3N)
  - pH (PH)
  - Aquacheck pH variants (PHAQCS, PHAQCU)
  - Phosphate (PO4P)
  - Potassium
  - Sulphate (SO4S)
  - Sodium
  - Stage (water level)
  - Total Nitrogen (TOTALN)
  - Total Phosphorus (TOTALP)
  - Quality codes Q1–Q6 related to data quality
- Each field has associated units (e.g., mg/L, pH, microSiemens/cm, mm), enabling consistent GIS attribute schema.

## Quality Codes

- A comprehensive set of quality codes covers data gaps, sampling conditions, laboratory issues, and unusual events (e.g., 100 No information, 101 No sample taken, 105 Snow in funnel, 200 Adverse weather, 501 Laboratory: No sample, 999 Unusual event).
- Textual explanations for certain codes are provided in ECN_WC_qtext.csv.

## Supporting Documentation

- ECN_WC2.csv: Lab analysis details and timing (site, date, lab, pH measurement times, filtration date, analysis completion).
- ECN_WC_qtext.csv: Explanatory text for quality events and issues, linked to quality codes.
- Explanatory information and variable definitions are provided to aid interpretation and GIS mapping.

## How to use in GIS workflows

- Use SITECODE, LCODE, and SDATE for time-enabled site-based mapping and temporal analyses.
- Map variables (FIELDNAME) with VALUE as constituent measurements; leverage QC fields (Q1–Q6) and QC text for data quality filtering.
- Integrate site coordinates from the Site Codes section to spatially represent ECN sites and their measurement points.
- Reference the Supporting Documentation to interpret lab metadata, quality assessments, and unusual events, ensuring robust data cleaning and provenance tracking.