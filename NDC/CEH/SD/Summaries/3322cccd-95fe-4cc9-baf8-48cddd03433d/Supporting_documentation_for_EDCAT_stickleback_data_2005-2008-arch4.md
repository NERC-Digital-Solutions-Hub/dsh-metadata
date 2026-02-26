# EDCAT stickleback data 2005-2008. Pottinger, T. G., Cook, A., Matthiessen, P. (2017)

## Overview
- Dataset documenting three-spined sticklebacks from River Ray (downstream of Rodbourne WWTW) and reference rivers (River Ock, Childrey Brook) between 2005–2008, including pre- and post-remediation with granular activated carbon (GAC) tertiary treatment.
- Aims to capture biochemical and physiological endpoints: cytochrome P4501A activity (EROD), cortisol, glucose, RNA:DNA ratio, and basic morphometrics (length, weight).
- Some analyses (VTG and spiggin) are noted but not presented in this dataset.
- Data are intended for assessment of pollutant exposure and stress-related responses in fish and have supported published work.

## Sampling regime and collection methods
- Sampling sites:
  - Ray (R. Ray): Rodbourne WWTW, Elborough Bridge, Tadpole Bridge, Seven Bridges.
  - Ock: Charney Basset, Garford.
  - Childrey Brook: Venn Mill.
- Temporal framework: pre-remediation (2005–2007) and post-remediation (2008).
- Collection and handling:
  - Fish captured with hand net; euthanised with 2-phenoxyethanol (1:1000); stored frozen for transport.
  - On arrival: weights and lengths recorded; ventral organs dissected for VTG/spiggin (not analysed here); remainder homogenised and frozen (-20°C) for assays.
- Storage and processing:
  - Tissue homogenates prepared with buffered solutions and cooled between steps; aliquots stored for later analysis.
  - Tissue used for EROD, cortisol, glucose, and nucleic acids analyses.

## Analytical methods
- EROD (cytochrome P4501A) activity:
  - Microplate kinetic assay using 7-ethoxyresorufin; liver homogenate as the enzyme source; fluorescence readout (excitation 530 nm, emission 590 nm).
  - Protein normalization via a microplate fluorometric assay.
- Cortisol:
  - Ethyl acetate extraction from whole homogenate; radioimmunoassay for quantification.
- Glucose:
  - Hexokinase-based microplate assay.
- Nucleic acids:
  - Extraction with 1% sarcosyl; Quant-It RiboGreen for total nucleic acids; RNase treatment followed by DNA-specific quantification to derive RNA:DNA ratio.
- Data normalization:
  - EROD values normalized to liver protein concentration; other measures reported per whole-body homogenate.

## Sampling locations and metadata
- Geographic and project metadata captured:
  - River name, site description, grid reference, latitude/longitude, and distance from Rodbourne WWTW (where applicable).
- Site-level details included to support data discoverability and spatial analyses.

## Data structure
- Data format:
  - Comma-separated values (CSV) with columns:
    - Sampling_date, River, Site_within_river, Fish_code, Length_mm, Weight_mg, Sex, KF (K-factor), EROD_pmol_min_mg_protein, RNA_DNA_ratio, Whole_body_cortisol_ng_g, Whole_body_glucose_mg_g.
- Each row corresponds to an individual fish from a specific site and sampling date.
- Metadata clarifies measurement descriptions and units.

## Data quality, limitations, and governance
- Some analytes (VTG, spiggin) present in collection protocol but not included in the dataset.
- Methods rely on established literature references for assay protocols, supporting reproducibility and comparability.
- Data provenance links to downstream publications, enabling traceability from raw measurements to interpretations.

## Data usage and publications
- The dataset has informed multiple publications:
  - Katsiadaki et al., 2012: Field surveys identifying anti-androgens in an effluent-receiving river using stickleback biomarkers.
  - Pottinger et al., 2011: Effects of sewage effluent remediation on body size, RNA:DNA ratio, and chemical exposure markers.
  - Pottinger et al., 2011 (J Fish Biol): Indices of stress in sticklebacks related to extreme weather and wastewater exposure.
- The data are suitable for cross-site comparisons, temporal analyses (pre-/post-remediation), and integration with other biomarker datasets.

## References and methodological notes
- Core methodological references for EROD, cortisol, nucleic acid measurements, and related protocols cited to underpin the dataset’s analytical framework.
- Dataset usage in peer-reviewed studies demonstrates applicability for environmental monitoring and data-driven assessment of effluent-related stressors.