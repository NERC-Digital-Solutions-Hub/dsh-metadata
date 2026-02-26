# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

- A dataset describing brain morphology across Heliconiini butterflies, including neuropil volumes, Kenyon cell counts, and synapse/microglomeruli data.
- Used to analyze evolutionary expansions and specialization of learning/memory centres in Heliconiini, with related analyses published in Couto et al. (2023).

## What the data include

- Measurements of:
  - Mushroom body structures (calyx, peduncle, lobes) and other brain regions (central brain, medulla, antennal lobe).
  - Kenyon cell numbers (estimated for calyx-associated clusters).
  - Synapse density and counts within the mushroom body calyx; microglomeruli counts (with and without phalloidin labeling for select species).
- Units and derived metrics:
  - Volumes in cubic micrometers (µm3) for various neuropils.
  - Kenyon cell density and total estimates per hemisphere.
  - Synapse counts, densities, and total estimates; microglomeruli counts/densities.
  - For Kenyon cells: log-transformed calyx volume and KC number, KC density.
- File set:
  - Table1: Neuropil volumes (Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv)
  - Table2: Kenyon cell counts (Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts)
  - Table3: Synapse/microglomeruli counts (Heliconiini_NeuroData_Table3_Synapse_Counts)

## Study design and scope

- Taxa and sampling:
  - 41 Heliconiini species sampled wild across Central and South America; 318 wild-caught individuals for volumetric brain measurements.
  - 63 individuals (8 species per species; mostly 8, except H. doris) reared under controlled conditions for neural tracing and brain region segmentation.
  - 50 individuals across 6 species for Kenyon cell and synapse counting (sectioned brains).
- Geographic and habitat range:
  - Costa Rica, Panama, French Guiana, Ecuador, Peru, and other locations within Central/South America; includes a variety of habitats from dry to wet forests and sea level to ~2500 m.
- Permits and field work:
  - Detailed permits and affiliations noted for each locality, with field collection, export permits, and institutional collaborations acknowledged.

## Methods and data collection workflow

- Tissue fixation and preservation:
  - Brains fixed in zinc-formalin solution (ZnFA), stored in methanol, and rehydrated prior to processing.
- Neuropil labeling and imaging:
  - Immunostaining with anti-SYNORF1 (synapsin) to reveal neuropil structure.
  - Blocking steps with normal goat serum; secondary antibodies used for fluorescence.
  - Dextran-conjugated dyes for neuronal tracing to label projection neurons from sensory neuropils (antennal lobe, optic lobe).
- Sectioning and mounting:
  - 80 µm frontal sections; samples embedded in agarose; mounted in glycerol for confocal imaging.
- Kenyon cell visualization:
  - HRP labeling to identify Kenyon cells; DAPI counterstaining; ~ high-magnification imaging for cell counts.
- Synapse and microglomeruli assessment:
  - Anti-SYNORF1 with and without phalloidin to reveal presynaptic boutons and Kenyon cell dendrites; confocal imaging for density calculations.
- Confocal imaging and 3D reconstruction:
  - Whole-brain and subregion imaging with Leica SP5/SP8 confocal microscopes; tiled stacks for whole-brain coverage; higher magnification for Kenyon cell clusters.
  - 3D reconstructions in Amira; manual/automated segmentation to quantify volumes.
- Quantification:
  - Kenyon cell numbers estimated by counting nuclei in 25 x 25 x 15 µm cubes, scaled to whole calyx-associated clusters.
  - Synapses counted in 3D cubes via 3D Object Counter; microglomeruli counts derived from defined subvolumes.
  - Corrections for imaging artifacts:
    - Z-dimension correction factors: 1.52 (methyl salicylate mounting) and 1.85 (glycerol mounting).
- Quality control and consistency:
  - Damaged or poorly stained samples excluded.
  - Measurements aligned with previously published methodologies (Montgomery et al., 2016).

## Data structure and file details

- Table1: Neuropil volumes (in µm3) across species and individuals; includes visual system, olfactory system, mushroom bodies (calyx, peduncle, lobes, total MB), central brain, and body size metrics.
- Table2: Kenyon cell counts for insectary-reared individuals; includes calyx volume, estimated KC number, and log-transformed values (LOG10 CALYX VOLUME, LOG10 KC NUMBER) plus KC density.
- Table3: Synapse/microglomeruli data; includes synapse counts from anti-SYNORF1, densitites, estimated total synapse numbers, microglomeruli counts and densities, with species and individual identifiers.
- Note: Data tables include metadata fields such as species, sex, country of origin, and anatomical measurements; derived metrics use log transformations where indicated.

## Quality, provenance, and reproducibility

- Provenance:
  - Part of the NERC Independent Research Fellowship NE/N014936/1; analyses published in Couto et al. 2023 (Nature Communications).
  - Related methodologies documented in Montgomery et al. 2016.
- Quality controls:
  - Multiple measures per species; exclusion of damaged/poorly stained samples.
  - Standardized acquisition, staining, imaging, and analysis procedures to ensure cross-species comparability.

## Considerations for data governance and reuse

- Comprehensive methodological detail supports reproducibility and cross-study comparability, but data provenance notes field collection permits and sample origin, which may influence reuse in policy or conservation contexts.
- Cross-species comparisons rely on consistent correction factors for imaging modalities; users should apply the same corrections if reanalyzing.
- The dataset integrates wild-caught and laboratory-reared specimens, so users should consider potential differences due to environment or age when interpreting results.
- Access and licensing not explicitly stated; reference Couto et al. (2023) for publication context and potential data sharing statements.

## References

- Couto A, Young FJ, Atzeni D, et al. Rapid expansion and visual specialisation of learning and memory centres in the brains of Heliconiini butterflies. Nature Communications. 2023, 14(1):4024.
- Montgomery SH, Merrill RM, Ott SR. Brain composition in Heliconius butterflies, posteclosion growth and experience-dependent neuropil plasticity. Journal of Comparative Neurology. 2016, 524(9):1747-69.