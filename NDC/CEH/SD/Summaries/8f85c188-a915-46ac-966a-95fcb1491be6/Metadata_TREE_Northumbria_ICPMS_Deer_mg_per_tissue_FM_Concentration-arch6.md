# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Overview
- Dataset of deer tissue metal concentrations measured by ICP-MS, expressed as mg per total deer tissue fresh mass.
- Contains both metadata and a wide panel of elemental concentrations (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) across samples.
- Metadata fields include Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Tissue.
- Notes indicate some values are reported as “less than” (e.g., <Be, <Al, <V, etc.) to denote detection limits.
- Repeated note: No data for Roe deer 4 thyroid in several concentration columns, indicating missing data for that specific tissue/species combination.
- Source identifiers reference UKCEH sample codes and descriptions.

## Dataset structure and key fields
- Species metadata:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
- Sample specifics:
  - Tissue
- Concentration fields (mg per tissue, fresh mass):
  - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Be_mg_per_tissue_FM, Na_mg_per_tissue_FM, Mg_mg_per_tissue_FM, Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM, Ti_mg_per_tissue_FM, V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM, Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM, Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM, Cs_mg_per_tissue_FM
  - Ba_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM
- Special data conventions:
  - “<” markers indicate concentrations reported as less-than detection limits.
  - “No data for Roe deer 4 thyroid” highlights specific missing data for roe deer thyroid tissue.

## Data quality, caveats, and cleaning notes
- Data include patchy or missing values, notably “No data for Roe deer 4 thyroid” across several elements.
- Detection-limit indicators (“<”) require careful treatment in analyses (censoring or imputation decisions).
- Consistency challenges due to multiple formats and potential gaps across roe deer samples.
- Units are mg per total deer tissue (fresh mass); ensure consistent unit handling when integrating with other datasets.

## How to use and typical outputs
- Enables cross-sample exploration by species, site, date, tissue, and a broad suite of elements.
- Typical self-serve outputs:
  - Dashboards comparing element concentrations across sites or species.
  - Pivot tables aggregating mean/median concentrations by tissue type or sampling date.
  - Tables/plots showing detection-limit values and missing data patterns.
- Useful for environmental monitoring, dietary/biomonitoring studies, and regulatory assessments where tissue metal burdens are of interest.

## Data preparation recommendations for enabling exploration
- Align and harmonize metadata (species names, site labels) to enable robust joins with external data.
- Handle < values explicitly (decide on censoring vs. imputation before visualization).
- Flag and document missing Roe deer 4 thyroid data; consider excluding or treating as NA for specific analyses.
- Normalize or transform concentrations if required by downstream analyses; maintain raw values for traceability.
- Preserve UKCEH sample codes and descriptions to support traceability and provenance.

## Known data gaps and challenges
- Roe deer 4 thyroid data absent for many elements.
- Incomplete data coverage across species, sites, or dates for several elements due to patchiness.
- Varied data formats and potential inconsistencies across datasets or collection systems.

## Data provenance and context
- Data are associated with Northumbria ICPMS Deer concentration measurements and UKCEH sampling workflows.
- Sample identifiers (CEH_Sample_Codes) and descriptions provide traceability to the UKCEH lab and sampling events.
- The dataset is suited for integration with broader environmental and wildlife datasets to support policy, research, or public data dissemination.