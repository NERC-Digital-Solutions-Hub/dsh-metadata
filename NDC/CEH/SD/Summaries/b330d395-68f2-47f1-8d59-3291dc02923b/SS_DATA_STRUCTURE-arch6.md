# Dataset Originator ECN Data Centre

- The ECN Data Centre provides a standardized environmental dataset aimed at understanding environmental change, with site monitoring and network coordination funded by multiple UK government bodies and agencies.
- Data use should be acknowledged, and researchers are requested to send one reprint of any publication citing ECN data.

## Data provenance and governance

- Dataset Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of government departments and agencies (list includes DEFRA, Natural England, NERC, etc.).
- ECN requests acknowledgment of data usage and a reprint of publications that cite ECN data.

## Data structure and download format

- Primary download fields:
  - SITECODE: Unique ECN site code
  - SDATE: Sampling/record date
  - RID: Replicate ID
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting data files provide additional context:
  - ECN_SS2.csv: Lab analysis information per site/replicate
  - ECN_SS_qtext.csv: Free-text quality notes linked to quality codes
  - ECN_QC1.csv: Quality control solution data (lab-level QC)
  - ECN_QC2.csv: Additional lab analysis details for QC datasets
- Site codes and locations (T01–T12) with site names and GPS coordinates; further site information available via the CEH catalogue.

## Protocol and data comparability

- ECN uses standard operating procedures to ensure data comparability across sites; see ss.pdf for collection methods.
- Data collection is designed to be consistent across sites and over time.

## Usage notes and data quality

- Measurement method: Suction samplers for soil solution chemistry; samples collected fortnightly.
- Replicate handling: If a sampler fails, a new RID is assigned; if insufficient sample collected, days may be bulked (RIDs XXS for shallow, XXD for deep).
- Quality control: A standard QC solution is analyzed with field samples; QC data are included in the dataset and quality information should be consulted when using data.
- Quality codes: Site managers assign standard ECN quality codes to indicate data quality factors; a special code 999 is used for unusual events with accompanying text in ECN_SS_qtext.csv.

## Variables and units (FIELDNAME and related information)

- A wide range of water chemistry variables is recorded, including:
  - Alkalinity (ALKY), Calcium (CALCIUM), Chloride (CHLORIDE), Conductivity (CONDY), Dissolved Organic Carbon (DOC)
  - Major ions such as Aluminium (ALUMINIUM), Iron (IRON), Magnesium (MAGNESIUM), Potassium (POTASSIUM), Sodium (SODIUM)
  - Nutrients: Ammonium (NH4N), Nitrate-N (NO3N), Phosphate (PO4P), Total Nitrogen (TOTALN), Total Phosphorus (TOTALP)
  - Analyte-focused measures: Colour (COLOUR), pH (PH) with multiple pH-related measurements
  - Volume and other metadata: VOLUME, VACUUM
- Each FIELDNAME has a description and units (e.g., mg/L, pH, µS/cm).

## Quality codes and interpretation

- Codes cover data gaps and issues such as:
  - 100: No information available
  - 101–111, 113, 115, 122, 123, 124, 126, 137, 140: Various sampling or field issues (equipment, weather, materials)
  - 200–223: Adverse conditions or non-standard sampling
  - 501–508, 509, 511: Laboratory issues (no sample, contamination, pre-filtered samples, filter deposits)
  - 999: Unusual event; see accompanying quality text for details
- Quality codes are provided per FIELDNAME (Q1–Q5) to indicate the quality status of each measurement.

## How to use the data to create products

- Combine across sites and time using SITECODE, RID, and SDATE to build horizon scans, trend analyses, or dashboards for environmental monitoring.
- Leverage accompanying QC and quality text to filter data or annotate uncertainties.
- Use the site metadata (names, coordinates) to spatially visualize site-specific trends and to link with other environmental datasets.

## Practical considerations for data support

- Expect data in multiple CSV files with clear schema; validate RID continuity and handle bulked samples via RID conventions.
- Always consult ECN_qtext and ECN_QC1/ECN_QC2 documentation to interpret data quality and QC backgrounds before analysis or visualization.
- Acknowledge ECN data usage in any outputs and share reprints of publications citing ECN datasets.