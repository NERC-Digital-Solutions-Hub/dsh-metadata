# Environmental_CBPeru.csv

- Overview
  - A dataset of measured physicochemical variables from 10 rivers in the glacial valleys of Parón, Huaytapallana, and Llanganuco in the Cordillera Blanca, Ancash, Peru.
  - Linked to the study on how declining glacier cover drives changes in aquatic macroinvertebrate biodiversity; data used to analyze physicochemical changes along a gradient of glacial coverage.

- Sampling and sites
  - Fieldwork conducted in two periods: October 14–30, 2019 and October 7–16, 2020.
  - Rivers originate on the western flank of glaciers Huandoy and Huascarán.
  - 10 sites coded P01–P10 with geographic and glacial-context information (Valley, basin area, glacier area, glacier coverage, distance from glacier, slope, altitude, etc.).
  - Glacier coverage (GCC) varies across sites (from 0.00% to 66.1%), with some sites having missing GCC values.
  - Geographic data derived from 12.5 m DEM (slope) and Sentinel-2 imagery (distance to glacier; glacier delineation).

- Measured parameters (37 environmental variables)
  - In situ measurements: water temperature (WT, °C), electrical conductivity (CE, µS/cm), pH, dissolved oxygen (DO, mg/L), turbidity (Turb, NTU).
  - Laboratory analyses: total nitrogen (TN, mg/L), total phosphorus (TP, mg/L), dissolved organic carbon (DOC, mg/L), dissolved inorganic carbon (DIC, mg/L), dissolved carbon (DC, mg/L), and a suite of metals and ions (e.g., Al, B, Ca, K, Mg, Na, Zn, Fe, etc.; various units as mg/L).
  - Anions and cations: F, Cl, SO4, NO3 (mg/L).
  - Methods: metals by ICP-OES; TN/TP by Skalar Sans++; NO3 by HPLC-IC (Dionex ICS3000); DOC/DIC by Analytik Jena Multi NC2100; turbidity by Oakton T-100 173 sensor.
  - Channel stability: Pfankuch Index (measures substrate stability across six bed components).

- Data structure and organization
  - Data stored in a single Excel sheet.
  - Columns: sampling site (P01–P10) in the first column; environmental variables in the first row; an explicit Season indicator (w = wet, d = dry) for each record.
  - 37 environmental variables represented with clear units (e.g., Turb NTU, WT °C, CE µS/cm, TN mg/L, TP mg/L, DOC mg/L, DIC mg/L, DC mg/L, NO3 mg/L, Al mg/L, Ca mg/L, etc.).

- Topography and geographic information
  - Site-level variables include: basin area (km²), glacier area (km²), GCC (%), distance from glacier (km), slope (%), altitude (m a.s.l.).
  - Data sources: DEM-based slope (12.5 m resolution) and Sentinel-2 imagery (10 m resolution) for glacier distance and delimitation.

- Quality control and data provenance
  - Equipment calibrated before each field campaign.
  - Calibration standards included Environment and Climate Change Canada materials and ERM-CA022a references for metals.
  - Clear delineation of roles: sample collection, laboratory analysis, supporting information, and planning/management contributors.

- Access, provenance, and references
  - Data file: Environmental_CBPeru.csv.
  - Contributors: Palacios, E.; Medina, K.; Loarte, E.; Gamboa, M.; Brown, L.; Castañeda, A.; Polo, R.; Tapia, P.; Pellicciotti, F.
  - Reference material: Pfankuch, J. D. (1975) on stream reach inventory and channel stability.