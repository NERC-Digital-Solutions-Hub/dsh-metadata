# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

## Study area and sampling strategy
- 2019: water samples from remediation systems (n = 31) in Bihar’s Middle Ganga Plain; districts include Patna (n = 18), Buxar (n = 3), Gaya and Katihar (n = 2 each), and Aurangabad, East Champaran, Nawada, Munger, Vaishali (n = 1 each); one additional system in Ballia District, Uttar Pradesh included due to proximity and co-location with Bihar.
- Sampling conducted within a larger stratified random groundwater campaign (~300 tubewells across Bihar); remediation systems were identified opportunistically during field visits.
- Sampling was performed as spot checks under typical operating conditions with owners unaware in advance; urban Patna showed higher sampling due to density of groundwater points and prevalence of household point-of-use systems.
- “Remediation” is used broadly to include point-of-use treatments and other mitigation options (e.g., switching to less-contaminated sources).

## Remediation system sampling & characterization
- For each system, samples were collected from: (i) untreated groundwater feed/inlet and (ii) corresponding finished product/outlet water.
- In some cases, packaged water from local suppliers was sampled; inlet water could not always be sampled for packaged water.
- Inlet samples collected directly from handpumps or household taps; outlet samples from system outlets or nearest access point (e.g., connected storage vessel).
- Samples stored in plastic beakers, thoroughly rinsed between samples.
- Filtration (0.45 μm) prior to laboratory analysis; inlet/outlet water samples stored, then acidified with 2% HNO3 after transport to MAGU for cation/trace metal analysis.

## Chemical analysis (laboratory)
- Analyses conducted at Manchester Analytical Geochemistry Unit (MAGU).
- Major and trace elements measured by:
  - ICP-MS (Agilent 7500cx) for As, U, Zn.
  - ICP-AES (Perkin-Elmer Optima 5300) for Fe, P, Ca, Mg, Mn, Na, K, Si.
- Additional method details and QA/QC procedures available in related publications (Richards et al., 2020).

## Data structure, units and definitions
- Datafile schema (11 columns) includes:
  - System_ID: identifier for remediation system.
  - As_Retention_%: calculated retention of arsenic = (1 − (C_outlet_As / C_inlet_As)) × 100.
  - Tech_Type_Code: remediation technology type (1 = reverse osmosis or other membrane; 2 = non-membrane system).
  - Setting_User_Type_Code: system setting/user type (3 = household; 4 = non-household).
  - Inlet water concentrations: Fe_Inlet_ppm, P_Inlet_ppm, As_Inlet_ppb, Ca_Inlet_ppm, Mg_Inlet_ppm, Na_Inlet_ppm, Si_Inlet_ppm.
- Units:
  - As_Inlet_ppb, As_Retention_% in percent.
  - Fe_Inlet_ppm, P_Inlet_ppm, Ca_Inlet_ppm, Mg_Inlet_ppm, Na_Inlet_ppm, Si_Inlet_ppm in ppm.
- Note: Values below detection are input as 0.1 ppb for As and 0.001 for Fe and P.
- The dataset focuses on remediation samples with paired inlet-outlet data; full description available in related publication.

## Data structure details (selected)
- Spreadsheet contains data for 31 remediation systems, with 11 columns including System_ID, As_Retention%, Tech_Type_Code, Setting_User_Type_Code, and selected inlet water parameters (Fe, P, As, Ca, Mg, Na, Si).

## Quality control and references
- Quality control details described in Richards et al., 2022.
- Key related publications:
  - Richards, L.A. et al. (2020). Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. International Journal of Environmental Research and Public Health, 17, 2500.
  - Richards, L.A. et al. (2022). Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection. Science of the Total Environment, 830, 154580.

## Data availability and contact
- Data Identifier: 77700f8e-5da6-45ab-9c12-df1a7d20bc32
- Primary Data Contacts: Dr Laura Richards (laura.richards@manchester.ac.uk) or Prof. David Polya (david.polya@manchester.ac.uk)