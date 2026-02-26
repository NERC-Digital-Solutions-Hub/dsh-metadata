# Overview of data

- Purpose and scope
  - Datasets record wood block decomposition to compare ground vs suspended wood and to quantify the contribution of macro-invertebrates to decomposition.
  - Includes abiotic conditions to contextualize decomposition dynamics.
  - Covers drought and non-drought periods to assess climate effects.

- Datasets included
  - WoodBlocksData.csv: decomposition after ~1 year for blocks placed on the ground or in the canopy, with open (macro-invertebrate access) and closed (microbial decay only) mesh bags; includes treatment (ant suppression, termite suppression, control), placement height, and damage/weight-change metrics.
  - AbioticData.csv: climatic variables (temperature, relative humidity) recorded at 5 m intervals from ground to canopy over five days, across plots and treatments.
  - DroughtNondroughtWoodBlocksData.csv: decomposition data for blocks deployed during drought and non-drought periods, detailing weight loss, proportion lost, mesh type, plot treatment, and overall treatment condition.

- Experimental design and setting
  - Location: lowland old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Twelve 50 x 50 m plots within a 42-hectare area; four plots per treatment: control, ant suppression, termite suppression.
  - Insecticide-based suppression methods:
    - Ant suppression: two baits (Synergy Pro® with hydramethylnon/pyriproxyfen and a sugar solution with imidacloprid) under integrated pest management.
    - Termite suppression: removal of mounds; soil treatment with imidacloprid; use of poisoned toilet paper rolls and tea bags with fipronil; re-poisoning every six months from 2014–2017.
  - Wood blocks: untreated Pinus radiata blocks (9 x 9 x 5 cm) placed in two mesh conditions (open vs closed); placed in ground, understory, and canopy; 10 blocks per plot (5 open, 5 closed), paired across vertical heights; retrieved after ~1 year.
  - Sampling completed across central plots to avoid edge effects; blocks placed on tree trunks to maximize discovery by decomposers.

- Data collection and processing methods
  - WoodBlocksData.csv
    - Block preparation: drying to constant mass, sealed in 300 µm mesh bags (open or closed), edges sealed to restrict entry.
    - Measurements: initial and final dry weights, weight loss, proportional weight loss, and scores for fungal and termite damage (0–4 scale).
  - AbioticData.csv
    - Data loggers placed at 5 m intervals on the largest sampled tree per plot; measurements every 30 minutes over five days.
  - DroughtNondroughtWoodBlocksData.csv
    - Same wood block assay as WoodBlocksData.csv, conducted during drought (2015–2016) and non-drought (2016–2017) periods; records weight loss and treatment combinations.

- Data structure and key variables
  - WoodBlocksData.csv
    - Plot, Treatment (A=ant suppression, C=control, T=termite suppression), Location (Ground/Understory/Canopy), Tree_Set, Height, Mesh (Open/Closed/Drilled), Strata, Date_set, Date_collected, Days, Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil, Weight_lost, Prop_weight_loss, Fungal_damage, Termite_damage.
  - AbioticData.csv
    - Date, Plot, Treatment, Tree_Set, Height, Strata, Day, Time, Temperature (°C), Humidity (%).
  - DroughtNondroughtWoodBlocksData.csv
    - Condition (Drought/Non-drought), Time.woodblocks.deployed (months), Dates, Days, Plot, Plot.Treatment, Mesh, Weight.loss (%), Proportion, Treatment (composite: Control open/closed; Termite open/closed).
  
- Relevance for environmental monitoring and governance
  - Demonstrates end-to-end monitoring workflow: from experimental manipulation to standardized measurement of ecological processes and abiotic context.
  - Highlights importance of metadata, data standardization, and data sharing (underpinning data governance and transparency).
  - Provides a multi-factor dataset (biotic manipulations, vertical stratification, anthropogenic/insecticide interventions, and climate context) useful for evaluating policy-relevant environmental health measures and informing future monitoring decisions.
  
- Practical considerations and challenges for monitoring frameworks
  - Data accessibility and sharing: potential barriers due to open data requirements and sensitive methodological details (e.g., pesticide use).
  - Metadata quality: detailed variable definitions are provided, but alignment with broader data standards would facilitate interoperability.
  - Data transformation needs: consistent units and naming across datasets; some fields (e.g., height and strata) require careful interpretation for cross-study comparability.
  - Data governance: clear provenance and documentation needed to ensure datasets meet quality standards and are usable for policy evaluation and future decision-making.