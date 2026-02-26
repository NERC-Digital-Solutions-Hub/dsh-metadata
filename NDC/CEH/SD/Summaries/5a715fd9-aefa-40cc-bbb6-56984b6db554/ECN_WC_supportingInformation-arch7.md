# ECN Water Chemistry Dataset Description

- Overview
  - Dataset from the ECN Data Centre detailing surface water chemistry measurements across multiple UK sites.
  - Includes weekly dip-sample chemistry data with a long temporal span (1990s–2012) and multiple sites.
  - Data rich in chemical parameters, with quality control and accompanying metadata to inform data usage.

- Data Origin and Providers
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology) — email: ecn@ceh.ac.uk; website: http://data.ecn.ac.uk
  - Data Providers: UK Environmental Change Network (ECN) partners and funders (numerous government departments and agencies listed).
  - Usage acknowledgement required; return one reprint of any publication citing the data.

- Protocol and Data Quality
  - Sampling protocol: surface water dip samples collected weekly.
  - Quality control: standard QC solution analyzed with field samples; QC data available with dataset.
  - Use accompanying quality information when using the data; protocol referenced as surfaceWaterChemistryProtocol.pdf.

- Data Structure (Core)
  - SITECODE, Description: Unique ECN site code
  - LCODE, Description: Location code per site for core measurements
  - SDATE, Description: Sampling date
  - FIELDNAME, Description: Measured variable (chemical parameter)
  - VALUE, Description: Measured value

- Site Codes (Geographic and Temporal Coverage)
  - T02 Glensaugh (coordinates provided); date range 1993–2012
  - T04 Moor House - Upper Teesdale; multiple location codes with varying date ranges (1992–2011)
  - T05 North Wyke; date range 1993–2012
  - T06 Rothamsted; date range 1994–2012
  - T07 Sourhope; date range 1993–2012
  - T08 Wytham; multiple location codes; date ranges 1993–2012
  - T11 Y Wyddfa – Snowdon; date range 1997–2012
  - T12 Cairngorms; date range 1999–2012
  - Each site’s entries include precise coordinates and dataset date coverage per location

- Fieldnames and Units (Selected Parameters)
  - Alkalinity (ALKY) – mg/L
  - Aluminium (ALUMINIUM) – mg/L
  - Calcium (CALCIUM) – mg/L
  - Chloride (CHLORIDE) – mg/L
  - Colour (COLOUR) – absorbance at 436 nm (nM)
  - Conductivity (CONDY) – microSiemens/cm
  - Dissolved Organic Carbon (DOC) – mg/L
  - Iron (IRON) – mg/L
  - Magnesium (MAGNESIUM) – mg/L
  - Ammonium (NH4N) – mg/L
  - Nitrate Nitrogen (NO3N) – mg/L
  - pH (PH) – pH units
  - Aquacheck pH (PHAQCS, PHAQCU) – pH scale 1–14
  - Phosphate Phosphorus (PO4P) – mg/L
  - Potassium (POTASSIUM) – mg/L
  - Sulphate Sulphur (SO4S) – mg/L
  - Sodium (SODIUM) – mg/L
  - Stage (STAGE) – water level in mm
  - Total Nitrogen (TOTALN) – mg/L
  - Total dissolved Phosphorus (TOTALP) – mg/L
  - Quality codes (Q1–Q6) for data quality indicators; no-unit placeholders

- Additional Analytical Information
  - ECN_WC2.csv provides extended measurements: SITECODE, LCODE, sampling date/time (SDATE, SHOUR, SMINS), LAB_NID, pH measurement timing, filtration date (FILTDATE), analysis completion date (COMPDATE)
  - This supports temporal precision and labs involved in analysis

- Quality Coding
  - ECN quality codes indicate data quality factors (e.g., sample loss, equipment issues, weather impacts, laboratory issues, unusual events)
  - Codes range from 100–999 with specific meanings (e.g., 100 no information, 101 no sample, 501–-508 laboratory-related issues, 999 unusual event)
  - Site managers assign codes; descriptive text available for non-standard cases (code 999)

- How GIS Specialists Can Use This Dataset
  - Spatial integration: use SITECODE/LCODE with site coordinates to map sampling locations and visualize spatial patterns in water chemistry.
  - Temporal analysis: leverage SDATE (and SHOUR/SMINS from ECN_WC2.csv) to study seasonal and annual trends across sites.
  - Multi-parameter mapping: map key variables (e.g., nitrate, phosphate, pH, alkalinity) to assess spatial gradients and ecosystem implications.
  - Data quality awareness: filter or weight data based on ECN quality codes to ensure reliable map products.
  - Data preparation: join ECN_WC2.csv for precise timing and laboratory metadata; ensure unit consistency across parameters before GIS rendering.

- References and Usage Notes
  - Acknowledgement and data citation requested; publication reprints encouraged.
  - Refer to surfaceWaterChemistryProtocol.pdf for detailed collection and QA procedures.
  - Ensure alignment with provided quality information when analyzing or visualizing the dataset in GIS workflows.