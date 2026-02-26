# Overview of data

- Datasets included
  - WoodBlocksData.csv: decomposition of Pinus radiata wood blocks after ~1 year, comparing ground vs suspended blocks and the effect of macro-invertebrate access (open vs closed vs drilled mesh) across four plot treatments (Control, Ant suppression, Termite suppression) over 12 experimental plots (2016–2017).
  - AbioticData.csv: climatic variables (temperature and relative humidity) recorded at 5 m height intervals from ground to canopy in 2016.
  - DroughtNondroughtWoodBlocksData.csv: ground-deployed wood block decomposition during drought (2015–2016) and non-drought (2016–2017) periods, with open/closed mesh and plot treatments.

- Study purpose
  - Compare decomposition of fallen ground wood vs suspended wood.
  - Assess the relative contribution of macro-invertebrates to wood decomposition.
  - Examine effects of drought versus non-drought on decomposition.

- Experimental design (location and setup)
  - Location: lowland old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Timeframe: plots established Oct 2014; treatments maintained through Oct 2017.
  - Plot layout: 12 plots within a 42-ha area (50 x 50 m plots with 80 m x 80 m treated area); central 50 x 50 m used for sampling.
  - Treatments (4 plots each): Control, Ant suppression, Termite suppression (ant and termite plots separated by ≥100 m).
  - Ant suppression: two bait types (Synergy Pro® and sugar-soaked Whiskas® with imidacloprid) using an integrated pest management approach.
  - Termite suppression: removal of mounds; soil treated with imidacloprid; targeted use of poisoned toilet paper rolls and tea bags with fipronil; re-poisoning every six months.

- Wood blocks and mounting protocol (WoodBlocksData.csv)
  - Blocks: untreated Pinus radiata, 9 x 9 x 5 cm, dried to constant weight, sealed in 300 μm mesh bags (open, closed, or drilled).
  - Placement: within plots (Ground, Understory, Canopy); 10 blocks per plot (5 open, 5 closed) placed in a cross per plot; additional canopy placements on emergent trees at 0–40 m heights.
  - Retrieval: after ~1 year; blocks cleaned, dried, and weighed; termite damage, soil, and non-termite soil removed for final dry weight.
  - Recorded outcomes: start/end dry weight, weight loss, proportional weight loss, fungal and termite damage scores.

- Drought vs non-drought data (DroughtNondroughtWoodBlocksData.csv)
  - Deployment periods: drought (Aug 2015–Aug 2016) and non-drought (Jul 2016–Jul 2017).
  - Conditions: ground blocks with open/closed mesh; 10 blocks per plot (5 open, 5 closed).
  - Outcomes: weight loss metrics (Weight.loss, Proportion) and treatment classifications (Plot.Treatment, Mesh, Treatment).

- Abiotic data collection (AbioticData.csv)
  - Data loggers placed at 5 m intervals on the largest sampled tree per ant suppression and control plot.
  - Measurements: temperature (°C) and humidity (%) every 30 minutes over 5 days per height level.
  - Data handling: loggers protected from rain; day markers indicate sequence within the 5-day period.

- Data structure and key variables (column headings)
  - WoodBlocksData.csv
    - Plot, Treatment, Location, Tree_Set, Height, Mesh, Strata, Date_set, Date_collected, Days
    - Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil
    - Weight_lost, Prop_weight_loss
    - Fungal_damage, Termite_damage
  - AbioticData.csv
    - Date, Plot, Treatment, Tree_Set, Height, Strata, Day, Time, Temperature, Humidity
  - DroughtNondroughtWoodBlocksData.csv
    - Condition, Time.woodblocks.deployed, Dates, Days, Plot, Plot.Treatment, Mesh
    - Weight.loss, Proportion, Treatment

- Data collection and interpretation responsibilities
  - Collection: S.J. Law, H.M. Griffiths, L.A. Ashton
  - Interpretation: S.J. Law, H.M. Griffiths, L.A. Ashton, P. Eggleton, C.L. Parr

- Programme and context
  - Part of the NERC Human-modified Tropical Forest (HMTF) Programme
  - Location coordinates and plot details provided to enable replication and cross-study comparisons

- Data usability and potential outputs for a Data Support perspective
  - Opportunity to build self-serve data products (dashboards, pivot tables) enabling comparison of decomposition across treatments, heights, and mesh types.
  - Combine WoodBlocksData with AbioticData to analyze correlations between microclimate (temperature/humidity) and decomposition metrics.
  - Compare drought vs non-drought periods within DroughtNondroughtWoodBlocksData.csv to assess climate-related effects.
  - Data can be used to create summaries, charts, and statistical models linking termite/ant suppression, macro-invertebrate access, and decomposition outcomes across vertical strata (Ground, Understory, Canopy).