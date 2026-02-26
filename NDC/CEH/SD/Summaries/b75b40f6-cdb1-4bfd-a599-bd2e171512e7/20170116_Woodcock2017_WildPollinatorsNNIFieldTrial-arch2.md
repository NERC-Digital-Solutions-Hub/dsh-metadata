# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes a multi-country study on how three neonicotinoid seed treatments (clothianidin, thiamethoxam) and a fungicide-only control affect wild pollinators.
- Focuses on two model pollinator systems: Bombus terrestris (bumblebee) and Osmia bicornis (solitary bee).
- Data cover population responses, neonicotinoid residues in bee meals (pollen/nectar), and landscape context around colonies.

## Study design and data collection
- Location and timing:
  - 33 commercial sites across the UK (12), Hungary (12), and Germany (9).
  - Winter-sown oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015 for biodiversity assessment.
- Experimental setup:
  - Large oilseed rape blocks (mean ~63 ha) arranged in three-site blocks, within-block spacing ~5.5 km; blocks >10 km apart.
  - Randomly assigned within each block to three treatments: clothianidin (CTD), thiamethoxam (TMX), or control (fungicide-only).
- Species and sampling:
  - Bombus terrestris: 12 commercial colonies per site, clustered into four multi-hives; measurements based on multi-hive data due to colony expansion.
  - Osmia bicornis: 50 cocoons released per site with two artificial trap nests; assessed for reproductive cell production and residues in pollen/nectar.
- Timeline of measurements:
  - Bumblebees: assessments during oilseed rape flowering in 2015; six colonies (two multi-hives) used for brood measurements over 51–60 days post-exposure; colonies weighed weekly.
  - Solitary bees: post-flowering period analyses of trap nests; counts of reproductive cells and pollen/nectar residues; pollen/color differences used to distinguish forage sources.

## Neonicotinoid residue analysis
- Compounds measured: clothianidin (CTD), thiamethoxam (TMX), imidacloprid (IMI).
- Methods and quality:
  - Liquid chromatography–tandem mass spectrometry (LC-MS/MS) with UKAS-accredited ISO17025:2005 standards.
  - Limits: LoQ ≈ 0.53 ng/g; LoD ≈ 0.38 ng/g (specific for B. terrestris; similar values for Osmia).
  - Below LoQ values treated as half LoD for analyses.
- Residue metrics:
  - Median and maximum residue concentrations calculated for each species and sample type.
  - A combined neonicotinoid index (NNI) computed to reflect overall exposure using a toxicity-weighted sum based on honeybee LD50s (TMX, CTD, IMI with relative toxicities 1:0.758:0.74).
  - Separate median and peak NNI values, including both raw and LD50-corrected (adjusted) forms.

## Landscape context
- Contextual data within 1.5 km of each bee colony:
  - Land-use categorised into crops (oilseed rape, cereals, legumes, vegetables), horticulture, various grasslands, woodland, scrub, water, and urban.
  - Environmental diversity quantified using Shannon–Weiner diversity index.

## Data files and metadata
- bombus_sites.csv: Site-level data for Bombus terrestris, including country, site, block, treatment, pre-exposure worker numbers, colony counts, queen/drone/cell numbers, adult worker numbers, colony weights, oilseed rape cover (OSR_cover), landscape diversity (landscape_div), neonicotinoid residues, and NNI metrics (median/peak, raw and corrected). Days of exposure and weight trajectories captured (R1–R8).
- osmia_sites.csv: Site-level data for Osmia bicornis, including similar fields as bombus_sites.csv, plus trap-nest counts, osmia larvae, total cells, pre-weight, post-exposure weights, OSR_cover, landscape_div, residue metrics, NNI metrics, and days of exposure (R1–R8) including pre-exposure weight.
- osmia_residue.csv: Residue data for Osmia bicornis within pollen/nectar used to provision larvae; includes TrapNest identifiers, total_rows, osmia_larvae, color-specific residues (TMX, CTD, IMI) in nectar and pollen, along with NNI values and color-specific residues. Indicates NA where data are not available.
- Metadata notes:
  - Data include ‘NA’ where data are not available.
  - Columns cover country, site, treatment, block, residue measurements by compound and sample type, and derived metrics (e.g., NNI, days of exposure, weights).

## Data processing, quality, and provenance
- Funding and provenance:
  - Conducted in 2015 under CEH National Capability funding (Project NEC05829).
  - Experimental platform funded by Syngenta Ltd. and Bayer CropScience.
- Quality and standardisation:
  - Use of standardised field design and sampling across three countries to ensure comparability.
  - Residue analyses performed with validated LC-MS/MS methods; LD50-based toxicity weighting for cross-species exposure metrics.
- Data handling for monitoring purposes:
  - Outputs are prepared for clear interpretation (counts, weights, residue levels, landscape context) and stored for integration into monitoring portals.
  - Emphasis on enabling broader reuse and cross-study comparability.

## Implications for environmental monitoring and analysis
- Provides a consistent, multi-country dataset linking agricultural seed treatments to pollinator population responses and residues in forage.
- Enables integrated analyses combining biological endpoints with chemical exposure and landscape context.
- Demonstrates approaches to standardise data collection, processing, and metadata to support transparency and policy evaluation.
- Highlights data access considerations and opportunities to couple these data with additional environmental datasets for broader monitoring value.