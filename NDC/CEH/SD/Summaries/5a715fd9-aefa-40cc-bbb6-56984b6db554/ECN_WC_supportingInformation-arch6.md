# ECN Water Chemistry dataset

- Origin and providers
  - Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology), http://data.ecn.ac.uk; ecn@ceh.ac.uk
  - Data providers: UK Environmental Change Network (ECN) partners including Defra, Natural England, Scottish Government agencies, and other UK departments and national bodies

- Purpose and usage
  - Purpose: environmental water chemistry data to understand environmental change; enabling analysis and data products for exploration
  - Acknowledgement: please acknowledge use of ECN data in publications; send one reprint of any publication citing the data

- Protocol and data collection
  - Protocol: surfaceWaterChemistryProtocol.pdf accompanies this document
  - Sampling: weekly dip samples for stream water chemistry
  - Quality control: standard QC solution analyzed with field samples; QC data accompany the dataset
  - Data use note: use the accompanying quality information when using the data

- Data structure (core)
  - Core fields: SITECODE (site ID), LCODE (location code within site), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value)

- Site codes and coverage
  - Example sites (with coordinates and date ranges):
    - T02 Glensaugh
    - T04 Moor House – Upper Teesdale
    - T05 North Wyke
    - T06 Rothamsted
    - T07 Sourhope
    - T08 Wytham
    - T11 Y Wyddfa – Snowdon
    - T12 Cairngorms
  - Date ranges vary by site and location code (1993–2012 in the provided ranges)

- Fieldnames and units (selected)
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, absorbance at 436 nm, nM)
  - Conductivity (CONDY, µS/cm)
  - Dissolved Organic Carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Magnesium (MAGNESIUM, mg/L)
  - Ammonium (NH4N, mg/L)
  - Nitrate-Nitrogen (NO3N, mg/L)
  - pH (PH, pH units)
  - Aquacheck pH readings (PHAQCS, PHAQCU, pH scale)
  - Phosphate (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Stage (STAGE, mm)
  - Total Nitrogen (TOTALN, mg/L)
  - Total Phosphorus (TOTALP, mg/L)
  - Additional QA/QC fields (Q1–Q6)

- Additional analytical information
  - ECN_WC2.csv: contains extended metadata for measurements
    - SITECODE, LCODE, SDATE, SHOUR, SMINS
    - LAB_NID (laboratory), PHDATE/PHHOUR/PHMINS (pH measurement timing)
    - FILTDATE, COMPDATE (filtration and analysis completion dates)

- Quality codes and data quality
  - ECN quality codes indicate data quality issues; multiple codes may apply
  - Common codes include:
    - 100, 101, 102, 103, 105, 106, 108, 109, 110, 111, 113, 114, 115, 116, 118, 119, 126, 127, 169, 170, 182, 191, 200, 203, 207, 208, 222, 229
    - 501–511, 999 (Unusual event)
  - 999 indicates an unusual event; accompanying quality text explains circumstances
  - Users should review the attached quality information for each dataset entry

- Practical considerations for data users
  - Expect patchy data across sites and time periods; dates vary by location code
  - Use ECN quality codes to filter or flag questionable measurements
  - Cross-reference ECN_WC2.csv and the main dataset for complete sampling timing and lab information
  - Properly cite ECN data and consider requesting a reprint for publications

- Access and contact
  - Data hosted by ECN data portal: http://data.ecn.ac.uk
  - For questions or guidance, contact ecn@ceh.ac.uk