# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - The UK Environmental Change Network (ECN) dataset is managed by the ECN Data Centre, Centre for Ecology and Hydrology.
  - Dataset Owners: ECN programme, sponsored by a consortium of UK government departments and agencies funding site monitoring or network coordination (e.g., DEFRA, Natural England, NERC, etc.).
  - Usage requirement: Users should acknowledge the data source and send one reprint of any publication that cites ECN data.

- Data provenance and governance
  - Protocols: ECN has standard operating procedures to ensure comparability of data across sites; accompanying documentation explains data collection methods.
  - Metadata and documentation: Data downloads are accompanied by detailed metadata and explanatory files to support reuse.

- Data collection protocol and quality assurance
  - Measurement method: Passive diffusion tubes measure NO2 concentration over a two-week exposure period.
  - Quality controls: Blank tubes are deployed and analyzed with experimental tubes as a quality check.
  - Quality information: Users must apply accompanying quality information when using the data; site managers assign quality codes to flag data quality issues.

- Data structure and metadata
  - Primary download schema: SITECODE, SDATE, TUBEID, FIELDNAME, VALUE.
  - Site and sample documentation: Supporting ECN_AN2.csv provides site, tube deployment, and sampling date/time details.
  - Quality context: ECN_AN_qtext.csv contains narrative quality notes for unusual events; QUALITY codes (Q1–Q8) accompany data rows.
  - Quality codes: Standard list includes codes for equipment issues, sample loss, environmental disturbances, processing anomalies, and other factors; 999 indicates an unusual event with accompanying text.

- Variables and measurement details
  - FIELDNAME options: WEIGHTNO2 (mesh weight), NO2 (NO2 concentration in micrograms/m3), NO2PPB (NO2 concentration in ppb), TDIFF (exposure time in minutes), Q1–Q8 (quality code values).
  - Units: WEIGHTNO2 in micrograms; NO2 in micrograms/m3; NO2PPB in ppb; TDIFF in minutes.

- Site information
  - Explanatory information lists 12 ECN sites (T01–T12) with site names and geographic coordinates; examples include Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, and Cairngorms.
  - Additional information about ECN sites is available via the ECN catalogue link.

- Data access and updates
  - Data are shared via ECN data portals with defined field names and value conventions; ongoing updates and standardization are supported by the protocols and accompanying documentation.

- Practical considerations for Data Stewards
  - Use of standardized procedures is essential to maintain cross-site comparability.
  - Ensure metadata completeness and linkage to supporting files (ECN_AN2.csv, ECN_AN_qtext.csv).
  - Monitor and document data quality using the QC codes (Q1–Q8) and narrative quality text for unusual events (quality code 999).
  - Be mindful of potential data limitations highlighted by site managers (e.g., equipment issues, ambient disturbances) and reflect these in data sharing and governance practices.
  - Maintain proper citation and request reprints to demonstrate data value and usage.