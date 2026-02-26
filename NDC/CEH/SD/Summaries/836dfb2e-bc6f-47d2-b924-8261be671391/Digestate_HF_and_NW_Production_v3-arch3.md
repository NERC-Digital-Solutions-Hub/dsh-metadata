# Digestate_HF_and_NW_Production.csv

## Overview
- Dataset from a 2017 wheat trial comparing digestate amendments and mineral nitrogen across two sites: Henfaes (HF) and North Wyke (NW).
- Contains 90 rows and 7 columns, focusing on yield-related measures under different fertilizer treatments.
- Aimed at informing monitoring and evaluation of agricultural nutrient management strategies, including digestate use.

## Data structure and content
- Columns (with explanations and units):
  - Site: HF or NW.
  - Plot: Experimental plot number.
  - Block: Blocking factor in a randomized block design (1–5).
  - Treatment: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP), N-75, N-150, N-225, N-300 (mineral NH4NO3 at specified rates).
  - Plant_yield: Whole plant yield at 100% dry matter, in tonnes per hectare (t ha^-1).
  - Grain_yield: Grain yield at 100% dry matter, in t ha^-1.
  - TGW: Thousand grain weight at 100% dry matter, in grams.
- All yield data reported at 100% dry matter; NA indicates not assessed.
- Dataset includes two sites (HF and NW), multiple plots per site, and a mix of digestate treatments and mineral N benchmarks.

## Experimental design
- Randomised block design with 5 blocks per site.
- Plot sizes differ by site and treatment category:
  - HF: 1.2 m × 6.5 m (harvest area) for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: 2 m × 4.5 m (harvest area) for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI.

## Treatments and variables
- Treatments compare digestate forms and processing (digestate, acidified digestate) with and without nitrification inhibitors, alongside mineral N fertiliser at multiple rates.
- Primary response variables are plant yield, grain yield, and TGW, enabling assessment of productivity and grain characteristics under different nutrient sources.

## Data quality and metadata considerations
- The dataset is accompanied by metadata detailing column headers, explanations, and units.
- Potential data governance considerations for monitoring applications:
  - Public sharing of underlying data may be a barrier in some contexts.
  - Metadata gaps or inconsistencies can hinder reuse; clarity on measurement methods and timing is essential.
  - Data governance, quality assurance, and data transformation steps are important for integration into monitoring frameworks.

## Relevance for monitoring frameworks
- Provides a concrete, site-comparative dataset to evaluate the performance of digestate-based nutrient strategies versus mineral N in wheat production.
- Supports assessments of nutrient use efficiency, yield outcomes, and grain quality under different fertilizer regimes.
- Useful for developing evidence-based monitoring measures related to environmental health implications of manure-based fertilisers and nitrification inhibitors.
- Highlights data management considerations (metadata completeness, data sharing, and governance) crucial for scalable monitoring programs.