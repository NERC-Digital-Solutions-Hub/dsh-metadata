# Dataset: Macrolepidoptera observations from the UK Environmental Change Network (ECN)

- Purpose and scope
  - Aims to monitor environmental health over time using standardized moth observations.
  - Data derived from established ECN monitoring sites; designed for comparability and policy/performance scrutiny.
  - Observations collected nightly using Rothamsted Insect Survey methodology; quality information accompanies data.
  - Outputs typically include datasets, maps, and charts; datasets stored/uploaded to appropriate portals.

- Data provenance and acknowledgements
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: UK Environmental Change Network programme funded by a consortium of government departments/agencies (list includes DEFRA, Natural England, Environment Agency, Scottish Government, etc.).
  - You are asked to acknowledge ECN data usage and to send one reprint of any publication citing ECN data.

- Methodology and data format (key notes)
  - Protocol: standard light-trap approach for Macrolepidoptera; Rothamsted Insect Survey methodology.
  - Data captured nightly; accompanying quality information must be used.
  - Data structure (Table 1): each observation includes SITECODE (site), LCODE (trap location code; fixed to 1 in this dataset), SDATE (sampling date), FIELDNAME (either a quality code or a species code), VALUE (quality detail or count of individuals).
  - Site details (examples): Drayton (T01), Glensaugh (T02), Hillsborough (T03), Moor House-UP Teesdale (T04), North Wyke (T05), Rothamsted (T06), Sourhope (T07), Wytham (T08), Alice Holt (T09), Porton Down (T10), Cairngorms (T12); coordinates and dataset date ranges provided.
  - Supplemental information: ECN_IM2.csv describes trap open period (period in days); ECN_IM_qtext.csv contains quality notes for observations.

- Quality and species codes (critical reference tables)
  - Quality codes (Table 3a and Table 4): codes such as 100 (no information), 101 (no sample/reading), 999 (unusual event text), and many event-specific codes describing sampling conditions, equipment, environment, and data edits.
  - Species codes (Table 3b): extensive catalogue of moth species and corresponding numeric codes (e.g., 100 = Furcula bicuspis; 22 = Maniola jurtina; 31 = Cynthia cardui; 935 = Biston betularia; 331 = Noctua fimbriata, etc.). A parallel set of 1- or multi-part codes differentiates Latin names and common names.
  - Quality and identification confidence: codes exist to indicate confidence levels (e.g., 239, 240, 241 for high/medium/low confidence taxon IDs).

- Site and data coverage
  - Ten listed sites with varying date ranges spanning early 1990s to around 2012; site-specific data ranges are provided (e.g., Drayton 1993–2012, Glensaugh 1994–2012, Rothamsted 1992–2012, Cairngorms 2001–2012, etc.).
  - The dataset supports long-term monitoring analyses and trend evaluation across multiple locations.

- Data quality, handling, and usage cautions
  - Use the accompanying quality codes to interpret data quality; unusual events are documented via 999 with accompanying text in quality information files.
  - Supplemental quality information files provide context for absences or data inconsistencies.
  - The period of trap operation (PERIOD) can affect counts; refer to ECN_IM2.csv for open-day periods when interpreting results.

- Outputs, sharing, and value enhancement
  - Outputs include standardized formats suitable for time-series analyses, mapping, and visualization of environmental health indicators.
  - A key challenge for analysts: increase dataset value by integrating ECN moth data with other relevant environmental datasets.
  - Another focus: enabling access to underlying data (beyond final outputs) to support broader reuse and verification.

- Endnotes and additional resources
  - More information on ECN sites and data can be accessed via the ECN catalogue and the ECN data portal.
  - Supplemental files ECN_IM2.csv and ECN_IM_qtext.csv provide additional operational and quality context for the dataset.