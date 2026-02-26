# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Overview
- This is a data dictionary/schema for the TREE_Northumbria_ICPMS_Water_FM_Concentration dataset, detailing sample metadata and concentrations of a wide range of elements in water.
- Designed to support data discovery, cleaning, transformation, and the creation of user-friendly data products (dashboards, reports) for exploration and interpretation.
- Aims to enable self-serve access to concentration data across multiple elements and sites, with metadata to contextualise samples.

## Data structure and key fields
- Metadata fields
  - CEH_Sample_Identifier: UKCEH sample code
  - CEH_Sample_Description: UKCEH sample description
  - Site: Sampling site
  - Sampling_Date: Date sample collected
  - Notes: Notes on preparation
- Concentration fields (all in mg/L unless noted)
  - Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l
  - Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l
  - Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l
  - Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l
- Notes on special values
  - Several concentration fields include “less than” indicators (denoted by a < marker), e.g., Cs_mg_l, Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l.
  - Some fields include placeholders indicating non-applicable units or explanatory notes (e.g., “n/a” in units explanations) and occasional typographical inconsistencies in descriptions.

## Data quality and preparation considerations
- Handle censored data: interpret and document “less than” values appropriately (e.g., as left-censored data) during analysis.
- Unit consistency: standardise all concentration fields to mg/L for analysis.
- Data integrity: be aware of typographical errors in field descriptions; validate field mappings to ensure correct element identification.
- Metadata completeness: verify sample identifiers, site names, and sampling dates for accurate linking across datasets.

## How this supports data use
- Enables combining sample metadata with multi-element concentration data for site- and time-based analyses.
- Facilitates the creation of dashboards and pivotable summaries to compare concentration patterns across elements and sites.
- Supports data dissemination to end users with self-serve access to concentration measurements and their contextual metadata.

## Practical considerations for analysts (Data Support perspective)
- Clean and harmonise: unify field naming where needed, fix obvious typos, and ensure consistent units across all records.
- Address non-detects: decide on a consistent approach for less-than values (e.g., substitution, censoring) prior to visualization or statistical analysis.
- Document data lineage: maintain clear mapping between UKCEH sample codes, sample descriptions, and site identifiers to ensure traceability.
- Promote data reuse: consider publishing pre-aggregated views (per site or per date range) and clear usage guidance to improve uptake and reduce redundant work.