# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset describing concentrations of multiple elements in frog whole-organism samples from Northumbria, measured using ICP-MS.
- Aims to support environmental health monitoring, policy scrutiny, and informing future decisions by identifying exposure levels in amphibians.

## Data content and structure
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (tissue descriptions related to the calculation)
- Concentration measurements (in mg/kg fresh mass, FM) for a wide range of elements, including I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- Special values:
  - Some entries marked as "<" indicating concentrations below a detection threshold.
  - Several notes indicate “Not calculated” for certain elements (e.g., I).
- Data format emphasizes tissue used, date of collection, and site to support traceability and downstream analyses.

## Units and interpretation
- Concentrations provided in milligrams per kilogram fresh mass (mg/kg FM).
- Some fields denote below-detection values or not-calculated measurements, which require careful treatment in analysis.

## Data quality, sharing, and governance implications
- Metadata is essential for verifiability (species, site, date, tissue notes).
- Open sharing of underlying data can be a barrier when there are sensitive or incomplete metadata; governance processes should ensure data quality, provenance, and appropriate disclosure.
- The dataset’s structure supports integration into dashboards and reports for monitoring policy outcomes, provided metadata completeness and standardization are maintained.

## Relevance for monitoring frameworks and policy decisions
- Enables assessment of environmental exposure to multiple metals in amphibian populations, informing pollution control and site-management decisions.
- Supports trend analysis across sites and time to evaluate effectiveness of regulatory measures.
- Helps identify data gaps (e.g., missing metadata or non-calculated measurements) to prioritize data collection and standardization in future monitoring.