# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

## Overview
- Presents hydrogeochemical data for groundwater remediation systems identified in Bihar (Middle Ganga Plain) during 2018–2022, with one additional system from nearby Ballia District, Uttar Pradesh.
- Data collected as part of a larger stratified groundwater sampling campaign (~300 tubewells) to understand contaminant distribution (arsenic, uranium) and remediation performance.
- Remediation is a broad term including point-of-use water treatment and switching to less-contaminated sources; the study captures systems where remediation is in operation under typical conditions.

## Study area & sampling strategy
- Field sites: Bihar across multiple districts (Patna, Buxar, Gaya, Katihar, Aurangabad, East Champaran, Nawada, Munger, Vaishali) with higher sampling density in Patna; one adjacent Ballia site included due to proximity.
- Sampling design: opportunistic “spot check” within the larger groundwater campaign; access secured at each location; some systems were already known to researchers.
- System scale: 31 remediation systems sampled in Bihar; broader campaign involved ~300 tubewells to contextualize remediation units and prevalence.

## Remediation system sampling & characterization
- For each system, paired samples collected:
  - Inlet water (untreated groundwater) used by the system.
  - Outlet water (treated water) from the system.
- Some additional packaged water from local suppliers was included.
- Sampling details: inlet collected from handpumps or household taps; outlet collected from system outlets or nearest accessible point; samples stored in rinsed plastic glassware.
- Remediation types include various technologies (e.g., reverse osmosis or other membrane systems vs non-membrane systems) and household vs non-household settings.

## Chemical analysis (laboratory)
- Analyses conducted at Manchester Analytical Geochemistry Unit (MAGU).
- Elements/parameters measured:
  - Arsenic (As), Uranium (U), Zinc (Zn) by ICP-MS.
  - Iron (Fe), Phosphorus (P), Calcium (Ca), Magnesium (Mg), Manganese (Mn), Sodium (Na), Potassium (K), Silicon (Si) by ICP-AES.
- Quality assurance/quality control details referenced to Richards et al. (2020) and extended in Richards et al. (2022).

## Nature and units of recorded values
- Data file structure includes: System_ID, As_Retention_% (calculated), Tech_Type_Code (remediation tech category), Setting_User_Type_Code (household vs non-household), inlet/outlet concentrations for Fe, P, As, Ca, Mg, Na, Si, etc.
- Calculations:
  - As_Retention_% = (1 - (As_outlet / As_inlet)) × 100
- Data codings:
  - Tech_Type_Code: 1 = reverse osmosis or other membrane system; 2 = non-membrane system.
  - Setting_User_Type_Code: 3 = household; 4 = non-household.
- Notes on data values:
  - Non-detects (below detection limit) recorded as 0.1 ppb for As (ICP-MS) and 0.001 for Fe and P (ICP-AES).

## Data structure & content
- Spreadsheet contains data for 31 remediation systems in Bihar, with 11 columns detailing arsenic retention, technology category, setting category, and inlet water composition for selected ions (Fe, P, As, Ca, Mg, Na, Si).

## Quality control
- QA/QC procedures described in Richards et al. (2022); detailed methodology available there.

## Relevance for monitoring frameworks
- Demonstrates how field sampling of remediation systems can be integrated with laboratory analyses to quantify remediation performance (e.g., As retention) across different technologies and settings.
- Provides metadata-rich data (system identifiers, technology type, setting type, inlet/outlet chemistry) useful for evaluating remediation strategies and informing policy/decision-making.
- Highlights data governance considerations:
  - Clear data structure and codes enable comparability across systems.
  - Open questions about data sharing, metadata completeness, and the need for standardized data management practices.
- Useful for evaluating remediation options in policy contexts, supporting decisions on technology deployment, setting of monitoring requirements, and assessment of real-world effectiveness.

## Limitations & notes
- Data pertain to remediation samples only where paired inlet–outlet data were available; representation is therefore subset of the broader sampling campaign.
- More remediation units encountered in urban Patna reflect population density and prevalence of household point-of-use systems.
- Some data aspects rely on supplementary details in the associated full publication (Richards et al., 2020; 2022).

## References
- Richards, L.A.; Kumar, A.; Shankar, P.; Gaurav, A.; Ghosh, A.; Polya, D.A. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. Int. J. Environ. Res. Public Health 17, 2500.
- Richards, L.A.; Parashar, N.; Kumari, R.; Kumar, A.; Mondal, D.; Ghosh, A.; Polya, D.A. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection, Science of the Total Environment, 830, 154580.