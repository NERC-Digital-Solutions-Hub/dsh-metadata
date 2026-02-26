# Overview of data

- Purpose of the datasets
  - Examine decomposition of wood blocks after ~1 year under different conditions: ground vs suspended (canopy), and availability of macro-invertebrates (open vs closed mesh).
  - Assess the relative contribution of macro-invertebrates to wood decomposition.
  - Compare decomposition under drought vs non-drought periods.

- Datasets included
  - WoodBlocksData.csv: Decomposition data for Pinus radiata wood blocks placed on the ground and in the canopy, with ant/termite suppression treatments, including open/closed mesh to control macro-invertebrate access.
  - AbioticData.csv: Climate variables (temperature and relative humidity) recorded at multiple heights (5 m intervals) from ground to canopy during 2016.
  - DroughtNondroughtWoodBlocksData.csv: Wood block decomposition data for drought (2015–2016) and non-drought (2016–2017) periods, including mesh and treatment combinations.

- Experimental setting
  - Location: lowland, old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Plot design: 12 plots within a 42-ha area, each 50 x 50 m with a 15 m buffer; central 50 x 50 m used for sampling.
  - Treatments: 4 control, 4 ant suppression, 4 termite suppression plots, separated by at least 100 m.
  - Suppression methods:
    - Ant suppression: two bait types (Synergy Pro with hydramethylnon and pyriproxyfen; custom bait with imidacloprid).
    - Termite suppression: removal of termite mounds; soil treatment with imidacloprid; poisoned toilet paper rolls and tea bags treated with fipronil; deployment at regular intervals to maintain suppression (Oct 2014–Oct 2017).

- Wood block experimental design
  - Blocks: Pinus radiata, 9 cm x 9 cm x 5 cm, dried to constant mass, sealed in 300 µm mesh bags (open, closed, or drilled for macro-invertebrate access).
  - Placement: across plots in a cross pattern; 10 blocks per plot (5 open, 5 closed); blocks placed on ground and on trees at canopy/height intervals (0, 10, 20, 30, 40 m), with canopy blocks positioned on trunks above first branch.
  - Retrieval: after about one year; processing includes cleaning, drying, separating termite soil, and weighing.

- Drought context
  - Drought and non-drought periods studied: drought (El Niño event) during 2015–2016 and non-drought period 2016–2017.
  - Repeated measurements of wood block decomposition under both conditions in the same experimental framework.

- Data collection and authorship
  - Abiotic data loggers placed on the largest sampled tree within each ant suppression and control plot; temperature and humidity recorded every 30 minutes for five days at each height.
  - Data collection and interpretation credited to S. J. Law, H. M. Griffiths, L. A. Ashton, P. Eggleton, and C. L. Parr; study conducted as part of the NERC Human-modified Tropical Forest (HMTF) Programme.

- Data structure and variable descriptions
  - WoodBlocksData.csv
    - Plot, Treatment (A = ant suppression; C = control; T = termite suppression), Location (Suspended or Ground), Tree_Set (tree identifier), Height (0, 10, 20, 30, 40 m; Top), Mesh (Closed, Open, Drilled), Strata (Ground, Understory, Canopy), Date_set, Date_collected, Days, Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil, Weight_lost, Prop_weight_loss, Fungal_damage (0–4), Termite_damage (0–4).
  - AbioticData.csv
    - Date, Plot, Treatment (A, C), Tree_Set, Height, Strata, Day, Time, Temperature (°C), Humidity (%).
  - DroughtNondroughtWoodBlocksData.csv
    - Condition (Drought, Non-drought), Time.woodblocks.deployed (months), Dates, Days, Plot, Plot.Treatment (Control, Termite), Mesh (Closed, Open), Weight.loss (%), Proportion, Treatment (Control open, Control closed, Termite open, Termite closed).

- Relevance for data strategy and governance
  - Provides multi-dimensional data linking decomposition outcomes to biotic (ant/termite suppression) and abiotic (height, canopy position) factors across drought contexts.
  - Rich metadata and structured variables support discoverability, cross-file integration, and reproducible analyses of decomposition dynamics.
  - Clear coding for treatments, mesh types, and spatial placements facilitates consistent data interpretation and potential cross-study comparisons within data networks.