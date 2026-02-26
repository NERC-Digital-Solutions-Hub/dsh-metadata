# Neuropil volumes for sensory structures in the brains of ithomiini butterflies

## Overview
- Dataset of neuropil volumes in sensory brain structures of ithomiini butterflies from eastern Ecuador.
- Context: Mullerian mimicry; pigmentation patterns and mimicry ring assignments described in Elias et al. (2008).
- Builds on prior work (Montgomery & Ott 2015; Wainwright & Montgomery 2022; Wainwright et al. 2024) to understand how sensory environments shape brain investment.
- Aims to quantify relative investment in central and sensory brain regions across species and mimicry contexts.

## Study site and specimens
- Fieldwork conducted along trails around Estación Científica Yasuní, Parque Nacional Yasuní, Orellana Province, Ecuador (primary lowland Amazon rainforest; ~4.5 km2).
- Sampling periods: Nov/Dec 2011–2012; Aug–Oct 2022; permits obtained from local authorities and PUCE support.
- Genera identified by wing venation and local race IDs; vouchers preserved as wings; nonretained individuals IDed, sexed, and marked prior to release.
  
## Data collection and methods
- Wild-caught sample for sensory neuroanatomy: 392 individuals across 49 species; variable species sample sizes.
- Dissection and fixation: HEPES-buffered saline (HBS) and zinc formaldehyde solution (ZnFA) with controlled fixation times; stored in methanol and later -20°C.
- Immunostaining: brains immunostained against synapsin (pre-synaptic protein) using primary antibody 3C11 and Cy2-conjugated secondary antibody; extensive blocking and washing steps; glycerol/PBSd clearing steps.
- Imaging: confocal microscopy (Leica SP5/SP5-II) at 10x, 0.4 NA; dual-sided scans (anterior and posterior); image stacks merged with Amira; z-dimension correction applied (multiplied by 1.52) prior to segmentation.
- Segmentation: manual segmentation of five of the six primary optic lobe neuropils (medulla, lobula plate, lobula, accessory medulla, ventral lobula) plus anterior optic tubercle and antennal lobe; lamina excluded due to fragility; ventral lobula absent in many individuals (especially females).
- Volumetry: volumes extracted with measure statistics; central brain, anterior optic tubercle, and antennal lobe volumes used to calculate a rest-of-central-brain measure (allometric control) by subtracting the two olfactory/visual centers from the central brain measure.
- Transformations: volumes for each neuropil were doubled and log10 transformed; combined optic lobe volume defined as the sum of the four major optic lobe neuropils.

## Data processing and transformations
- Central brain volume derived by summing medulla, lobula plate, lobula, and accessory medulla; rest-of-central-brain used as allometric control with anterior optic tubercle and antennal lobe subtracted from central brain.
- All paired neuropils multiplied by two to account for bilateral symmetry before log10 transformation.
- Log10-transformed volumes (µm3) used for downstream analyses; z-stack merging and homogenization performed to ensure comparability across samples.

## Quality control
- Data include multiple measures per species to support within-species variability analysis.
- Damaged or poorly stained samples excluded.
- Measurements aligned with established methodologies (Montgomery & Ott 2016) for cross-species comparability.

## Data schema and column definitions
- Year collected: Year of sample collection.
- ID: Individual identifiers linking samples and metadata.
- Subtribe: Taxonomic rank.
- Species: Taxonomic species name.
- Sex: Male or Female.
- Mimicry ring: Mimicry ring assignment based on Elias et al. (2008) wing patterns.
- log10(rest of central brain volume µm3): Log10-transformed volume of the rest-of-central-brain (allometric control).
- log10(medulla volume µm3): Log10-transformed medulla volume.
- log10(lobula plate volume µm3): Log10-transformed lobula plate volume.
- log10(lobula volume µm3): Log10-transformed lobula volume.
- log10(accessory medulla volume µm3): Log10-transformed accessory medulla volume.
- log10(ventral lobula volume µm3): Log10-transformed ventral lobula volume.
- log10(antennal lobe volume µm3): Log10-transformed antennal lobe volume (olfactory).
- log10(anterior optic tubercule volume µm3): Log10-transformed anterior optic tubercle volume.
- log10(optic lobe volume µm3): Log10-transformed combined optic lobe volume (sum of medulla, lobula plate, lobula, ventral lobula).

## Data provenance and references
- Data generated as part of NERC Independent Research Fellowship NE/N014936/1.
- Key references for context and methodologies:
  - Elias et al. 2008
  - Montgomery & Ott 2015; Montgomery & Ott 2016
  - Wainwright & Montgomery 2022
  - Wainwright et al. 2024 (bioRxiv)
  
## Potential uses and repurposing
- Facilitate cross-species comparisons of sensory-brain investment in mimetic butterfly communities.
- Support allometric analyses contrasting central vs. sensory brain investments across mimicry rings and ecological contexts.
- Enable creation of data products such as dashboards or visualization tools showing neuropil volumes across species, sexes, and mimicry rings.
- Provide a reproducible workflow for image-based brain volumetry (immunostaining, confocal imaging, segmentation, and transformation) suitable for similar datasets.