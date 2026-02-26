# seedlings_herbivory.csv

- Study purpose and scope
  - Describes a dataset of seedling herbivory and associated biotic factors collected within the Amazon Fertilization Experiment (AFEX) in the KM41 reserve of the Biological Dynamics of Forest Fragments Project (BDFFP).
  - Aims to support analysis of how nutrient fertilization affects seedling herbivory, leaf damage, and related biotic interactions over a year.

- Study area
  - Location: KM41 reserve, BDFFP, ~100 km from Manaus, Brazil (02 24'S, 59 52'W).
  - Climate: humid, wet; mean temperature ~26.7°C; annual precipitation ~2200 mm; dry season July–September; peak rainfall March–April.
  - Vegetation: dense Terra Firme rainforest; canopy 30–37 m, emergents up to ~55 m.
  - Soils: red-yellow podsols (clayey) and yellow latosols; highly weathered, acidic, low fertility; WRB class ferrasols.
  - Figure references: location and plot layouts provided (KM41 reserve).

- Amazon Fertilization Experiment (AFEX)
  - Design: full factorial with seven nutrient treatments plus a control; factorial combination of N, P, and cations (K, Ca, Mg).
  - Treatments: Control; N; P; CATIONS; N+P; N+CATIONS; P+CATIONS; N+P+CATIONS.
  - Replication and layout: 32 plots total (4 replicates per treatment), arranged in four independent blocks at least 250 m apart.
  - Plot sizes and spacing: each plot 50 x 50 m; blocks separated by at least 100 m.
  - Fertilization regime: annual, delivered in three applications to reduce leaching/runoff.
  - Application details: N 125 kg N ha-1 year-1 (as urea); P 50 kg P ha-1 year-1 (as triple superphosphate); K 50 kg K ha-1 year-1 (as KCl); Ca 160 kg Ca ha-1 year-1 (as dolomitic limestone); Mg 160 kg Mg ha-1 year-1 (as dolomitic limestone).

- Seedling sampling setup
  - Sub-plot structure: within each 50 x 50 m plot, four 1 x 1 m sub-plots embedded in a 30 x 30 m area.
  - Treatment-level replication: 16 sub-plots per treatment, 128 sub-plots in total across all treatments.
  - Selection criteria: all plant individuals >20 cm tall with diameter at ground height (DGH) < 1 cm identified and tagged; palms and lianas not sampled.
  - Leaf monitoring: for each individual, the closest 10 mature leaves to the apical region marked with permanent ink and tracked bi-monthly for 12 months.
  - Measurements per leaf: herbivory damage (leaf area loss, %); presence/absence of galls (GAIL), fungi (FUNGUS), and leaf miners (LEAF_MINERS).
  - Sampling cadence: six campaigns per sub-plot (four during the rainy season, two during the dry season); duration covers 12 months.

- Data file and structure
  - Data file: seedlings_herbivory.csv
  - Size and columns: 27,510 rows and 14 columns.
  - Key columns and meanings:
    - CENSUS: sampling number
    - MONTH: month of sampling
    - DATE: sampling day
    - TRT: plot treatment (reference AFEX design)
    - BLOCK: block number (1–4)
    - PLOT: plot number within block (1–8)
    - SUBPLOT: sub-plot number (1–4)
    - INDIVIDUAL: seedling tag
    - LEAF: leaf tag
    - HERBIVORY: leaf area loss due to herbivory (percentage)
    - GAIL: gall presence (1) or absence (0)
    - FUNGUS: fungus presence (1) or absence (0)
    - LEAF_MINERS: leaf miners presence (1) or absence (0)
    - MORTALITY: seedling leaf death (1) or survival (0)

- Methods and data quality notes
  - Herbivory assessment based on direct visual estimates following Johnson et al. (2016); accuracy enhanced by using a millimetre grid to sector leaves.
  - Data collected across six campaigns to capture seasonal variation; bimonthly leaf-level monitoring over one year.
  - Exclusions: no sampling of palms or lianas; focus on seedlings with >20 cm height and DGH < 1 cm.
  - Data provenance and structure designed to support cross-dataset integration (e.g., linking treatment, plot, and sub-plot metadata with leaf-level measurements).

- References (contextual)
  - Soil and site characterization references (Chauvel 1982; Quesada et al. 2010, 2011; Ranzani 1980; RADAMBRASIL 1978; Laurance et al. 1999).
  - herbivory measurement method (Johnson et al. 2016).
  - AFEX and BDFFP context (Lovejoy & Bierregaard 1990; Comita et al. 2007).