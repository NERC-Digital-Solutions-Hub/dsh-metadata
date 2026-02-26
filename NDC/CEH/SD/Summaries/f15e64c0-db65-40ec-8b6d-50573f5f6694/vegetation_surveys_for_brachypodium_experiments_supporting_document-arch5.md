# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

- Purpose and context
  - Investigates management of calcareous grasslands threatened by tor-grass (Brachypodium pinnatum) through two experimental trials at Martin Down National Nature Reserve: 1) herbicide spraying with reseeding, and 2) cut and graze strategies.
  - This dataset supports assessment of treatment effects on vegetation composition over time (2019 baseline, 2020–2022 post-treatment).

- Experimental design
  - Herbicide spraying experiment
    - Three blocks over dense B. pinnatum; each block has four plots (8 m x 5 m).
    - Treatments (randomized within blocks): 
      1) spray and reseed; 2) spray and no reseed; 3) spray twice and reseed; 4) spray twice and no reseed.
    - Herbicide applications: Roundup Biactive (Sept 19, 2019) and Rodeo (June 23, 2020) for second spray; subsequent cut/removal and reseeding (Sept 2020).
    - Seeding: 160 g per plot (40 m2) with 80% Bromopsis erecta and 20% forbs.
    - Forbs selected as indicators for calcareous grassland or typical Martin Down species; common ragwort targeted for control in 2021.
  - Cut and graze experiment
    - One large plot with nine sub-plots (20 m x 18 m); three replicates of three treatments.
    - Treatments: autumn cut and graze; spring cut and graze; spring and autumn cut and graze.
    - Grazing: sheep, 1300–1400 sheep days, starting 3–4 weeks after cutting.

- Data collection and sampling design
  - Baseline vegetation surveys conducted in September 2019; post-treatment surveys in 2020, 2021, and 2022.
  - Spray experiment: five 50 cm x 50 cm quadrats per plot (along a W-shaped transect), avoiding outer 50 cm to reduce drift risk.
  - Cut and graze experiment: seven quadrats per plot (five in a central diamond, plus two on edges) to capture variability.
  - Recorded metrics per quadrat: percent cover of B. pinnatum, all other vascular plants, bare ground; additional tallies for sward height, bryophyte cover, litter, thatch, seedlings, fungi, and a combined species-by-species cover matrix.

- Data structure and content
  - Data file: Vegetation_surveys_for_Brachypodium_experiments.csv
  - Key fields and structure:
    - Date, Year: survey date and survey year (2019–2022)
    - Treatment_no, Treatment: numeric and descriptive treatment identifiers
    - Plot: plot number (Spray: 1–12; Cut & graze: 13–21)
    - Quadrat: quadrat number within plot (Spray: 1–5; Cut & graze: 1–7)
    - Unique_ID: concatenation of Plot_Quadrat_Year
    - Sward_height: height of the sward (cm)
    - Species columns: percentage cover for each listed species; includes Achillea millefolium, Viola riviniana, etc.
    - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi: percentage cover or presence indicators
    - NA: indicates missing data
  - Species composition and abundance data are recorded as percentage cover within each quadrat.

- Seed mix and species included
  - Sept 2020 sowing in the spray experiment included 15 g Agrimonia eupatoria, 5 g Anthyllis vulneraria, 1.24 g Briza media, 130 g Bromopsis erecta, 0.0 g Cirsium acaule, 0.0 g Filipendula vulgaris, 0.0 g Galium verum, 0.0 g Helianthemum nummularium, 0.0 g Leontodon hispidus, 0.0 g Linum catharticum, 0.0 g Lotus corniculatus, 0.0 g Primula veris per plot (weight distribution as listed in Table 2).

- Data quality and provenance
  - Collected by experienced field ecologists; the same team conducted all surveys to ensure consistency.
  - Paper data sheets were digitised into Excel and checked for anomalies.
  - The methodology and context are aligned with JNCC Common Standards for Lowland Grassland Monitoring (JNCC, 2004); further context provided in Ridding et al. (under review).

- Governance, access and context
  - Dataset captures multi-year vegetation responses to management treatments; intended to support evaluation of control strategies for B. pinnatum and restoration of calcareous grassland.
  - Data are organized for reuse in ecological meta-analysis and management planning; linked context available in the associated under-review publication.