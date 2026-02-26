# ECN Water Chemistry Dataset Documentation

## Dataset Originator
- ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology

## Data Providers
- UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, Scottish Government, Welsh Government, etc.)
- ECN requests acknowledgment of data use and one reprint of any publication citing ECN data

## Protocol and Data Quality
- Standard operating procedures ensure data comparability across sites; see accompanying wc.pdf for data collection explanations
- Dip samples collected weekly to measure stream water chemistry
- Standard quality control solution used by labs (QC) and analyzed alongside field samples
- Quality information accompanying the data should be used for proper interpretation

## Usage Notes
- Dip samples: weekly stream water chemistry measurements
- QC checks: standard quality control solution analyzed with field samples
- Include accompanying quality information when using the data

## Data Download and Structure
- Core data format: SITECODE (ECN Site), LCODE (location ID within site), SDATE (sampling date), FIELDNAME (variable), VALUE (measured value)
- Supporting documentation files:
  - ECN_WC2.csv: lab analysis metadata (e.g., SITECODE, LCODE, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
  - ECN_WC_qtext.csv: site manager quality text for data quality factors; includes FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION, and associated quality codes
  - ECN_QC1.csv: quality control solution data (SITECODE, SDATE, FIELDNAME, VALUE)
  - ECN_QC2.csv: lab analysis details for QC (dates, times, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
- Explanatory site codes (e.g., T02 Glensaugh; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T11 Snowdon; T12 Cairngorms) with GPS coordinates

## Explanatory Information: Variable Names (FIELDNAME)
- Alkalinity (ALKY, mg/L)
- Aluminium (ALUMINIUM, mg/L)
- Calcium (CALCIUM, mg/L)
- Chloride (CHLORIDE, mg/L)
- Colour (COLOUR, nM)
- Conductivity (CONDY, µS/cm)
- Dissolved Organic Carbon (DOC, mg/L)
- Iron (IRON, mg/L)
- Magnesium (MAGNESIUM, mg/L)
- Ammonium (NH4N, mg/L)
- Nitrate-N (NO3N, mg/L)
- pH (PH)
- Aquacheck pH (PHAQCS, PHAQCU, both on pH scale 1–14)
- Phosphate (PO4P, mg/L)
- Potassium (POTASSIUM, mg/L)
- Sulphate (SO4S, mg/L)
- Sodium (SODIUM, mg/L)
- Water stage (STAGE, mm)
- Total Nitrogen (TOTALN, mg/L)
- Total Phosphorus (TOTALP, mg/L)
- Quality codes (Q1–Q6)

## Quality Codes
- Codes indicate data quality issues or unusual events (e.g., 100 No information, 101 No sample taken, 103 Partial loss, 200 Adverse weather, 501–511 laboratory/sample issues, 999 Unusual event)
- The dataset includes a quality text field (ECN_WC_qtext.csv) to describe circumstances not covered by standard codes

## Purpose for Analysts Monitoring the Environment
- Provides standardized, cross-site water chemistry data for environmental health assessment and policy performance over time
- Facilitates data verification, quality assurance, cleaning, and transformation to produce comparable outputs
- Supports data discovery and reuse by enabling access to underlying data and rich metadata
- Encourages integration with other datasets to increase the value of monitoring data and support transparent policy analysis