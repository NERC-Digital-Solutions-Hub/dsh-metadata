# Neuropil volumes for sensory structures in ithomiini butterflies

## Overview
- Dataset of neuropil volumes for sensory brain structures in ithomiini butterflies from a single eastern Ecuadorian community.
- Aims to understand how sensory environments shape investment in sensory brain centres, in the context of Müllerian mimicry rings and ecological niche convergence.
- Builds on prior work to examine relationships between ecological environment and brain composition.

## Field site, collection and sampling design
- Fieldwork conducted along designated trails around Estación Científica Yasuní, Parque Nacional Yasuní, Orellana Province, Ecuador (primary lowland Amazon rainforest).
- Area ~4.5 km2 with high ithomiine diversity (≈60 species recorded locally).
- Sampling periods: November/December 2011; September/October 2012; August–October 2022.
- Permits obtained from Parque Nacional Yasuní and related authorities; affiliation with PUCE and Estación Científica Yasuní staff.
- Species identification: wing venation patterns and ID sheets; voucher wings stored; nonretained individuals identified, sexed, and marked to avoid resampling.

## Sensory neuroanatomy measurements (sample and preparation)
- Primary sample: wild-caught ithomiines (2011–2012) comprising 392 individuals across 49 species; individual species samples ranged from 1 to 28 individuals.
- Dissection and fixation: brains dissected in HEPES-buffered saline; fixed in zinc formaldehyde solution (ZnFA) 16–20 hours with agitation; subsequent washes and storage in methanol/DMSO.
- Immunostaining: brains immunostained for synapsin (pre-synaptic marker) using standard protocols; details include blocking, primary antibody (anti-SYNORF, 1:30), secondary antibody (Cy2-conjugated anti-mouse, 1:100), and extensive washing.
- Clearing and imaging: samples cleared in methyl salicylate; imaged with confocal laser-scanning microscope (Leica SP5/SP5-II) across anterior and posterior sides; z-stacks captured and merged in Amira software.
- Imaging parameters and preprocessing: 10x objective (0.4 NA); 488 nm excitation; z-step 2 μm; x-y resolution 512x512; z-dimension corrected by multiplying voxel size by 1.52 to account for distortion.
- Neuropil segmentation: manual segmentation of five optic lobe neuropils (medulla, lobula plate, lobula, accessory medulla, ventral lobula); central brain volumes derived excluding lamina (too thin and damaged in smaller species). Anterior optic tubercle and antennal lobe also segmented to assess olfactory investment; volumes for these two structures subtracted from central brain to form “rest of central brain” as an allometric control.
- Volume calculation and transformation: volumes (raw) extracted via measure statistics; volumes for paired neuropils doubled; all volumes log10 transformed. Optic lobe total is the sum of medulla, lobula plate, lobula, ventral lobula; lamina excluded.

## Data structure and variables
- Columns (example descriptors):
  - Year collected
  - ID (individual identifier)
  - Subtribe
  - Species
  - Sex
  - Mimicry ring (based on Elias et al., 2008)
  - log10(rest of central brain volume μm3)
  - log10(medulla volume μm3)
  - log10(lobula plate volume μm3)
  - log10(lobula volume μm3)
  - log10(accessory medulla volume μm3)
  - log10(ventral lobula volume μm3)
  - log10(antennal lobe volume μm3)
  - log10(anterior optic tubercule volume μm3)
  - log10(optic lobe volume μm3) (combined medial shared volumes)
- Note: 5 optic lobe neuropils + anterior optic tubercle + antennal lobe measured; lamina excluded; ventral lobula absent in many individuals, especially females.

## Quality control and standardization
- Individual-level data include multiple measures per species; damaged or poorly stained specimens excluded.
- Measurements follow previously published, standardized methodologies (consistent with Montgomery & Ott, 2016).
- Data generation and processing steps are designed for cross-species comparability and reproducibility.

## Provenance, reproducibility, and related work
- Dataset created as part of a NERC Independent Research Fellowship NE/N014936/1.
- Grounded in a sequence of studies linking sensory environment to brain structure:
  - Montgomery & Ott (2015)
  - Wainwright & Montgomery (2022)
  - Wainwright et al. (2024)
  - Elias et al. (2008) for mimicry ring context
- Data collection and analysis pipelines include standardized dissection, immunostaining, imaging, segmentation, and transformation suitable for comparative analyses of ecological neural investment.

## References
- Elias M, Gompert Z, Jiggins C, Willmott K. Mutualistic interactions drive ecological niche convergence in a diverse butterfly community. PLoS biology. 2008.
- Montgomery SH, Ott SR. Brain composition in Godyris zavaleta, a diurnal butterfly, reflects an increased reliance on olfactory information. Journal of Comparative Neurology. 2015.
- Wainwright JB, Loupasaki T, Ramirez F, et al. Mutualisms within light microhabitats drive sensory convergence in a mimetic butterfly community. bioRxiv. 2024.
- Wainwright JB, Montgomery SH. Neuroanatomical shifts mirror patterns of ecological divergence in three diverse clades of mimetic butterflies. Evolution. 2022.