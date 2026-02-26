# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

- Purpose of the dataset
  - Contains Macrolepidoptera (moths) monitoring data from the UK Environmental Change Network (ECN) programme.
  - Used to understand environmental change effects on moth communities and support scientific reporting and decision-making.

- Data providers and governance
  - Dataset Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
  - Acknowledgement and publication requests: please acknowledge data use and send one reprint of publications citing the data.

- Protocol and methodology
  - Standardized operating procedures to ensure cross-site comparability (im.pdf explains data collection).
  - Methodology follows Rothamsted Insect Survey light-trap protocol; data recorded nightly.
  - Data intended to identify macrolepidoptera and to support quality control via supplemental materials.

- Data structure and download fields
  - Core identifiers
    - SITECODE: unique code for each ECN site.
    - LCODE: location ID (unique within site).
  - Temporal and sampling fields
    - SDATE: sampling date.
    - FROMDATE / SPERIOD_D: period over which traps were set (days) as per ECN_IM2.csv.
    - YEAR, WEEK: year and week of sampling.
  - Measurements
    - FIELDNAME: variable being measured (e.g., Q1, Q2, etc.; each corresponds to a species code).
    - VALUE: numeric count or code value for the given FIELDNAME.
  - Site and location details
    - Explanatory information provides site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Cairngorms) with geographic coordinates.
  - Supporting documentation
    - ECN_IM2.csv: period (days) traps were open; most often SPERIOD_D = 1.
    - ECN_IM_qtext.csv: quality codes and free-text explanations for data quality issues.

- Species coding and interpretation
  - FIELDNAME values (e.g., Q1, Q2, etc.) map to moth species via code numbers (e.g., 100 = Alder Kitten; 101 = Poplar Kitten; many entries cover hundreds of species with common names in accompanying mapping).
  - Explanatory Information section lists a large mapping of numeric codes to species names.
  - Note on special cases: species 3392 (Mesapamea secalis/didyma) is a inseparable pair; species 3394 (Amphipyra berbera berbera) can appear as 2507 in past records.
  - The dataset may include both typical and melanic forms for some species (e.g., deviations in 2530–2539 series).

- Quality and quality codes
  - ECN_IM_qtext.csv provides quality codes to indicate factors affecting data quality (e.g., weather, sampling issues, debris in trap, equipment problems, etc.).
  - Quality code descriptions include a broad set (e.g., 100 = No information; 101 = No sample/readings; 200s for adverse conditions; 500s for laboratory/processing issues; 999 = Unusual event).
  - The text field accompanying codes captures context when codes do not cover a specific circumstance.

- Data usage considerations for analysts
  - Local-scale and cross-site comparability enabled by standardized protocol and site metadata, but users should be mindful of:
    - Potential data gaps or periods with quality issues (as flagged by ECN_IM_qtext.csv).
    - Variation in trap periods (SPERIOD_D) and site-specific reporting.
    - Complex species mappings and occasional unidentifiable entries requiring careful handling.
  - Data often require incorporating quality codes and site metadata to ensure robust analyses.
  - Data can support correlations between moth catches and environmental variables, and can feed predictive models of moth abundance under environmental change scenarios.

- Accessibility and metadata quality
  - Data are organized by site and sampling date, with explicit metadata on site coordinates and sampling protocols.
  - The ECN data portal and accompanying documentation enable discoverability and reproducibility (site codes, location IDs, and quality notes).

- Practical guidance for analysts
  - Start from ECN_IM2.csv and ECN_IM_qtext.csv to understand sampling periods and data quality before modeling.
  - Use SITECODE and LCODE to join with site metadata (location, coordinates) for spatial analyses.
  - Leverage the FIELDNAME–VALUE pairs to map species counts, using the ECN_IM_qtext.csv mapping for species identifications and quality context.
  - Acknowledge data provenance and provide one reprint for publications citing ECN data.