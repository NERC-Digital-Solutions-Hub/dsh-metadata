# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Overview
- A tabular data collection of concentration ratios comparing vegetation (fresh mass) to soil (dry mass) for ICP-MS measurements.
- Each record links a plant species and sampling event to a soil sample used to calculate the concentration ratio.
- Includes sample identifiers, descriptions, dating, and notes about vegetation preparation.
- Contains concentration-ratio fields for a broad suite of elements; some values are marked as less-than indicators.

## Key fields and structure
- Taxonomy and naming
  - Latin_Species_Name, Common_Species_Name
- Sampling and site details
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Notes (preparation notes)
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (link to soil sample used)
- Concentration ratio measurements (for many elements)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Sr_Concentration_Ratio, Pb_Concentration_Ratio, Tl_Concentration_Ratio, U_Concentration_Ratio
  - Notation/formatting markers indicate less-than values (e.g., "<I", "<Li", "<Mo", "<As", etc.)
  - Some fields include dual or misformatted descriptions (e.g., “1 = n/a / 2 = …” or stray markers), suggesting inconsistencies in the data dictionary
- Units and explanations
  - Units are largely n/a for many fields
  - Each concentration-ratio field is described as the ratio of Fresh Mass Vegetation to Dry Mass Soil

## Spatial and GIS considerations
- Primary use: map-based visualization of element uptake across sampling sites and species.
- Relationships to map layers
  - Link sample records to site point data for spatial mapping
  - Optional overlay with soil concentration data to analyze vegetation-to-soil uptake patterns
- Data handling for GIS
  - Manage less-than values as censored data points in analyses/maps
  - Standardize field names and ensure consistent schema before joining with other GIS datasets

## Data quality, limitations, and preparation needs
- Data quality issues
  - Inconsistent field naming and formatting (typos and misaligned descriptions)
  - Mixed or unclear handling of less-than markers and the meaning of certain “1 = n/a / 2 = …” annotations
  - Some fields may require cleaning, standardization, and normalization
- Gaps and resolutions
  - Data may be sparse for some elements or sites; resolution may vary between sampling events
  - Lack of explicit units for ratios (most are n/a); require documentation for end users
- Recommended preparation steps
  - Clean field names, harmonize to a consistent schema
  - Clearly define how to treat "<" values in analyses and maps
  - Link vegetation records to precise site coordinates and associated soil samples
  - Document data provenance (origin from CEH samples, Northumbria ICPMS study) for traceability

## How to use in GIS workflows
- Create point or small-extent polygon maps showing concentration ratios by element for each site/species
- Facet or filter by species, site, date, or target elements to explore spatial patterns
- Use color scales or symbols to represent ratio magnitudes; consider log-transformed scales for wide ranges
- Integrate with soil data to assess vegetation-to-soil uptake relationships
- Handle less-than values appropriately in analyses and communicate these decisions in maps and metadata

## Provenance and context
- Appears to originate from a Northumbria ICPMS vegetation study with CEH sample identifiers and related soil samples
- Data dictionary is partially present but contains formatting inconsistencies that require careful curation before release or sharing with GIS end-users