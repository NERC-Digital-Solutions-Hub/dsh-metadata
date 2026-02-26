# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme]

- Overview
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) studying soil biota diversity and biogeochemical functions in a long-term field experiment at Sourhope, Scotland.
  - Focus: effects of sewage sludge and lime amendments on bacterial community structure and key soil processes in upland grassland soils.

- Study design and context
  - Location: Sourhope Research Station, Cheviot Hills, Southern Scotland; soil type: acidic brown forest soils.
  - Experimental setup: randomized block design with three replicates across four treatments – untreated (control), lime only, sludge only, sludge with lime.
  - Treatments applied: lime (600 g m-2) over two years; sewage sludge applied in 1999 and 2000; lime and sludge applied in combination for one treatment.
  - Sampling strategy: soil cores collected throughout spring and summer of 1999–2000; in 1999 most activity occurred in the root zone, so 2000 sampling focused on the root zone.
  - Time points for sludge-treated plots: 1, 3, 16, 30, and 58 days after sludge application in May 2000.

- Measurements and analyses
  - Soil chemistry and physical properties: pH (1:2 soil-water), moisture, total carbon, total organic carbon, total Kjeldahl nitrogen, soil NH3; baseline weather and vegetation data also tracked.
  - Soil process measurements: basal respiration (CO2 production) and autotrophic nitrification potentials (NO2- production) under specific conditions.
  - Molecular analyses: TTGE (temporal temperature gradient electrophoresis) of:
    - Eubacterial 16S rDNA fragments to monitor broad bacterial community changes.
    - Ammonia-oxidizer 16S rDNA fragments to assess specific functional groups.
  - Data processing and analysis: 
    - DNA extraction and TTGE gel electrophoresis with standardized conditions.
    - Band pattern analysis to compute Sorensen similarity coefficients; cluster analysis using UPGMA.
    - Statistical testing via two-factor (time and treatment) ANOVA on replicates; exploratory multivariate methods not emphasized due to experimental design.

- Datasets and data structure
  - Dataset 1034: Soil analysis data (2000) – includes soil characteristics (pH, moisture, TOC, NH3, TKN) and soil process metrics (basal respiration, nitrification potential) with associated sample metadata.
  - Dataset 1035: Soil analysis data – Bulk Sampling Details (sampling unit identifiers and sampling coordinates such as BLOCK, MAIN_PLOT, SUB_PLOT, etc.).
  - Dataset 1124: Numerical analysis of eubacterial community profiles (TTGE) – TTGE band patterns across treatments and times.
  - Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (TTGE) – TTGE patterns for ammonia-oxidizer communities.
  - Dataset 1126: Numerical analysis of ammonia oxidizer community profiles for sludge-only treatment.
  - Dataset 1127: Numerical analysis of ammonia oxidizer community profiles for untreated soil only.
  - Each TTGE-related dataset includes sample identifiers, block/main-plot/sub-plot information, treatment, horizon, days after sludge, and band-related measurements (band numbers, relative intensities) as appropriate.
  - Data structure notes: comprehensive metadata accompany each dataset, including sampling dates, plot design references, soil status, and measurement units.

- Quality assurance and governance
  - Verification steps: numeric range checks, formatting checks, and logical integrity checks to ensure data consistency.
  - Limitations: datasets subject to quality assurance but not guaranteed by NERC; no liability for accuracy or fitness for a given use.
  - Data sharing and provenance: contextual information and references provided; some baseline data and handbooks available via the Environmental Information Centre (EIDC) catalogue.
  - Documentation and references: extensive methodological references and related publications listed to support reuse and interpretation.

- Reuse notes for monitoring framers
  - Demonstrates end-to-end monitoring workflow: from experimental design and field Sampling to chemical/biological measurements, TTGE-based community profiling, and robust statistical analysis.
  - Highlights data governance challenges and practical solutions for environmental data sharing:
    - Importance of rich metadata (sampling units, plot geometry, treatment, horizon, timing).
    - Need for standardised data formats and clear documentation to enable cross-study reuse.
    - Potential metadata barriers (public sharing requirements, data transformation needs, and provision of raw vs. processed outputs).
  - Useful references and linked data products (e.g., field data handbook and related ecological studies) to aid interpretation and cross-study comparisons.

- References and further reading
  - Methodological and background references for soil analyses, TTGE, and related microbial ecology studies are provided, including data-handbook and foundational TTGE and sequencing methods.
  - Key associated publications: studies on sludge amendment effects on gas dynamics and microbial community structure in upland soils, and rapid co-extraction methods for DNA/RNA from natural environments.