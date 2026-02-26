# Overview of data

- Objective and scope
  - Document describes three datasets from a tropical rainforest decomposition experiment.
  - Aims: compare decomposition of ground (fallen) vs suspended wood blocks and quantify the relative contribution of macro-invertebrates to decomposition; assess drought vs non-drought effects on wood block decay.
  - Part of the NERC Human-modified Tropical Forest (HMTF) Programme; conducted in Sabah, Malaysia (Maliau Basin Conservation Area).

- Study design and setting
  - Location: lowland, old-growth dipterocarp rainforest in Maliau Basin, Sabah, Malaysia.
  - Experimental setup: twelve 50 x 50 m plots within a 42-ha area; central 50 x 50 m used for sampling; four plots per treatment group: control, ant suppression, termite suppression.
  - Treatments and pest management:
    - Ant suppression plots: two poison baits (Synergy Pro® with hydramethylnon and pyriproxyfen; custom bait with imidacloprid).
    - Termite suppression plots: physical mound removal plus soil-applied imidacloprid; targeted use of poisoned toilet paper rolls and tea bags with fipronil to protect wood-feeding termites.
  - Duration: treatments maintained Oct 2014–Oct 2017.
  - Experimental units: 289 treated half TPRs and 500 tea bags deployed; blocks and sampling arranged to minimize edge effects.

- Data files and contents
  - WoodBlocksData.csv
    - Purpose: material decomposition and macro-invertebrate influence on wood blocks.
    - Block placement: 9 cm x 9 cm x 5 cm Pinus radiata blocks; placed as open (macro-invertebrate access) or closed (microbial decay only); some blocks drilled for entry.
    - Placement: on the ground and on trees (suspended) across plots; blocks positioned at ground, understory, and canopy heights (0, 10, 20, 30, 40 m; Top).
    - Key variables: Plot, Treatment (A, C, T), Location (Ground, Suspended), Tree_Set, Height, Mesh (Closed, Open, Drilled), Strata, Date_set, Date_collected, Days, Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil, Weight_lost, Prop_weight_loss, Fungal_damage, Termite_damage.
  - AbioticData.csv
    - Purpose: climatic context for blocks (temperature and humidity by height).
    - Data collection: data loggers at 5 m height intervals per tree; measurements every 30 minutes over 5 days per logger.
    - Key variables: Date, Plot, Treatment, Tree_Set, Height, Strata, Day, Time, Temperature, Humidity.
  - DroughtNondroughtWoodBlocksData.csv
    - Purpose: decomposition under drought vs non-drought periods.
    - Design: wood blocks on ground; drought (Aug 2015–Aug 2016) and non-drought (July 2016–July 2017) periods.
    - Key variables: Condition (Drought/Non-drought), Time.woodblocks.deployed (months), Dates, Days, Plot, Plot.Treatment, Mesh, Weight.loss (percent), Proportion, Treatment (e.g., Control open, Control closed, Termite open, Termite closed).

- Experimental measurements and processing
  - Wood blocks
    - Block preparation: dried at 60°C+ for 48 hours; sealed in 300 µm nylon mesh bags; open bags allow macro-invertebrate access; edges sealed to prevent intrusion.
    - Retrieval: after ~1 year; exterior soil brushed; blocks dried again at 60°C for ~5 days; termites’ soil and workings separated from wood; dry mass recorded.
    - Decomposition metrics: weight change (start vs end), weight loss, proportional weight loss; damage scores for fungal and termite effects.
  - Abiotic data collection
    - Data loggers protected in rain-shielded cups; measurements logged for 5 days per tree per height; data used to contextualize decomposition rates.
  - Drought experiment
    - Parallel blocks deployed during drought and non-drought windows to evaluate moisture stress effects on decay and faunal contributions.

- Data structure and units
  - WoodBlocksData.csv
    - Units: mass in grams; heights in meters; Days in days.
    - Categorical fields: Plot, Treatment (A, C, T), Location (Ground, Suspended), Mesh (Closed/Open/Drilled), Strata (Ground/Understory/Canopy).
    - Damage scores: Fungal_damage and Termite_damage on a 0–4 scale.
  - AbioticData.csv
    - Temperature in degrees Celsius; Humidity in percent.
    - Height, Strata, Day, Time define sampling context.
  - DroughtNondroughtWoodBlocksData.csv
    - Weight_loss reported as percentage; Proportion as proportional weight loss.
    - Condition (Drought/Non-drought) and Time.woodblocks.deployed (months) describe deployment context.

- Data provenance and authorship
  - Data collection led by S.J. Law, H.M. Griffiths, and L.A. Ashton; interpretation by Law, Griffiths, Ashton, P. Eggleton, and C.L. Parr.

- Relevance to environmental monitoring and data quality
  - Uses standardized, repeatable methods to isolate biotic (macro-invertebrates, termites) vs abiotic decay processes.
  - Includes multiple spatial scales (ground to canopy), blocking of faunal access, and drought context for robust environmental health inferences.
  - Data are organized with explicit metadata on plots, treatments, block placement, and collection dates to facilitate cross-study comparison and time-series monitoring.
  - Maintains data traceability from field collection to mass measurement, with explicit damage scoring to support multivariate analyses of decay drivers.