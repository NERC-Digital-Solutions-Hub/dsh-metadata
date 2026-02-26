# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

## Background
- Calcareous grasslands are increasingly threatened by tor-grass (Brachypodium pinnatum).
- This dataset supports a study with two experimental trials at Martin Down National Nature Reserve:
  - herbicide spraying experiment
  - cut and graze experiment
- Related findings are discussed in Ridding et al (under review).

## Experimental design

### Herbicide spraying experiment
- Three experimental blocks over dense B. pinnatum patches; each block has four plots (8 m x 5 m).
- Treatments (randomised within each block): 
  1) spray and reseed
  2) spray and no reseed
  3) spray twice and reseed
  4) spray twice and no reseed
- Herbicides: Roundup Biactive glyphosate (initial spray 19 Sep 2019), second spray (23 Jun 2020) with Rodeo glyphosate; rate ~360 g L-1 active ingredient; application under low wind.
- Post-spray management: cut and removal of dead material (April 2020; September 2020); reseeding where applicable.
- Seeding: 160 g seed per plot (40 m2) with 80% Bromopsis erecta and 20% forbs; harvest seeds from Martin Down; July 2021 ragwort control by cutting.
- Seed species list provided (Table 2) for seeding.

### Cut and graze experiment
- One large plot over sparser B. pinnatum cover; nine sub-plots (20 m x 18 m).
- Three replicate treatments: autumn cut and graze, spring cut and graze, and spring + autumn cut and graze.
- Sheep grazing: approximately 1300–1400 sheep-days; autumn cutting occurs early September with grazing starting 3–4 weeks later; spring cutting in April with grazing 3–4 weeks later.

## Data collection

### Timeline
- Baseline vegetation surveys: Sept 2019 (before treatments).
- Post-treatment surveys: Aug/Sep 2020, 2021, 2022.

### Sampling protocol
- Spraying plots: five 50 cm x 50 cm quadrats per plot, along a W-shaped transect (~1 m apart), excluding outer 50 cm to reduce drift.
- Cut and graze plots: seven quadrats per plot (diamond center cluster plus two edge quadrats).
- Variables recorded per quadrat:
  - percentage cover of B. pinnatum
  - percentage cover of other vascular plants
  - bare ground
  - sward height
  - bryophyte cover
  - thatch
  - seedling cover
  - litter
  - fungi
- Data collection conducted by the same experienced ecologists; paper forms digitised into Excel with anomaly checks.

## Data structure and units

- Data file: Vegetation_surveys_for_Brachypodium_experiments.csv
- Key fields:
  - Date (survey date), Year (2019–2022)
  - Treatment_no and Treatment (see Table 1)
  - Plot (Spray experiment 1–12; Cut & graze 13–21)
  - Quadrat (Spray: 1–5; Cut & graze: 1–7)
  - Unique_ID (Plot_Quadrat_Year)
  - Sward_height (cm)
  - Species composition columns (full scientific names with percentage cover)
  - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi
  - NA indicates missing data

## Quality control

- Data collected by experienced ecologists; same team performed all surveys.
- Paper forms digitised to Excel and checked for anomalies.

## Context and references

- Data aligned with JNCC (2004) Common Standards Monitoring Guidance for Lowland Grassland Habitats.
- See Ridding et al. for broader context on practical strategies for B. pinnatum control and grassland restoration.