# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

## Overview
- Dataset of metal concentrations in wood mouse tissues, measured by ICP-MS, from Northumbria.
- Key identifiers include Latin and Common species names, sampling site, date collected, UK CEH sample codes and descriptions, and tissue type.
- Concentrations are reported as mg per tissue (fresh mass) for multiple elements (e.g., I, Li, Na, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Tl, Pb, U).
- Some values are annotated as less-than (<) markers indicating detection limits.
- Data gaps: certain tissues (e.g., Hind Leg Bone, liver for woodmice 8) have no data; thyroid-related data are often not collected; several elements/tissues show no dataCollected notes.

## Data structure and fields
- Core metadata fields:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
- Concentration fields (examples):
  - I_mg_per_tissue_FM
  - Li_mg_per_tissue_FM
  - Na_mg_per_tissue_FM
  - Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM
  - K_mg_per_tissue_FM
  - Ca_mg_per_tissue_FM
  - Ti_mg_per_tissue_FM
  - V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM
  - Mn_mg_per_tissue_FM
  - Fe_mg_per_tissue_FM
  - Co_mg_per_tissue_FM
  - Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM
  - Zn_mg_per_tissue_FM
  - As_mg_per_tissue_FM
  - Se_mg_per_tissue_FM
  - Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM
  - Mo_mg_per_tissue_FM
  - Ag_mg_per_tissue_FM
  - Cd_mg_per_tissue_FM
  - Cs_mg_per_tissue_FM
  - Tl_mg_per_tissue_FM
  - Pb_mg_per_tissue_FM
  - U_mg_per_tissue_FM
- Data notes embedded in fields include:
  - Instances of “<” markers indicating values below detection limits.
  - Explicit notes such as “No data for Hind Leg Bone and woodmouse 8 liver” and “No data collected for woodmice thyroid” for various elements.

## Data quality and completeness
- Mixed completeness across tissues and elements.
- Clear gaps where certain tissues or thyroid data are unavailable; some elements have no data collected for thyroid or other tissues.
- Presence of placeholder notations (e.g., n/a, < markers) requiring careful handling during analysis.
- Metadata provides explicit descriptions of each field and the meaning of markers (e.g., <I, <Al indicating less-than values).

## Data governance and access
- Documentation ties data to UKCEH sample codes and descriptions, enabling traceability.
- Emphasis on appropriate metadata (species, site, date, tissue, and concentrations) to support discoverability and reuse.
- Requires ongoing coordination with data creators to fill gaps (e.g., missing tissues or non-collected data) and to maintain up-to-date records.
- Sharing limitations and embargoes should be respected; updates should be catalogued and uploaded to relevant data portals.

## Usage notes and caveats
- Concentrations are per total wood mouse tissue in milligrams fresh mass (FM).
- Interpreting “<” values: treat as censored data at the stated limit; standard practices (e.g., imputation or reporting as upper bound) should be applied per project policy.
- Data incompleteness (missing tissues, thyroid data, and some elements) may affect cross-sample comparisons and broader analyses.
- Ensure alignment of units and column mappings if integrating with other datasets.

## Recommendations for Data Stewards
- Validate and standardize metadata fields across records (e.g., site names, date formats, tissue terminology).
- Document data gaps explicitly and maintain a provenance log for missing or non-collected data.
- Implement data quality checks for detection-limit markers and ensure consistent handling of < values.
- Coordinate with data creators to obtain missing tissue data (e.g., hind leg bone, liver for specific samples, thyroid measurements) or to confirm intentional omissions.
- Ensure dataset is discoverable by cataloguing with proper keywords (ICPMS, wood mouse, mg_per_tissue_FM, Northumbria, CEH, tissue concentrations).
- Prepare a clear data dictionary and data release notes describing measurement methods, units, detection limits, and any data suppression rules.
- Plan for updates and versioning; reflect changes in both metadata and data files and communicate updates to data users.
- Provide usage guidance highlighting limitations due to incomplete data and offering recommended analytical approaches for censored data.

## Challenges to anticipate
- Incomplete coverage across tissues and elements requiring careful interpretation.
- Heterogeneous data collection methods or formats across samples, complicating interoperability.
- Need for stakeholder alignment to fill data gaps and validate metadata accuracy.