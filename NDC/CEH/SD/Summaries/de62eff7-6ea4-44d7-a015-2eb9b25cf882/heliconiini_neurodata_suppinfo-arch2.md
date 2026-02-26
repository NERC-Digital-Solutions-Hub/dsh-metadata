# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Overview
- Datasets measuring brain structure components in Heliconiini butterflies to analyze evolutionary changes in mushroom body size.
- Data collected 2012–2016; intended to support analyses published in Couto et al. (2023) comparing Heliconius butterflies to close relatives.
- Key outputs include volumes of specific brain regions, estimates of Kenyon cell numbers, and synapse/microglomeruli metrics.
- Part of a broader effort to enable standardized, cross-species comparisons of neural investment and sensory processing.
- Includes detailed sampling, fixation, staining, imaging, and analysis workflows to ensure reproducibility and comparability.

## Purpose and context for monitoring/environmental-analysis perspective
- Provides a standardized neuroanatomical dataset across many species and individuals for evolutionary and comparative analyses.
- Emphasizes quality control, consistent methodologies, and metadata to support scrutiny and reuse in subsequent environmental/biological research.

## Sampling and study sites
- Phylogenetic sampling across Heliconiini butterflies from Central and South America.
- Habitat range includes dry to wet forests, sea level to ~2500 m.
- Field sampling in:
  - Costa Rica (La Selva, Las Cruces, Le Leona, Orosí) with specific permits.
  - Panama (Pipeline Road, Soberanía National Park) with permits.
  - French Guiana (urban sites around Cayenne) where permits not required for non-park sampling.
  - Ecuador (Estación Científica Yasuní, Parque Nacional Yasuní) with multiple export/collection permits; field assistance noted.
  - Peru (various sites near Tarapoto, Excalera) with multiple permits.
- Includes both wild-caught individuals and additional insectary-reared samples for controlled analyses of cellular composition and sensory domains.

## Methods snapshot (data production pipeline)
- Fixation: brains fixed in zinc-formalin (ZnFA), followed by methanol/DMSO dehydration and storage; rehydration prior to processing.
- Neuropil staining: anti-SYNORF1 for visualizing neuropil, with blocking, primary/secondary antibodies, and glycerol/methyl salicylate mounting.
- Neuronal tracing: dextran-conjugated dyes injected into MB calyx, antennal lobe, and optic lobe pathways to label projection neurons.
- Sectioning and mounting: 80 µm frontal brain sections cut with vibratome; embedded in agarose; mounted for microscopy.
- Kenyon cell identification: HRP immunostaining to mark Kenyon cell bodies, with DAPI nuclear stain.
- Synapse/microglomeruli staining: SYNORF1 for presynaptic boutons; phalloidin for F-actin to reveal Kenyon cell dendritic profiles; selective dual-staining for detailed counting in some species.
- Confocal imaging: whole-brain and targeted MB calyx imaging with multiple channels; z-stacks acquired and later fused/stitched as needed; axial corrections applied for refractive-index differences.
- Image analysis: 3D segmentation in Amira to reconstruct neuropils; volumes extracted; Kenyon cell numbers estimated from cell-body density; synapse counts via 3D Object Counter in ImageJ; microglomeruli densities measured in defined cubes.
- Corrections: z-dimension scaling factors applied (1.52 for methyl salicylate mounts; 1.85 for glycerol-mounted slices) to account for mounting media effects.

## Quality control
- Multiple measures per species at the individual level.
- Exclusion of damaged or poorly stained samples.
- Adherence to previously published methodologies (consistency with Montgomery et al., 2016) to enable cross-study comparability.

## Data files and contents
- i) Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv
  - Interspecific neuropil volumes for wild-caught individuals.
  - Columns include: GENUS, SPECIES, SEX, COUNTRY OF ORIGIN, VISIBLE neuropil volumes (VISUAL), MEDULLA, VLOB, OLFACTORY (ANTENNAL LOBE), MUSHROOM BODIES including MBCA (calyx), MBPED (peduncle), MBLOBES (lobes), MBLOPE (TOTAL MB), CENTRAL BRAIN metrics (CBR, rest-of-CBR, rCBR), BODY SIZE metrics (BODY LENGTH, WINGSPAN, BODY MASS).
- ii) Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts
  - Kenyon cell counts and calyx-related metrics from insectary-reared individuals.
  - Columns include: INDIVIDUALS, SPECIES, CALYX VOLUME, ESTIMATED KENYON CELL NUMBER, LOG10 transforms of CALYX VOLUME and KC NUMBER, KC DENSITY.
- iii) Heliconiini_NeuroData_Table3_Synapse_Counts
  - Synapse and microglomeruli data from insectary-reared individuals.
  - Columns include: SYNAPSE COUNTS (two fields), AGE, SPECIES, CALYX VOLUME, SYNAPSE NUMBER per CUBE, SYNAPSE DENSITY, ESTIMATED SYNAPSE NUMBER, MICROGLOMERULI COUNTS, MICROGLOMERULI DENSITY, with identifiers for individuals and species.

## Scale and coverage
- 318 wild-caught individuals across 41 Heliconiini species reconstructed for brain volumes (one hemisphere scaled to total brain).
- 63 insectary-reared individuals across 8 species used for neuronal tracing analyses.
- 50 insectary-reared individuals across 6 species used for Kenyon cell counts and synapse density analyses.
- Comprehensive data enabling cross-species comparisons of mushroom body investment and sensory domain organization.

## References
- Couto A, et al. Rapid expansion and visual specialisation of learning and memory centres in the brains of Heliconiini butterflies. Nature Communications. 2023.
- Montgomery SH, Merrill RM, Ott SR. Brain composition in Heliconius butterflies, posteclosion growth and experience-dependent neuropil plasticity. Journal of Comparative Neurology. 2016.

## Data administration and accessibility notes
- Detailed methodological documentation supports reproducibility and reuse in environmental/biological monitoring contexts.
- Metadata includes sampling sites, permits, and collection details to enable traceability and data provenance.
- Dataset design emphasizes standardization and verifiability to facilitate long-term monitoring and cross-study synthesis.