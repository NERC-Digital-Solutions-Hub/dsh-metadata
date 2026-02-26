# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

- Purpose and relevance: Provides long-term environmental health data (precipitation chemistry) to scrutinise policy, evaluate environmental Change drivers, and inform future decisions. ECN data are intended to support monitoring frameworks with traceable, comparable measurements across sites and time.

- Dataset origin and governance:
  - Originator: ECN Data Centre, Centre for Ecology and Hydrology.
  - Data providers: UK government departments and agencies sponsoring ECN, including multiple environmental and scientific bodies.
  - Usage notes: Acknowledgement of ECN data use is requested; authors should send one reprint of any publication citing the data.

- Protocol and quality assurance:
  - Sampling method: Bulk collectors used to measure precipitation chemistry; samples collected weekly.
  - Quality control: A standard QC solution is analyzed with field samples to verify laboratory performance; use quality information accompanying the dataset.
  - Data handling: Data are quality assured, cleaned, transformed, analyzed, and presented via reports, charts, or dashboards; underlying data should be shared appropriately under governance rules.

- Data structure and contents:
  - Core structure: SITECODE (site ID), SDATE (sample date), FIELDNAME (variable measured), VALUE (measured value).
  - Supporting metadata: VOLUME (sample volume) and quality codes (Q1–Q6) describing data quality factors.

- Site codes and temporal coverage:
  - 12 ECN sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) with geographic coordinates.
  - Date ranges vary by site, spanning from the early 1990s to 2012 (some sites end earlier than others).

- Measured variables (Fieldnames) and units:
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, nM; absorbs at 436 nm)
  - Conductivity (CONDY, µS/cm)
  - Dissolved Organic Carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Magnesium (MAGNESIUM, mg/L)
  - Ammonium (NH4N, mg/L)
  - Nitrate-N (NO3N, mg/L)
  - pH (PH, pH units)
  - Aquacheck pH (PHAQCS, PHAQCU, pH units)
  - Phosphate (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Total Nitrogen (TOTALN, mg/L)
  - Total dissolved Phosphorus (TOTALP, mg/L)
  - Volume of sample (VOLUME, mL)
  - Additional QA fields: Q1–Q6 (quality codes)
  - Additional notes: Data fields linked to QC and QC-related metadata

- Additional analytical information:
  - ECN_PC2.csv provides further measurement context (timestamps for deployment, sampling, filtration, and analysis) to support reproducibility and quality assessment.

- Quality codes and data quality management:
  - ECN quality codes (examples): 100 (no information available), 101–124 (various sampling or sample issues), 501–511 (laboratory issues), 999 (unusual event requiring textual QA notes).
  - Codes are assigned by site managers to flag factors affecting data quality; unusual events documented in accompanying quality text.

- Metadata and documentation:
  - Supplementary materials include “UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012” and related quality information.
  - The accompanying documentation emphasizes the need to use quality information when analyzing data and to consult metadata for interpretation.

- Implications for monitoring frameworks:
  - Strengths: Longitudinal, multi-site chemistry data enable trend analysis, cross-site comparison, and assessment of policy impacts on environmental chemistry.
  - Data governance considerations: Importance of metadata richness, standardised quality codes, and clear sharing rules to support transparent monitoring. Potential barriers include data silos, access delays, imperfect metadata, and the need for data transformation for usability.
  - Practical use: Use for calibration of environmental health indicators, informing monitoring design, and evaluating data quality governance across agencies. Requires adherence to data sharing and acknowledgment practices to maximize utility and credit.