# Amazon Fertilization Experiment (AFEX)

- Purpose and scope
  - A fertilization experiment within the Biological Dynamics of Forest Fragments Project (BDFFP) area, aiming to understand how nutrient additions affect seedling growth and health under controlled nutrient treatments.
  - AFEX is a full factorial design with seven treatments plus a control, enabling analysis of individual and combined nutrient effects on early tree establishment.

- Study area
  - Location: KM41 reserve, approximately 100 km from Manaus, along BR-174 (02°24'S, 59°52'W).
  - Climate: humid/wet, mean ~26.7°C; annual rainfall ~2200 mm; dry season July–September; peak rainfall March–April.
  - Vegetation: dense Terra Firme rainforest; canopy 30–37 m, emergent trees to ~55 m.
  - Soils: clayey red-yellow podzols and yellow latosols, highly weathered, acidic, low fertility; WRB class ferralsols.

- Experimental design (AFEX)
  - Start: March 2017.
  - Treatments: seven nutrient treatments plus Control (CONTROL); N (125 kg N ha-1 y-1 as urea), P (50 kg P ha-1 y-1 as triple superphosphate), CATIONS (50 kg K ha-1 y-1 as KCl; 160 kg Ca ha-1 y-1; 160 kg Mg ha-1 y-1 as dolomitic limestone); combinations N+P, N+CATIONS, P+CATIONS, N+P+CATIONS.
  - Structure: full factorial with four replicates per treatment, totaling 32 plots; arranged in four independent blocks (distance ≥250 m apart).
  - Plot layout: each plot 50 x 50 m; treatments distributed within blocks as described.
  - Fertilization: applied annually in three applications to mitigate leaching and runoff; fertilizers spread manually during systematic plot walks.

- Seedling sampling methodology
  - Subplot layout: four 1 x 1 m subplots within a 30 x 30 m area inside each 50 x 50 m plot, yielding 16 subplots per treatment and 128 total across all treatments.
  - Target individuals: all seedlings >20 cm height and DGH < 1 cm; palms and lianas excluded.
  - Measurements per seedling: height (cm), diameter at ground height (DGH, mm), total leaves, leaves with herbivory damage, and mortality (binary: 1 = death, 0 = alive).
  - Temporal scheme: data collected bimonthly over 12 months (six replications per subplot; four in the rainy season, two in the dry season).

- Data management (seedlings_growth.csv)
  - Contents: 3,409 data rows and 13 columns.
  - Column definitions:
    - CENSUS: sampling number
    - MONTH: month of sampling
    - DATA: sampling date
    - TRT: plot treatment (descriptions in section 2.1)
    - BLOCK: block (1–4)
    - PLOT: plot (1–8)
    - SUBPLOT: subplot number (1–4)
    - INDIVIDUAL: seedling tag
    - DGH: diameter at ground height (mm)
    - HEIGHT: height (cm)
    - TOTAL_LEAVES: total leaves
    - LEAVES_WITH_HERBIVORY: leaves with herbivory damage
    - MORTALITY: 1 if dead, 0 if alive
  - Notes: The data file provides structured metadata to support quality assurance, reproducibility, and downstream analyses.

- References
  - Chauvel (1982); Comita, Condit, & Hubbell (2007); Laurance et al. (1999); Lovejoy & Bierregaard (1990); Quesada et al. (2010, 2011); RADAMBRASIL (1978); Ranzani (1980).