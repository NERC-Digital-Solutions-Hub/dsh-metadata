# ECN Data Centre dataset documentation

- The ECN dataset provides precipitation chemistry data from the UK Environmental Change Network (ECN) across 12 sites, with weekly bulk-collected samples and accompanying quality control data.
- Originator and scope: Dataset originates from the ECN Data Centre; part of a program funded by multiple UK government departments and agencies to study environmental change.

## Data provenance and access

- Data providers: ECN programme funded by organisations including DEFRA, Natural England, Environment Agency, Scottish Government, Welsh Government, NERC, and others.
- Acknowledgement and citation: Users must acknowledge the data use and send a reprint of any publication citing ECN data.
- Protocol and comparability: Standard operating procedures ensure data comparability across sites; refer to the accompanying PC.pdf for collection methods.

## Protocol and quality

- Sampling method: Bulk collectors measure precipitation chemistry; samples collected weekly.
- Quality control: A standard QC solution is analysed with field samples; QC data are provided alongside data; use accompanying QC information.
- Textual quality notes: Site managers assign quality codes from a standard list; unusual events are described in ECN_PC_qtext.csv (quality code 999).

## Data structure and files

- Primary data fields in data downloads: SITECODE (site), SDATE (sampling date), FIELDNAME (variable), VALUE (measured value).
- Supporting documentation files:
  - ECN_PC2.csv: Lab analysis metadata (e.g., FROMDATE/FROMHOUR/FROMMINS, LAB_NID, PHDATE/PHHOUR/PHMINS, etc.).
  - ECN_PC_qtext.csv: Quality text for non-codified issues (SITECODE, FIELDNAME, dates, DESCRIPTION).
  - ECN_QC1.csv: Quality control solution data (SITECODE, SDATE, FIELDNAME, VALUE).
  - ECN_QC2.csv: Additional lab analysis metadata for QC (FROMDATE/FROMHOUR/FROMMINS, SDATE, SHOUR/SMINS, LAB_NID, PHDATE/PHHOUR/PHMINS, FILTDATE, COMPDATE).
- Explanatory site information: Site codes T01–T12 with site names and geographic coordinates and a link for further site information.

## Site codes and variables

- Sites (Site codes and names): T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Y Wyddfa - Snowdon; T12 Cairngorms.
- Variables measured (FIELDNAME) include key chemistry and water quality indicators:
  - Alkalinity (ALKY), Aluminium, Calcium, Chloride, Colour (absorbance), Conductivity (CONDY), Dissolved Organic Carbon (DOC)
  - Iron, Magnesium, Ammonium (NH4N), Nitrate-N (NO3N), pH, PHAQCS/PUAQCU (pH measurements), Phosphate (PO4P), Potassium, Sulphate (SO4S), Sodium, Total Nitrogen (TOTALN), Total Phosphorus (TOTALP), Volume of sample
  - Quality codes Q1–Q6 accompanying measurements
- Units are provided for each variable where applicable (e.g., mg/L, microSiemens per cm, pH units, ml, etc.).

## Data quality and filtering guidance

- Quality codes: A standard ECN list ranges from 100 (no information) to 999 (unusual event). Codes indicate issues such as missing samples, contamination, equipment problems, or lab issues.
- Quality text: 999 indicates an unusual event; view associated details in ECN_PC_qtext.csv.
- Post-hoc chemistry QC: ECN_PC_chemistry-QC.csv provides checks comparing measured conductivity to theoretical values, and ratios of cations to anions.
  - COND_RATIO_OK: 1 if conductivity ratio is within 0.8–1.2 (when all ions are recorded).
  - ION_DIFF_OK: 1 if anion-cation differences are within ±10 μeq/L (useful where conductivity is missing or very dilute).
  - PO4_OK: 1 if PO4 concentration is ≤5 μeq/L (potential contamination flagged if >5 μeq/L); 1 if PO4 not measured.
  - OVERALL_CHECK_OK: 1 if PO4_OK is 1 and either COND_RATIO_OK = 1 or ION_DIFF_OK = 1; only data with OVERALL_CHECK_OK = 1 are recommended for temporal analyses or flux calculations.
- Practical use: For robust analyses of temporal trends or fluxes, prioritize data with OVERALL_CHECK_OK = 1.

## Usage notes for analysts

- Ensure QC information is used alongside primary measurements; maintain awareness of site-specific quality issues and unusual events.
- The dataset is designed to be discoverable and reusable, with metadata and supporting documentation facilitating data integration across sites and variables.
- When publishing, cite ECN data and provide a reprint of the publication as requested.