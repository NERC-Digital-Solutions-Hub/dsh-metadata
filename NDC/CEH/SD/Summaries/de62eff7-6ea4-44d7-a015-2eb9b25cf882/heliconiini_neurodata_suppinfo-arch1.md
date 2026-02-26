# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Overview
- A dataset of neuropil volumes, Kenyon cell counts, and synapse counts in the mushroom body calyx of Heliconiini butterflies.
- Intended to enable analyses of evolutionary expansion and specialization of mushroom body size in Heliconius and relatives; informs comparative neuroanatomy and brain evolution.
- Basis for analyses reported in Couto et al. (2023); methods align with Montgomery et al. (2016).

## Sampling and specimens
- Broad phylogenetic sampling across Heliconiini (Central and South America); habitats range from dry to wet forest and altitudes from sea level to ~2500 m.
- Wild-caught individuals: 318 brains representing 41 Heliconiini species.
- Insectary-reared subsets for specific measurements:
  - Kenyon cell counts: 50 individuals across 6 species (calyx volume, KC number, densities).
  - Neuronal tracing and synapse/microglomeruli analyses: 63 individuals across 8 species (subset of species per experiment).
- Localities and permits spanning Costa Rica, Panama, French Guiana, Ecuador, and Peru; includes field collection and export permits and associated acknowledgments.
- Additional pupal material from commercial sources used for selected lineages; body size metrics (length, wingspan, mass) recorded.
- Data files include volumetric and count data; measurements follow standardized methodologies with quality controls.

## Fixation, staining, and tissue processing
- Fixation: brains fixed in zinc-formalin (ZnFA), followed by dehydration in 80% methanol/20% DMSO, then storage in 100% methanol at -20°C.
- Rehydration prior to processing: gradual methanol series into Tris buffer.
- Neuropil labeling: mono-clonal anti-SYNORF1 (anti-synapsin) to reveal neuropil; blocking with normal goat serum; Cy2-conjugated secondary antibody; glycerol clearing for mounting.
- Neuronal tracing: dextran dyes injected into calyx and projection neuron target neuropils (antennal lobe, optic lobe) for visual/olfactory pathway mapping; overnight incubation before dissection.
- Kenyon cell labeling: HRP (anti-HRP) to identify Kenyon cells; staining with Cy3 secondary antibody and DAPI.
- Synapse/microglomeruli staining: anti-SYNORF1 with and without phalloidin to reveal F-actin and Kenyon cell dendrites; selective manual counting on subset with combined markers.

## Sectioning, imaging, and 3D analysis
- Sectioning: horizontal 80 µm brain sections with vibratome after embedding in low-melting agarose.
- Confocal imaging:
  - Whole-brain: 10x objective, mosaic tiling (2–3 tiles per brain), z-steps ~2 µm; channels for SYNORF1 (green) and dextran tracers (red/far-red); refractive index corrections applied.
  - Kenyon cell clusters and calyx: higher magnification (63x glycerol objective) for detailed cell counts and synaptic bouton/microglomeruli analysis.
- 3D reconstruction and volumetry:
  - Software: Amira 5.x for segmentation and volumetric modeling; manual/automatic region labeling via brightness/contrast.
  - Corrective scaling factors applied to z-dimension (e.g., 1.52 or 1.85 depending on mounting medium).
  - Neuropil volumes measured for MB calyx (MBCA), MB peduncle (MBPED), MB lobes (MBLOBES), combined MB (MBLOPE), central brain (CBR), antennal lobes (AL), medulla, ventral lobula, optic lobe projections, etc.
  - Rest-of-Central Brain (rCBR) calculated as CBR minus AL and MB volumes.
- Kenyon cell counts:
  - Density estimates from 25 × 25 × 15 µm cubes sampled in clusters; total KC number per hemisphere computed by density × MB cluster volume.
- Synapse and microglomeruli quantification:
  - Synapse density from 50 × 50 × 15 µm cubes; total synapse number estimated from densities and volumes.
  - Microglomeruli counts and densities derived from designated cube regions; cross-validated with manual counts for select species.
- Data handling:
  - ImageJ used for cube-based density measurements and synapse counting via 3D Object Counter.
  - All analyses report volumes in µm³ and counts/densities with corresponding metadata and transformations (log transforms for KC numbers and calyx volumes where appropriate).

## Data records (files)
- Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv
  - Interspecific neuropil volumes (µm³) including MB calyx (MBCA), MB peduncle (MBPED), MB lobes (MBLOBES), total MB (MBLOPE), central brain (CBR), and other visual/olfactory structures (e.g., AL, MEDULLA, VLOB).
  - Metadata: GENUS, CLADE, SPECIES, SEX, COUNTRY OF ORIGIN, body size traits (length, wingspan, mass), and corresponding neuropil volumes.
- Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts.csv
  - Kenyon cell counts with associated calyx volumes, log-transformed calyx volumes, log KC numbers, KC density, and individual identifiers.
- Heliconiini_NeuroData_Table3_Synapse_Counts.csv
  - Synapse and microglomeruli data including synapse counts (raw and estimated), synapse density, calyx volume, synapse count per cube, microglomeruli counts and densities, and species/individual identifiers.

## Data quality and reliability
- Individual-level data include multiple measures per species to support robust comparisons.
- Damaged or poorly stained samples excluded from analysis.
- Measurements aligned with previously published methodologies (consistency with Montgomery et al. 2016).

## Usage and context for analysis
- Enables correlations between mushroom body investment (calyx/MB volumes) and body size, central brain volume, and ecological/phylogenetic factors across Heliconiini.
- Facilitates modeling of evolutionary expansions and specialization of learning/memory centers in butterfly brains.
- Data have been used to support broader analyses of brain composition and posteclosion growth in Heliconius butterflies (see Couto et al. 2023).