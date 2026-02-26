# Environmental_CBPeru.csv

- Dataset of measured physicochemical variables in 10 rivers from glacial valleys in the Cordillera Blanca, Ancash, Peru (Parón, Huaytapallana, Llanganuco) derived from the study of glacier retreat and its relation to aquatic biodiversity.

## Aim

- Document and standardize environmental data to analyze physicochemical changes under glacial retreat and relate them to macroinvertebrate biodiversity.
- Provide a consistent dataset suitable for monitoring environmental health and policy performance over time.

## Scope and Study Area

- Location: Rivers originating on western flanks of Huandoy and Huascarán glaciers.
- Sites: 10 rivers, coded P01–P10.
- Valleys: Parón, Huaytapallana, Llanganuco.
- Glacier coverage at sites ranges widely (GCC percentages provided for each site).
- Related article focus: Declining glacier cover drives changes in aquatic macroinvertebrate biodiversity in the Cordillera Blanca.

## Data Collection and Methods

- Sampling periods: October 14–30, 2019 and October 7–16, 2020 (two seasons: wet and dry).
- In-field measurements (every 5 seconds, averaged to 5 minutes):
  - Water temperature, electrical conductivity, pH, dissolved oxygen.
  - Instrument: Multi 3630 IDS multiparameter.
- Laboratory measurements:
  - Turbidity (lab analysis).
  - Nutrients: total nitrogen (TN), total phosphorus (TP).
  - Dissolved organic carbon (DOC), dissolved inorganic carbon (DIC).
  - Metal ions: analyzed by ICP-OES.
  - Anions: NO3 and others analyzed by HPLC-IC.
  - Dissolved carbon (DC).
  - Turbidity (confirmed with field data).
- Channel stability:
  - Pfankuch Index (six components: substrate angularity, rock brightness, particle size/compactness, scouring/deposition, stable channel percentage, vegetation).
- Topography:
  - Slope from a 12.5 m resolution DEM (ALOS PALSAR).
  - Distance to glacier along river channel using a 10 m Sentinel-2 image.
- Site metadata and geographic context provided (coordinates, basin area, glacier area, GCC, distance to glacier, slope, altitude).

## Variables and Measurements

- 37 environmental variables recorded per site per season.
- Variables include:
  - Turbidity (NTU), Water Temperature (°C), Electrical Conductivity (µS/cm), pH, Dissolved Oxygen (mg/L), Pfankuch Index.
  - Nutrients: Total Nitrogen (mg/L), Total Phosphorus (mg/L), DOC (mg/L), DIC (mg/L), DC (mg/L).
  - Anions: F, Cl, SO4, NO3 (all mg/L).
  - Cations and trace metals: Al, B, Be, Ca, K, Mg, Na, Si, Zn, Sr, Li, Mn, Ni, Fe, Cu, Co, Cr, Pb, Cd, Se, Te, Ti, etc. (units mg/L as specified).
- Special notes: Data reported in a single Excel sheet with sites as rows and variables as columns; season indicated by a separate column (w = wet, d = dry).

## Site and Geographic Information

- Site codes: P01–P10, corresponding to sampling locations.
- Geographic context for each site includes:
  - Valley name (Parón, Huaytapallana, Llanganuco).
  - Basin area (km²), Glacier area (km²), GCC (%).
  - Distance from glacier (km), Slope (%), Altitude (m a.s.l.).
- Example highlights:
  - GCC ranges from near 0% to 66.1% across sites.
  - Some sites have complete glacier proximity data; one site shows zero GCC (glacier-free).
- Table 2 (in document) provides site-specific geographic variables and GCC values.

## Data Structure and Access

- Data structure: Environmental_CBPeru.csv with one sheet containing all sampling periods.
  - First column lists Sites; first row lists environmental variables.
  - Season column indicates sampling period (w for wet, d for dry).
- Nature and units:
  - 37 variables with units such as NTU, °C, µS/cm, mg/L, and others as listed (Table 3 in document).
- Versioning:
  - Version 1.0; metadata describes authorship, data collection roles, and planning/management contributions.

## Quality Control

- In-field equipment calibrated before each field campaign.
- Calibration standards used to ensure accuracy (including Environment and Climate Change Canada ERM-CA022a and interlaboratory standards for metals in soft water).
- Quality assurance applied to measurement accuracy and precision across parameters.

## Data Management, Use, and Context

- Data collected to support analysis of how glacial retreat drives changes in river chemistry and aquatic biodiversity.
- Dataset is intended for broader use beyond the originating study and aligns with the aim of enabling data reuse and transparency.
- Researchers and policymakers can combine this dataset with other environmental or biodiversity data to enhance monitoring and evaluation of environmental health over time.

## Contributors and Version

- Sample collection: Palacios, E.; Medina, K.; Loarte, E.
- Laboratory analysis: Palacios, E.; Gamboa, M.; Brown, L.
- Supporting information: Castañeda, A.; Polo, R.; Tapia, P.
- Planning and Management: Medina, K.; Loarte, E.; Brown, L.; Pellicciotti, F.
- Authoring and version control: Palacios, E. (Version 1.0).