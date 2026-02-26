# Amazon Fertilization Experiment (AFEX)

- Study area: AFEX is conducted inside the Biological Dynamics of Forest Fragments Project (BDFFP) in the KM41 reserve, near Manaus (~100 km away) along BR-174. Key geographic and environmental context:
  - Humid, wet climate; average temperature ~26.7°C; annual rainfall ~2200 mm; wet (July–Sept) and peak rainfall in March–April.
  - Vegetation: dense Terra Firme rainforest; canopy 30–37 m on average (emergents up to ~55 m).
  - Soils: red-yellow podzols (clayey) and yellow latosols; highly weathered, acidic, low fertility; WRB classification ferrasols.
  - Location reference: KM41 reserve (yellow on Figure 1).

- Experimental design (AFEX 2.0 and overall design):
  - Treatments: full factorial with seven nutrient treatments plus a control, total of 8 treatment combinations.
  - Nutrients applied: N (125 kg N ha-1 year-1 as urea), P (50 kg P ha-1 year-1 as triple superphosphate), and cations (K 50 kg K ha-1 year-1 as KCl; Ca 160 kg Ca ha-1 year-1; Mg 160 kg Mg ha-1 year-1 as dolomitic limestone).
  - Plot structure: 32 plots organized into four independent blocks; plots are 50 x 50 m, with each block containing replicated plots at least 250 m apart; plots are spaced at least 100 m from one another.
  - Replication: four replicates per treatment combination.
  - Fertilization schedule: annual applications in three increments to mitigate leaching/runoff.

- Plot and delineation details:
  - AFEX 2.0 plot delineation includes a layout of fertilized blocks and plots within the KM41 reserve (plot location maps referenced).

- Seedling sampling framework:
  - Sub-plot layout: within each 50 x 50 m plot, four 1 x 1 m sub-plots are embedded inside a 30 x 30 m core area, resulting in 16 sub-plots per treatment and 128 sub-plots in total.
  - Tree/seedling selection: within each sub-plot, all individuals >20 cm tall and with diameter at ground height (DGH) < 1 cm are identified and tagged (palm and lianas excluded).
  - Leaf-level monitoring: for each tagged seedling, the closest 10 mature leaves are marked and monitored bi-monthly to assess herbivory at the leaf level.
  - Herbivory and damage measurements: leaf-area loss from herbivory is estimated (percentage), following a standardized grid/sector approach to improve accuracy; additional data on galls, pathogens, and leaf miners are recorded as presence/absence (qualitative).
  - Sampling frequency: six campaigns per sub-plot over 12 months, with six campaigns total per sub-plot (four in the rainy season, two in the dry season).

- Data spreadsheet – seedlings_herbivory.csv:
  - Structure: 27,510 rows and 14 columns.
  - Columns and meanings:
    - A CENSUS: Sampling number
    - B MONTH: Month of sampling
    - C DATE: Sampling day
    - D TRT: Plot treatment (per AFEX design)
    - E BLOCK: Block (1–4)
    - F PLOT: Plot (1–8)
    - G SUBPLOT: Sub-plot number (1–4)
    - H INDIVIDUAL: Seedling individual tag
    - I LEAF: Leaf tag
    - J HERBIVORY: Leaf-area loss due to herbivory (percent)
    - K GAIL: Gall presence (1) or absence (0)
    - L FUNGUS: Fungus presence (1) or absence (0)
    - M LEAF_MINERS: Leaf miners presence (1) or absence (0)
    - N MORTALITY: Leaf death (1) or survival (0)

- Temporal and data-management notes:
  - Data were collected across six sampling campaigns per sub-plot, with a seasonal balance (rainy vs dry).
  - The dataset integrates spatial design (blocks, plots, sub-plots) with plant-level and leaf-level measurements, enabling spatially explicit analyses of fertilization effects, herbivory, and associated biotic damage.

- References (supporting context and methods):
  - Soil and habitat references (e.g., Chauvel 1982; Quesada et al. 2010, 2011; RADAMBRASIL 1978).
  - Methodological references for herbivory quantification and sampling (Johnson et al. 2016; Comita et al. 2007).
  - Forest and soil relationships in Amazonia (Lovejoy & Bierregaard 1990; Laurance et al. 1999).