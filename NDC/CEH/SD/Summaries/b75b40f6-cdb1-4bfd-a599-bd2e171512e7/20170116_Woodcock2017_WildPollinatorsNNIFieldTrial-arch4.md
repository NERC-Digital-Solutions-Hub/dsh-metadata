# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes a 2015 field study on the effects of neonicotinoid seed treatments on wild pollinators across Hungary, Germany, and the UK.
- Focuses on two model pollinator systems: the solitary bee Osmia bicornis and the bumblebee Bombus terrestris.
- Investigates reproductive outcomes, colony development, and neonicotinoid residues in pollen/nectar associated with different seed treatments.

## Study design and scope
- Locations: 33 commercial oilseed rape sites (UK: 12; Hungary: 12; Germany: 9).
- Treatments: Clothianidin (CTD), Thiamethoxam (TMX), and a control (fungicide-only).
- Crop timing: Oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015.
- Experimental structure: Large blocks per site (mean area ~63 ha); three treatments randomized within blocks; blocks separated by at least 10 km.
- Species-specific sampling windows aligned with flowering and post-exposure periods.

## Data collected per species

### Bombus terrestris (bumblebees)
- Colony setup: 12 commercial colonies per site, organized into four multihives (clusters of three colonies).
- Measurements: Developmental stage counts within colonies (e.g., workers, drones, eggs, larvae) after 51–60 days; weekly weight monitoring of multihives.
- Residue sampling: Two multihives per site for stored pollen/nectar residues; additional pollen from worker pollen baskets tested.
- Timepoints: Residues measured during/near flowering; colony post-exposure assessments conducted in June 2015.
- Landscape context: Surrounding habitat characterized within 1.5 km of colonies (land-use categories + Shannon-Weiner diversity).

### Osmia bicornis (solitary bees)
- Release and nesting: 50 cocoons released per site with two artificial trap nests per site.
- Measurements: Counts of reproductive cells per trap nest after flowering; color-coded pollen/nectar provisioning tracked to infer foraging sources.
- Residue sampling: Pollen/nectar residues collected from trap nests; pollen/nectar from trap nests analyzed for neonicotinoids.
- Timepoints: Sampling aligned with end of oilseed rape flowering (2015).
- Landscape context: Similar 1.5 km radius landscape metrics as for B. terrestris.

## Neonicotinoid residue analysis and metrics
- Target compounds: Clothianidin (CTD), Thiamethoxam (TMX), Imidacloprid (IMI).
- Analytical method: Liquid chromatography with triple quadrupole mass spectrometry (LC-MS/MS); accredited under ISO17025:2005.
- Quantification: LOQ ~0.53 ng/g; LOD ~0.38 ng/g; values below LOQ treated as half LOD.
- Metrics:
  - Site-level medians and maximum residues for each compound.
  - Combined neonicotinoid index (NNI) aggregating TMX, CTD, IMI with LD50-based toxicity weighting.
  - Raw (median_raw, peak_raw) and corrected (median_corrected, peak_corrected) NNI values using acute oral LD50 corrections.
  - Exposure timing captured as Days_of_exposure across measurement rounds.

## Data files and metadata structure
- bombus_sites.csv: Site-level data for Bombus terrestris, including country, site identifier, treatment, block, colony metrics, OSR cover, landscape diversity, compound-specific residue metrics, NNI metrics, exposure days, and colony weights.
- osmia_sites.csv: Site-level data for Osmia bicornis, including similar fields as bombus_sites.csv plus trap-nest specific counts and residues related to O. bicornis.
- osmia_residue.csv: Residue data at the trap-nest level for Osmia bicornis, detailing per-color pollen/nectar residues (TMX, CTD, IMI) and derived NNI values (raw and corrected).

## Key notes and considerations
- Cross-country differences in seed treatment formulations and site conditions are present.
- LD50-based corrections used for wild pollinators due to lack of species-specific toxicity values.
- Some sites lacked pollen/nectar samples or detectable nest cells, affecting certain residue analyses or counts.
- Data are organized to support end-to-end data lifecycle: collection, processing, residue analysis, metadata, and derived toxicity-weighted metrics.

## Relevance for data strategy and governance
- The study demonstrates comprehensive data lifecycle management, including:
  - Multi-species, multi-country experimental design with clear replication and randomization.
  - Rich metadata on landscape context and habitat diversity to support ecological interpretation.
  - Detailed, standardized measurement units and derived metrics (e.g., NNI) enabling cross-site comparisons.
  - Transparent data formats and explicit handling of below-LOD/LOQ values.
- Highlights the importance of harmonized metadata and clear data schemas when integrating complex ecological datasets across networks and partners.