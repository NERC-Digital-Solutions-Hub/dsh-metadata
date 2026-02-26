# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Purpose and scope
- Dataset of neuropil volumes, Kenyon cell counts, and synapse counts in the mushroom body calyx of Heliconiini butterflies.
- Designed to analyze evolutionary expansion of mushroom body size; linked to analyses published in Couto et al. (2023).
- Includes measurements of mushroom body structures, central brain, other neuropils, Kenyon cell numbers, synapse density, and calyx microglomeruli.
- Data contributed as part of a NERC Independent Research Fellowship.

## Data content and variables
- Volumes (μm³) for: central brain, mushroom body calyx (MBCA), MB peduncle (MBPED), MB lobes (MBLOBES), total MB (MBLOPE), and major sensory neuropils (visual: VLOB, medulla; olfactory: AL).
- Kenyon cell data: estimated Kenyon cell numbers; calyx volume; KC density; log-transformed KC numbers and calyx volume.
- Synapse data: total synapse counts (two estimates), synapse density, and microglomeruli counts/densities (in cubes measured within calyx areas).
- Additional body size traits: body length, wingspan, body mass; plus sample identifiers (GENUS, SPECIES, COUNTRY, SEX, etc).
- Datasets span interspecific wild-caught data (318 individuals, 41 species) and insectary-reared samples for Kenyon cells and synapses (63 individuals across 8 species for KC counts; 50 individuals across 6 species for synapse/microglomeruli counts).

## Sampling and locality
- Phylogenetic sampling across Heliconiini: Central and South American habitats from dry to wet forests, sea level to ~2500 m.
- Wild-caught samples collected in:
  - Costa Rica (La Selva, Las Cruces, Le Leona, Orosí) and permits noted
  - Panama (Pipeline Road, Gamboa; Soberanía National Park)
  - French Guiana (Cayenne area)
  - Ecuador (Estación Científica Yasuní, Parque Nacional Yasuní; additional sites in Vilcabamba and Balsas Canton)
  - Peru (Tarapoto region, Escalera, Abra Patricia, etc.)
- Additional insectary-reared samples for controlled analyses (pupae from commercial suppliers; adults assessed after eclosion).

## Methods and data collection workflow
- Fixation: brains dissected in buffer; fixed in zinc-formalin (ZnFA); dehydration and storage in methanol/DMSO; rehydration prior to processing.
- Neuropil staining: anti-SYNORF1 (synapsin) to reveal neuropil structure; blocking and antibody incubations with multiple washes; secondary antibody labeling; glycerol clearing and mounting.
- Neuronal tracing: labeling projection neurons with dextran-conjugated dyes to map visual and olfactory input to MB calyx (inject into mushroom body calyx and target sensory neuropils).
- Sectioning and mounting: horizontal 80 μm brain sections; embedding in agarose; confocal imaging preparations.
- Kenyon cell staining: HRP antibody labeling to identify Kenyon cell nuclei; second staining with Cy3 secondary antibody and DAPI.
- Synapse/microglomeruli staining: anti-SYNORF1 (and phalloidin for actin in some experiments); dual-stain procedures to visualize presynaptic boutons and Kenyon cell dendrites; methanol-free formaldehyde fixation for phalloidin compatibility.
- Imaging: confocal microscopy for whole-brain and targeted MB calyx; multi-channel acquisition to separate labels; z-stacks with specific step sizes; refractive index corrections applied.
- Image analysis: 3D segmentation in Amira to reconstruct neuropils; volumes computed for MB components, central brain, optic and antennal lobes.
- Kenyon cell counting: density-based estimator from small 25×25×15 μm cubes; total KC number inferred by density×MB cluster volume.
- Synapse/microglomeruli counting: automated 3D object counting in 50×50×15 μm cubes; background filtering; manual counting for select species when needed.
- Calibration: z-dimension corrections using calibration beads; correction factors applied (1.52 or 1.85 depending on mounting medium).

## Data processing and analysis
- 3D reconstruction and volume extraction for: MB calyx, peduncle, lobes; optic lobe neuropils (medulla, ventral lobula); antennal lobe; central brain; rest-of-CBR as allometric control.
- Kenyon cell number estimation per hemisphere; synapse density and total synapse counts; microglomeruli density where applicable.
- Analyses align with published methodologies (Montgomery et al., 2016) for brain composition and with Couto et al., (2023) for rapid expansion of learning/memory centres.

## File contents and data structure
- Table 1: Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv
  - Interspecific volumetric data for wild-caught individuals.
  - Columns include GENUS, CLADE, SPECIES, SEX, COUNTRY, and volumes for visual system (VLOB), central brain (CBR), MB components (MBCA, MBPED, MBLOBES, MBLOPE), OLFACTORY system (AL), and TOTAL MB, plus BODY SIZE traits (LENGTH, WINGSPAN, BODY MASS) and derived metrics (e.g., rCBR).
- Table 2: Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts
  - Kenyon cell counts from insectary-reared individuals.
  - Columns include INDIVIDUALS, SPECIES, CALYX VOLUME, ESTIMATED KENYON CELL NUMBER, LOG10 transformations (CALYX VOLUME, KC NUMBER), KC DENSITY.
- Table 3: Heliconiini_NeuroData_Table3_Synapse_Counts
  - Synapse and microglomeruli data from insectary-reared individuals.
  - Columns include SYNAPSE COUNTS (two estimates), INDIVIDUAL, AGE, SPECIES, CALYX VOLUME, SYNAPSE NUMBER/CUBE, SYNAPSE DENSITY, ESTIMATED SYNAPSE NUMBER, MICROGLOMERULI COUNTS, MICROGLOMERULI DENSITY.

## Quality control
- Individual-level data provide multiple measures per species.
- Damaged or poorly stained samples excluded.
- Measurements follow established methods and are cross-species consistent (cited Montgomery et al. 2016).

## Usage and references
- Primary publication: Couto A, et al. Rapid expansion and visual specialisation of learning and memory centres in the brains of Heliconiini butterflies. Nature Communications, 2023.
- Related brain composition work: Montgomery SH, Merrill RM, Ott SR. Brain composition in Heliconius butterflies, posteclosion growth and experience-dependent neuropil plasticity. J Comp Neurol, 2016.
- Data intended to enable cross-species comparisons of brain architecture and cellular composition within Heliconiini, and to support analyses of evolutionary brain investment patterns.