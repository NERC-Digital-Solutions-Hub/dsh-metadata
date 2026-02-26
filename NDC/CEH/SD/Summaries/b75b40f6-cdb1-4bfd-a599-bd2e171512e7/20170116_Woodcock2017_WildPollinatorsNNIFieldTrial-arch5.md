# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes a dataset on the effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam, and a control) on wild pollinators across Hungary, Germany, and the UK.
- Focuses on two pollinator model systems: Osmia bicornis (solitary bee) and Bombus terrestris (bumblebee).
- Includes population responses (reproduction metrics, colony development), neonicotinoid residues in pollen/nectar, and landscape context around colonies.
- Data were collected in 2015 as part of CEH/NERC work with industry funding support.

## Experimental design and scope
- 33 commercial oilseed rape sites: UK (12), Hungary (12), Germany (9); oilseed rape established Aug–Sep 2014 and flowering Apr–Jun 2015.
- Large blocks per site (mean ~63 ha); three-treatment randomized block design within blocks.
- Treatments:
  - Clothianidin (Modesto®) with fungicide
  - Thiamethoxam (Cruiser®) with fungicide
  - Control (fungicide-only)
- Key goals: assess population-level responses of wild pollinators to treated crops and quantify neonicotinoid residues in hive/store products.

## Species and sampling approach
- Bombus terrestris:
  - 12 commercial colonies per site, clustered into four multi-hives; measurements based on multi-hive units.
  - Residue analysis in stored pollen/nectar from two multi-hives per site.
  - Assess reproductive success via colony-level metrics (abundance of developmental stages, queen production) and weekly colony weight.
  - Six colonies per site used for weight tracking; exposure window includes flowering period.
- Osmia bicornis:
  - 50 cocoons released per site with two artificial trap nests per site during flowering.
  - Post-flowering dissections to count reproductive cells; pollen/nectar residues analyzed per trap nest (color-based housing of pollen/nectar for tracing foraging).
  - Some sites yielded no O. bicornis cells; pollen/nectar residues extracted and analyzed accordingly.

## Neonicotinoid treatments and residue analysis
- Neonicotinoids quantified in pollen and nectar using LC-MS with a triple quadrupole instrument (ESI interface).
- Analytical parameters:
  - Limits of quantification (LoQ) around 0.53 ng/g; LoD around 0.37–0.38 ng/g depending on sample type.
  - Residues reported for clothianidin (CTD), thiamethoxam (TMX), and imidacloprid (IMI); where below LoQ treated as half LoD.
- Metrics computed:
  - Median and maximum residues per site for each neonicotinoid.
  - A combined neonicotinoid metric (NNI) derived from LM/TMX/IMI values, normalised to honeybee LD50s to approximate overall toxicity burden.
  - Both median- and maximum-based NNI values reported (raw and LD50-corrected).
- Exposure timing captured via Days_of_exposure alongside R1–R8 measurement windows for colonies.

## Landscape context and metadata
- Landscape around colonies characterized within a 1.5 km radius using ARCGIS.
- Land-use categories included crops (oilseed rape, cereals, legumes, vegetables), horticulture, grassland, woodland, scrub, water, urban.
- Derived metrics:
  - Shannon–Weiner diversity index for surrounding habitats.
  - Oilseed rape (OSR) cover percentage within radius.

## Data files and metadata structure
- bombus_sites.csv
  - Site-level data for Bombus terrestris: country, site, block, treatment, pre-exposure counts, colony-level metrics (e.g., queen/drones counts, worker counts, egg masses), OSR_cover, landscape_div, neonicotinoid residues (CTD/TMX/IMI) including medians, peaks, and NNI metrics, days_exposure, and weight data.
- osmia_sites.csv
  - Site-level data for Osmia bicornis: country, site, block, treatment, trap-nest results, OSR_cover, landscape_div, residues (medians/peaks for TMX/CTD/IMI and NNIs), days_exposure, pre_weight, weights across R1–R8, and relative weight metrics.
- osmia_residue.csv
  - Residue data from Osmia trap nests by trap nest/color; includes TMX/CTD/IMI residues in nectar and pollen, per color, total rows, osmia-specific counts (larvae, cells_total, osmia_larvae), and related metadata (trap nest IDs, colors, etc.).
- Metadata for the three CSVs provide detailed field descriptions, units, and data interpretation notes (e.g., color-based pollen distinctions, NA entries indicating missing data).

## Data quality, governance, and provenance
- Data primarily prepared for pesticide risk assessment and pollinator conservation context.
- Metadata include precise method details (LC-MS protocol, LOQ/LOD), measurement timelines, and field identifiers to facilitate data reuse and reproducibility.
- Acknowledges limitations and occurrences of incomplete data (NA values), site-level variability, and species-specific sampling constraints (e.g., some sites lacking O. bicornis cells).
- Data lineage linked to EFSA context and references, with explicit consent to publish residues and exposure data.
- Encourages standardized data sharing practices, including consistent units, complete metadata, and transparent documentation of data processing steps for future discovery and reuse.