# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

## Overview
- A multi-site dataset of precipitation chemistry from the UK Environmental Change Network (ECN) covering 1992–2012.
- Bulk collectors measure weekly precipitation chemistry; includes a quality control (QC) solution analyzed alongside field samples.
- Data are provided with accompanying quality information to support proper use; users should acknowledge data and may be asked to send a reprint of citing publications.

## Data Origin and Providers
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH) – http://data.ecn.ac.uk.
- Data Providers: ECN programme funded by a consortium of UK government departments and agencies, including (among others) DEFRA, Environment Agency, Natural England, Natural Resources Wales, Scottish Government, Scottish Environment Protection Agency, and UK research councils.
- Usage acknowledgement: ECN requests acknowledgement of data usage and one reprint of any publication citing ECN data.

## Protocol and Data Collection
- Sampling method: Bulk collectors measure precipitation chemistry; samples collected weekly.
- Quality control: A standard QC solution is sent to laboratories; QC data accompany the dataset for quality assurance.
- Data handling: Use the accompanying quality information when analyzing data.

## Data Structure
- Core data fields: SITECODE, SDATE, FIELDNAME, VALUE.
  - SITECODE: Unique ECN site code.
  - SDATE: Sampling date.
  - FIELDNAME: Measured variable.
  - VALUE: Measured value.

## Site Codes (Site Details and Time Ranges)
- T01 Drayton – 52° 11' 37.95" N, 1° 45' 51.95"W; 14-Apr-1993 to 19-Dec-2012.
- T02 Glensaugh – 56° 54' 33.36" N, 2° 33' 12.14"W; 14-Oct-1993 to 26-Dec-2012.
- T03 Hillsborough – 54° 27' 12.24" N, 6° 4' 41.26"W; 02-Feb-1994 to 27-Dec-2012.
- T04 Moor House - Upper Teesdale – 54° 41' 42.15" N, 2° 23' 16.26"W; 06-Oct-1992 to 24-Dec-2012.
- T05 North Wyke – 50° 46' 54.96" N, 3° 55' 4.10"W; 29-Sep-1993 to 26-Dec-2012.
- T06 Rothamsted – 51° 48' 12.33" N, 0° 22' 21.66"W; 02-Feb-1994 to 12-Dec-2012.
- T07 Sourhope – 55° 29' 23.47" N, 2° 12' 43.32"W; 08-Dec-1993 to 26-Dec-2012.
- T08 Wytham – 51° 46' 52.86" N, 1° 20' 9.81"W; 09-Jun-1993 to 12-Dec-2012.
- T09 Alice Holt – 51° 9' 16.46" N, 0° 51' 47.58"W; 27-Apr-1994 to 12-Dec-2012.
- T10 Porton Down – 51° 7' 37.83" N, 1° 38' 23.46"W; 17-Jan-1996 to 26-Jan-2000.
- T11 Y Wyddfa – Snowdon – 53° 4' 28.38" N, 4° 2' 0.64"W; 02-Jul-1997 to 27-Dec-2012.
- T12 Cairngorms – 57° 6' 58.84" N, 3° 49' 46.98"W; 06-Oct-1999 to 26-Dec-2012.

Note: Each site has a distinct date range within the overall 1992–2012 span.

## Fieldnames (Measured Variables)
- Alkalinity (ALKY) – mg/L.
- Aluminium (ALUMINIUM) – mg/L.
- Calcium (CALCIUM) – mg/L.
- Chloride (CHLORIDE) – mg/L.
- Colour (COLOUR) – Absorbance at 436 nm, nM.
- Conductivity (CONDY) – μS/cm.
- Dissolved Organic Carbon (DOC) – mg/L.
- Iron (IRON) – mg/L.
- Magnesium (MAGNESIUM) – mg/L.
- Ammonium (NH4N) – mg/L.
- Nitrate Nitrogen (NO3N) – mg/L.
- pH (PH) – pH scale 1–14.
- Aquacheck pH (PHAQCS, PHAQCU) – pH (stirred and unstirred), 1–14.
- Phosphate Phosphorus (PO4P) – mg/L.
- Potassium (POTASSIUM) – mg/L.
- Sulphate Sulphur (SO4S) – mg/L.
- Sodium (SODIUM) – mg/L.
- Total Nitrogen (TOTALN) – mg/L.
- Total dissolved Phosphorus (TOTALP) – mg/L.
- Volume of sample collected (VOLUME) – mL.
- Quality codes (Q1–Q6) – quality code per measurement (see ECN QC codes).

Additional notes:
- There is an accompanying document ECN_PC2.csv with extra measurement metadata (see below).

## Additional Analytical Information
- ECN_PC2.csv provides measurement timing and laboratory details:
  - SITECODE, RID (replicate ID).
  - FROMDATE/FROMHOUR/FROMMINUTE (deployment of bulk collector).
  - SDATE/SHOUR/SMINS (sampling date/time).
  - LAB_NID (laboratory performing analysis).
  - PHDATE/PHHOUR/PHMINS (pH measurement time).
  - FILTDATE (date sample was filtered).
  - COMPDATE (date analysis completed).

## Quality Codes
- ECN quality codes (assigned by site managers) indicate factors affecting data quality. If applicable, multiple codes may be used; 999 indicates an unusual event with accompanying text.
- Standard ECN quality codes include:
  - 100 No information available - data lost
  - 101 No sample/reading taken - equipment out of action
  - 102 Sample lost or discarded
  - 103 Partial loss of sample
  - 104 Sample frozen when collected
  - 105 Snow in funnel during collection
  - 106 Snow during sampling period
  - 107 Bird droppings in funnel
  - 108 Insects in sample
  - 109 Leaves in sample
  - 110 Soil in sample
  - 111 Unidentified debris in sample
  - 112 Debris in funnel
  - 113 Sample discoloured
  - 114 Bonfire nearby during sampling
  - 115 Heather burning nearby
  - 116 Forest fire nearby
  - 117 Straw burning nearby
  - 118 Crop spraying nearby
  - 119 Construction work nearby
  - 120 Liming nearby
  - 121 Change of land use nearby
  - 122 Funnel assembly replaced with clean one
  - 123 Clip open
  - 124 Tubing damaged
  - 126 River/lake frozen – no sample
  - 133 Evidence of disease in plot/transect
  - 180 Trace rainfall recorded (marked as X)
  - 182 Snow or sleet during sampling period
  - 187 Snow cleared from rain gauge
  - 191 Hail during sampling period
  - 200 Adverse weather conditions affected sampling/recording
  - 222 Non-standard sampling date
  - 223 Non-standard sampling time
  - 501 Laboratory: No sample
  - 502 Laboratory: Sample lost or discarded
  - 503 Laboratory: Partial loss
  - 504 Laboratory: Sample discarded due to contamination
  - 505 Laboratory: Insufficient sample
  - 506 Laboratory: Equipment failure
  - 507 Laboratory: Pre-filtered
  - 508–510 Significant deposit in filter (black/brown/green)
  - 511 No separate acidified sub-sample for Al and Fe
  - 999 Unusual event – see accompanying quality text

## Additional Usage Notes
- The dataset is accompanied by links to supporting documentation and a DOi reference for the ECN data (ECN precipitation chemistry data: 1992–2012).
- For proper interpretation, users should consult the quality codes and accompanying QC documentation.

## Citations and Contact
- Acknowledge ECN data usage in publications.
- Return one reprint of any publication citing ECN data.
- For questions or access to the full metadata and files (including ECN_PC2.csv and quality information), refer to the dataset documentation and ECN data centre resources.