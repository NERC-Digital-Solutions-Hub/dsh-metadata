# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

- Overview
  - Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology, ecn@ceh.ac.uk)
  - Data providers: UK government departments/agencies consortium (e.g., DEFRA, Natural England, NERC, SEPA, etc.)
  - Scope: Precipitation chemistry data from ECN, 1992–2012, across 12 ECN sites
  - Purpose: Long-term environmental change research; fosters data awareness, reuse, and attribution

- Data scope and content
  - Measurement focus: Precipitation chemistry variables (alkalinity, major ions, pH, conductivity, dissolved organic carbon, etc.)
  - Sample collection: Weekly bulk samples; standard QC solution analyzed alongside field samples
  - Output format: Data organized by site, date, variable, and value
  - Data structure components:
    - SITECODE: Unique ECN site code
    - SDATE: Sampling date
    - FIELDNAME: Variable measured
    - VALUE: Measured value

- Site details
  - 12 sites with names, coordinates, and dataset date ranges (examples)
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
  - Date ranges per site vary (1992–2012 overall; some sites have gaps or shorter spans)

- Fieldnames and units (examples)
  - Alkalinity (ALKY, mg/L)
  - Aluminium (ALUMINIUM, mg/L)
  - Calcium (CALCIUM, mg/L)
  - Chloride (CHLORIDE, mg/L)
  - Colour (COLOUR, nM)
  - Conductivity (CONDY, µS/cm)
  - Dissolved Organic Carbon (DOC, mg/L)
  - Iron (IRON, mg/L)
  - Magnesium (MAGNESIUM, mg/L)
  - Ammonium (NH4N, mg/L)
  - Nitrate Nitrogen (NO3N, mg/L)
  - pH (PH, pH scale 1–14)
  - Aquacheck pH readings (PHAQCS, PHAQCU)
  - Phosphate Phosphorus (PO4P, mg/L)
  - Potassium (POTASSIUM, mg/L)
  - Sulphate Sulphur (SO4S, mg/L)
  - Sodium (SODIUM, mg/L)
  - Total Nitrogen (TOTALN, mg/L)
  - Total phosphorus (TOTALP, mg/L)
  - Volume (VOLUME, mL)
  - Quality codes (Q1–Q6)
- Metadata and supporting information
  - Additional documentation: ECN_PC2.csv with sampling and lab metadata (dates, times, labs, replicates)
  - Quality information: Site-managed ECN quality codes indicating data quality factors
  - Protocol: PreciptationChemistryProtocol.pdf (accompanying documentation)
  - Quality codes: Standard ECN codes (e.g., 100–133, 180, 182, 187, 191, 200, 222, 223, 501–507, 508–511, 999) with explanations; 999 indicates unusual events and can include accompanying narrative text
  - Supporting documentation URL/DOI: 10.5285/0cd4abd2-1bc9-48bc-b5c2-cebdeaa23ceb

- Data quality, provenance, and usage guidelines
  - Quality assurance: Weekly field samples analyzed with a concurrent QC standard; QC data linked to measurements
  - Usage guidance: Use accompanying quality information to assess data suitability; acknowledge ECN data usage and provide a reprint for publications citing ECN data
  - Data governance: Data is managed with site-specific quality codes and metadata; full provenance is documented in ECN_PC2.csv and the associated protocol

- Access, usage, and citation considerations
  - Data usage acknowledgement: ECN requests acknowledgment and a reprint of any citing publications
  - Access pathways: Data site and supporting docs (ECN_PC2.csv, protocol) are organized to support discovery and reuse; consult the provided DOI for full documentation

- Practical implications for Data Leaders
  - Strengths: Longitudinal, multi-site precipitation chemistry data with standardized fields and QC framework; rich metadata enables cross-site comparisons and trend analysis
  - Challenges to plan for: Data gaps by site/date, variable data quality flags, potential access barriers if relying on ancillary documents; need to integrate site-level quality codes into data governance processes
  - Opportunities: Leverage standardized fieldnames and QC codes to harmonize datasets; enable cross-partner data sharing and co-ownership of data products; use rich metadata to improve discoverability and reuse across environmental-change or policy analyses

- Contacts
  - Data originator: ECN Data Centre, Centre for Ecology and Hydrology (ecn@ceh.ac.uk)
  - Collaboration and acknowledgment: Follow ECN guidance on usage and reprints for scholarly work