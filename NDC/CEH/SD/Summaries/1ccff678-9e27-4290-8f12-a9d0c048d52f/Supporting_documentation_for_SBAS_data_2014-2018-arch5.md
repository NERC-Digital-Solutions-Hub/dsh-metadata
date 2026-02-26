# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2014 to 2018.

## Context and Scope
- Part of an ongoing fortnightly monitoring dataset for South Basin of Windermere, Cumbria, England.
- Time period: January 2014 to end of 2018.
- Measurements cover surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Water samples are integrated from 0 to 7 m and collected from a boat at a marked buoy location in the deepest part of the lake.

## Data Collected and Variables
- TEMP: Surface temperature in degrees Celsius.
- OXYG: Surface oxygen saturation (% air-saturation).
- SECC: Secchi depth in metres.
- ALKA: Alkalinity in µg CaCO3 per litre.
- pH: pH value.
- NH4N: Ammonium in µg N per litre.
- NO3N: Nitrate in µg N per litre.
- PO4P: Soluble reactive phosphate in µg P per litre.
- TOTP: Total phosphorus in µg P per litre.
- SIO2: Dissolved reactive silicon in µg per litre.
- TOCA: Phytoplankton chlorophyll a in µg per litre.

## Sampling Regime and Collection Methods
- Fortnightly sampling regime as part of ongoing monitoring.
- Measurements performed from a boat at a buoy, deepest part of the lake.
- Data entries include a detection-limit indicator for values below detection limit (<LOD).

## Data Structure and Documentation
- Data format: CSV file.
- Columns:
  - Date: Date of measurement.
  - Variable, Description: Name and description of each measured variable.
  - Value, Description: Measured value for each variable.
  - Sign (if<LOD), Description: Indicator if a value is below the detection limit.

## Quality Control and Data Quality
- Raw data have not yet been quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data are due to weather conditions or staff shortages.

## Data Availability and Sharing
- Data available for download as a CSV with the described structure and metadata.
- Dataset is part of a funded monitoring program and linked to ongoing data sharing under the relevant programme.

## Provenance and Funding
- Funding: Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Usage in recent publications (examples):
  - State of the Climate in 2018 (Blunden & Arndt, 2019)
  - The extent and variability of storm-induced temperature changes in lakes (Doubek et al., 2021)
  - Temporal and spatial variation in distribution of fish environmental DNA in England's largest lake (Lawson Handley et al., 2019)
  - Other related climate and lake-ecology studies (2016–2018)

## Stewardship Considerations and Challenges
- Incomplete picture of user needs and priorities.
- Timely data delivery from contributors.
- Ensuring data creators meet standards (metadata, format, accuracy).
- Interoperability across many systems and formats.
- Handling large datasets and legacy databases requiring bespoke solutions.

## Recommendations for Reuse and Next Steps
- Apply formal quality control and calibration to convert raw data into production-ready datasets.
- Enhance metadata to align with data governance standards (data lineage, provenance, methods, QC flags).
- Establish clear update and embargo policies, and create documented data-sharing agreements.
- Prepare data for ingestion into data portals and catalogues, ensuring consistent variable definitions and units.
- Link data with published studies and provide citations and usage notes to support reproducibility.