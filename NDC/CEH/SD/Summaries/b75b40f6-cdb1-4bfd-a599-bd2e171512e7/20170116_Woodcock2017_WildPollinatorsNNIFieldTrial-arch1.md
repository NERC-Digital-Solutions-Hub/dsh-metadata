# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Examines effects of three neonicotinoid seed treatments on wild pollinators: clothianidin, thiamethoxam, and a fungicide-only control.
- Target species: solitary bee Osmia bicornis and bumblebee Bombus terrestris.
- Measured endpoints include reproductive output and colony development (O. bicornis cells; B. terrestris worker, drone, queen numbers, egg masses), as well as neonicotinoid residues in pollen and nectar.
- Conducted across 33 commercial oilseed rape sites in the UK, Hungary, and Germany during the spring 2015 flowering period.
- Landscape context captured around colonies (1.5 km radius) using land-use categories and Shannon-Weiner diversity.
- Data products include site-level metadata, residue measurements, and composite toxicity-weighted metrics.

## Experimental Design
- Setting and timeline:
  - Oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015.
  - Large contiguous blocks per site (mean area ~63 ha); blocks separated by >10 km.
- Treatments:
  - Randomized within blocks: clothianidin (CTD), thiamethoxam (TMX), or control (fungicide only).
- Bombus terrestris (UK: audax/subsp.; HU/DE: terrestris):
  - 12 commercial colonies per site, clustered into four multihives (three colonies each).
  - Two multihives sampled for neonicotinoid residue testing in hive products; six colonies (two multihives) monitored for colony development and weighed over the flowering period.
- Osmia bicornis:
  - 50 cocoons released per site with two artificial trap nests per site.
  - After flowering, nests dissected to count reproductive cells; pollen/nectar residues sampled and analyzed.
  - Color-coded cells used to differentiate foraging sources; pollen/nectar collected for residue testing.
  
## Data Collected and Measurements
- Biological endpoints:
  - Bombus terrestris: total development (workers, drones, queens), queen and worker counts, egg masses, and colony weights across measurement rounds.
  - Osmia bicornis: number of reproductive cells, larvae within cells, and related developmental metrics.
- Timing data:
  - Measurements recorded at multiple exposure timepoints (R1–R8) corresponding to days of exposure to the oilseed rape crop.
- Residue analysis:
  - Neonicotinoids quantified: clothianidin, thiamethoxam, and imidacloprid.
  - Analytical method: liquid chromatography with triple quadrupole mass spectrometry (UKAS ISO17025:2005 standards).
  - Limits: LoQ ~0.53 ng/g; LoD ~0.38 ng/g; below-LoQ values set to half LoD.
  - Residues reported as medians and maxima per site, for pollen, nectar, and stored hive products.
  - Combined toxicity metric (NDI or NNI) computed by summing weighted residues across the three compounds using honeybee LD50-based toxicity weights (TMX: 0.005 μg/bee; CTD: 0.00379 μg/bee; IMI: 0.0037 μg/bee; weights scaled to 1:0.758:0.74).
  - Both raw (median/maximum) and corrected NNI values provided (median_raw, median_corrected, peak_raw, peak_corrected).
- Landscape and habitat context:
  - 1.5 km radius around colonies categorized into crops, grassland, woodland, scrub, water, urban; diversity index computed (Shannon-Weiner).

## Datasets and Metadata
- bombus_sites.csv
  - Site-level data for B. terrestris, including country, site ID, treatment, block, pre-exposure numbers, developmental endpoints (e.g., queen, worker, drone counts), colony weights, OSR cover, landscape diversity, and resonance metrics (CTD/TMX/IMI concentrations, NNI metrics).
- osmia_sites.csv
  - Site-level data for O. bicornis, including country, site ID, treatment, block, trap-nest metrics (total_rows, osmia_larvae, cells_total), OSR cover, landscape diversity, and resonance metrics (TMX/CLT/IMI concentrations, NNI metrics, medians and peaks).
- osmia_residue.csv
  - Residue data from Osima pollen/nectar in reproductive cells by trap nest and color category; includes TMX, CLT, and IMI residues by color, total rows, and NNI metrics.
- Residues and exposure metadata:
  - Detailed concentrations per medium (nectar, pollen, pollen baskets), per compound (TMX, CTD, IMI), including medians, peaks, and corrected NNI values.
  - Days_of_exposure_R1...R8 and weight-related measures (pre_weight, Weight_R1...Weight_R8, relative_peak_weight).

## Analytical Context for Analysts
- Purpose: enable analysis of whether neonicotinoid seed treatments affect wild pollinator populations, considering both direct exposure (residues) and landscape context.
- Data structure supports:
  - Comparisons of reproductive output and colony health across treatments and countries.
  - Relationships between neonicotinoid residues in pollen/nectar and population responses.
  - Influence of landscape diversity on sensitivity to seed treatments.
- Considerations:
  - Mixed-field, multi-country design; treat effects may interact with local context.
  - Toxicity weighting uses honeybee LD50 due to lack of species-specific data for wild pollinators; interpret NNI with this caveat.
  - Data include NA values; methodological details for residue quantification and data handling are specified.

## Notes and Limitations
- Experimental platform funded by CEH with industry support; results pertain to 2015 field conditions and the particular crop (winter-sown oilseed rape).
- Uses surrogate toxicity weights from honeybees for wild pollinators due to limited species-specific LD50 data.
- Data complexity: multiple endpoints, timepoints, and a composite exposure metric requiring careful statistical modeling to disentangle treatment, residue, and landscape effects.