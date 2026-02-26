# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Purpose and Scope
- Data schema for recording ICP-MS measured concentrations of elements in water samples from UKCEH/Northumbria sources.
- Captures sample metadata (identifier, site, sampling date, description, preparation notes) and a wide range of element concentrations in milligrams per litre (mg/L).
- Designed to support consistent environmental health assessment and policy performance monitoring over time.

## Data Schema Overview
- Core identifiers: CEH_Sample_Identifier (UKCEH sample code), Site (sampling site), Sampling_Date (date sample collected), Notes (preparation notes), CEH_Sample_Description.
- Measurement data: numerous element concentration fields expressed as Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l, Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l, all in mg/L.
- Special markers: several columns indicate “less than” values (e.g., <Cs, Mo_mg_l) to denote censored data where the concentration is below a detection or reporting threshold.

## Data Fields and Annotations (highlights)
- CEH_Sample_Identifier: UKCEH sample code.
- Site: Sampling site description.
- Sampling_Date: Date sample collected.
- Notes: Preparation or handling notes.
- Element concentration columns: Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l, Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l.
- Units: All element concentrations use mg/L.
- Notation for censored data: Markers indicating values reported as “less than” a threshold (e.g., <Cs_mg_l) are used to identify censored concentrations.

## Measurement Details and Data Quality
- Data are derived from ICP-MS measurements and linked to a single sampling event per row with associated site and date.
- Some metadata fields contain typographic inconsistencies in this description; the intended structure is to support QA, data cleaning, and transformation workflows.
- Concentrations may include censored values (below detection/quantification limits), flagged with a “less than” notation.

## Use in Environmental Monitoring
- Enables standardized reporting of environmental health indicators and policy performance over time.
- Outputs can be produced as reports, maps, and charts to illustrate spatial and temporal trends in metal concentrations.
- Datasets should be stored and uploaded to appropriate data portals to ensure long-term accessibility and re-use.

## Data Management and Accessibility
- Follows standardised data formats with clear field definitions to support verification and quality assurance.
- Analysts should verify data provenance, perform QA/QC, and clean/transform data as needed before analysis.
- Structured to facilitate cross-site comparisons and trend analyses across time.

## Challenges and Opportunities for Analysts
- Increasing value: combine these concentration datasets with other environmental data to enhance monitoring insights and avoid single-use limitations.
- Improving access: ensure underlying data are accessible to stakeholders and compatible with standard environmental data portals.