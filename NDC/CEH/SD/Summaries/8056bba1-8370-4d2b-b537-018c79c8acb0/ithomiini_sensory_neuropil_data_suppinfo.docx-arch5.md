# Neuropil volumes for sensory structures in ithomiini butterflies in eastern Ecuador

## Overview
- A dataset of neuropil volumes for sensory brain structures in a single ithomiini butterfly community from eastern Ecuador (Parque Nacional Yasuní, Estación Científica Yasuní area).
- Focuses on how sensory environments influence investment in sensory processing centers.
- Ties to prior work on mimicry, sensory ecology, and brain composition (Elias et al. 2008; Montgomery & Ott 2015; Wainwright & Montgomery 2022; Wainwright et al. 2024).

## Scope and context
- Field site: primary lowland Amazon rainforest around Estación Científica Yasuní, Yasuní National Park, Ecuador.
- Specimens collected under multiple permits across two periods: 2011–2012 and 2022.
- Taxonomic and mimicry information: species identified to species level; mimicry ring assignments based on wing patterns (Elias et al., 2008).
- Sample sizes: sensory neuroanatomy measurements from 392 individuals across 49 species; uneven species representation (e.g., Hypothyris anastasia n=28; Callithomia alexirrhoe n=1).
- Voucher specimens preserved; nonretained individuals ID’d, sexed, and marked to avoid resampling.

## Data collection and provenance (methods)
- Dissection and preparation:
  - Specimens dissected in HEPES-buffered saline; fixed in ZnFA for 16–20 hours.
  - Tissues washed and stored in methanol/DMSO, later in methanol, then shipped for processing.
- Immunostaining and imaging:
  - Immunostaining for synapsin to label pre-synaptic regions; primary antibody incubation for 3.5 days at 4°C; secondary antibody with Cy2 conjugate; extensive washing.
  - Brains cleared in methyl salicylate and imaged with confocal microscopy (Leica SP5/SP5-II) across anterior and posterior sides; stacking and merging in Amira 2021.2.
- Image processing and segmentation:
  - Z-dimension correction factor applied (multiplied by 1.52) to address artificial shrinkage.
  - Manual segmentation of neuropils based on immunofluorescence; interpolation for unsampled sections; 3D smoothing.
  - Volumetric measurements extracted for five optic lobe neuropils (medulla, lobula plate, lobula, accessory medulla, ventral lobula) plus anterior optic tubercle and antennal lobe.
  - Rest of central brain calculated by subtracting anterior optic tubercle and antennal lobe from central brain volume; used as allometric control.
  - All paired neuropils scaled by factor of two; volumes log10-transformed.
- Coverage notes:
  - Lamina excluded due to thinness and damage risk; ventral lobula absent in many individuals (notably females).
  - Raw optic lobe volumes aggregated to derive overall optic lobe volume.
- Data provenance:
  - Part of an NERC Independent Research Fellowship (NE/N014936/1); aligns with published methodologies (Montgomery & Ott 2016) for cross-species comparability.

## Data structure and fields (metadata and measurements)
- Core metadata:
  - Year collected; Individual ID; Subtribe; Species; Sex; Mimicry ring (based on Elias et al., 2008).
- Neuroanatomical measurements (log10-transformed volumes, in µm³):
  - Rest of central brain
  - Medulla
  - Lobula plate
  - Lobula
  - Accessory medulla
  - Ventral lobula
  - Antennal lobe
  - Anterior optic tubercle
  - Optic lobe (combined medulla, lobula plate, lobula, ventral lobula)
- Purpose of measurements:
  - Assess relative investment in sensory processing centers and test for allometric relationships against central brain size.

## Quality control and limitations
- Quality controls:
  - Multiple measures per species; damaged or poorly stained samples excluded.
  - Methods standardized to be consistent with Montgomery & Ott (2016).
- Limitations and data considerations:
  - Lamina not measured; ventral lobula missing in many individuals.
  - Uneven species representation; some very small sample sizes (e.g., single individuals for certain species).
  - Image-based segmentation subject to manual tracing variability, mitigated by consistent protocol and use of allometric controls.

## Data use, governance, and provenance
- Data governance:
  - Permits and field collection details documented (permit numbers and issuing authorities).
  - Voucher specimens preserved; clear species identification and mimicry ring classification documented.
- Publication readiness:
  - Data are processed into standardized, logged, and repackaged volumetric measurements suitable for comparative analyses across species and mimicry rings.
  - Metadata and methodological details enable reproducibility and re-use in studies of sensory ecology and brain evolution.
- Potential research applications:
  - Investigation of how mimicry-associated sensory environments relate to brain structure investments.
  - Cross-species comparisons of olfactory and visual processing investments in mimetic butterfly communities.
  - Integration with ecological and behavioral data to explore neural correlates of habitat and niche differences.

## References
- Elias M, Gompert Z, Jiggins C, Willmott K. Mutualistic interactions drive ecological niche convergence in a diverse butterfly community. PLoS Biology, 2008.
- Montgomery SH, Ott SR. Brain composition in Godyris zavaleta, a diurnal butterfly, reflects an increased reliance on olfactory information. Journal of Comparative Neurology, 2015.
- Wainwright JB, Montgomery SH. Neuroanatomical shifts mirror patterns of ecological divergence in three diverse clades of mimetic butterflies. Evolution, 2022.
- Wainwright JB et al. Mutualisms within light microhabitats drive sensory convergence in a mimetic butterfly community. bioRxiv, 2024.