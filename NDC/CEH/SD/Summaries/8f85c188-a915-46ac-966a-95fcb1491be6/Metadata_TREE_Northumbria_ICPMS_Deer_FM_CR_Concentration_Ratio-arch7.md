# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- A dataset of concentration ratios comparing woodmice (fresh mass, wholebody) to soil (dry mass) at Northumbria sampling sites, derived from ICP-MS measurements.
- Purpose: support GIS-based visualization and exploration of element transfer or accumulation between woodmice and their soil environment.

## Data structure and key fields
- Species and site information
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of the soil sample used for the ratio)
- Concentration ratio variables (per element)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Each ratio is defined as: Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil
  - Some fields indicate special coding:
    - "1 = n/a" and "2 = [value]" suggesting a two-part encoding (missing vs. actual value)
    - "<I" or similar markers indicate a less-than value for a given concentration ratio (e.g., <I_Concentration_Ratio)
- Units and data conventions
  - Units: listed as n/a (no units provided) for concentration ratios
  - Formatting irregularities present in the header (some field names appear truncated or inconsistently spaced)

## Semantics and interpretation
- Spatial/temporal context: Each row corresponds to a sampling event at a Site on Date_Sample_Collected, with an associated woodmice sample and a co-located soil sample used to compute the concentration ratio.
- Data interpretation notes:
  - Concentration ratios are derived by comparing woodmice tissue mass to soil mass, enabling spatial comparisons of metal uptake or exposure across sites.
  - Some ratio fields may be missing or encoded with a placeholder (1 = n/a) or flagged as less-than values; careful handling is required during GIS processing.
  - The dataset relies on a CEH sample description and site-level metadata to contextualize the ratios.

## Data quality, standards, and preparation considerations
- Potential issues to address for GIS use:
  - Inconsistent field naming and possible header corruption in the provided data dictionary.
  - Missing or ambiguous values due to 1 = n/a encodings and less-than indicators.
  - Absence of explicit units for each concentration ratio; assume dimensionless or unitless ratio unless metadata specifies otherwise.
  - Data distributed across multiple sources may require harmonization and provenance tracking.
- Recommended preparation steps:
  - Normalize field names (remove extra spaces, standardize to a consistent naming convention).
  - Decode 1 = n/a vs. 2 = value to construct a clean numeric field, and explicitly handle less-than values (censor the data or store as a flag plus the bound value).
  - Parse Date_Sample_Collected to a proper date field; ensure Site identifiers align with GIS layers.
  - Validate Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio descriptions and link to soil data layers if available.
  - Document data provenance and any data cleaning steps for reproducibility.

## GIS usage and best practices
- Suggested workflows:
  - In a point feature layer representing sampling sites, attach attributes from Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Description, Notes, and Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio.
  - Add each element concentration ratio field as an attribute to enable multi-attribute analysis and map-by-element symbology.
  - Create maps of concentration ratios by site, using color ramps to depict magnitude and applying separate layers or charts for elements of interest.
  - Use Date_Sample_Collected to create time-based visualizations (if multiple years or dates exist).
  - For less-than values, implement censoring logic in GIS (e.g., treat as upper bounds) or split into a separate boolean flag and numeric bound field.
- Analyses to consider:
  - Spatial patterns of metal uptake across sites; identify hotspots.
  - Correlations between specific elements and site characteristics or species.
  - Temporal trends if multiple collection dates exist.

## caveats and limitations
- Data quality depends on resolving header inconsistencies and decoding value encodings (1/2, < markers).
- Units are not specified; avoid assuming units beyond what is documented.
- Some fields may be partially populated or missing, requiring careful handling when aggregating or visualizing.
- The dataset ties woodmice samples to soil samples via co-located data; ensure accurate spatial linkage to GIS site features.