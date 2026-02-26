# Experimental design

- Context and design
  - Large tree diversity experiment in SW France (ORPHEE), planted in 2008.
  - Location: 8 blocks covering 12 ha, with five native tree species (Quercus robur, Quercus pyrenaica, Quercus ilex, Betula pendula, Pinus pinaster).
  - Experimental layout: fully factorial design for tree species richness, spanning monocultures to five-species mixtures; each block contains 32 treatment plots randomly distributed; each treatment replicated once per block, plus an additional replication of the five-species mixture.
  - Plot structure: 100 trees per plot (10 rows × 10 trees) at 2 m spacing; systematic alternate species planting to ensure local mixing.

- Irrigation treatment
  - Since 2015, half the blocks receive irrigation (May–October) to alleviate summer drought.
  - Irrigation adds approximately 3 mm precipitation per night per plot, using a central 2.30 m pole.
  - Previously shown to increase soil/plant water content and predawn water potential.

- Treatments and focal focus
  - Focused on broadleaved hosts by surveying Q. robur in all mixtures except those containing pine.
  - Treatment gradient (8 realizations per block): Qr monoculture; three 2-species mixtures with Qr; three 3-species mixtures with Qr; one 4-species mix (three oaks + birch).
  - Apparency concept: focal oak height relative to surrounding trees, driven by birch presence; allows comparison of plots with identical richness but different oak apparency.

- Data collection protocol
  - Blocks surveyed: blocks 1–6 (3 irrigated, 3 non-irrigated).
  - In each plot: randomly select four Q. robur trees for damage assessment.
  - Measurements per tree:
    - Insect herbivory on primary shoots; powdery mildew on lammas shoots.
    - Shoot sampling: eight shoots per tree; for each shoot, five leaves examined; record mines per leaf; sum to shoot or tree level.
    - Damage classification: leaf chewers and skeletonisers combined into seven classes (0–6) per leaf; for mildew, five classes (0–4) per lammas shoot.
    - Five leaves per lammas shoot assessed for mildew; averages calculated at shoot (5 leaves) and tree (40 leaves) levels using class medians.
    - Additional covariates: length of primary and lammas shoots (mm) and tree height (cm).
  - Outputs are calculated as:
    - MeanChewerTree (average leaf-chewer damage per tree)
    - MeanDefolTree (average total defoliation by chewers and miners)
    - SumMinersTree (sum of miner abundance across leaves)
    - MeanMildewTree (average mildew infection per tree)
    - MeanPShootLength, MeanLShootLength (mean shoot lengths)

- Quality control
  - Data entered manually into Excel from field datasheets.
  - Visual checks for outliers and missing values; additional validation with df_status() in R to identify NAs.

- Data structure and recorded values
  - Key columns in the data frame:
    - Tree.ID: unique identifier for each tree (coordinate-based within ORPHEE plan)
    - Date.Surveyed: survey date (day/month/year)
    - Block: experimental block (nested within site)
    - Plot: plot within block (nested within site)
    - Irrigation: yes/no for block-level irrigation
    - Plot.Composition: coded species composition (Qr, Qp, Qi, Bp)
    - Resource.Dilution: proportion of non-Q. robur species (0–0.75)
    - Richness: number of tree species in plot (1–5)
    - PA.Birch: birch present (Y) or absent (N)
    - MeanChewerTree, MeanDefolTree, SumMinersTree, MeanMildewTree: infestation/defoliation metrics
    - MeanPShootLength, MeanLShootLength: mean primary and lammas shoot lengths (mm)
    - H.2018: Q. robur height measured in 2018 (cm)

- Data interpretation and units
  - Leaf damage classes are ordinal; results summarized as means at tree level.
  - Shoot lengths in millimeters; tree height in centimeters.
  - Plot composition uses species codes: Qr (Quercus robur), Qp (Q. pyrenaica), Qi (Q. ilex), Bp (Betula pendula).
  - Resource.Dilution reflects proportion of non-Q. robur species in a plot (0–0.75).

- References for context
  - Bert et al. (2016) on powdery mildew and oak growth.
  - Castagneyrol et al. (2017, 2013, 2018) on diversity effects on herbivory, apparency, and drought interactions.