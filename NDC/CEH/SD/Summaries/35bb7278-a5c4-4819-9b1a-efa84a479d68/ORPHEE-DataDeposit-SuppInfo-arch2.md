# Experimental design

- Study site and design
  - Large tree diversity experiment in SW France (ORPHEE), planted in 2008.
  - Randomised blocked design with eight blocks covering 12 hectares.
  - Five native tree species: Quercus robur, Quercus pyrenaica, Quercus ilex, Betula pendula, Pinus pinaster.
  - Fully factorial design for tree species richness spanning monocultures to five-species mixtures; 32 treatment plots per block (eight blocks × 32 treatments).
  - Each treatment replicated once per block, plus an extra replication of the five-species mixture, totaling 32 plots per block.
  - Plot structure: 10 rows × 10 trees per plot (100 trees), planted at 2 m spacing; systematic alternating pattern to mix species.

- Irrigation treatment
  - Since 2015, half the blocks receive irrigation (May–October) while the other half rely on rainfall.
  - Irrigation: 3 mm per night per experimental plot from a central pole.
  - Prior work showed irrigation increases soil/plant water content and predawn water potential; irrigation effect not repeated in detail here.

- Focal sampling and diversity gradient
  - Plots surveyed along a tree diversity gradient, focusing on Quercus robur as the focal host in all mixtures except those containing pine.
  - Treatment spectrum: Q. robur monoculture; three 2-species mixes with Q. robur; three 3-species mixes with Q. robur; one 4-species mix (three oaks + birch).
  - Apparency defined as the height of focal oaks relative to the mean height of surrounding trees; birch presence affects apparent oak height.
  - Blocks 1–6 surveyed (3 irrigated, 3 non-irrigated); within each plot, four Q. robur trees randomly selected for damage assessment.

- Data collection and measurements
  - Responses recorded: insect herbivory on primary shoots and powdery mildew on lammas shoots (distinguished by ring scar).
  - Sampling per tree: eight shoots (primary and lammas) at various heights/angles; eight leaves per primary shoot (five leaves per shoot analyzed for mines).
  - Damage assessment:
    - Chewers (leaf miners included in this group): seven damage classes per leaf (0, 1:1–5%, 2:6–15%, 3:16–25%, 4:26–50%, 5:51–75%, 6: >76%).
    - Mildew: five classes per lammas shoot (0, 1:1–25%, 2:26–50%, 3:51–75%, 4:76–100%).
  - Data processing: average damage at shoot and tree level using the median of the damage classes.
  - Covariates: length of primary and lammas shoots (mm) and tree height (cm); 2018 height of Q. robur recorded as H.2018.

- Data structure and recorded variables
  - Tree.ID: unique per ORPHEE plotting plan.
  - Date.Surveyed: survey date.
  - Block: experimental block (nested within site).
  - Plot: plot within block/site.
  - Irrigation: Y/N (block-level).
  - Plot.Composition: species planted in the plot (codes: Qr, Qp, Qi, Bp).
  - Resource.Dilution: proportion of non-Q. robur species in a plot (0–0.75).
  - Richness: number of tree species in a plot.
  - PA.Birch: birch presence (Y/N) in the plot.
  - MeanChewerTree: average leaf chewer damage per tree (percent).
  - MeanDefolTree: average total defoliation by chewers and miners per tree (percent).
  - SumMinersTree: total miner abundance per tree.
  - MeanMildewTree: average oak mildew infection per tree (percent).
  - MeanPShootLength: mean primary shoot length per tree (mm).
  - MeanLShootLength: mean lammas shoot length per tree (mm); NA if no lammas shoots observed.
  - H.2018: height of Q. robur in 2018 (cm).

- Quality control and data processing
  - Data entered manually from datasheets into Excel.
  - Visual checks for outliers and missing values.
  - Additional quality check using df_status() from the R package funModeling to identify missing values.

- Analytical relevance and potential uses
  - Enables assessment of how tree species richness, plot composition, and oak apparency influence herbivory and mildew.
  - Facilitates comparisons across irrigation regimes and gradients of diversity.
  - Provides a structured, replicate-rich dataset suitable for multilevel analyses (plot, block, tree level) of plant-insect-pathogen interactions in a controlled experimental context.

- References
  - Bert et al. (2016). Powdery mildew and oak growth.
  - Castagneyrol et al. (2017). Bottom-up/top-down effects of tree diversity on leaf herbivory.
  - Castagneyrol et al. (2013). Plant apparency and associational resistance.
  - Castagneyrol et al. (2018). Interactions of drought and tree neighbors on herbivory.