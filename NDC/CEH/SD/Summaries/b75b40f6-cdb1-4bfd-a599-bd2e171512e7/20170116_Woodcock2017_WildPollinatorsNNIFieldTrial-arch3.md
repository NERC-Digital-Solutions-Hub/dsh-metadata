# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes population responses of two wild pollinator model systems (Bombus terrestris and Osmia bicornis) to neonicotinoid seed treatments (clothianidin, thiamethoxam) applied to winter-sown oilseed rape.
- Countries involved: Hungary, Germany, and the UK; timeframe centered on 2015 flowering and post-exposure assessments.
- Data collected include colony/individual-level reproductive metrics, neonicotinoid residues in pollen and nectar, and landscape context around colonies.

## Study design and scope
- Experimental setup across 33 commercial oilseed rape sites (UK: 12; Hungary: 12; Germany: 9).
- Within-country block design: three seed treatments per block (clothianidin, thiamethoxam, and a fungicide-only control), with blocks separated by geography to minimize cross-site interference.
- Large cropping blocks per site (mean ~63 ha).
- Flowering period in 2015 (April–June) used to assess pollinator responses.

## Biological measures and sampling
- Bombus terrestris (UK audax, Hungary and Germany terrestris sub-species):
  - 12 commercial colonies per site grouped into four multi-hives; measurements based on multi-hive units.
  - Assessed reproductive success via colony metrics (developmental stages, queen/worker/drones, egg masses) and colony weight over time.
  - Neonicotinoid residues measured in stored hive products (pollen and nectar) from multi-hives; pollen baskets on returning workers also sampled.
- Osmia bicornis (solitary bees):
  - Release of 50 cocoons per site with artificial trap nests; post-flowering dissection to count reproductive cells.
  - Residue measurements in pollen and nectar associated with cells; some sites lacked pollen/nectar data if no cells were found.

## Chemical exposure and analysis
- Neonicotinoids measured: clothianidin, thiamethoxam, and imidacloprid in pollen and nectar.
- Analytical method: LC-MS/MS (double quadrupole mass spectrometry) with UKAS-accredited standards; dedicated protocol referenced for residue analysis.
- Limits: LoQ ~0.53 ng/g; LoD ~0.38 ng/g; non-detects imputed as half LoD.
- Exposure metrics:
  - Site-level median and maximum residue concentrations for each neonicotinoid.
  - A combined Neonicotinoid Exposure Index (NNI) calculated using a weighted sum based on relative acute oral LD50 values to reflect overall toxicity risk across the three compounds.
  - Both raw (median/peak) and corrected (LD50-based) NNIs provided.

## Landscape and habitat context
- Within 1.5 km of colony locations, land-use parcels categorized into crops, grassland, woodland, scrub, water, urban, etc.
- Landscape diversity quantified using Shannon-Weiner index to capture habitat heterogeneity around colonies.

## Datasets and metadata
- bombus_sites.csv: Site-level Bombus terrestris population responses (medians across multi-hives), landscape context, and neonicotinoid residues in nests.
- osmia_sites.csv: Site-level Osmia bicornis population responses, landscape context, and neonicotinoid residues in nests.
- osmia_residue.csv: Detailed residues within Osmia reproductive cells, including per-color pollen/nectar residues and various aggregated exposure metrics.
- Metadata schemas: Comprehensive description of site, treatment, block, residue measures (per neonicotinoid and combined metrics), exposure days, colony weight data, and landscape variables (OSR cover, landscape_div).
- Residue-related variables include medians, peaks, and several NNI iterations (raw and LD50-corrected) for both Bombus and Osmia datasets.

## Data quality, governance, and notes
- Data collection funded by CEH (NERC NEC05829) with platform support from industry partners; data quality emphasizes QA, cleaning, and transparent reporting of methods.
- Metadata indicate data availability challenges such as incomplete pollen/nectar sampling at some sites and the need to transform data for interoperability.
- All datasets include explicit handling of non-detects (half LoD) and standardized units (ng/g for residues, counts for colony metrics, percentages for habitat cover).

## Relevance for monitoring, evaluation, and decision-making
- Provides a structured, multi-country, field-scale dataset linking neonicotinoid seed treatments to measurable outcomes in wild bee populations and their exposure pathways.
- Combines biological endpoints (colony and reproductive metrics) with chemical exposure data and landscape context, enabling integrated monitoring and weight-of-evidence assessments.
- Includes explicit data governance considerations (data sharing, metadata completeness, and transformation requirements) useful for policy-relevant monitoring frameworks.
- Supports evidence-informed risk assessment and decision-making regarding neonicotinoid use and pollinator protection, contributing to policy evaluation and future monitoring design.