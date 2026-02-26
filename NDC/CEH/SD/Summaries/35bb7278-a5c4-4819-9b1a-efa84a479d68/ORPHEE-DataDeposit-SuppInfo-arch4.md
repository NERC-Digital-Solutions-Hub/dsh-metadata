# Experimental design

- Study site and design
  - Large tree diversity experiment located in SW France (ORPHEE), planted in 2008 at 44°44'0"N, 0°46'0"W.
  - Randomised blocked design: 8 blocks, each with 32 treatments (fully factorial for tree species richness).
  - Species: Quercus robur, Quercus pyrenaica, Quercus ilex, Betula pendula (birch), Pinus pinaster (maritime pine).
  - Each block contains 32 plots arranged randomly within the block; plots consist of 10 rows of 10 trees (100 trees per plot) at 2 m spacing.
  - Irrigation treatment applied at block level from May–October to half of the blocks (3 mm per night per plot); irrigation increases soil and plant water content and predawn water potential.

- Treatments and sampling design
  - Focus on broadleaved species; focal host Q. robur surveyed in all mixtures except those with pine.
  - Treatments span oak apparency gradient: 
    - Q. robur monoculture
    - Three 2-species mixes with Q. robur
    - Three 3-species mixes with Q. robur
    - One 4-species mix of the three oak species and birch
  - Apparency defined as focal oak height relative to mean height of surrounding trees; birch taller than oaks, shaping apparency.
  - Surveyed blocks 1–6 (3 irrigated, 3 non-irrigated); within each plot, four Q. robur trees were randomly selected for damage assessment.

- Data collection and measurements
  - Variables recorded per tree:
    - Insect herbivory on primary shoots; powdery mildew infection on lammas shoots.
    - Shoot selection: eight shoots per tree; five leaves per primary shoot; record mines per leaf; sums calculated at shoot and tree level.
    - Damage classification: leaf chewers and skeletonisers grouped into seven leaf damage classes (0–6).
    - Mildew: five leaves on each lammas shoot; mildew infection classified into five classes (0–4).
    - Calculations: median class values used to compute mean chewer damage (MeanChewerTree), mean defoliation by chewers and miners (MeanDefolTree), and mean mildew infection (MeanMildewTree).
    - Additional covariates: length of primary and lammas shoots (mm) and tree height.
  - Data alignment and structure:
    - Date of survey; Block; Plot; Irrigation status; Plot composition (species codes: Qr, Qp, Qi, Bp); Resource.Dilution (proportion of non-Q. robur species, 0–0.75); Richness (number of species in plot); PA.Birch (present/absent).
    - Height data: H.2018 (height of Q. robur in cm) recorded in 2018.
  - File structure and units:
    - Tree.ID: unique coordinate-based identifier.
    - Measurements mainly recorded as percentages (chewers, mildew) or lengths (shoot length, height in cm).

- Data quality control and validation
  - Data entered manually into Excel from datasheets.
  - Visual checks for outliers and missing values; additional validation using df_status() from the R package funModeling.

- Data structure and key variables (summary)
  - Tree.ID, Date.Surveyed, Block, Plot, Irrigation, Plot.Composition, Resource.Dilution, Richness, PA.Birch
  - MeanChewerTree, MeanDefolTree, SumMinersTree, MeanMildewTree
  - MeanPShootLength, MeanLShootLength
  - H.2018 (Q. robur height)

- References
  - Bert et al. (2016) on powdery mildew and oak growth.
  - Castagneyrol et al. (2017, 2013, 2018) on plant diversity, apparency, and drought effects on herbivory and defenses.