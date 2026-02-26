# Amazon Fertilization Experiment (AFEX)

- Study area
  - Conducted inside the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil (02 24'S, 59 52'W).
  - Humid, wet climate; mean temperature ~26.7°C; annual rainfall ~2200 mm; dry season July–Sept; rain peak March–April.
  - Dense Terra Firme rainforest vegetation; canopy 30–37 m, emergents up to ~55 m.
  - Soils: clayey red-yellow podzols and yellow latosols with high weathering, acidity and low fertility (WRB ferralsols).

- Amazon Fertilization Experiment (AFEX) – experimental design
  - Full factorial fertilization with seven treatments plus control; four replicates per treatment (32 plots total) across four independent blocks (≥250 m apart).
  - Treatments (N, P, and Cations): N (125 kg N ha-1 yr-1 as urea); P (50 kg P ha-1 yr-1 as triple superphosphate); CATIONS (K 50 kg K ha-1 yr-1 as KCl; Ca 160 kg Ca ha-1 yr-1; Mg 160 kg Mg ha-1 yr-1 as dolomitic limestone).
  - Treatment combinations: Control; N; P; CATIONS; N+P; N+CATIONS; P+CATIONS; N+P+CATIONS.
  - Plot size and layout: each plot 50×50 m, with all plots ≥100 m apart; located within areas of similar soil, vegetation, and topography (referenced in Figure 2).

- Fertilization protocol
  - Annual fertilization divided into three applications to mitigate nutrient loss via leaching and runoff.
  - Fertilizers applied by hand during a systemic walk within plots.

- Seedling sampling design
  - Within each 50×50 m plot, four 1×1 m sub-plots are nested inside a 30×30 m area per treatment (total 16 sub-plots per treatment; 128 sub-plots overall).
  - All plant individuals >20 cm tall with ground-diameter height (DGH) <1 cm identified and tagged; palms and lianas not sampled.
  - Sub-plots arranged as per a defined layout (illustrated in Figure 3).

- Leaf herbivory and related data collection
  - For each seedling, the closest 10 mature leaves are marked and tracked bimonthly for leaf-level herbivory assessment.
  - Herbivory measured as leaf-area loss (%) using a standardized method; leaves sectored with a millimetre grid to improve accuracy.
  - Additional qualitative data collected per leaf: galls, pathogens, and trail herbivory presence/absence.
  - Sampling cadence: six campaigns per sub-plot over 12 months (four during the rainy season, two during the dry season).

- Data spreadsheet and structure
  - Dataset: seedlings_herbivory.csv with 27,510 rows and 14 columns.
  - Columns and meanings:
    - CENSUS: Sampling number
    - MONTH: Month of sampling
    - DATE: Sampling day
    - TRT: Plot treatment (as described in AFEX section)
    - BLOCK: Block (1–4)
    - PLOT: Plot (1–8)
    - SUBPLOT: Subplot number (1–4)
    - INDIVIDUAL: Seedling tag
    - LEAF: Leaf tag
    - HERBIVORY: Leaf-area loss by herbivory (%)
    - GAIL: Gall presence (1) or absence (0)
    - FUNGUS: Fungus presence (1) or absence (0)
    - LEAF_MINERS: Leaf miner presence (1) or absence (0)
    - MORTALITY: Leaf death (1) or survival (0)

- References
  - Chauvel (1982); Comita, Condit, & Hubbell (2007); Johnson, Bertrand, & Turcotte (2016); Laurance et al. (1999); Lovejoy & Bierregaard (1990); Quesada et al. (2010, 2011); RADAMBRASIL (1978); Ranzani (1980).