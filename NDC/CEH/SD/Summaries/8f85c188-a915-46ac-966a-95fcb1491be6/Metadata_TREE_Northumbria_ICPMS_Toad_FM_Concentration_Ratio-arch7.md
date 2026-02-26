# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

## Overview
- A data dictionary for a dataset that records ICP-MS concentration ratios of metals/metalloids in toad tissue relative to co-located soil.
- Covers samples from Northumbria, with detailed metadata on species, site, collection date, and CEH sample codes.
- Each row includes multiple element concentration ratio fields (fresh mass of toad vs. dry mass soil) and accompanying explanations.

## Dataset Structure
- Single table format containing:
  - Taxonomy and identification fields
  - Spatial and temporal metadata
  - CEH sampling metadata
  - Notes on preparation
  - Co-located soil sample reference used to calculate ratios
  - A large set of concentration ratio fields for numerous elements

## Key Fields and Descriptions
- Latin_Species_Name: Latin name of the species
- Common_Species_Name: Common name of the species
- Site: Sampling site
- Date_Sample_Collected: Date of sample collection
- CEH_Sample_Code: CEH sample code
- CEH_Sample_Description: Description of the CEH sample
- Notes: Notes about preparation of toads
- Co_Located_Soil_Sample_Used_To _Calculate_Concentration_Ratio: Description of the soil sample used to compute the ratio
- I_Concentration_Ratio to U_Concentration_Ratio: Concentration ratios for each element, defined as the Fresh Mass Toad (wholebody) divided By Dry Mass Soil
  - Elements included: I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- All units are listed as n/a (dimensionless)

## Data Quality and Processing Considerations
- Data are a mix of species, site, and sampling metadata aligned with ratio calculations.
- Ratios are dimensionless (no units) and rely on a co-located soil sample for each toad sample.
- The dataset includes notes on sample preparation, which can affect comparability across sites or years.
- Some field names contain spacing or typographical inconsistencies (e.g., Co_Located_Soil_Sample_Used_To _Calculate_Concentration_Ratio), which may require data cleaning for GIS use.

## GIS Use and Visualization Notes
- The Site field provides a spatial anchor; join to a spatial layer of sampling locations to map distributions of each concentration ratio.
- The wide format (one row per site/sample with many element ratios) is suitable for feature-based styling or for pivoting to long format for time-series or multi-layer visualizations.
- Visual opportunities include choropleth or graduated symbol maps by specific element ratios, and cross-element comparisons by site or species.

## Data Gaps and Challenges
- Potential lack of standardized resolutions or consistent data standards across records.
- Data cleaning and normalization may be needed before integration with other GIS datasets.
- Missing or incomplete fields could impact spatial analyses if coordinates or precise locations are not available.