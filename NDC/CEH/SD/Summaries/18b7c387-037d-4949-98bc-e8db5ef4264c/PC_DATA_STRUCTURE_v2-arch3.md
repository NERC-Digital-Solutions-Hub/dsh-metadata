# ECN Data Centre - Dataset Documentation and Protocol

- Purpose and context
  - The ECN dataset is designed to monitor environmental change and inform policy decisions by providing standardized health-related environmental measurements.
  - Data are intended to scrutinize and evaluate policy impacts and to inform future decisions.

- Origin and governance
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Data Providers: The ECN programme funded by a consortium of UK government departments and agencies (e.g., Defra, Natural England, UK Research Councils, devolved administrations, and other agencies).
  - Acknowledgement and sharing: Researchers are asked to acknowledge ECN data use and to send one reprint of any publication citing the data.

- Protocol and data standardization
  - ECN uses standard operating procedures to ensure data are comparable across sites.
  - A detailed accompanying protocol (pc.pdf) explains data collection methods and quality controls.
  - Data are supplemented by extensive supporting documentation to ensure reproducibility and transparency.

- Data structure and download
  - Core dataset fields for download include:
    - SITECODE (site identifier)
    - SDATE (sampling date)
    - FIELDNAME (variable measured)
    - VALUE (measured value)
  - Supporting files provide:
    - ECN_PC2.csv: lab analysis details per site and sample
    - ECN_PC_qtext.csv: qualitative quality text tied to quality codes
    - ECN_QC1.csv and ECN_QC2.csv: additional quality control data and lab analyses
  - Explanatory information covers site codes, variable names, units, and quality codes.

- Site information
  - 12 ECN sites (T01–T12) with named locations (e.g., Drayton, Glensaugh, Hillsborough, Moor House, etc.) and geographic coordinates.
  - Additional site information is available via the ECN catalogue.

- Variables measured (FIELDNAME)
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, nM)
  - Conductivity (CONDY, µS/cm)
  - Dissolved organic carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Magnesium (MAGNESIUM, mg/L)
  - Ammonium (NH4N, mg/L)
  - Nitrate nitrogen (NO3N, mg/L)
  - pH (PH)
  - Aquacheck pH values (PHAQCS, PHAQCU; both on pH scale 1–14)
  - Phosphate phosphorus (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Total nitrogen (TOTALN, mg/L)
  - Total dissolved phosphorus (TOTALP, mg/L)
  - Sample volume (VOLUME, mL)
  - Quality codes (Q1–Q6) indicating data quality factors

- Quality management and codes
  - Site managers assign quality codes from a standard ECN list; codes include 100–508 for various data issues and 999 for unusual events.
  - Examples of codes cover no information, sample issues, laboratory problems, equipment failures, contamination indicators, and unusual events.
  - If a code 999 is used, accompanying text explains the unusual event.
  - Quality codes are included in ECN_PC_qtext.csv for context.

- Quality assurance and data quality checks
  - The ECN conducts quality control using standard QC solutions analyzed alongside field samples (ECN_QC1.csv and ECN_QC2.csv).
  - Supporting documentation clarifies lab analyses, deployment timing, sampling hours, and processing steps.
  - The ECN_PC_chemistry-QC.csv file provides a post-hoc screening of ECN PC measurements, including:
    - Comparison of measured versus theoretical conductivity (COND_RATIO_OK: 1 if within 0.8–1.2; 0 otherwise)
    - Ion balance checks (ION_DIFF_OK: 1 if differences < ±10 µeq/L; 0 otherwise)
    - Phosphate contamination check (PO4_OK: 1 if ≤ 5 µeq/L or not measured; 0 otherwise)
    - Overall data quality (OVERALL_CHECK_OK: 1 if PO4_OK and either COND_RATIO_OK or ION_DIFF_OK are satisfied)
  - Recommendation: Use only samples with OVERALL_CHECK_OK = 1 for trend analysis and flux calculations.

- Data accessibility and barriers (as relevant to monitoring framework authors)
  - Data are publicly shareable, though sharing underlying datasets can be a barrier depending on governance.
  - Metadata completeness and consistency are essential for verification and reuse.
  - Data format and transformation may require effort to ensure usability across analyses.
  - Governance processes and clear data provenance support transparent dissemination and accountability.