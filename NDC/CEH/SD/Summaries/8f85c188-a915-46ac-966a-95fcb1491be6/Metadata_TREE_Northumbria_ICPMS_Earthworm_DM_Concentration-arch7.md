# TREE_Northumbria_ICPMS_Earthworm_DM_Concentration

## Overview
- Dataset capturing ICP-MS measured elemental concentrations in earthworms from Northumbria, with concentrations expressed as mg/kg dry mass (DM).
- Includes taxonomic details, sampling context, and UKCEH sampling references to support spatial analyses and map-based visualisations.

## Data Schema / Key Fields
- Taxonomy and identification:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Concentration measurements (mg/kg DM) for elements:
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Each field has an accompanying Units = mg/kg_DM and Explanation describing the element concentration in dry mass.

## Data Provenance and Units
- Data appear to be UKCEH-related (CEH_Sample_Codes/Description) and gathered under a Northumbria ICPMS earthworm study.
- All elemental concentrations are reported in milligrams per kilogram of dry mass (mg/kg DM).

## GIS Use and Visualization
- Suitable for:
  - Mapping elemental concentrations by sampling site and date.
  - Comparing species-specific distribution of elements.
  - Creating choropleth or point-based maps of trace element levels across sites.
- Useful join keys:
  - Site, Date_Sample_Collected, Latin_Species_Name/Common_Species_Name, CEH_Sample_Codes.
- Consider integrating with site boundary layers, allowing spatial summaries (means, medians) by location.

## Data Quality and Challenges
- Potential issues common to GIS data:
  - Data dispersed across multiple sources; reconciliation may be needed.
  - Incomplete fields (e.g., missing concentrations for some elements or sites).
  - Variability in data standards and metadata completeness.
  - Need for unit consistency checks if combining with other datasets (though this dataset uses mg/kg DM).

## Practical Considerations for Analysis
- Ensure proper handling of missing values and detection limits for trace elements.
- Normalize or compare across species and sites by grouping on Latin_Species_Name/Common_Species_Name and Site.
- Leverage CEH_Sample_Codes and CEH_Sample_Description for provenance and reproducibility.
- Use Date_Sample_Collected to explore temporal trends if multiple sampling events exist.