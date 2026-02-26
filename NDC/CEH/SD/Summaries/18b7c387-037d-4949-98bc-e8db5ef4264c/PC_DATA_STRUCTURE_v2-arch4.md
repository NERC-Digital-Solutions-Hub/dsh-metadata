# Dataset Originator

- The ECN Data Centre (Centre for Ecology and Hydrology) is the originator of the dataset.
- Data is provided by the UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
- Partner organisations include: BBSRC, NRW, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Northern Ireland Environment Agency, Scottish Environment Protection Agency, Scottish Government, and Scottish Natural Heritage.
- ECN requests acknowledgement of data usage and submission of one reprint for publications citing ECN data.

## Protocol and Governance

- ECN employs standard operating procedures to ensure data comparability across sites.
- A accompanying pdf (pc.pdf) explains data collection protocols.
- Quality control: a standard QC solution is sent to laboratories and analyzed alongside field samples; accompanying quality information must be used when using the data.

## Usage Notes and Data Quality

- Bulk collectors measure precipitation chemistry with weekly sampling.
- A QC solution is analyzed with field samples as a quality check; use accompanying QC information.
- Site managers assign quality codes to indicate factors affecting data quality; codes can be combined, and unusual events are described in accompanying quality text (code 999).

## Data Download Structure

- Primary data fields: SITECODE (site code), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
- Supporting documentation files accompany the dataset:
  - ECN_PC2.csv: lab analysis details (e.g., FROMDATE, FROMHOUR, PHDATE, etc.).
  - ECN_PC_qtext.csv: quality text explanations for codes; includes SITE, FIELDNAME, date ranges, and text.
  - ECN_QC1.csv: quality control results for QC samples (DATE, FIELDNAME, VALUE).
  - ECN_QC2.csv: additional lab analysis details for QC samples (dates, lab, pH, etc.).
- Explanatory information provided for:
  - Site Codes (T01–T12 with site names and coordinates; T01 Drayton, T02 Glensaugh, etc.).
  - Variable being measured (FIELDNAME): list includes alkalinity, aluminium, calcium, chloride, colour, conductivity, dissolved organic carbon, iron, magnesium, ammonium, nitrate, pH, phosphorus, potassium, sulphate, sodium, total nitrogen, total phosphorus, sample volume, and quality codes Q1–Q6.
  - Quality Codes: an extensive standard list (100–511, 999) indicating data issues or events (e.g., no information, sample loss, equipment failure, contamination, adverse weather, etc.).
- The dataset emphasizes using the accompanying quality information to assess data suitability.

## Quality Assurance and Chemistry Checks

- ECN_CCU chemistry QC file: post-hoc screening of ECN PC measurements.
- Conductivity checks: compare measured conductivity with theoretical conductivity calculated from major ions (cations and anions); acceptable ratio range is 0.8 to 1.2 when all ion data are present.
- Ion balance checks: use absolute differences between anions and cations (ION_DIFF_OK) with a threshold of ±10 µeq L−1.
- Phosphate (PO4) checks: PO4 3− concentration > 5 µeq L−1 may indicate contamination; code as PO4_OK accordingly.
- Overall_OK: samples not flagged as potentially contaminated and that pass conductivity/ion-balance checks can be used for temporal trend analyses and mean concentration calculations.

## Site Information and Accessibility

- Explanatory information: ECN site codes and locations available; a map/resource is provided at the ECN catalogue link.
- Additional information about ECN sites is available at the ECN catalogue URL.

## Practical Guidance for Data Leaders

- Ensure clear provenance: acknowledge ECN data usage and cite data sources.
- Use the standard protocols and QC information to verify data quality before analysis.
- Leverage site codes and variable metadata to enable cross-site comparisons and system-wide data governance.
- Rely on quality codes and the QC files to assess data suitability and to filter data for analysis (prefer samples with OVERALL_CHECK_OK = 1).
- Coordinate with the wider data community and maintain up-to-date metadata to minimize data gaps and improve discoverability.