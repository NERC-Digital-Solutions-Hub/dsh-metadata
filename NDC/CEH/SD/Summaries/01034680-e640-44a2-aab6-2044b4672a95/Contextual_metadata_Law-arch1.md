# Overview of data

- Datasets included
  - WoodBlocksData.csv: decomposition of Pinus radiata wood blocks after about one year; blocks placed on the ground and at various heights on trees; open (macro-invertebrates allowed) vs closed (excluded) mesh to isolate biological vs microbial decay; 12 plots (2016–2017) across ground, understory, and canopy.
  - AbioticData.csv: climate variables (temperature and relative humidity) recorded at multiple height intervals from ground to canopy during 2016.
  - DroughtNondroughtWoodBlocksData.csv: ground-block decomposition during drought (2015–2016) and non-drought (2016–2017) periods; open vs closed mesh; data collected on 10 blocks per plot.

- Study location and design
  - Location: lowland, old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Experimental plots: 12 plots within a 42-ha area, each 50 x 50 m with 15 m buffer; central 50 x 50 m area sampled to avoid edge effects.
  - Treatments: four plots per treatment category – control, ant suppression, and termite suppression (four plots each; separated by ≥100 m).
  - Insecticide/ant- and termite-suppression approach:
    - Ant suppression: two bait types (Synergy Pro® with hydramethylnon and pyriproxyfen; Whiskas-cat-food bait with imidacloprid) using integrated pest management.
    - Termite suppression: removal of termite mounds and application of imidacloprid to soil; use of poisoned half toilet paper rolls and tea bags with fipronil; repeated dosing every six months.
  - Suppression maintained from Oct 2014 to Oct 2017.

- Wood block preparation and deployment
  - Blocks: untreated Pinus radiata, 9 cm x 9 cm x 5 cm, dried to constant weight, sealed in 300 μm nylon mesh bags (open, closed, or drilled).
  - Deployment within each plot: a cross-design with 10 blocks per plot (5 open, 5 closed); blocks placed on the ground and on trees at 0, 10, 20, 30, and 40 m height; location recorded as Ground, Understory, or Canopy.
  - Retrieval: after approximately one year; blocks cleaned, dried (60 °C for ~5 days), and weighed; termite soil/soil translocated material separated; fungal and termite damage scored.

- Abiotic data collection
  - Data loggers placed at 5 m vertical intervals on the largest sampled tree per ant suppression and control plot.
  - Temperature and humidity recorded every 30 minutes for five days per height level.

- Key dates and periods
  - Initial setup: October 2014; plots established and suppression treatments started.
  - Wood blocks retrieved after ~1 year (dates embedded in dataset fields).
  - Drought period study: drought (Aug 2015–2016) and non-drought (Jul 2016–Jul 2017) blocks deployed and retrieved as specified.

- Data structure and column highlights
  - WoodBlocksData.csv
    - Plot, Treatment (A=ant suppression; C=control; T=termite suppression), Location (Suspended vs Ground), Tree_Set, Height, Mesh (Closed/Open/Drilled), Strata (Ground/Understory/Canopy), Date_set, Date_collected, Days
    - Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil
    - Weight_lost, Prop_weight_loss
    - Fungal_damage (0–4 scale), Termite_damage (0–4 scale)
  - AbioticData.csv
    - Date, Plot, Treatment, Tree_Set, Height, Strata, Day, Time, Temperature (°C), Humidity (%)
  - DroughtNondroughtWoodBlocksData.csv
    - Condition (Drought/Non-drought), Time.woodblocks.deployed (months), Dates, Days, Plot, Plot.Treatment (Control/Termite), Mesh (Open/Closed)
    - Weight.loss (percentage), Proportion (proportional weight loss), Treatment (e.g., Control open, Control closed, Termite open, Termite closed)

- Analytical opportunities and questions
  - Quantify decomposition rates by location (Ground vs Suspended) and by height (ground, understory, canopy).
  - Assess the contribution of macro-invertebrates to decomposition by comparing open vs closed mesh blocks.
  - Evaluate the effects of ant suppression and termite suppression on wood block decomposition.
  - Examine how drought vs non-drought periods influence decomposition, controlling for mesh type and treatment.
  - Link abiotic conditions (temperature and humidity at different heights) to decomposition rates and damage scores.