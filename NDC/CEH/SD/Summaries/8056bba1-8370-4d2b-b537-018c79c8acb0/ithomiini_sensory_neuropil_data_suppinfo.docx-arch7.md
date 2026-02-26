# Neuropil volumes for sensory structures in the brains of ithomiini butterflies forming a single community in eastern Ecuador

## Overview
- A dataset describing neuropil volumes for sensory brain structures in ithomiini butterflies collected from eastern Ecuador (Estación Científica Yasuní, Parque Nacional Yasuní).
- Includes 392 individuals across 49 species, representing multiple mimicry rings within a Mullerian mimicry community.
- Builds on prior work examining how sensory environments shape investment in sensory brain centres.
- Data were generated from wild-caught specimens collected in 2011–2012 and 2022; voucher specimens were kept, and individuals were sexed.

## Spatial and field context
- Field site: Estación Científica Yasuní, near coordinates 0°40'27" S, 76°23'50" W, within a ~4.5 km² area of primary lowland Amazon rainforest.
- Sampling relied on designated trails with permits (collection and export) issued by Parque Nacional Yasuní and related authorities; support from PUCE and Estación Científica Yasuní.
- Location and sampling are suitable for linking brain morphology data with spatial and ecological context (e.g., habitat, local species diversity, mimicry patterns).

## Data and methods (measurement workflow)
- Tissue preparation and imaging:
  - Dissections performed on wild-caught specimens; brains immunostained for synapsin.
  - Confocal laser-scanning microscopy used to image anterior and posterior brain regions; stacks merged for 3D analysis.
  - Z-dimension adjusted by a factor of 1.52 to correct for imaging geometry.
- Segmentation and volume extraction:
  - Manual segmentation of neuropils in Amira 2021.2 on every third slice, using synapsin signal to delineate boundaries.
  - Intervening slices interpolated to reconstruct complete volumes; smoothing applied in three dimensions.
  - Volumes computed for: medulla, lobula plate, lobula, accessory medulla, ventral lobula (part of the optic lobe), anterior optic tubercle, antennal lobe; total optic lobe volume is the sum of the first four neuropils.
  - Lamina excluded due to thinness and fragility in smaller species; ventral lobula presence varied (absent in many individuals, especially females).
  - For bilateral structures, volumes were doubled to represent both hemispheres.
  - Raw volumes for anterior optic tubercle and antennal lobe subtracted from central brain to create a rest-of-central-brain measure (an allometric control for analyses).
- Data transformation and structure:
  - All volumes (including rest-of-central-brain and optic-lobe components) were log10 transformed.
  - A dedicated dataset column set includes: year collected, individual ID, subtribe, species, sex, mimicry ring, log10(rest of central brain), log10(medulla), log10(lobula plate), log10(lobula), log10(accessory medulla), log10(ventral lobula), log10(antennal lobe), log10(anterior optic tubercule), log10(optic lobe) (combined).
- Note on scope: lamina excluded; ventral lobula absent in many individuals; anterior optic tubercle and antennal lobe volumes used as controls in analyses.

## Variables and data structure
- Columns present: Year collected; ID; Subtribe; Species; Sex; Mimicry ring; log10(rest of central brain); log10(medulla); log10(lobula plate); log10(lobula); log10(accessory medulla); log10(ventral lobula); log10(antennal lobe); log10(anterior optic tubercule); log10(optic lobe).
- The dataset supports cross-species comparisons of sensory brain investment and potential associations with mimicry rings and ecological context.

## Quality control and provenance
- Quality checks:
  - Individual-level data includes multiple measures per species.
  - Damaged or poorly stained samples excluded.
  - Measurements aligned with previously published methodologies (Montgomery & Ott, 2016).
- Provenance:
  - Dataset created as part of NERC Independent Research Fellowship NE/N014936/1.
- References guiding methods:
  - Elias et al. (2008); Montgomery & Ott (2015); Wainwright & Montgomery (2022, 2024).