# Overview of data

- Scope and purpose
  - Describes three related datasets from a tropical rainforest experiment in Maliau Basin, Sabah, Malaysia (2016–2017, drought and non-drought periods).
  - Aims to compare ground vs suspended wood-block decomposition and assess the contribution of macro-invertebrates; includes abiotic climate data.

- Datasets and their contents
  - WoodBlocksData.csv
    - 12 experimental plots within a 42-hectare area; each plot 50 x 50 m with an 80 x 80 m treatment zone.
    - Four plots per treatment: control, ant suppression, termite suppression (separated by at least 100 m).
    - Treatments
      - Ant suppression: Synergy Pro® bait and imidacloprid via custom bait.
      - Termite suppression: removal of mounds plus imidacloprid soil treatment; poisoned toilet paper rolls (TPR) and tea bags (TBs) with fipronil.
    - Block setup
      - Pinus radiata wood blocks (9 x 9 x 5 cm), dried, placed in nylon mesh bags (open, closed, or drilled variants).
      - Blocks placed: on the ground (Ground) and on trees (Suspended) at heights 0, 10, 20, 30, 40 m; canopy vs understory defined by trunk location.
      - Per plot: 10 blocks (5 open, 5 closed) in a cross pattern; blocks on three emergent trees per plot at vertical intervals; central 50 x 50 m sampling area to avoid edge effects.
      - Retrieval after about one year; measurements include dry weights, weight loss, proportional weight loss, and damage scores (fungal and termite).
  - AbioticData.csv
    - Climate data collected with data loggers (iButtons) at 5 m vertical intervals on the largest sampled tree per ant-suppression and control plots.
    - Measurements: temperature (°C) and relative humidity (%) every 30 minutes for five days per height level.
  - DroughtNondroughtWoodBlocksData.csv
    - Ground-deployed wood blocks under drought (2015–2016) and non-drought (2016–2017) periods.
    - Setup similar to WoodBlocksData, with 10 blocks per plot (5 open, 5 closed); blocks deployed for 12 months.
    - Two conditions: Drought vs Non-drought; data include weight loss percentages and treatment combinations (e.g., Control open/closed, Termite open/closed).

- Experimental design and location
  - Location: lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
  - Plots: 12 plots within a 42-ha area; each plot 50 x 50 m, with a 15 m buffer; central sampling area 50 x 50 m.
  - Timeline: Inoculation and suppression treatments established October 2014; maintained until October 2017.
  - Plot-level treatments split into four groups: Control, Ant suppression, Termite suppression (with targeted application methods to minimize broader ecosystem impact).

- Data structure and key fields
  - WoodBlocksData.csv
    - Plot, Treatment (A=ant suppression, C=control, T=termite suppression)
    - Location (Ground, Suspended)
    - Tree_Set (tree identifier)
    - Height (0, 10, 20, 30, 40 m; Top indicates maximum height with no exact meter)
    - Mesh (Closed, Open, Drilled)
    - Strata (Ground, Understory, Canopy)
    - Date_set, Date_collected
    - Days
    - Dry_weight_start, Dry_weight_end
    - Dry_weight_termite_workings_and_soil
    - Weight_lost, Prop_weight_loss
    - Fungal_damage (0–4)
    - Termite_damage (0–4)
  - AbioticData.csv
    - Date, Plot, Treatment (A, C)
    - Tree_Set, Height, Strata
    - Day (1–5), Time (hh:mm)
    - Temperature (°C), Humidity (%)
  - DroughtNondroughtWoodBlocksData.csv
    - Condition (Drought, Non-drought)
    - Time.woodblocks.deployed (months)
    - Dates (start–end)
    - Days
    - Plot, Plot.Treatment (Control, Termite)
    - Mesh (Open, Closed)
    - Weight.loss (%), Proportion
    - Treatment (Control open/closed; Termite open/closed)

- Data provenance and collection
  - Primary data collection and interpretation led by S.J. Law, H.M. Griffiths, L.A. Ashton; interpretation involving P. Eggleton and C.L. Parr.
  - Part of the NERC Human-modified tropical forest (HMTF) Programme.

- GIS and data product considerations
  - Spatially explicit design: plots and blocks with ground vs canopy placement, vertical stratification, and precise plot layout enable map-based visualisations of decomposition patterns.
  - Multisource integration: aligns biological (decomposition, termite/macroinvertebrate access) with abiotic variables (temperature, humidity) across heights and treatments.
  - Data preparation needs: careful handling of mesh treatments and damage scores, alignment of height/strata categories, temporal alignment across datasets for combined analyses.