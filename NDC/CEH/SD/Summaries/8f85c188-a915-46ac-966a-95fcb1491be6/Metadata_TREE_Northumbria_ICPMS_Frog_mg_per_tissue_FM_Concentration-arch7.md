# TREE_Northumbria_ICPMS_Frog_mg_per_tissue_FM_Concentration

## Overview
- Dataset name describing ICPMS-based concentrations of various elements in frog tissue from Northumbria, UK.
- Likely intended to support environmental monitoring and spatial analysis via GIS.
- Focuses on concentrations expressed as mg per total frog tissue fresh mass (FM), with some values given as "less than" detection limits.

## Data structure and key fields
- Taxonomy and sampling identifiers
  - Latin_Species_Name, Common_Species_Name
  - Site (sampling location)
  - Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description (UKCEH identifiers and notes)
  - Tissue (tissue sampled)
- Data description fields
  - Units and Explanation for each column (e.g., I_mg_tissue_FM, Li_mg_tissue_FM, Be_mg_tissue_FM, etc.)
  - Some columns include “<” markers (e.g., <Be, <Ni) indicating concentrations below detection limits
  - Some fields show n/a or inconsistent explanations (e.g., certain lines mistakenly describe Ti or Ca for different elements)
- Measurement scope
  - Concentrations for a wide range of elements (I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U, etc.)
  - Units consistently related to mg per total frog tissue fresh mass (FM)
- Data quality hints
  - Note: “No data indicates no data available for some tissues.”
  - Some column definitions appear misaligned or inconsistent (likely metadata transcription issues)

## Data quality and standardization considerations for GIS
- Data provenance and integration
  - Data appears to span multiple fields and may be combined with spatial identifiers; ensure consistent joining keys (Site, CEH_Sample_Code).
- Metadata reliability
  - Some column explanations are inconsistent or mislabelled (e.g., Ti_mg_tissue_FM with “Concentration of Ca” in explanation). Verify column mappings before GIS use.
- Value handling
  - Presence of “<” values requires censored data handling in analyses derived from maps (e.g., symbolization with capped values or separate indicators for below-detection samples).
- Missing and n/a values
  - Expect some missing data by tissue or site; plan for gaps in spatial analyses.
- Temporal and spatial scope
  - Date of collection and sampling sites are present; ensure accurate geocoding of Site to enable map-based visualizations.

## GIS usage and visualization guidance
- Spatial integration
  - Join the dataset to a site-level spatial layer (points) using Site or CEH_Sample_Code.
  - If available, enrich with coordinates or shapefile of Northumbria sampling locations.
- Map design
  - Create separate maps or faceted views by element or by tissue type.
  - Use graduated symbol or choropleth approaches to show concentration levels across sites.
  - Represent below-detection values with a distinct symbol or censoring layer.
- Data cleaning steps before visualization
  - Normalize and standardize column names and units (confirm mg_tissue_FM).
  - Correct or flag inconsistent explanations (repair metadata mappings).
  - Resolve any mislabelled columns (e.g., ensure element names map to correct measurement columns).
  - Handle “<” values appropriately in derived products.
- Derived products
  - Spatial distribution maps of individual elements or composite contamination indices.
  - Temporal comparisons if multiple collection dates exist.
  - Species- or tissue-specific concentration maps to explore ecological exposure.

## How this aligns with the GIS Specialist role
- Provides a rich, map-ready dataset for communicating spatial patterns of trace elements in amphibian tissue.
- Requires data cleaning, standardization, and careful handling of censored data to produce reliable maps.
- Reflects common GIS challenges highlighted in the archetype (data scattered across fields, variable quality, and need for data transformation and audience-focused visualization).

## Suggested next steps
- Validate and harmonize metadata (correct any mislabelled column explanations).
- Geocode sampling sites and assemble a clean GIS-ready dataset (CSV/GeoJSON with coordinates or a linked shapefile).
- Establish a standard workflow for handling below-detection values and missing data.
- Create an initial set of spatial visualizations (element concentration maps by site, with tissue and species filters).