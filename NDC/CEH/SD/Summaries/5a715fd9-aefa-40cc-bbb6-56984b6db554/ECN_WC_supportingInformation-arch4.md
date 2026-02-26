# Dataset Originator

## Overview
- Origin: ECN Data Centre, Centre for Ecology and Hydrology (ECN dataset on surface water chemistry).
- Part of the UK Environmental Change Network (ECN) program, funded by multiple UK government departments and agencies.
- Data span multiple UK sites with weekly dip-sample chemistry measurements and accompanying quality control.

## Data Providers and Stewardship
- Providers: Consortium of UK government departments/agencies including AFBI, BBSRC, NRW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, and others.
- Usage acknowledgement: Please acknowledge the use of ECN datasets and send one reprint of any publication citing the data.

## Data Collection and Quality Assurance
- Sampling method: Dip samples collected weekly to measure stream water chemistry.
- Quality control: Standard QC solution analyzed alongside field samples; QC information accompanies the dataset and should be used in analysis.
- Protocol: Related Surface Water Chemistry Protocol (surfaceWaterChemistryProtocol.pdf) accompanies the data.

## Data Structure and Coverage
- Core data fields: SITECODE, LCODE, SDATE, FIELDNAME, VALUE.
  - SITECODE: Unique ECN site id.
  - LCODE: Location code within each site.
  - SDATE: Sampling date.
  - FIELDNAME: Measured variable.
  - VALUE: Measured value.
- Additional analytical information: ECN_WC2.csv provides extended fields:
  - SHOUR, SMINS: Sampling time.
  - LAB_NID: Laboratory doing analyses.
  - PHDATE/PHHOUR/PHMINS: pH measurement timing.
  - FILTDATE: Filter date; COMPDATE: Analysis completion date.
- Site codes and locations (selected examples):
  - T02 Glensaugh (1993–2012)
  - T04 Moor House – Upper Teesdale (multiple sub-locations with varying date ranges)
  - T05 North Wyke (1993–2012)
  - T06 Rothamsted (1994–2012)
  - T07 Sourhope (1993–2012)
  - T08 Wytham (1993–2012)
  - T11 Y Wyddfa – Snowdon (1997–2012)
  - T12 Cairngorms (1999–2012)

## Variables and Field Names
- Key chemical and related measurements (examples):
  - ALKY (Alkalinity, mg/L)
  - ALUMINIUM (Aluminium, mg/L)
  - CALCIUM (Calcium, mg/L)
  - CHLORIDE (Chloride, mg/L)
  - COLOUR (Absorbance at 436 nm, nM)
  - CONDY (Conductivity, μS/cm)
  - DOC (Dissolved Organic Carbon, mg/L)
  - IRON (Iron, mg/L)
  - MAGNESIUM (Magnesium, mg/L)
  - NH4N (Ammonium, mg/L)
  - NO3N (Nitrate Nitrogen, mg/L)
  - PH (pH)
  - PHAQCS/PH_AQCU (Aquacheck pH readings)
  - PO4P (Phosphate Phosphorus, mg/L)
  - POTASSIUM (Potassium, mg/L)
  - SO4S (Sulphate Sulphur, mg/L)
  - SODIUM (Sodium, mg/L)
  - STAGE (Water level stage, mm)
  - TOTALN (Total Nitrogen, mg/L)
  - TOTALP (Total dissolved phosphorus, mg/L)
- Quality codes Q1–Q6 accompany measurements; additional Q codes exist and 999 indicates an unusual event with accompanying text.

## Quality and Data Integrity
- Quality codes: ECN standard codes indicate data issues or conditions affecting data quality (e.g., no information, sample loss, equipment issues, weather effects, laboratory issues, etc.), plus 999 for unusual events with explanatory text.
- Data integrity notes: Use accompanying quality information and the QC dataset when analyzing results.

## Usage and Compliance
- Data usage: Data are accompanied by metadata and quality information to support proper interpretation.
- Publication and sharing: Acknowledge ECN data use and provide copies of publications when cited.
- Additional resources: The dataset includes related documentation (Surface Water Chemistry Protocol and ECN_WC2.csv) to support data utilization and interpretation.