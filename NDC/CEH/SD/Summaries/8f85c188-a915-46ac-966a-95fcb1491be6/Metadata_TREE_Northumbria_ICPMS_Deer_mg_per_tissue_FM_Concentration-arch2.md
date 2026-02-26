# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Overview
- Dataset of element concentrations in deer tissue collected for environmental monitoring, using ICP-MS.
- Aims to standardise data to support assessment of environmental health and policy performance over time.
- Likely produced by an organisation with set monitoring responsibilities (e.g., UKCEH/Northumbria context) and designed for reuse in reports, maps, and charts.

## Dataset structure and key fields
- Biological and sampling metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site (sampling location), Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description (UKCEH linkage)
  - Tissue (type of deer tissue sampled)
- Measurement details:
  - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Be_mg_per_tissue_FM, Na_mg_per_tissue_FM, Mg_mg_per_tissue_FM, Al_mg_per_tissue_FM, P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM, Ti_mg_per_tissue_FM, V_mg_per_tissue_FM, Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM, Ni_mg_per_tissue_FM, Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM, Rb_mg_per_tissue_FM, Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM, Cs_mg_per_tissue_FM, Ba_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM
- Data formatting notes:
  - Units are milligrams per total deer tissue fresh mass (mg per tissue FM).
  - Some entries are prefixed with “<” indicating a less-than value (e.g., “<Be”, “<Al”, “<V”, “<Cr”, “<Ni”, “<Mo”, “<Ag”, “<Ba”, “<Pb”, “<U”).
  - Some data gaps exist (e.g., “No data for Roe deer 4 thyroid” across several elements).

## Data quality and standardisation
- Concentrations are presented in a uniform unit (mg per tissue FM) to enable cross-sample comparability.
- Detection-limit indicators (“<” values) are noted where applicable.
- Some missing data are explicitly flagged (e.g., Roe deer 4 thyroid data not available).
- Metadata links (CEH_Sample_Codes and CEH_Sample_Description) facilitate traceability to original sample records.

## Purpose in environmental monitoring
- Supports assessment of environmental contamination and biological uptake in wildlife over time.
- Enables categorisation or benchmarking of environmental health against standards, aligned with standardised reporting formats.
- Designed to be stored in appropriate data portals and used to generate outputs such as reports, maps, and charts.

## Practical considerations for analysts
- When using: account for < value entries as censoring/detection limits in analyses.
- For Roe deer 4 thyroid data: expect gaps; plan imputation or exclusion where appropriate.
- Consider enriching with external data (e.g., additional environmental datasets) to increase data value and support cross-dataset analyses.
- Ensure data provenance by linking to CEH sample codes and descriptions for reproducibility.