# Data dictionary and QA metadata for dissolved constituents in water samples

- The document is a comprehensive data dictionary and quality/metadata specification for dissolved chemical constituents in water samples, detailing a wide range of analytes (e.g., Al, Gran alkalinity, Ca, Cl, Fe, NO3, SO4, P, K, etc.) with standardized fields per analyte.
- It combines analytical details, sample processing, and data quality flags necessary for consistent data capture, storage, and interpretation across a data system.

## Data structure and fields

- For each determinate, the following fields are defined and populated:
  - FORM, DETERMINAND, UNITS, LQDC, QUOTE TO, ANALYTICAL METHOD QC, DATA QUALIFIER, FILTRATION, PRESERVATION, METHOD, COMMENT.
- Common processing and handling details:
  - Filtration: typically 47 mm filters (0.45 μm) in field (exceptions for rain/cloud), with some entries using GF/C glass fiber or unfiltered (but allowed to settle).
  - Preservation: acidification to 1% with high-purity nitric acid; some samples stored at 4°C in the dark; for carbon- or TOC-related measurements, specific storage/handling rules apply.
  - Methodologies: inductively coupled plasma (ICP-AES/ICP-OES), ICP-MS, automated colorimetry, pH electrometric methods, and TOC/chemical assays (e.g., molybdenum blue reactions, titanium-based methods).
  - Units vary by analyte (e.g., ug/l, mg/l, mg/l-NH4, uEq/l for alkalinity).
- Survey and data flow context:
  - Some entries describe flow-related sampling (baseflow vs stormflow) and survey design (e.g., after extended dry periods or during intensely wet periods).

## Quality assurance, accuracy, and data integrity

- Accuracy validation sources:
  - Interlaboratory proficiency testing: Aquacheck LGC scheme for ICP-OES/ICP-MS element determinations.
  - Trace element accuracy: Standard Reference Material 1643b (NBS) for ICP-MS determinations.
- Data qualifier semantics and handling:
  - 10: Raw data from the instrument with no LQD (no rounding); quotations to laboratory standards via LQDC and Quote To values.
  - 11: Raw data at or below detection limit for most time series.
  - 12: Raw data with historical method-change issues (sensitivity or calibration changes).
  - 13: Very unusual data with systematic patterns; removal from database advised; treat with extreme caution.
  - 14: Data corrected for interference (e.g., Si); notes on potential degradation with long storage where concentrations are low.
- Ongoing QA notes within the dataset:
  - Instances of data irregularities (e.g., sensitivity changes, atypical weekly patterns) are documented and flagged for cautious handling or removal when justified.

## Coverage and context

- Analytes covered include a broad suite of major and trace elements, anions, and related parameters (e.g., Al, Gran alkalinity, Ca, Cl, NO3, SO4, Fe, Mn, Ni, P, K, Na, NH4, F, DOC, TOC, pH, flow status).
- The document emphasizes data standardization, discoverability, and metadata richness to support cross-partner analytics and broader data-system interoperability.
- It notes historical methodological changes (e.g., 1992–1998 ICP/AAS method shifts) that affected data sensitivity and interpretation, highlighting the need for careful data curation and documentation of methodological provenance.

## Implications for Data Leaders

- Data system design:
  - Build and enforce a standardized metadata schema that captures analyte-specific fields (FORM, DETERMINAND, UNITS, LQDC, etc.) and processing details (FILTRATION, PRESERVATION, METHOD, QC).
  - Ensure clear data provenance, including instrument type, method changes, and quality flags to support traceability and auditability.
- Data quality governance:
  - Integrate external QA references (interlaboratory schemes and SRMs) into routine data validation and confidence scoring.
  - Maintain and communicate data qualifiers and their meanings to downstream users, including cautions about raw data vs processed data.
- Data discovery and stewardship:
  - Provide robust documentation of sample collection context (flow type, baseflow vs stormflow) and survey design to aid interpretation and cross-network coordination.
  - Address historical data gaps and standardization issues (method-change periods, unit conventions) to improve comparability across time and datasets.
- Collaboration and community practice:
  - Align with wider data communities to share best practices for analyte metadata, QA protocols, and data-cataloging standards.
  - Use the proficiency-testing and SRM references to benchmark internal laboratories and maintain a living quality-assurance framework.

## Recommendations

- Establish a central data catalog with standardized fields for all analytes and consistent use of qualifiers (10–14) and LQDC/Quote To semantics.
- Implement formal data provenance tracking, capturing method, filtration, preservation, instrument, and QA references for every observation.
- Regularly review and annotate data during known method-change windows; flag affected records with appropriate qualifiers and notes.
- Integrate proficiency-testing results and SRMs into the data quality dashboard to monitor ongoing accuracy across laboratories and time.
- Document the survey design and sampling contexts (baseflow vs stormflow) to support downstream analyses and cross-partner collaborations.