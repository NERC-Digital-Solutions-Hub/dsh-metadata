# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme]

## Overview and aims
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biota diversity and functional roles in key ecological processes.
- Studies the effects of soil improvement treatments (sewage sludge and lime) on bacterial community structure and soil process activities in upland grassland.
- Addresses whether treatment-induced changes in bacterial populations align with functional (biogeochemical) outcomes, and how community structure relates to process activity.

## Study design and data collection
- Location: Sourhope Research Station, Cheviot Hills, Southern Scotland; acidic brown forest soils.
- Experimental design: randomised block with three replicates and four treatments — untreated (control), lime only, sludge only, sludge followed by lime.
- Treatments and timing: lime applied in 1999–2000; sewage sludge applied in 1999 and 2000; soil sampling focused on the root zone in 2000 (after sludge application).
- Sampling schedule: samples collected days 1, 3, 16, 30, and 58 after sludge application (May 30, 2000).
- Analyses performed on samples: soil characteristics (pH, moisture, total carbon, total organic carbon, total Kjeldahl nitrogen, NH3), basal respiration, nitrification potential; molecular analyses of microbial communities (TTGE-based profiling of eubacteria and ammonia-oxidizing bacteria).

## Data collected and methods
- Soil process analyses: basal respiration via CO2 evolution; autotrophic nitrification potential via nitrite production in chlorate-treated slurries; standard methods referenced for chemical metrics.
- Molecular analyses: TTGE of PCR-amplified 16S rDNA (eubacterial) and ammonia-oxidizer (AOB) fragments; data collected as band patterns over TTGE gels.
- Data processing: extraction of DNA/RNA, TTGE gel analysis, band-intensity and position assessment, similarity coefficients (weighted Sorensen), cluster analysis (UPGMA), and time/treatment ANOVA on replicates.
- Documentation and metadata: detailed lab procedures, gel conditions, and data processing steps described; references to methodological standards and related studies provided.

## Datasets included (P2116)
- Dataset 1034: Soil analysis data (2000)
  - Variables include: SampleID, BLOCK, MAIN_PLOT, SUB_PLOT, pH, SM (soil moisture), TOC, TKN, RES (soil respiration), AM_OX (ammonia oxidation potential), NIT_RED (nitrification-related), METH_GEN (methane generation), METH_OX (methane oxidation), etc.
  - Measurements taken May–Aug 2000; analyses conducted at University of Newcastle.
- Dataset 1035: Soil analysis data — Bulk Sampling Details (P2116_SOIL_ANALYSIS_SAMPINFO.csv)
  - Metadata for sampling units: SUID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SOIL_HORIZON, TIME_AFTER_SLUDGE, SAMPLE_TYPE, etc.
- Dataset 1124: Numerical analysis of eubacterial community profiles (P2116_EUBACTERIAL_CP.csv)
  - TTGE-based community profiles for eubacteria across treatments/timepoints; fields include SampleID, SUID, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT, HORIZON, DAYS_AFTER_SLUDGE, BANDS1–BANDS54 (band intensity data).
- Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (P2116_AMMONIA_OXIDISER_CP.csv)
  - TTGE-based profiles for ammonia-oxidizing communities; similar structure to 1124 with BANDS1–54 data and RELATIVE_INTENSITY metrics.
- Dataset 1126: Numerical analysis of ammonia oxidizer community profiles (TTGE) for sludge only (P2116_AMMONIA_SLUDGE.csv)
  - TTGE data for sludge-only treatment across timepoints; band data plus RELATIVE_INTENSITY and related fields.
- Dataset 1127: Numerical analysis of ammonia oxidizer community profiles (TTGE) for untreated soil only (P2116_AMMONIA_UNTREATED.csv)
  - TTGE data for untreated soil across timepoints; band data plus RELATIVE_INTENSITY and related fields.

## Data structure and key variables
- TTGE-based datasets (1124–1127): include hierarchical identifiers (BLOCK, MAIN_PLOT, SUB_PLOT), treatment and horizon info, days after sludge, and multi-band intensity data (BANDS1–BANDS54) with relative intensity measures.
- Soil analysis dataset (1034): includes core soil metrics (pH, moisture, TOC, TKN, NH3), respiration, nitrification, and gas-formation metrics (METH_GEN, METH_OX), with precise measurement units and data statuses.
- Sampling info dataset (1035): links samples to spatial-temporal coordinates (CELL_X/Y), sampling unit identifiers, and treatment metadata to enable linkage across TTGE and soil-chemistry datasets.

## Data quality, governance, and access
- Quality control: numeric range checks, format validation, and logical integrity checks performed.
- Limitations: data providers (NERC) do not warrant accuracy or fitness for a specific use; no liability for data use.
- Access and provenance: datasets referenced with links to related literature and the Environmental Information Centre (EIDC) catalogue for data access and supporting information.

## Practical implications for data leaders
- Asset management: multiple interlinked datasets (chemical, process, and TTGE-based microbial profiles) require coherent metadata and robust linkage keys (SampleID, SUID, BLOCK, MAIN_PLOT, SUB_PLOT).
- Discoverability and metadata completeness: datasets include detailed field definitions and sampling metadata; ensure consistent naming, data dictionaries, and versioning for reuse across projects.
- Data standards and interoperability: TTGE band data (BANDS1–BANDS54) and relative intensity metrics should be harmonized with other microbial community datasets for cross-study comparisons.
- Data governance and access: clear provenance, licensing, and disclaimers; data can support ecological/in biogeochemical modeling, microbial ecology studies, and evaluation of sludge amendments on soil function.
- Use cases: assess relationships between sludge-induced changes in bacterial community structure and soil processes (respiration, nitrification, methane dynamics); explore time-series dynamics across treatments; compare eubacterial versus ammonia-oxidizer community responses.

## References and related materials
- Methodological references (standard methods, TTGE analysis, DNA co-extraction methods) and related publications listed in the dataset documentation.
- Related data handbooks and additional context available via the EIDC catalogue and cited literature.