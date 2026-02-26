# ECN_AN2.csv

- Overview
  - Source: Dataset Originator is ECN Data Centre; ECN data are managed by the UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.
  - Purpose: Provide NO2 monitoring data across ECN sites to understand environmental change, support research, and inform policy decisions.
  - Acknowledgement: Data users should acknowledge ECN data use and send one reprint of any publication citing ECN data.

- Provenance and Ownership
  - Dataset Owner organisations: Agri-Food and Biosciences Institute; Biotechnology and Biological Sciences Research Council; Natural Resources Wales; Defence Science & Technology Laboratory; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; NI Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
  - Usage notes emphasize citing ECN and following their data-use guidelines.

- Data Protocol and Quality Assurance
  - Protocol: Standard operating procedures ensure comparability across sites; two-week tube exposure; use of blank tubes for quality checks; accompanying quality information provided with data.
  - Quality assurance: Data undergo cleaning, transformation, and analysis; site managers assign quality codes to reflect factors affecting data quality; unusual events may be documented with free text (quality code 999).

- Data Structure and Content
  - Primary download format fields: SITECODE, SDATE, TUBEID, FIELDNAME, VALUE.
  - Supporting metadata:
    - ECN_AN2.csv contains sample collection information: DEPDATE, DEPHOUR, DEPMINS; SDATE, SHOUR, SMINS.
  - Quality context: ECN_AN_qtext.csv holds site-manager quality explanations for data quality codes (linked via SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).
  - Site-wide identifiers and mapping: Explanatory Information for Site Codes provides 12 ECN sites (T01–T12) with site names and geographic coordinates; additional site information available at the ECN catalogue link.

- Variable Definitions
  - WEIGHTNO2: Weight of NO2 on the mesh (micrograms).
  - NO2: NO2 concentration (micrograms per cubic meter).
  - NO2PPB: NO2 concentration (parts per billion).
  - TDIFF: Exposure time (minutes).
  - Q1–Q8: Quality code fields indicating data quality factors (integers). Quality codes are defined in the ECN quality code list.

- Quality Codes (selected examples)
  - 100: No information available – data lost.
  - 101–+ متفاوت: Various reasons for no sample/reading (equipment out of action, sample lost, etc.).
  - 200–205, 507–513: Adverse conditions or laboratory-related issues; data corrections or notes.
  - 501–509, 510–513: Laboratory-level issues or sample processing details.
  - 999: Unusual event – see accompanying quality text.

- Explanatory Information
  - Site Codes: Detailed mapping of T01–T12 to site names and coordinates (e.g., T01 Drayton; T02 Glensaugh; ...; T12 Cairngorms).
  - Variable Meaning: Clarifies FIELDNAME values and units; confirms measurement intent and data interpretation.
  - Data Access and Use: Additional ECN site information available via the provided catalogue URL.

- Usage and Citations
  - Acknowledge use of ECN datasets and submit one reprint of resulting publication.
  - ECN data are accompanied by metadata to support verification and reproducibility; data may require transformation to align with local governance and reporting standards.

- Particular Challenges (as it pertains to monitoring framework authors)
  - Data gaps and gaps in metadata can hinder usability; policy monitoring requires robust, well-documented metadata.
  - Data access and timely availability may be constrained by governance or data-sharing barriers.
  - Siloed information across organisations can impede integration; shared data governance processes are essential.
  - Public sharing requirements for datasets can discourage data use if not accompanied by clear provenance and licensing.
  - Ensuring data remains up-to-date, well-described, and compliant with standards necessitates ongoing metadata enrichment and data stewardship.