# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

## Background
- Calcareous grasslands are increasingly threatened by torgrass (Brachypodium pinnatum); no clear consensus on best management yet.
- Study established two experimental trials at Martin Down National Nature Reserve to test methods for reducing dense B. pinnatum and preventing expansion of sparse cover: (1) herbicide spraying experiment and (2) cut and graze experiment.
- Related findings discussed in Ridding et al (under review).

## Experimental design
- Herbicide spraying experiment
  - Three experimental blocks over dense B. pinnatum; each block has four plots (8 m × 5 m).
  - Plots precisely relocatable year to year using a Leica Zeno 20 RTK dGPS (±3 cm).
  - Four treatments per block: spray and reseed; spray and no reseed; spray twice and reseed; spray twice and no reseed.
  - Herbicide applications: Roundup Biactive glyphosate (360 g l-1) on 19 Sep 2019; a second spray on 23 Jun 2020 with Rodeo glyphosate (360 g l-1); additional cut/removal and reseeding in 2020.
  - Seeding: seed mix applied at 160 g per plot (40 m2) with 80% Bromopsis erecta and 20% forbs; forbs chosen as indicators for CG2/3 grassland or typical calcareous grassland species.
  - Ragwort reduction: common ragwort cut in July 2021.

- Cut and graze experiment
  - One large plot over sparser B. pinnatum; nine plots measuring 20 m × 18 m.
  - Three treatments with three replicates: autumn cut and graze; spring cut and graze; both spring and autumn cut and graze.

- Seed mix and sowing (for spray treatments)
  - Seed weights per plot listed (Table 2); seed mix includes Bromopsis erecta and various forbs (values per species provided in dataset).
  - Seeds sown in September 2020 for the spray experiment.

## Data collection
- Timeline
  - Baseline vegetation surveys: September 2019 (before treatments).
  - Post-treatment surveys: August/September 2020, 2021, and 2022.
- Plot and quadrat layouts
  - Spraying experiment: five 50 cm × 50 cm quadrats per plot selected along a W-shaped transect; outermost 50 cm avoided to reduce drift.
  - Cut and graze experiment: seven quadrats per plot (five central diamond-form quadrats 5 m apart; plus two edge quadrats).
- Measurements within each quadrat
  - Percentage cover of B. pinnatum.
  - Percentage cover of all other vascular plants.
  - Bare ground, plus additional habitat components (thatch, seedling, litter, fungi, bryophytes).
  - Sward height (cm).
- Data collection
  - Conducted by experienced field ecologists; same team across surveys.
  - Paper forms digitised into Excel; checked for anomalies.

## Data structure and units
- Dataset: Vegetation_surveys_for_Brachypodium_experiments.csv
- Key fields
  - Date (dd/mm/yyyy), Year, Treatment_no, Treatment
  - Plot (Spray experiment: 1–12; Cut & graze: 13–21)
  - Quadrat (Spray: 1–5; Cut & graze: 1–7)
  - Unique_ID (Plot_Quadrat_Year)
  - Sward_height (cm)
  - Species columns: percentage cover for each species (e.g., Achillea millefolium, Viola riviniana, etc.)
  - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi
  - NA indicates missing data
- Sampling details
  - Spray experiment: five quadrats per plot
  - Cut & graze: seven quadrats per plot

## Seed mix and sowing details
- Seed mix composition and per-plot weights (as listed in Table 2) for September 2020 sowing in the spray experiment
- Predominant seed included Bromopsis erecta (80%) with a selection of forbs to support calcareous grassland indicators
- Seeding performed after herbicide treatment; ragwort control implemented through subsequent cutting

## Quality control and standards
- Data collected by the same experienced ecologists to ensure consistency
- Paper records digitised and quality-checked for anomalies

## Data availability and usage
- Data enable spatially explicit analysis of B. pinnatum cover dynamics across treatments and time
- Suitable for GIS-based mapping of cover change by plot and quadrat, time-series analysis, and integration with RTK-GPS coordinates for precise relocation and spatial trend assessment

## References
- JNCC, 2004. Common Standards Monitoring Guidance for Lowland Grassland Habitats. Peterborough, UK.