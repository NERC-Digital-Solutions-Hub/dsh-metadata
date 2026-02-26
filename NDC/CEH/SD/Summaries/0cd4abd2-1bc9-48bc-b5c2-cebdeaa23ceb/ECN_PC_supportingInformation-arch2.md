# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

## Overview
- Long-term dataset of precipitation chemistry from 12 ECN sites across the UK (1992–2012).
- Data intended to support monitoring environmental change and policy-relevant analyses.
- Variables cover key chemical and physical properties of precipitation and its quality indicators.

## Data Origin and Providers
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk).
- Data Providers: UK ECN programme funded by multiple government departments and agencies (e.g., DEFRA, Natural England, Environment Agency, NERC institutes, Scottish Government, Welsh Government, etc.).
- Request: Acknowledge data usage and provide one reprint of any publication citing the data.

## Protocol and Quality Assurance
- Sample collection: Bulk collectors used; weekly sampling.
- Quality control: Standard QC solution analyzed alongside field samples; quality information accompanies the dataset.
- Data use: Refer to accompanying quality information and ECN quality codes for data reliability.

## Data Structure
- Core structure: SITECODE (site ID), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
- Additional metadata available in accompanying documentation (ECN_PC2.csv) detailing collection and analysis timing.

## Site Codes
- 12 ECN sites with standardized naming, coordinates, and dataset date ranges:
  - T01 Drayton (52°11'37.95" N, 1°45'51.95"W): 14-Apr-1993 to 19-Dec-2012
  - T02 Glensaugh (56°54'33.36" N, 2°33'12.14"W): 14-Oct-1993 to 26-Dec-2012
  - T03 Hillsborough (54°27'12.24" N, 6°04'41.26"W): 02-Feb-1994 to 27-Dec-2012
  - T04 Moor House - Upper Teesdale (54°41'42.15" N, 2°23'16.26"W): 06-Oct-1992 to 24-Dec-2012
  - T05 North Wyke (50°46'54.96" N, 3°55'4.10"W): 29-Sep-1993 to 26-Dec-2012
  - T06 Rothamsted (51°48'12.33" N, 0°22'21.66"W): 02-Feb-1994 to 12-Dec-2012
  - T07 Sourhope (55°29'23.47" N, 2°12'43.32"W): 08-Dec-1993 to 26-Dec-2012
  - T08 Wytham (51°46'52.86" N, 1°20'9.81"W): 09-Jun-1993 to 12-Dec-2012
  - T09 Alice Holt (51°9'16.46" N, 0°51'47.58"W): 27-Apr-1994 to 12-Dec-2012
  - T10 Porton Down (51°7'37.83" N, 1°38'23.46"W): 17-Jan-1996 to 26-Jan-2000
  - T11 Y Wyddfa - Snowdon (53°4'28.38" N, 4°2'0.64"W): 02-Jul-1997 to 27-Dec-2012
  - T12 Cairngorms (57°6'58.84" N, 3°49'46.98"W): 06-Oct-1999 to 26-Dec-2012

## Fieldnames and Units
- Alkalinity (ALKY) — mg/L
- Aluminium (ALUMINIUM) — mg/L
- Calcium (CALCIUM) — mg/L
- Chloride (CHLORIDE) — mg/L
- Colour (COLOUR) — nM (absorbance at 436 nm)
- Conductivity (CONDY) — µS/cm
- Dissolved Organic Carbon (DOC) — mg/L
- Iron (IRON) — mg/L
- Magnesium (MAGNESIUM) — mg/L
- Ammonium (NH4N) — mg/L
- Nitrate Nitrogen (NO3N) — mg/L
- pH (PH) — pH units
- Aquacheck pH (PHAQCS, PHAQCU) — pH units
- Phosphate Phosphorus (PO4P) — mg/L
- Potassium (POTASSIUM) — mg/L
- Sulphate Sulphur (SO4S) — mg/L
- Sodium (SODIUM) — mg/L
- Total Nitrogen (TOTALN) — mg/L
- Total dissolved Phosphorus (TOTALP) — mg/L
- Volume (VOLUME) — mL
- Quality codes (Q1–Q6) — codes describing data quality

## Additional Metadata and Documentation
- Supporting document: ECN_PC2.csv with detailed timing for deployment, sampling, and analysis.
- Quality codes are assigned by ECN site managers from a standard list; an unusual event is recorded as code 999 with accompanying text.

## Quality Codes (selected)
- 100–199: No information or sample/readings issues (e.g., 100 No information; 101 No sample/reading; 102–113 various sample issues; 114–119 environmental interferences; 120–122 operational changes; 123–133 debris and sample integrity issues)
- 180, 182, 187, 191: Adverse weather, snow, hail, and related sampling conditions
- 200–223: Laboratory or field-related issues (e.g., 501–511 laboratory issues such as no sample, contamination, insufficient sample)
- 999: Unusual event (textual description provided)

## Usage and Access
- Data curated for monitoring environmental health and policy performance over time.
- Researchers are encouraged to acknowledge ECN usage and submit a reprint of publications citing the data.
- Supporting and accompanying documentation accessible via provided DOI and ECN data portal links.