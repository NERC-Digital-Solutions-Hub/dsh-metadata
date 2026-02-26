# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- A dataset capturing concentrations of multiple elements in frog tissue (frog and frogspawn) from Northumbria, using ICP-MS.
- Includes detailed sampling and specimen metadata to support environmental health monitoring and policy scrutiny.
- Aims to inform decision-making and future monitoring strategies by providing a comprehensive contaminant profile.

## Data Structure and Content
- Taxonomic metadata:
  - Latin_Species_Name, Common_Species_Name
- Sampling metadata:
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue sampled (e.g., frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio (ratio of fresh to dry mass)
- Sample identifiers and descriptions to support traceability
  - CEH_Sample_Codes, CEH_Sample_Description
- Measurements:
  - Concentrations reported on a mg/kg dry mass basis (I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, B_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, S_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM).
  - Some entries use a “<” marker to indicate concentrations below reporting/quantification limits for certain elements (e.g., <Be, <Al, <Ni, <Se, <Ag, <Ba, <U).
- Data structure emphasizes flagging detection limits and ensuring traceability back to original sample descriptions.

## Data Quality, Processing, and Presentation
- Data are intended to be quality assured, cleaned, transformed, and clearly presented (e.g., in reports, charts, dashboards).
- Metadata explanations accompany each column to aid interpretation and verification of datasets against monitoring requirements.
- Underlying data sharing is supported to enable transparency, with careful handling of detection-limit values and non-detect annotations.

## Interpretation and Use for Monitoring Frameworks
- Enables assessment of contaminant burdens in amphibians as an environmental health indicator.
- Supports spatial comparisons across sampling sites and temporal trends after appropriate QA and standardization.
- Facilitates policy scrutiny of environmental quality and informs future monitoring design and data governance needs.

## Challenges and Barriers (Typical for Monitoring Framework Authors)
- Lack of data or data at insufficient quality for decision-making.
- Limited access to data in a timely manner.
- Information silos within and between organisations.
- Public sharing requirements for datasets posing barriers to data usage.
- Keeping data up to date and maintaining metadata quality.
- Inadequate metadata hindering verification of data suitability.
- Data formats requiring substantial transformation before use.
- Communicating complex findings clearly to stakeholders.
- Implementing data governance to ensure standards, storage, sharing, and currency of datasets.