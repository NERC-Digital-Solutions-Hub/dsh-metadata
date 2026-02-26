# Experimental design

- Location and design
  - Large tree diversity experiment in SW France (ORPHEE), planted in 2008 (44°44′ N, 00°46′ W)
  - Randomised blocked design with eight blocks covering 12 ha
  - Eight blocks established with five native tree species: three oaks (Quercus robur, Quercus pyrenaica, Quercus ilex), one other broadleaved species (silver birch, Betula pendula), and one conifer (Pinus pinaster)
  - Fully factorial design for tree species richness, spanning monocultures to five-species mixtures; 32 treatment plots per block
  - Each treatment replicated once per block, plus an extra replication of the five-species mixture; plots randomly distributed within blocks
  - Each plot: 10 rows of 10 trees at 2 m spacing (100 trees per plot)

- Irrigation treatment
  - Since 2015, annual irrigation at block level for half of the blocks (May–October)
  - Irrigation: sprinkling the equivalent of 3 mm precipitation per night per plot from a central pole
  - Previous work shows irrigation increases plant/soil water content and summer predawn water potential

- Sampling focus and treatments used
  - Surveyed plots along a tree diversity gradient, focusing on Quercus robur as focal host in all mixtures except those with pine
  - Treatments surveyed: Q. robur monoculture; three 2-species mixes with Q. robur; three 3-species mixes with Q. robur; one 4-species mix (three oaks and birch)
  - Gradient designed around oak apparency: height of focal oaks relative to surrounding trees; apparency driven by birch proportion

- Sampling design and timing
  - Blocks 1–6 surveyed (3 irrigated, 3 non-irrigated)
  - Within each plot, four Q. robur trees randomly selected for damage assessment

- Data collected per tree
  - Insect herbivory on primary shoots and powdery mildew on lammas shoots
  - Shoots: eight per tree; both primary and lammas shoot types considered
  - Leaves: five leaves per primary shoot; mines counted per leaf and summed at shoot or tree level
  - Damage classification: chewing/skeletonising combined into seven leaf-level classes (0 to >76%)
  - Powdery mildew: five lammas-shoot leaves per shoot; mildew cover classified into five classes (0 to 76–100%)
  - Averages: mean leaf-level damage and mean tree-level damage using medians of class points
  - Additional covariates: length of primary and lammas shoots; tree height

- Data quality and workflow
  - Data entered manually into Excel from datasheets
  - Visual checks for outliers/missing values; df_status() from R’s funModeling used to assess missing values

- Data structure and recorded variables (columns)
  - Tree.ID: unique tree identifier within the ORPHEE plan
  - Date.Surveyed: survey date (day/month/year)
  - Block: experimental block (nested within site)
  - Plot: plot within block (nested within site)
  - Irrigation: irrigation treatment (Y/N)
  - Plot.Composition: species planted in the plot; species codes: Qr (Quercus robur), Qp (Q. pyrenaica), Qi (Q. ilex), Bp (Betula pendula)
  - Resource.Dilution: proportion of non-Q. robur species in the plot (0–0.75)
  - Richness: number of tree species planted in the plot
  - PA.Birch: birch presence (Y) or absence (N)
  - MeanChewerTree: average percentage leaf-chewer damage per tree
  - MeanDefolTree: average defoliation by chewers/miners per tree
  - SumMinersTree: total miner abundance per tree
  - MeanMildewTree: average powdery mildew infection per tree
  - MeanPShootLength: mean primary shoot length (mm) per tree
  - MeanLShootLength: mean lammas shoot length (mm) per tree
  - H.2018: Quercus robur height measured in 2018 (cm)

- References for methodology and context
  - Bert et al. 2016: powdery mildew impacts on oak growth
  - Castagneyrol et al. 2017, 2013, 2018: diversity effects on herbivory, plant apparency, and drought interactions