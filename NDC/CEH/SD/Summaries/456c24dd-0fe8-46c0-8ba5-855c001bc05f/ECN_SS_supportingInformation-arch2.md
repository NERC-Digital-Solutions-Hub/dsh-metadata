# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

- Overview
  - Purpose: provide a consistent, monitorable view of soil solution chemistry over time to support environmental health assessment and policy performance.
  - Origin and stewardship: Dataset from the ECN Data Centre (Centre for Ecology and Hydrology) with data providers including a consortium of UK government departments and agencies.
  - Acknowledgment: users should acknowledge ECN data and send one reprint of any publication citing the data.

- Protocol and Sampling
  - Sampling method: suction samplers used to measure soil solution chemistry.
  - Frequency: fortnightly sampling.
  - Data integrity: sampler replacements indicated by a new replicate ID (RID); if insufficient samples, days may be bulked with RID codes XXS (shallow) or XXD (deep).
  - Quality control: standard QC solution analyzed alongside field samples; QC data accompany the dataset and should be used in analysis.

- Data Structure and Coverage
  - Core data fields: SITECODE (site ID), SDATE (sampling date), RID (replicate ID), FIELDNAME (variable), VALUE (measured value).
  - Site coverage: 12 ECN sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa/Snowdon, Cairngorms) with precise coordinates and dataset date ranges.
  - Date ranges: most sites span 1992–2012 with some variations (e.g., Porton Down 1996–2000, Snowdon 1997–2012, Cairngorms 1999–2012).

- Measurements and Field Names
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, absorbance at 436 nm, nM)
  - Conductivity (CONDY, µS/cm)
  - Dissolved Organic Carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Magnesium (MAGNESIUM, mg/L)
  - Ammonium (NH4N, mg/L)
  - Nitrate-N (NO3N, mg/L)
  - pH (PH, pH scale 1–14)
  - Aquacheck pH (PHAQCS, pH scale 1–14; stirred)
  - Aquacheck pH (PHAQCU, pH scale 1–14; unstirred)
  - Phosphate Phosphorus (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate Sulphur (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Total Nitrogen (TOTALN, mg/L)
  - Total dissolved Phosphorus (TOTALP, mg/L)
  - Vacuum (vacuum, bar)
  - Volume (VOLUME, mL)
  - Quality codes (Q1–Q5)

- Quality and Quality Codes
  - Site managers assign ECN quality codes from a standard list to flag data quality issues; codes cover issues from no information to sample loss or measurement problems.
  - Common codes include 100–199 (data gaps), 501–509 (laboratory issues), 999 (unusual event with accompanying text).
  - Unusual events with 999 are documented in accompanying quality text.
  - Quality information accompanies the dataset and should be consulted when using the data.

- Additional Analytical Information
  - An accompanying document, ECN_SS2.csv, provides expanded measurements metadata, including sampling deployment dates/times, lab ID, and timing of pH measurements, filtration, and analysis completion.

- Data Access and Use
  - Data usage should be acknowledged to demonstrate dataset value and impact for environmental change research.
  - Users are requested to send one reprint of any publication citing ECN soil solution chemistry data.

- Supporting Documentation and Access
  - Additional documentation: “UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012” with DOI: http://doi.org/10.5285/456c24dd-0fe8-46c0-8ba5-855c001bc05f
  - Purpose of accompanying materials: provide detailed data structure, quality codes, and measurement context to support robust data QA/QC and reuse.