# TREE_Northumbria_ICPMS_Frog_mg_per_tissue_FM_Concentration

## Overview
- A dataset of metal concentrations in frog tissue measured by ICP-MS, focused on Northumbria (UK Centre for Ecology and Hydrology context).
- Captures elemental concentrations across a range of elements (I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) expressed as mg per total frog tissue fresh mass.
- Includes essential metadata for each sample: Latin and common species names, sampling site, collection date, UKCEH sample code and description, and the tissue sampled.

## Data schema and fields
- Core identifiers and context:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Tissue
- Concentration measurements (mg per tissue FM) for:
  - I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Data nuances:
  - Some values use a less-than sign (<) indicating a concentration below a reporting/ detection threshold.
  - Some entries include "No data" or "n/a" indicating missing data for particular tissues or measurements.

## Key data fields and units
- Concentrations are reported as mg_tissue_per_tissue_FM (mg per total frog tissue fresh mass) for each element.
- Tissue-specific context is provided per sample, enabling comparisons by species, site, date, and tissue type.
- The dataset uses standard column naming conventions (e.g., I_mg_tissue_FM, Li_mg_tissue_FM, Be_mg_tissue_FM, etc.) to denote each element’s concentration.

## Data notation and quality flags
- "<" markers denote that the concentration is reported as less than the stated value (censored data).
- Some rows include inconsistencies in the description (e.g., mismatched element explanations in a few fields), which may require careful data cleaning during analysis.
- Occasional "n/a" or "No data" entries indicate missing measurements or metadata gaps for certain tissues.

## Data quality and challenges for analysts
- Data may have scale and access challenges common in environmental datasets:
  - Missing data for certain tissues or elements.
  - Values represented as censored (<) data requiring appropriate handling (e.g., survival analysis methods, imputation limits).
  - Potential inconsistencies or typos in column explanations that need verification during data cleaning.
- Metadata richness (species names, site, date, sample codes) supports cross-analysis but requires careful provenance tracking and standardization for reproducible results.

## Potential analyses and uses
- Assess metal bioaccumulation patterns across frog species, tissues, and sites.
- Explore temporal trends in sampling dates and corresponding elemental concentrations.
- Correlate tissue concentrations with environmental or site characteristics to infer exposure pathways.
- Develop exposure risk indicators for wildlife health assessments and support regulatory or conservation decisions.
- Build and validate predictive models of tissue metal burdens under varying environmental conditions.

## Provenance, access, and reproducibility
- Data linked to UKCEH sampling codes and descriptions; facilitates traceability to original sample records.
- Aligns with practices of making datasets discoverable with metadata to enable reuse and replication of analyses.