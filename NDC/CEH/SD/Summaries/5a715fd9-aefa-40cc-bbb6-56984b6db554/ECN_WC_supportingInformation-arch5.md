# Dataset Originator

- E CN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology
- Data Providers: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies
  - Agencies include: Agri-Food and Biosciences Institute, BBSRC, Cyfoeth Naturiol Cymru (Natural Resources Wales), DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and Scottish Natural Heritage
- Usage acknowledgement: Please acknowledge use of ECN data and send one reprint of any publication citing the data

## Purpose and Protocol

- ECN aims to understand environmental change through site monitoring and network coordination
- Protocol highlights
  - Dip samples collected weekly to measure stream water chemistry
  - A standard QC solution is analysed alongside field samples for quality control
  - QC data accompanies the dataset; use the accompanying quality information when using the data

## Data Structure and Core Fields

- Core data fields (Dataset structure)
  - SITECODE, Description: Unique ECN site identifier
  - LCODE, Description: Replicate location code within a site for core measurements
  - SDATE, Description: Sampling/recording date
  - FIELDNAME, Description: Variable measured
  - VALUE, Description: Measured value
- Additional information on measurements is provided in ECN_WC2.csv (structure below)
  - SITECODE, LCODE, SDATE
  - SHOUR, SMINS: Sampling time
  - LAB_NID: Laboratory performing analyses
  - PHDATE, PHHOUR, PHMINS: Date/time of pH measurement
  - FILTDATE: Date sample was filtered
  - COMPDATE: Date analysis completed

## Site Codes and Coverage

- Multiple sites with coordinates and dataset date ranges, including:
  - T02 Glensaugh (56° 54' 33.36" N, 2° 33' 12.14"W): data 12-May-1993 to 26-Dec-2012
  - T04 Moor House - Upper Teesdale: various location codes with overlapping and multi-period date ranges
  - T05 North Wyke: data from 29-Sep-1993 to 26-Dec-2012
  - T06 Rothamsted: 29-Jun-1994 to 26-Dec-2012
  - T07 Sourhope: 19-May-1993 to 26-Dec-2012 (two location codes)
  - T08 Wytham: 14-Jan-1993 to 19-Dec-2012 (multiple location codes)
  - T11 Y Wyddfa - Snowdon: 02-Jul-1997 to 27-Dec-2012
  - T12 Cairngorms: 18-Aug-1999 to 30-May-2012
- Site and location codes enable replication and traceability of sampling locations across time

## Measured Variables (Fieldnames) and Units

- Alkalinity (ALKY): mg per litre
- Aluminium (ALUMINIUM): mg per litre
- Calcium (CALCIUM): mg per litre
- Chloride (CHLORIDE): mg per litre
- Colour (COLOUR): absorbance at 436 nm (nM)
- Conductivity (CONDY): microSiemens per centimetre
- Dissolved Organic Carbon (DOC): mg per litre
- Iron (IRON): mg per litre
- Magnesium (MAGNESIUM): mg per litre
- Ammonium (NH4N): mg per litre
- Nitrate Nitrogen (NO3N): mg per litre
- pH (PH): pH units
- Aquacheck pH (PHAQCS, PHAQCU): pH scales (1-14)
- Phosphate Phosphorus (PO4P): mg per litre
- Potassium (POTASSIUM): mg per litre
- Sulphate Sulphur (SO4S): mg per litre
- Sodium (SODIUM): mg per litre
- Stage (STAGE): water level (mm)
- Total Nitrogen (TOTALN): mg per litre
- Total dissolved Phosphorus (TOTALP): mg/L
- Quality codes (Q1–Q6): indicate data quality aspects
- Note: Q-codes are described in the Quality Codes section

## Quality Information and Codes

- ECN site managers assign quality codes from a standard ECN list to indicate data quality factors
- If an uncommon event occurs outside standard codes, code 999 is used, with accompanying quality text
- Standard ECN quality codes include (examples):
  - 100 No information available
  - 101 No sample/reading taken
  - 102 Sample lost
  - 103 Partial loss of sample
  - 105–119 Various contamination or interference issues (snow, insects, leaves, etc.)
  - 126–129 Site-related conditions (frozen rivers, dry sites)
  - 169–182 Weather or sampling impacts (snow, frost, fire, crop spraying)
  - 200 Adverse weather affecting sampling/recording
  - 501–511 Laboratory-specific issues (no sample, contamination, filtration notes, etc.)
  - 999 Unusual event (see accompanying quality text)
- Detailed descriptions are provided in the dataset’s Quality Codes documentation

## Additional Analytical Information

- An accompanying file ECN_WC2.csv provides extended measurement metadata
  - Includes site/location/date/time information and laboratory details
- This enables precise interpretation of timestamps and lab analyses beyond the core fields

## Usage Guidance and Acknowledgements

- Acknowledge ECN data usage in publications
- Provide ECN with one reprint of any publication citing ECN data
- Use accompanying quality information to assess data suitability
- Be mindful of data provenance: site-specific periods, location codes, and potential gaps or quality issues indicated by quality codes

## Data Governance and Stewardship Considerations

- Data stewardship focus reflected in:
  - Clear data provenance from multiple national agencies
  - Defined data structure with standardized fields and units
  - Rigorous quality control via QC samples and site-managed quality codes
  - Comprehensive site and location metadata to support discovery and reuse
  - Instructions for acknowledging data usage and returning publication outputs
- Potential challenges acknowledged for data stewards:
  - Incomplete user needs perspective and timely data receipt
  - Heterogeneous systems and formats across sites
  - Large or complex datasets and outdated databases requiring bespoke solutions
  - Ensuring proper metadata, data formats, and update mechanisms for ongoing sharing