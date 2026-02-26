# Seedlings_growth.csv

- Study area and environmental context
  - Location: Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
  - Climate and vegetation: humid/wet climate, mean temperature 26.7°C, annual precipitation ~2200 mm, dry season July–September; dense Terra Firme rainforest; canopy 30–37 m (emergents up to 55 m).
  - Soils: clayey red-yellow podzols with high weathering, acidity, and low nutrient fertility; WRB designation geric ferrasols.

- Amazon Fertilization Experiment (AFEX)
  - Design: full factorial experiment with seven treatments plus control, four replicates per treatment (total 32 plots), organized in four independent blocks at least 250 m apart.
  - Treatments: Control; N (125 kg N ha-1 yr-1 as urea); P (50 kg P ha-1 yr-1 as triple superphosphate); CATIONS (50 kg K ha-1 yr-1 as KCl; 160 kg Ca ha-1 yr-1; 160 kg Mg ha-1 yr-1 as dolomitic limestone); all combinations N+P, N+CATIONS, P+CATIONS, N+P+CATIONS.
  - Plot structure: each plot is 50 x 50 m; plots are paired/clustered in four blocks; fertilization applied annually in three applications to reduce leaching/runoff.

- Seedling sampling design
  - Within-plot sampling: within each 50 x 50 m plot, a 30 x 30 m sub-plot is established; inside this sub-plot, four 1 x 1 m sub-plots are used for seedling sampling.
  - Total per treatment: 16 sub-plots per treatment, 128 sub-plots across all treatments.
  - Target seedlings: individuals >20 cm height and diameter at ground height (DGH) < 1 cm; palms and lianas excluded.
  - Measurements and timing: seedling height, DGH, total leaves, leaves with herbivory damage, and mortality recorded; data collected every two months over 12 months (six sampling events per sub-plot; four during the rainy season and two during the dry season).

- Data file: seedling measurements and structure
  - Dataset size: 3409 rows with 13 columns.
  - Columns and meanings:
    - CENSUS: Sampling number
    - MONTH: Month of sampling
    - DATA: Sampling day
    - TRT: Plot treatment (as described in AFEX)
    - BLOCK: Block number (1–4)
    - PLOT: Plot number (1–8) within a block
    - SUBPLOT: Subplot number (1–4)
    - INDIVIDUAL: Seedling tag identifier
    - DGH: Diameter at ground height (mm)
    - HEIGHT: Height (cm)
    - TOTAL_LEAVES: Total leaves per seedling
    - LEAVES_WITH_HERBIVORY: Leaves showing herbivory damage
    - MORTALITY: Survival status (1 = dead, 0 = alive)

- References and context
  - Cited works on soils, forest biomass, and related ecological methods informing site selection, soil classification, and sampling protocols (e.g., Chauvel 1982; Comita et al. 2007; Laurance et al. 1999; Lovejoy & Bierregaard 1990; Quesada et al. 2010, 2011; RADAMBRASIL 1978; Ranzani 1980).