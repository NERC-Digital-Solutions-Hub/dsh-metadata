# EDCAT stickleback data 2005-2008. Pottinger, T. G., Cook, A., Matthiessen, P. (2017)

## Overview
- Dataset on three-spined sticklebacks (Gasterosteus aculeatus L.) from SW England rivers, focusing on exposure to wastewater effluent and remediation effects.
- Primary sampling locations: River Ray (downstream of Rodbourne WWTW) around pre-remediation (2005–2007) and post-remediation with granular activated carbon (GAC) in 2008; reference sites in River Ock and Childrey Brook.
- Biomarkers and measurements include EROD activity (cytochrome P4501A), cortisol, RNA:DNA ratio, glucose, and body morphometrics.

## Sampling regime and collection methods
- Timing: 2005–2007 (pre-remediation) and 2008 (post-remediation).
- Fish collection: hand nets; immediate humane euthanization with 2-phenoxyethanol; tissue collection (heart, kidney, liver) and whole-body homogenates prepared and stored.
- Laboratory processing: liver homogenates for EROD assay; cortisol extracted from homogenates and measured by radioimmunoassay; glucose assay; nucleic acids extracted and quantified (RNA + DNA) with subsequent RNA/DNA distinction.
- Data handling: standardized buffers and procedures for tissue homogenization and subsequent biochemical assays.

## Analytical methods
- EROD assay: microplate kinetic assay using liver homogenates to measure ethoxyresorufin-O-deethylase activity (pmol/min/mg protein).
- Cortisol: radioimmunoassay after ethyl acetate extraction; dextran-coated charcoal in assay buffer.
- Glucose: hexokinase-based microplate assay.
- Nucleic acids: extraction with sarcosyl buffer; fluorescence quantification (RiboGreen) for total nucleic acids, with RNAse treatment to distinguish RNA vs DNA.

## Sampling locations
- River Ray
  - Rodbourne WWTW site: grid SU128865; 51.577 N, -1.817 W; 0.2 km from WWTW.
  - Elborough Bridge: grid SU121872; 51.584 N, -1.827 W; 1.8 km from WWTW.
  - Tadpole Bridge: grid SU111896; 51.605 N, -1.841 W; 5.9 km from WWTW.
  - Seven Bridges: grid SU119925; 51.631 N, -1.829 W; 9.5 km from WWTW.
- River Ock
  - Charney Basset: grid SU381944; 51.647 N, -1.451 W.
  - Garford: grid SU438962; 51.663 N, -1.368 W.
- Childrey Brook
  - Venn Mill: grid SU434948; 51.650 N, -1.374 W.
  - Marcham Mill: grid SU448954; 51.656 N, -1.354 W.
- Distances from Rodbourne WWTW are provided where available; some sites have unspecified distances.

## Data structure
- CSV file with the following columns:
  - Sampling_date, River, Site_within_river, Fish_code, Length_mm, Weight_mg, Sex, KF, EROD_pmol_min_mg_protein, RNA_DNA_ratio, Whole_body_cortisol_ng_g, Whole_body_glucose_mg_g.

## References
- Method development and background for assays and analyses cited (Hodson et al. 1996; Gorokhova & Kyle 2002; Lorenzen & Kennedy 1993; Pottinger & Carrick 2001).

## Dataset usage / publications
- Used in multiple publications examining endocrine disruption and responses to wastewater effluent remediation:
  - Katsiadaki et al., Aquatic Toxicology (2012)
  - Pottinger et al., Environment International (2011)
  - Pottinger et al., Journal of Fish Biology (2011)
- Additional studies link body size, RNA:DNA, and chemical exposure in sticklebacks to effluent and environmental conditions.

## GIS-relevant data attributes and mapping considerations
- Spatially explicit sampling design with multiple sites along River Ray and other rivers, enabling mapping of exposure gradients relative to Rodbourne WWTW.
- Site coordinates and distances from WWTW support spatial analyses, proximity to effluent sources, and potential correlation with biomarker responses.
- Data are primarily in CSV with biomarker and morphometric attributes; to map the locations, coordinates are required for each site (available in the location narrative but need consolidation for GIS use).
- Temporal coverage includes pre- and post-remediation periods (2005–2008), allowing temporal GIS analyses of remediation effects.
- When integrating with GIS layers (water quality, land use, infrastructure), ensure alignment of site IDs (River, Site_within_river, Fish_code) and coordinate formats.