# Amazon Fertilization Experiment (AFEX)

- Study area: BDFFP area inside KM41 reserve, ~100 km from Manaus, Brazil (02°24'S, 59°52'W). Humid, wet climate; mean temperature ~26.7°C; 2200 mm annual rainfall with a pronounced dry season (Jul–Sep) and rain peak (Mar–Apr). Dense Terra Firme rainforest; canopy 30–37 m; emergents up to 55 m. Soils are clayey red-yellow podzols and yellow latosols with high weathering, acidity, and low fertility (ferrasols in WRB). Location shown in Figure 1; AFEX blocks/plots shown in Figure 2.

- Experimental design (Amazon Fertilization Experiment, AFEX):
  - Full factorial design with seven nutrient treatments plus a control, total 8 treatments:
    - Control
    - N
    - P
    - CATIONS (K, Ca, Mg)
    - N+P
    - N+CATIONS
    - P+CATIONS
    - N+P+CATIONS
  - 32 plots in total: four independent blocks (at least 250 m apart), four replicates per treatment (8 treatments × 4 replicates).
  - Plot layout:
    - Each AFEX plot is 50 x 50 m.
    - Treatments are implemented across four blocks, with eight plots per block.
  - Fertilization regime:
    - Annual application divided into three events to mitigate leaching/runoff.
    - N: 125 kg N ha^-1 year^-1 (as urea)
    - P: 50 kg P ha^-1 year^-1 (as triple superphosphate)
    - Cations: 50 kg K ha^-1 year^-1 (as KCl); Ca: 160 kg Ca ha^-1 year^-1; Mg: 160 kg Mg ha^-1 year^-1 (as dolomitic limestone)

- Seedling sampling design:
  - Within each 50 x 50 m plot, a 30 x 30 m sub-plot contains four 1 x 1 m sub-plots used for seedling sampling.
  - Per treatment: 4 replicates × 4 sub-plots = 16 sub-plots per treatment; 128 sub-plots in total across all treatments.
  - Target individuals: all seedlings taller than 20 cm and with diameter at ground height (DGH) < 1 cm; palms and lianas not identified/sampled.
  - Measurements per seedling per sub-plot:
    - DGH (mm)
    - HEIGHT (cm)
    - TOTAL_LEAVES
    - LEAVES_WITH_HERBIVORY
  - Mortality: MORTALITY (1 = dead, 0 = alive)

- Data collection and timing:
  - Seedling data collected bi-monthly over 12 months (6 sampling events per sub-plot: 4 in the rainy season, 2 in the dry season).

- Data file and structure:
  - Seedling data file: seedlings_growth.csv
  - Contents: 3409 rows, 13 columns
  - Columns:
    - CENSUS: Sampling number
    - MONTH: Month of sampling
    - DATA: Sampling date
    - TRT: Plot treatment (as described in section 2.1)
    - BLOCK: Block number (1–4)
    - PLOT: Plot number (1–8)
    - SUBPLOT: Sub-plot number (1–4)
    - INDIVIDUAL: Seedling tag
    - DGH: Diameter at ground height (mm)
    - HEIGHT: Height (cm)
    - TOTAL_LEAVES: Total number of leaves
    - LEAVES_WITH_HERBIVORY: Leaves with herbivory damage
    - MORTALITY: 1 if dead, 0 if alive

- References and context:
  - Includes foundational soil and forest ecology sources detailing soil types, productivity, and environmental context relevant to the BDFFP and AFEX site (Chauvel 1982; Comita et al. 2007; Laurance et al. 1999; Lovejoy & Bierregaard 1990; Quesada et al. 2010, 2011; RADAMBRASIL 1978; Ranzani 1980).