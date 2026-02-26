# ECN Water Chemistry Data

## Overview
- Source dataset of surface water chemistry from the UK Environmental Change Network (ECN).
- Weekly dip-sampler measurements of stream water chemistry across multiple ECN sites.
- Includes a wide range of chemical and physical parameters (alkalinity, major ions, nutrients, pH, conductivity, colour, dissolved organic carbon, etc.).
- Emphasizes data quality, metadata, and governance; accompanying quality information should be consulted when using the data.

## Dataset Origin and Providers
- Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH) (dataset: http://data.ecn.ac.uk; ecn@ceh.ac.uk).
- Data Providers: UK government departments and agencies funding ECN through site monitoring or network coordination, including:
  - Agri-Food and Biosciences Institute
  - Biotechnology and Biological Sciences Research Council
  - Cyfoeth Naturiol Cymru - Natural Resources Wales
  - Defence Science & Technology Laboratory
  - Department for Environment, Food and Rural Affairs
  - Environment Agency
  - Forestry Commission
  - Welsh Government (Llywodraeth Cymru)
  - Natural England
  - Natural Environment Research Council
  - Northern Ireland Environment Agency
  - Scottish Environment Protection Agency
  - Scottish Government
  - Scottish Natural Heritage
- Data use acknowledgement: Please acknowledge the use of ECN data and send one reprint of any publication citing ECN data.

## Protocol and Sampling Notes
- Protocol: surfaceWaterChemistryProtocol.pdf (accompanies the dataset).
- Sampling: dip samples collected weekly to measure stream chemistry.
- Quality control: a standard QC solution is sent to laboratories and analysed alongside field samples; data quality information accompanies the dataset and should be used as a reference.

## Data Structure and Metadata
- Core dataset structure:
  - SITECODE: Unique ECN site identifier
  - LCODE: Location code per site for core measurements
  - SDATE: Sampling/recording date
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Additional information: ECN_WC2.csv provides more measurement details, including:
  - SHOUR, SMINS: Sampling time components
  - LAB_NID: Laboratory performing analyses
  - PHDATE, PHHOUR, PHMINS: Date/time of pH measurement
  - FILTDATE, COMPDATE: Filter and analysis completion dates

## Site Codes and Temporal Coverage
- T02 Glensaugh
  - Location: 56° 54' 33.36" N, 2° 33' 12.14" W
  - Date range examples: 12-May-1993 to 26-Dec-2012
- T04 Moor House - Upper Teesdale
  - Location: 54° 41' 42.15" N, 2° 23' 16.26" W
  - Date ranges vary by location code (1992–2012 across multiple codes)
- T05 North Wyke
  - Location: 50° 46' 54.96" N, 3° 55' 4.10" W
  - Date range examples: 29-Sep-1993 to 26-Dec-2012
- T06 Rothamsted
  - Location: 51° 48' 12.33" N, 0° 22' 21.66" W
  - Date range example: 29-Jun-1994 to 26-Dec-2012
- T07 Sourhope
  - Location: 55° 29' 23.47" N, 2° 12' 43.32" W
  - Date range examples: 19-May-1993 to 26-Dec-2012
- T08 Wytham
  - Location: 51° 46' 52.86" N, 1° 20' 9.81" W
  - Date range examples: 14-Jan-1993 to 19-Dec-2012
- T11 Y Wyddfa - Snowdon
  - Location: 53° 4' 28.38" N, 4° 2' 0.64" W
  - Date range example: 02-Jul-1997 to 27-Dec-2012
- T12 Cairngorms
  - Location: 57° 6' 58.84" N, 3° 49' 46.98" W
  - Date range example: 18-Aug-1999 to 30-May-2012

## Fieldnames and Measurements
- Variables cover key water chemistry and related measurements, including:
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, nM; absorbance)
  - Conductivity (CONDY, µS/cm)
  - Dissolved Organic Carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Major cations and anions: Magnesium (MAGNESIUM, mg/L), Sodium (SODIUM, mg/L), Potassium (POTASSIUM, mg/L), Nitrate-N (NO3N, mg/L), Ammonium (NH4N, mg/L), Phosphate (TOTALP, PO4P, mg/L), Sulphate (SO4S, mg/L)
  - pH measurements (PH, pH units; PHAQCS, PHAQCU for Aquacheck pH with/without stirring)
  - Stage (WATER LEVEL, mm)
  - Total Nitrogen (TOTALN, mg/L)
  - Total Phosphorus (TOTALP, mg/L)
- Quality codes (Q1–Q6) accompany variables; additional quality information is provided in the accompanying quality information.
- Notes: Some metadata references include potential gaps (quality codes 999 for unusual events).

## Additional Analytical Information
- The dataset ECN_WC2.csv contains extended measurement details:
  - SITECODE and LCODE as identifiers
  - SDATE (sampling date), SHOUR/SMINS (sampling time)
  - LAB_NID (laboratory)
  - PHDATE/PHHOUR/PHMINS (pH measurement timing)
  - FILTDATE (filtration date) and COMPDATE (analysis completion date)

## Quality Codes and Data Quality
- ECN site managers assign standardized quality codes indicating data quality factors (multiple codes may apply).
- Examples of common codes include:
  - 100 No information available; data lost
  - 101 No sample/reading taken (equipment out of action)
  - 102 Sample lost or discarded
  - 103 Partial loss of sample
  - 200 Adverse weather effects on sampling/recording
  - 501–511 Laboratory-related issues (e.g., no sample, contamination, filtration issues)
  - 999 Unusual event – see accompanying quality text
- If a non-standard situation occurs, code 999 is used with accompanying text detailing the circumstances.

## Data Use and Governance
- Data should be used in conjunction with the accompanying quality information to assess data suitability.
- Data governance and metadata provision are emphasized, with attention to timely data access, cross-organization data sharing, and clear communication of complex findings.