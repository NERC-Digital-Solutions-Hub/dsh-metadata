# EDCAT stickleback data 2005-2008. Pottinger, T. G., Cook, A., Matthiessen, P. (2017)

## Objective and study design
- Evaluate environmental health indicators in three-spined sticklebacks (Gasterosteus aculeatus L.) from the River Ray downstream of Rodbourne Waste Water Treatment Works (WWTW) before (2005–2007) and after (2008) remediation with granular activated carbon (GAC) tertiary treatment.
- Include sampling from neighboring reference rivers: River Ock and Childrey Brook.
- Use biomarkers and physiological metrics to assess chemical exposure and stress in fish populations.

## Sampling regime and specimen handling
- Fish collected with a hand net from selected sites; after capture, individuals were euthanized, labeled, and frozen for transport to CEH Lancaster.
- In the lab, measurements recorded include weight (mg) and total length (mm); organs (heart, kidney) were dissected for VTG and spiggin analyses (data not presented here).
- Tissue was homogenized in buffer, aliquoted, and stored frozen until required for assays.
- Sampling followed two-day periods, with subsequent processing of liver and whole-body homogenates for analyses.

## Analytical methods
- EROD (ethoxyresorufin-O-deethylase) activity in liver as a measure of cytochrome P4501A induction; microplate kinetic assay using small tissue volumes.
- Cortisol measured by radioimmunoassay (RIA) after ethyl acetate extraction from whole homogenate.
- Glucose concentrations determined by a microplate hexokinase-based assay.
- Nucleic acids quantified from whole-body homogenates using a fluorescent dye-binding method; RNA and DNA quantified separately after RNase treatment to derive RNA:DNA ratio.

## Sampling locations and metadata
- River Ray downstream of Rodbourne WWTW (primary sampling site; distance from WWTW: 0.2 km; coordinates provided).
- Additional River Ray sites: Elborough Bridge (1.8 km), Tadpole Bridge (5.9 km), Seven Bridges (9.5 km).
- River Ock sites: Charney Basset and Garford (coordinates provided; distances to Rodbourne WWTW not specified).
- Childrey Brook site: Venn Mill (coordinates provided; distance to Rodbourne WWTW not specified).
- Site-specific coordinates and grid references included to locate sampling locations precisely.

## Data structure and content
- Data provided as a comma-separated values (CSV) file with the following columns:
  - Sampling_date: Date of the first day of the two-day sampling period.
  - River: R. Ray or R. Ock.
  - Site_within_river: Sampling location name.
  - Fish_code: Project identifier.
  - Length_mm: Total length of each fish.
  - Weight_mg: Weight of each fish.
  - Sex: Male (M) or Female (F).
  - KF: K-factor, condition (calculated as 100*weight/length^3).
  - EROD_pmol_min_mg_protein: EROD activity normalized to liver protein content.
  - RNA_DNA_ratio: RNA:DNA ratio in whole-body homogenate.
  - Whole_body_cortisol_ng_g: Cortisol concentration in whole-body homogenate.
  - Whole_body_glucose_mg_g: Glucose concentration in whole-body homogenate.

## Data quality, provenance and usage
- Methodology references provided for all analytical procedures (EROD, cortisol extraction/RIA, RNA/DNA quantification, protein assay).
- The dataset has supported multiple publications, illustrating its use in assessing effluent impacts and remediation effects, including:
  - Detecting anti-androgens and chemical exposure in effluent-receiving rivers.
  - Evaluating body size, RNA:DNA ratio, and markers of exposure post-remediation.
  - Indices of stress in sticklebacks in relation to extreme weather and effluent exposure.

## References and related publications
- Gorokhova E, Kyle M. (2002). Analysis of nucleic acids in Daphnia: development of methods and ontogenetic variations in RNA-DNA content.
- Hodson PV et al. (1996). Measuring induction of hepatic mixed-function oxygenase activity in fish.
- Lorenzen A, Kennedy SW. (1993). Fluorescence-based protein assay for microplates.
- Pottinger TG, Carrick TR. (2001). Stress responsiveness and social dynamics in trout.
- Katsiadaki I et al. (2012). Field surveys reveal anti-androgens in an effluent-receiving river using stickleback biomarkers.
- Pottinger TG et al. (2011–2012). Studies on remediation effects, somatic RNA:DNA ratio, stress indices, and responses to extreme weather and effluent exposure.