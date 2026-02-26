# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Overview
- Dataset of neuropil volumes, Kenyon cell counts, and synapse counts in the mushroom body calyx of Heliconiini butterflies.
- Purpose: analyze evolutionary expansion of mushroom body size in Heliconius with respect to relatives; related analyses published in Couto et al. (2023).
- Measurements include mushroom body substructures, central brain, visual and olfactory neuropils, Kenyon cell estimates, synapse density, and synapse counts.
- Part of a study funded by a NERC Independent Research Fellowship (NE/N014936/1).

## Data Organization and Contents
- Three CSV files are provided:
  - i) Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv: Volumes (in µm³) for neuropils including central brain, medulla, antennal lobe, mushroom body subregions (calyx, peduncle, lobes), total mushroom body, and body size traits (body length, wingspan, body mass). Includes metadata fields (GENUS, SPECIES, SEX, COUNTRY OF ORIGIN, CLADE).
  - ii) Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts: Estimated Kenyon cell numbers, calyx volumes, and related summaries (including log10 transformations and KC density) for individual butterflies (across multiple species).
  - iii) Heliconiini_NeuroData_Table3_Synapse_Counts: Synapse counts and densities, including total synapse estimates and microglomeruli counts/densities, linked to specific individuals and species.
- Data accompany descriptive fields for each measurement (e.g., specimen identifiers, geographic origin, age, calyx volume, synapse counting parameters).

## Sampling and Provenance
- Geographic scope: Central and South America; sampling across diverse habitats from dry to wet forests, from sea level to ~2500 m.
- Locales and permits highlighted:
  - Costa Rica (La Selva, Las Cruces, Le Leona, Orosí) with specific permits.
  - Panama (Pipeline Road, Soberanía National Park) with permits.
  - French Guiana (urban sites around Cayenne) with no permits required for sampling outside National Parks.
  - Ecuador (Estación Científica Yasuní, Parque Nacional Yasuní) with multiple export/collection permits.
  - Peru (Tarapoto region and other highland sites) with several collection permits.
- Sample types: wild-caught individuals and insectary-reared individuals (for certain analyses).
- Sample sizes: 318 wild-caught individuals representing 41 Heliconiini species reconstructed for neuropil volume analysis; 63 individuals from 8 species for neural tracing; 50 individuals from 6 species for Kenyon cell/synapse counting.
- Specimens fixed, dissected, and prepared using standardized protocols to enable cross-species comparisons.

## Methods and Workflow
- Fixation and preservation:
  - Brains dissected in isotonic buffer and fixed in zinc-formalin (ZnFA).
  - Dehydration into methanol/DMSO, storage at -20°C, rehydration prior to processing.
- Neuropil staining:
  - Anti-SYNORF1 antibody to reveal neuropil structure; blocking with normal goat serum; secondary antibody with Cy2 label; glycerol-based clearing for imaging.
- Neuronal tracing:
  - Fluorescent tracers (dextran conjugates) injected into mushroom body calyx and input/output regions to map projections.
  - Overnight incubation; brains preserved for later imaging.
- Sectioning and mounting:
  - Brains embedded in low-melting agarose; 80 µm frontal sections with vibratome; mounted in glycerol-based media.
- Kenyon cell and synapse staining:
  - Kenyon cells labeled with HRP; nuclei labeled with DAPI; imaging to differentiate Kenyon cells from glia.
  - Synapse/microglomeruli analysis using anti-SYNORF1, with optional phalloidin labeling for dendritic profiles; both automated and manual counting approaches used.
- Imaging and 3D reconstruction:
  - Confocal microscopy (Leica SP5/SP8); multi-channel acquisition to distinguish neuropil labels and tracers.
  - 3D reconstructions in Amira; volumetric measurements for neuropils (MB calyx, peduncle, lobes; optic lobe neuropils; antennal lobe; central brain).
  - All volumes derived from hemisphere measurements, then doubled to estimate total brain volumes.
- Data processing:
  - Kenyon cell numbers estimated from nuclei counts within defined cubes; synapse counts derived from automated counting within defined sample boxes; densities extrapolated to whole structures.
  - z-dimension corrections applied (factors 1.52 or 1.85) to account for mounting media differences.
  - Quality control measures implemented to ensure consistency with published methodologies (Montgomery et al. 2016).

## Data Quality and QC
- Individual-level data include multiple measures per species for cross-validation.
- Damaged or poorly stained samples excluded.
- Measurements aligned with established methodologies for comparability (Montgomery et al. 2016).

## Data Model and Variables
- Volume metrics:
  - Neuropils: MB calyx (MBCA), MB peduncle (MBPED), MB lobes (MBLOBES), total MB (MBLOPE).
  - Central brain and rest-of-Central Brain (rCBR) as allometric controls.
  - Visual system (VISUAL: medulla, ventral lobule), Olfactory system (OLFACTORY: antennal lobe).
  - Body size traits: body length, wingspan, body mass.
- Kenyon cells:
  - Calyx volume and estimated Kenyon cell number.
  - Logs: LOG10(CALYX VOLUME), LOG10(KC NUMBER); KC density.
- Synapses and microglomeruli:
  - Synapse counts (two estimates), synapse density, and total estimated synapse number.
  - Microglomeruli counts and densities for selected species.
- Units:
  - Volumes in cubic micrometers (µm³); body measurements in mm or g as indicated.
- Data relationships:
  - Individual-level measurements linked to species, genus, clade, sex, country, and sampling context.

## Data Access, Use, and References
- Data intended for facilitating cross-species comparisons of brain composition and evolutionary neuroanatomy in Heliconiini butterflies.
- Primary publications for context:
  - Couto et al. 2023 (Nature Communications): Rapid expansion and visual specialisation of learning and memory centres in Heliconiini brains.
  - Montgomery et al. 2016 (Journal of Comparative Neurology): Brain composition in Heliconius posteclosion growth and plasticity.
- Dataset supports replication and further analyses of mushroom body evolution, neural architecture, and comparative neuroanatomy across Heliconiini species.