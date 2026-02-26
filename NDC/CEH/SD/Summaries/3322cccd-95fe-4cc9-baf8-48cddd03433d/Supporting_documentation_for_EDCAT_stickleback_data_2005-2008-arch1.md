# EDCAT stickleback data 2005-2008. Pottinger, T. G., Cook, A., Matthiessen, P. (2017)

## Overview
- Dataset of three-spined sticklebacks (Gasterosteus aculeatus L.) collected from the River Ray (southwest England) downstream of Rodbourne Waste Water Treatment Works (WWTW) before (2005-2007) and after (2008) remediation with granular activated carbon (GAC) tertiary treatment.
- Additional sampling from neighbouring reference rivers (River Ock, Childrey Brook) for comparison.
- Aimed to support assessments of chemical exposure and stress biomarkers related to sewage effluent and remediation.

## Sampling regime and collection methods
- Fish captured with a hand net (38 cm D-frame, 0.5 cm mesh, 1.5 m handle).
- Euthanized humanely with 2-phenoxyethanol (1:1000), labeled, frozen in liquid nitrogen for transport, then stored at -80°C.
- On analysis day: fish weighed (mg) and measured (mm); ventral heart and kidney removed for VTG and spiggin analyses (data not presented here).
- Remainder homogenized in a Tris-HCl buffer with glycerol, EDTA, and DTT; aliquots stored at -20°C until assay.
- Analytical work focused on liver-based EROD activity, whole-body cortisol, glucose, and nucleic acid content (RNA:DNA).

## Analytical methods
- EROD (cytochrome P4501A monooxygenase) activity measured using a microplate kinetic assay with 7-ethoxyresorufin substrate; readings at 530 nm excitation and 590 nm emission; protein-normalized results.
- Cortisol extracted from whole homogenate with ethyl acetate and quantified by radioimmunoassay (RIA), with a dextran-coated charcoal cleanup modification.
- Glucose quantified in homogenate using a hexokinase-based microplate assay.
- Nucleic acids extracted from homogenate using sarcosyl buffer; total RNA+DNA quantified with a fluorescent dye (RiboGreen); RNA content determined after RNase treatment by difference.
- Note: VTG and spiggin data were collected but not presented in this dataset.

## Sampling locations
- River Ray (sampling downstream of Rodbourne WWTW)
  - Rodbourne WWTW site: SU128865, 51.577 N, -1.817 W, 0.2 km from Rodbourne WWTW
  - Elborough Bridge: SU121872, 51.584 N, -1.827 W, 1.8 km
  - Tadpole Bridge: SU111896, 51.605 N, -1.841 W, 5.9 km
  - Seven Bridges: SU119925, 51.631 N, -1.829 W, 9.5 km
- River Ock
  - Charney Basset: SU381944, 51.647 N, -1.451 W
  - Garford: SU438962, 51.663 N, -1.368 W
- Childrey Brook
  - Venn Mill: SU434948, 51.650 N, -1.374 W
- Distances listed indicate proximity to the Rodbourne WWTW; some sites do not have distance data provided.

## Data structure and variables
- Data provided as a comma-separated values (CSV) file with columns:
  - Sampling_date: Date of the first day of the two-day sampling period
  - River: R. Ray or R. Ock
  - Site_within_river: Specific sampling site
  - Fish_code: Project identifier
  - Length_mm: Total length (mm)
  - Weight_mg: Body weight (mg)
  - Sex: Male (M) or Female (F)
  - KF: K-factor (condition; 100*weight/length^3)
  - EROD_pmol_min_mg_protein: EROD activity normalized to liver protein
  - RNA_DNA_ratio: RNA:DNA ratio in whole-body homogenate
  - Whole_body_cortisol_ng_g: Cortisol concentration in whole-body homogenate (ng/g)
  - Whole_body_glucose_mg_g: Glucose concentration in whole-body homogenate (mg/g)

## Data availability, provenance, and references
- Samples processed and analyzed using specified laboratory protocols; data generated and stored for subsequent analysis.
- Method references include foundational work on EROD assays, cortisol ELISA/RIA, protein assays, and nucleic acid quantification (Gorokhova & Kyle 2002; Hodson et al. 1996; Lorenzen & Kennedy 1993; Pottinger & Carrick 2001).

## Related publications using this dataset
- Katsiadaki, I. et al. (2012). Field surveys reveal the presence of anti-androgens in an effluent-receiving river using stickleback-specific biomarkers. Aquatic Toxicology 122-123, 75-85.
- Pottinger, T. G. et al. (2011). Effects of sewage effluent remediation on body size, somatic RNA:DNA ratio, and markers of chemical exposure in three-spined sticklebacks. Environment International 37, 158-169.
- Pottinger, T. G. et al. (2011). Indices of stress in three-spined sticklebacks Gasterosteus aculeatus in relation to extreme weather events and exposure to waste-water effluent. Journal of Fish Biology 79, 256-279.