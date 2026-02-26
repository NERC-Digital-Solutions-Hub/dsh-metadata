# Data describing population responses of wild bees to oilseedrape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes the effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam) and a control on two wild pollinator models: Osmia bicornis (solitary bee) and Bombus terrestris (bumblebee) across 33 sites in the UK, Hungary, and Germany during 2015.
- Data include pollinator responses, neonicotinoid residues in pollen/nectar, and landscape context around colonies/sites.
- Study funded by CEH National Capability (NERC) and implemented on platforms funded by Syngenta Ltd. and Bayer CropScience.

## Study design and scope
- Sites: 33 commercial winter oilseed rape fields established Aug–Sept 2014; flowering Apr–Jun 2015.
- Geographic distribution: UK (12 sites), Hungary (12 sites), Germany (9 sites).
- Experimental layout: large blocks (mean area ~63 ha) with three sites per block; blocks separated by >10 km; within-block random assignment to three treatments: clothianidin (CTD), thiamethoxam (TMX), or control (fungicide only).
- Pollinator groups and deployment:
  - Bombus terrestris: 12 colonies per site, clustered into four multi-hives; measurements based on multi-hives; neonicotinoid residues tested in stored hive products and pollen baskets; six colonies per site used for colony reproductive metrics and weight tracking.
  - Osmia bicornis: 50 cocoons released per site with two artificial trap nests; post-flowering assessments of reproductive cells; residues tested in pollen/nectar within cells; color-based pollen foraging tracked; three sites lacked pollen/nectar data where no O. bicornis cells were found.

## Pollinator response measures
- Bombus terrestris (B. terrestris):
  - Reproductive output: total developmental stages within colonies; queen cells, eggs/larvae, workers, drones; colony weight tracked weekly during exposure.
  - Residue testing: neonicotinoid concentrations in hive products (pollen/nectar) and pollen baskets; two multihives per site sampled for residue analysis.
- Osmia bicornis (O. bicornis):
  - Reproductive output: number of O. bicornis cells in trap nests; larvae presence; adult counts; species-specific cell data captured after exposure.
  - Residue testing: residues in pollen and nectar used to provision larvae within cells; colour-associated foraging patterns used to separate residue data when applicable.
- Residue analysis and metrics:
  - Neonicotinoids measured: clothianidin (CTD), thiamethoxam (TMX), imidacloprid (IMI); analysis via LC-MS/MS with UKAS-accredited methods.
  - Limits: LoQ ~0.53 ng/g; LoD ~0.38 ng/g (site-specific LoQs; handling non-detects as half LoD).
  - Metrics per site:
    - Median and maximum residues for each chemical in relevant matrices.
    - Combined neonicotinoid index (NNI) calculated from TMX, CTD, IMI with a toxicity-weighted correction based on honeybee LD50s to provide a single exposure metric.
    - Both raw (median/peak) and corrected (LD50-based) NNI values reported.
- Exposure timing: Days of exposure recorded (R1–R8 timepoints) with pre-exposure measurements and weight tracking (weights R1–R8).

## Landscape context
- Habitat context within 1.5 km of colonies:
  - Land-use categories: oilseed rape, cereals, legumes, vegetables, horticulture, grassland, woodland, scrub, water, urban.
  - Diversity metric: Shannon-Weiner habitat diversity index derived from landscape composition.

## Data files and metadata
- bombus_sites.csv
  - Site-level data for B. terrestris: country, site, block, treatment; pre-exposure worker counts; colony-level metrics (queen/drones/workers), queen cells, weights, OSR cover, landscape diversity, residue metrics (CTD/TMX/IMI medians and peaks; NNI metrics), days of exposure (R-series).
  - Units include counts, percentages, and ng/g for residues.
- osmia_sites.csv
  - Site-level data for O. bicornis: country, site, block, treatment; trap nest data; total cells, larvae, osmia-specific counts; OSR cover; landscape diversity; residue metrics (TMX/CTD/IMI medians and peaks); NNI metrics; days of exposure; pre-weight and weight series.
- osmia_residue.csv
  - Residue data within Osmiabicorbis reproductive cells from trap nests: per TrapNest, total cells, larvae counts, non-Osmia cells; TMX/CTD/IMI residues in nectar and pollen by color-coded categories; multiple color palettes across cells; NNI metrics (median/peak; raw and corrected); detailed per-nest residue values (ng/g).
- Metadata conventions
  - NA denotes missing data.
  - Median values rounded up to whole numbers for site-level Bombus data.
  - Residue concentrations reported in ng/g w/w; OSR_cover in percent; weights in grams.
  - Data tables include many derived fields (e.g., NNI_median_raw, NNI_median_corrected, NNI_peak_raw, NNI_peak_corrected).

## Data quality and usage notes
- Data include both raw measures (counts, weights) and derived metrics (NNI, medians, peaks); useful for cross-site comparisons and landscape-context analyses in relation to neonicotinoid exposure.
- Some sites had missing pollen/nectar data for Osmia bicornis due to the absence of bees in trap nests.
- Use honeybee LD50-based corrections for NNI as a proxy for wild pollinator sensitivity in the absence of species-specific LD50s.

## References and context
- EFSA (2013) Conclusion on the pesticide risk assessment for clothianidin/thiamethoxam/imidacloprid.
- Technical methods for residue analysis detailed in CEH protocol document (linked in dataset description).