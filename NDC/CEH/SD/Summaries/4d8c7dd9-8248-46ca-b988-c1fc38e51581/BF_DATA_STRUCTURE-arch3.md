# Dataset Description and Usage Guidelines for ECN Frog Spawning Observations

- Overview
  - Dataset originates from the ECN Data Centre and is part of the UK Environmental Change Network program.
  - Purpose: provide environmental health measures (phenology of Common Frog spawning) to scrutinise and evaluate policy and inform future decisions.
  - Ownership and sponsorship: ECN programme supported by a consortium of UK government departments and agencies.

- Dataset provenance and use
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: UK government departments/agencies funding site monitoring or network coordination (e.g., DEFRA, Natural England, NERC, Scottish Government, Welsh Government, etc.).
  - Acknowledgement and credit: users should acknowledge ECN data and send one reprint of any publication citing the data.
  - Standard procedures: ECN provides standard operating procedures (BF.pdf) to ensure data comparability across sites.

- Methodology and scope
  - Phenology-based monitoring: spawning of Common Frog in selected pools and ditches; egg masses counted as an indicator of population health.
  - Complementary data: laboratory analyses of water sampled at observed pools.
  - Metadata and quality: accompanying quality information is essential when using the data.

- Data structure and access
  - Data download fields:
    - SITECODE: unique ECN site code
    - LCODE: location code (within site)
    - FROMDATE: start date of data quality text applicability
    - SDATE: sampling date
    - FIELDNAME: variable measured
    - VALUE: measured value
  - Supporting documentation: ECN_BF_qtext.csv contains site-quality text explanations for data quality issues.
  - Quality texts: site managers assign quality codes from a standard list; if a non-listed event occurs, code 999 is used with accompanying text.

- Variables and measurements
  - FIELDNAME categories include a wide range of chemical, physical, and biological measurements (examples):
    - Alkalinity (ALKY), alkalinity units
    - Major ions and nutrients (e.g., Aluminium, Calcium, Chloride, Conductivity, Ammonium, Nitrate-N, Total Nitrogen, Total Phosphorus)
    - Water chemistry and properties (pH, Temperature, Dissolved Organic Carbon, Colour/Absorbance, DOC, NO3N, NH4N, PO4P, SODIUM, POTASSIUM, S supports)
    - Biological/phenology indicators (CONGDATE, HATCHDATE, SPAWNDATE, NEWMASS, LEAVEDATE, SURFAREA, STAGE, PERCDEAD)
    - Physical parameters (DEPTH, MAXTMP, MINTMP, VOLUME, VACUUM)
  - QUALITY fields: Q1–Q8 and Q1–Q8 (quality codes) plus broader quality indicators (e.g., 501–513, 999) to denote data issues or unusual events.
  - Units: various units provided for each field (e.g., mg/L, mS/cm, pH, date, counts, percentages).

- Site codes and locations
  - Example sites and names with coordinates (T01–T11):
    - T01 Drayton
    - T02 Glensaugh
    - T03 Hillsborough
    - T04 Moor House - Upper Teesdale
    - T05 North Wyke
    - T06 Rothamsted
    - T08 Wytham
    - T09 Alice Holt
    - T10 Porton Down
    - T11 Y Wyddfa - Snowdon
  - Coordinates are provided for each site location.

- Data governance, quality, and transparency
  - Quality assurance: ECN standard SOPs ensure cross-site comparability and data are quality assured, cleaned, transformed, and clearly presented (via reports, charts, dashboards).
  - Metadata and quality barriers: data sharing may be hindered by metadata gaps; quality codes and accompanying text help mitigate interpretation issues.
  - Data updates: ongoing data quality and up-to-date information are emphasized; site managers actively annotate quality events.
  - Data sharing and governance: explicit emphasis on data sharing of underlying data and adherence to governance processes.

- Usage considerations and limitations
  - The data rely on site manager quality annotations; users should consult ECN_BF_qtext.csv for context on quality codes.
  - Some data transformations may be required to harmonize fields across sites; SOPs are provided to support this.
  - An unusual event (code 999) requires review of accompanying quality text for interpretation.

- Contact and further information
  - Dataset contact: ECN Data Centre (ecn@ceh.ac.uk).
  - Additional documentation: BF.pdf explains data collection protocols and ensures comparability across ECN sites.
  - Acknowledgement: use of data should include an acknowledgement and, where applicable, a reprint request for publications citing the data.