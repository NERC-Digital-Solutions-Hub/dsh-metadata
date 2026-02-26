# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

- This dataset supports two experimental trials at Martin Down National Nature Reserve to assess strategies for reducing dense Brachypodium pinnatum and preventing expansion of sparse cover: 1) herbicide spraying experiment and 2) cut and graze experiment.
- Vegetation data were collected to compare pre-treatment baselines (2019) with post-treatment outcomes (2020–2022).

## Experimental design

- Herbicide spraying experiment
  - Three experimental blocks over dense B. pinnatum patches; each block has four plots (8 m × 5 m).
  - Four treatments per block: (i) spray and reseed, (ii) spray and no reseed, (iii) spray twice and reseed, (iv) spray twice and no reseed.
  - Glyphosate applications: 19 Sept 2019 (Roundup Biactive, 360 g l-1, 1:67) and 23 June 2020 (Rodeo, 360 g l-1, 5 l ha-1) for second spray.
  - Post-spray management included cutting/removal of dead material, and reseeding in relevant treatments.
  - Seeding (Sept 2020) at 160 g per plot (40 m2) with 80% Bromopsis erecta and 20% forbs.
  - Forbs selected as positive indicators for CG2/3 grassland or typical calcareous grassland species.
  - Common ragwort control by July 2021 treatment.

- Cut and graze experiment
  - One large plot (over sparser B. pinnatum) with nine plots (20 m × 18 m).
  - Three treatments: autumn cut and graze, spring cut and graze, and both spring and autumn cut and graze (with three replicates each).
  - Autumn treatment: cut and removal in early Sept; grazing 3–4 weeks later (1300–1400 sheep days).
  - Spring treatment: cut in April; grazing 3–4 weeks later (sheep days as above).

- Plot sizes
  - Herbicide experiment: 8 m × 5 m plots within 3 blocks.
  - Cut and graze experiment: 20 m × 18 m plots.

## Data collection and sampling

- Baseline surveys: Sept 2019 (before treatments).
- Post-treatment surveys: Aug/Sep 2020, 2021, 2022.
- Sampling design
  - Herbicide plots: five 50 cm × 50 cm quadrats per plot arranged along a W-shaped transect (approximately 1 m between quadrats; outer 50 cm excluded to avoid drift effects).
  - Cut and graze plots: seven quadrats per plot (five central in a diamond formation, plus two edge quadrats, avoiding outer 2 m).
- Measurements within each quadrat
  - Percentage cover: B. pinnatum, other vascular plants, bare ground.
  - Additional metrics: sward height and percentage cover of bryophytes, litter, thatch, seedlings, fungi.
  - Species-level data: presence/coverage for all recorded species (scientific names provided in data columns).
- Data handling
  - Surveys conducted by experienced field ecologists (same team across years).
  - Paper forms digitised into Excel; checked for anomalies (quality control).
  - Data stored in a single dataset: Vegetation_surveys_for_Brachypodium_experiments.csv.
  - Data fields include date, year, treatment, plot, quadrat, unique ID, sward height, species covers, and auxiliary cover metrics.

## Data structure and units

- File: Vegetation_surveys_for_Brachypodium_experiments.csv
- Key fields
  - Date (dd/mm/yyyy), Year (2019–2022)
  - Treatment_no, Treatment (as per Table 1)
  - Plot (Spray experiment 1–12; Cut & graze 13–21)
  - Quadrat (Spray 1–5; Cut & graze 1–7)
  - Unique_ID (Plot_Quadrat_Year)
  - Sward_height (cm)
  - Species columns (percentage cover per recorded species)
  - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi (percentage cover)
  - NA indicates missing data

## Seed mix and management details

- Seeded post-treatment in relevant spray treatments (Sept 2020) with a mixture including:
  - Bromopsis erecta (130 g per plot)
  - Forbs such as Agrimony, Kidney vetch, and others (as listed in Table 2) with specified weights per plot
- Forbs were selected to support calcareous grassland indicators
- Management actions included cuts in autumn or spring and subsequent sheep grazing, aimed at reducing B. pinnatum dominance while promoting target vegetation

## Quality control and data integrity

- Data collected by experienced ecologists; same personnel conducted all surveys to ensure consistency.
- Paper data sheets digitised and checked for anomalies.
- QA practices documented to ensure reliability of long-term monitoring data.

## Data management and accessibility

- Data are stored as a structured dataset and prepared for upload to appropriate data portals, enabling reuse and integration with other environmental monitoring datasets.
- The dataset aligns with standardized monitoring guidance (JNCC, 2004) for lowland grassland habitats.

## References

- JNCC (2004). Common Standards Monitoring Guidance for Lowland Grassland Habitats. Peterborough, UK.