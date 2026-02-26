# Overview of data

- Datasets included
  - WoodBlocksData.csv: decomposition of Pinus radiata wood blocks after about one year, comparing ground vs suspended blocks and the effect of macro-invertebrate access. Data collected across 12 plots (2016–2017) with ant/termite suppression treatments.
  - AbioticData.csv: climatic variables (temperature and relative humidity) recorded at multiple heights from ground to canopy in 2016 using data loggers.
  - DroughtNondroughtWoodBlocksData.csv: decomposition of wood blocks placed on the ground during drought (2015–2016) and non-drought (2016–2017) periods, including open/closed mesh and treatment combinations.

- Experimental design and study context
  - Location: lowland old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Setup: 12 plots (50 x 50 m) within a 42-ha area; four plots per treatment: control, ant suppression, termite suppression.
  - Treatments: ant suppression using two bait types (Synergy Pro and imidacloprid-based custom bait); termite suppression via soil treatment and poisoned wood-contact devices; integrated pest management maintained Oct 2014–Oct 2017.
  - Wood blocks: standard assay using untreated 9 x 9 x 5 cm blocks; blocks dried to constant mass, sealed in 300 µm mesh bags (open, closed, or drilled). Placed on ground and on trees (suspension) from trunk base to canopy. Ten blocks per plot (five open, five closed) arranged in a grid; blocks retrieved after ~1 year.
  - Canopy vs ground: blocks placed at multiple heights (0, 10, 20, 30, 40 m) and categorized as Ground, Understory, Canopy. Top height logged when exact measurement unavailable.

- Data collection, processing, and variables
  - WoodBlocksData.csv
    - Core fields include: Plot, Treatment, Location (Suspended/Ground), Tree_Set, Height, Mesh, Strata, Date_set, Date_collected, Days, Dry_weight_start, Dry_weight_end, Dry_weight_termite_workings_and_soil, Weight_lost, Prop_weight_loss, Fungal_damage, Termite_damage.
    - Derived measures: Weight loss (g) and proportional weight loss; damage scores for fungal and termite activity.
    - Special notes: Height “Top” indicates the data logger was placed as high as possible with no exact height recorded.
  - AbioticData.csv
    - Core fields include: Date, Plot, Treatment, Tree_Set, Height, Strata, Day, Time, Temperature (°C), Humidity (%).
    - Data collected every 30 minutes over five days per logger.
  - DroughtNondroughtWoodBlocksData.csv
    - Core fields include: Condition (Drought/Non-drought), Time.woodblocks.deployed (months), Dates, Days, Plot, Plot.Treatment, Mesh, Weight.loss, Proportion, Treatment (composite: Control open/closed; Termite open/closed).

- Data provenance and responsibilities
  - Data collection: S.J. Law, H.M. Griffiths, L.A. Ashton.
  - Data interpretation: S.J. Law, H.M. Griffiths, L.A. Ashton, P. Eggleton, C.L. Parr.
  - Datasets are linked to the NERC Human-modified tropical forest (HMTF) Programme.

- Data structure and metadata details
  - Three CSV files with structured, documented columns and units (as described above).
  - Measurements include weights (grams), mass loss, proportions, and qualitative damage scores (0–4 for fungal and termite effects).
  - Abiotic measurements include temperature (°C) and relative humidity (%), at multiple vertical positions and time points.
  - Temporal coverage spans 2014–2017 for treatments, with block retrievals and abiotic measurements concentrated in 2016 (and drought period 2015–2017 for the drought experiment).

- Data quality, limitations, and considerations for reuse
  - Height measurements: height for blocks labeled as Top is not an exact value, which may affect height-specific analyses.
  - Experimental complexity: multiple overlapping treatments (ant suppression, termite suppression) and mesh types; careful alignment of treatment codes across datasets is required.
  - Mesh and block preparation: open/closed/drilled meshes influence macro-invertebrate access and microbial decay, requiring clear interpretation when reusing data.
  - Termite/ant suppression methods rely on specific baits and deployment schedules; documentation should be consulted to reproduce or compare treatments.
  - Abiotic data collected at fixed intervals and can be used to model environmental effects on decomposition, but cross-dataset alignment (dates, plots, heights) is essential.

- Practical guidance for data stewardship and reuse
  - Ensure metadata alignment across WoodBlocksData.csv, AbioticData.csv, and DroughtNondroughtWoodBlocksData.csv for integrated analyses (Plot, Treatment, Location, Tree_Set, Strata/Height, Date/time).
  - Maintain clear provenance references to data collection and interpretation responsibilities.
  - Document the exact meaning of derived fields (Weight_lost, Proportion, Fungal_damage, Termite_damage) and any data cleaning steps (e.g., removal of termite workings and soil prior to drying).
  - Provide notes on any deviations from protocol or missing data points to support reproducibility and proper interpretation.