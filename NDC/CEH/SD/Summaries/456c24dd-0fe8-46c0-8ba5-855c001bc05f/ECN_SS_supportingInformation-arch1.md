# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

- Overview
  - A long-term dataset of soil solution chemistry measurements collected by suction samplers, typically fortnightly.
  - Covers 1992–2012 across multiple UK sites, with structured metadata and quality information to support analysis.

- Data Origin and Providers
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Data providers: UK government departments and agencies (e.g., DEFRA, Natural England, National Environment bodies, NERC councils, Scottish/Welsh equivalents, NI Environment Agency, etc.).
  - Acknowledgement and publication request: Users should acknowledge the data and send one reprint of any citing publication.

- Protocol and Sampling
  - Sampling method: Suction samplers used to measure soil solution chemistry.
  - Frequency: Fortnightly sampling.
  - Replicates: Replacements indicated by a new RID; insufficient samples on a given day may be bulked (XXS for shallow, XXD for deep).
  - Quality control: A standard QC solution is analyzed with field samples; QC data available alongside the dataset; use accompanying quality information when using data.

- Data Structure and Content
  - Core data fields: SITECODE (site ID), SDATE (sampling date), RID (replicate ID), FIELDNAME (variable measured), VALUE (measured value).
  - Dataset components: Main ECN soil solution chemistry data plus additional analytical information file (ECN_SS2.csv) with sampling deployment times, lab IDs, and measurement timestamps.

- Site Coverage
  - 12 ECN sites:
    - T01 Drayton
    - T02 Glensaugh
    - T03 Hillsborough
    - T04 Moor House - Upper Teesdale
    - T05 North Wyke
    - T06 Rothamsted
    - T07 Sourhope
    - T08 Wytham
    - T09 Alice Holt
    - T10 Porton Down
    - T11 Y Wyddfa - Snowdon
    - T12 Cairngorms
  - Each site entry includes coordinates and the dataset date range (varies by site, from early 1990s to 2012).

- Variables and Units (Fieldnames)
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
  - Nitrate Nitrogen (NO3N, mg/L)
  - pH (PH, pH units)
  - Aquacheck pH (PHAQCS, pH units)
  - Aquacheck pH unstirred (PHAQCU, pH units)
  - Phosphate Phosphorus (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Total Nitrogen (TOTALN, mg/L)
  - Total Dissolved Phosphorus (TOTALP, mg/L)
  - Vacuum (VACUUM, bar)
  - Volume of sample (VOLUME, mL)
  - Quality codes (Q1–Q5)

- Additional Analytical Information
  - ECN_SS2.csv provides extended metadata:
    - SITECODE, RID, deployment/debulk dates/times, sampling times, lab ID, pH measurement times, filter dates, and analysis completion dates.

- Quality and Metadata
  - ECN quality codes describe data quality and operational issues (e.g., sample loss, equipment failure, abnormal sampling times, weather impacts, laboratory issues, etc.).
  - A special code 999 indicates an unusual event with accompanying text in the quality metadata.
  - Use the accompanying quality information to properly interpret data values and to identify potentially affected measurements.

- Supporting Documentation and Access Notes
  - Supporting doc: UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012 (doi: 10.5285/456c24dd-0fe8-46c0-8ba5-855c001bc05f).
  - Additional details are provided in ECN_SS2.csv and the linked protocols (soilSolutionChemistryProtocol.pdf).

- Practical Considerations for Analysts
  - Data may be missing or flagged with quality codes; filter or account for these using the ECN quality metadata.
  - Data are presented across multiple sites with varying date ranges; ensure proper temporal and spatial alignment when aggregating.
  - Data come with explicit documentation on sample handling (e.g., bulked samples, replicate IDs) and QC procedures to support reproducible analyses.
  - Acknowledgement and citation requirements should be followed, including sharing a reprint if the data are used in publications.

- Endnotes
  - The dataset is designed to support analyses of environmental change impacts on soil chemistry, with emphasis on robust metadata, quality control, and cross-site comparability.