# Experimental design

- Purpose and scope
  - Large-scale tree diversity experiment (ORPHEE) in SW France to study effects of species richness and composition on plant-insect interactions and disease.
  - Data governance context: design includes standardized treatments, structured blocks, and detailed measurements suitable for sharing, re-use, and meta-analyses across sites.

- Study design and treatments
  - Location and timeline: planted in 2008; eight experimental blocks over 12 hectares.
  - Species: five native tree species (Quercus robur, Quercus pyrenaica, Quercus ilex, Betula pendula, Pinus pinaster).
  - Design: fully factorial richness gradient from monocultures to five-species mixtures.
  - Replication: each treatment per block replicated once, plus an extra replication of the five-species mixture; 32 treatment plots per block.
  - Plot layout: each plot contains 100 trees (10 rows × 10 trees) spaced 2 m apart; trees planted in a systematic alternating pattern.
  - Irrigation: since 2015, half of the blocks receive an irrigation treatment (May–October) at ~3 mm per night per plot; irrigation affects soil and plant water status.

- Focus and diversity gradient
  - Focal host: Quercus robur examined in all mixtures except those containing pine, to emphasize broadleaved species.
  - Treatments sampled: monoculture of Q. robur; three two-species mixes with Q. robur; three three-species mixes with Q. robur; a four-species mix (three oaks + birch).
  - Apparency concept: relative height of focal oaks compared to surrounding trees; birch presence increases apparent height, influencing herbivory patterns.

- Survey sampling design
  - Blocks surveyed: 1–6 (3 irrigated, 3 non-irrigated).
  - Within each plot: four randomly selected Q. robur trees for damage assessment.

- Data collection: measurements and indicators
  - Damage assessment: insect herbivory on primary shoots; powdery mildew infection on lammas shoots.
  - Shoot sampling: eight shoots per tree (covering various heights/angles); primary shoots (8 per tree) used for leaf sampling.
  - Leaf sampling and rating:
    - Chewers: five leaves per shoot; classify chewing damage into seven percentage classes (0 to >76%).
    - Mildew: five leaves on lammas shoots; mildew cover classified into five classes (0 to 4).
  - Aggregation: leaf-class values converted to median points and averaged to shoot level (5 leaves) and tree level (40 leaves).
  - Covariates: shoot length (mm) for primary and lammas shoots; tree height (cm) measured in 2018.
  - Summary tree metrics:
    - MeanChewerTree: average percent chewing damage per tree.
    - MeanDefolTree: average defoliation from chewing and mildew per tree.
    - SumMinersTree: total abundance of mildew/leaf miners per tree.
    - MeanMildewTree: average mildew infection per tree.
    - MeanPShootLength, MeanLShootLength: mean primary and lammas shoot lengths per tree.
    - H.2018: height of Q. robur tree (cm) recorded in 2018.

- Data structure and coding
  - Key fields:
    - Tree.ID: unique identifier, plotted on a site-specific coordinate grid.
    - Date.Surveyed: survey date (day/month/year).
    - Block: experimental block (nested within site).
    - Plot: plot identifier (nested within block/site).
    - Irrigation: Y/N at block level.
    - Plot.Composition: species composition with codes (Qr, Qp, Qi, Bp).
    - Resource.Dilution: proportion of non-Q. robur species in plot (0–0.75).
    - Richness: number of species planted in the plot.
    - PA.Birch: presence/absence of birch in plot (Y/N).
    - MeanChewerTree, MeanDefolTree, SumMinersTree, MeanMildewTree: per-tree aggregated metrics.
    - MeanPShootLength, MeanLShootLength: shoot length metrics.
    - H.2018: Q. robur height in 2018.
  - Units and data types:
    - Height: cm; shoot length: mm; leaf damage as percentage classes transformed to medians for analysis.
    - Lammas vs. primary shoots distinguished; NA values occur when lammas shoots were not present.
  - Data completeness: lammas shoot data may have NAs; some measurements require imputation or careful handling in analyses.

- Quality control and data quality
  - Data entry: manual transcription from datasheets into Excel.
  - Validation: visual inspection for outliers and missing values; missing values checked with R df_status() from the funModeling package.
  - Documentation: dataset structure and variable definitions provided to aid reproducibility and reuse.

- Metadata, provenance and references
  - Data provenance: detailed description of experimental design, sampling protocol, and measurement methods enabling traceability to field procedures.
  - References supporting methods and interpretation (citations provided for powdery mildew effects, plant apparency, and herbivory dynamics).

- Data management considerations for Data Stewards
  - Ensure consistent coding for Plot.Composition and Resource.Dilution across datasets.
  - Maintain clear data dictionary with variable definitions, units, and calculation methods for aggregated metrics (MeanChewerTree, MeanDefolTree, SumMinersTree, etc.).
  - Track data collection dates and blocks to support temporal analyses and updates.
  - Prepare for data sharing via portals by providing standardized formats (preferably CSV/structured tabular formats in addition to Excel) and versioned releases.
  - Preserve provenance by linking data records to experimental blocks, plots, and tree IDs; maintain a log of any data corrections or re-encodings.

- Potential uses and downstream value
  - Enables cross-study comparisons of tree diversity effects on herbivory and disease.
  - Supports investigations into apparent-tree effects (apparency) and the role of birch co-options.
  - Facilitates meta-analyses on tree species interactions, irrigation effects, and long-term plant-insect dynamics.

- References
  - Bert et al. (2016); Castagneyrol et al. (2017, 2013, 2018) – sources for methodological and ecological context related to herbivory, apparency, drought, and plant-insect interactions.