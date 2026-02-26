# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Introduction
- Dataset of neuropil volumes, Kenyon cell counts, and synapse counts in the mushroom body calyx of Heliconiini butterflies.
- Purpose: enable analyses of evolutionary expansions in mushroom body size in Heliconius butterflies versus relatives; related analyses published in Couto et al. (2023).
- Measured variables include mushroom body volumes (calyx, peduncle, lobes), central brain, medulla, antennal lobe; estimated Kenyon cell numbers; synapse density and total synapse estimates.
- Created under a NERC Independent Research Fellowship (NE/N014936/1).

## Phylogenetic sampling and sampling sites
- Broad sampling across Heliconiini in Central and South America to ensure even phylogenetic coverage.
- Field trips to diverse habitats and elevations; permits obtained from multiple countries (Costa Rica, Panama, French Guiana, Ecuador, Peru, etc.).
- Wild-caught samples complemented with selected pupae from commercial sources for certain analyses.
- Body measures recorded; vouchers preserved; detailed permit acknowledgments and field assistance noted.

## Fixation and neuropil staining
- Brains dissected in isotonic buffer and fixed in zinc-formalin (ZnFA) for 16–20 hours.
- Samples dehydrated into methanol/DMSO, stored at -20°C, and rehydrated prior to processing.
- Neuropils visualized with monoclonal anti-synapsin (SYNORF1) staining; blocking with goat serum; antibodies applied with extensive incubation; secondary labeling with Cy2-conjugated antibody; tissues cleared in methyl salicylate for mounting.

## Neuronal tracing and sectioning
- Projection neurons labeled with dextran-conjugated dyes (fluoro-ruby or Alexa fluor 647) injected into mushroom body calyx and sensory neuropils to map visual/olfactory inputs.
- Heads prepared in custom holders; brains exposed in Ringer solution; dyes allowed to diffuse; brains preserved for later imaging.
- Brains sectioned horizontally at 80 µm using a vibratome; sections prepared for two parallel staining procedures (Kenyon cells and synaptic markers).

## Kenyon cell staining
- Neuronal nuclei labeled with HRP to distinguish Kenyon cells from other cells.
- Permeabilization, blocking, and primary/secondary antibody steps detailed; nuclei stained with DAPI; preparations mounted for imaging.

## Synapse and microglomeruli staining
- Presynaptic boutons labeled with anti-SYNORF1; combinations with Alexa 568 phalloidin for actin to reveal Kenyon cell dendrites.
- For select species, additional staining with HRP and phalloidin to quantify microglomeruli manually.
- Extra fixation steps used to preserve actin for phalloidin labeling; staining performed with extended incubations and multiple washes.

## Confocal image acquisition and 3D reconstruction
- Whole brains imaged with confocal microscopes (Leica SP5/SP8); tiled stacks acquired and stitched for complete volumes.
- MB calyx and surrounding Kenyon cell clusters imaged at higher magnification (63X objective for detailed microstructures).
- Multispectral channels to avoid crosstalk; z-dimension correction factors applied (1.52x for methyl salicylate mounting; 1.85x during glycerol mounting).
- 3D reconstructions performed in Amira; regions manually annotated and segmented; volumes extracted from models.

## Data processing and quantification
- Kenyon cell counts: nuclei density measured in 25 x 25 x 15 µm cubes; total Kenyon cells per hemisphere estimated by density × MB cluster volume.
- Synapse density and count: 3D Object Counter used on SYNORF1-stained sections; synapse counts in 5 cube samples per brain; background filtering to exclude small, likely spurious objects.
- Microglomeruli counts: analyzed in five regions per calyx with phalloidin and SYNORF staining; subset analyses performed with higher magnification.
- Calibration and correction: z-dimension corrected using calibration beads to account for refractive index differences; final estimates scaled to total brain volumes.

## Quality control
- Data include multiple measures per species; damaged or poorly stained samples excluded.
- Measurements aligned with previously published methodologies (Montgomery et al. 2016) to ensure cross-species consistency.

## Details of file contents
- Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv
  - Interspecific volumetric data for brain components (e.g., visual neuropils, olfactory neuropils, mushroom bodies: calyx, peduncle, lobes; central brain; rest-of-CBR; body size metrics such as length, wingspan, mass).
  - Columns include GENUS, SPECIES, SEX, COUNTRY, and volumes for various neuropils and body-size traits.
- Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts.csv
  - Interspecific Kenyon cell estimates.
  - Columns include INDIVIDUALS, SPECIES, CALYX VOLUME, ESTIMATED KENYON CELL NUMBER, LOG10 transformations, KC DENSITY.
- Heliconiini_NeuroData_Table3_Synapse_Counts.csv
  - Interspecific synapse/microglomeruli data.
  - Columns include SYNAPSE COUNTS (raw and estimated), INDIVIDUAL, AGE, SPECIES, CALYX VOLUME, SYNAPSE NUMBER PER CUBE, SYNAPSE DENSITY, ESTIMATED SYNAPSE NUMBER, MICROGLOMERULI COUNTS, MICROGLOMERULI DENSITY.

## References
- Couto A, et al. Rapid expansion and visual specialisation of learning and memory centres in the brains of Heliconiini butterflies. Nature Communications. 2023.
- Montgomery SH, Merrill RM, Ott SR. Brain composition in Heliconius butterflies, posteclosion growth and experience-dependent neuropil plasticity. Journal of Comparative Neurology. 2016.