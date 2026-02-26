# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

## Overview
- Investigates management options for calcareous grasslands threatened by torgrass (Brachypodium pinnatum).
- Two experimental trials established at Martin Down NNR:
  - Herbicide spraying experiment
  - Cut and graze experiment
- Context and broader findings referenced in Ridding et al (under review).

## Experimental Design

### Herbicide spraying experiment
- 3 blocks; each block contains 4 plots (8 m x 5 m).
- Treatments (within each block): 
  1) spray and reseed
  2) spray and no reseed
  3) spray twice and reseed
  4) spray twice and no reseed
- Herbicide applications:
  - First spray: Roundup Biactive glyphosate (360 g l-1) at 1:67 dilution, 19 Sep 2019.
  - Second spray (if applicable): Rodeo glyphosate (360 g l-1) at 5 l ha-1, 23 Jun 2020.
- Post-spray management: cut and removal of dead material (Apr 2020); second spray and final cut/removal (Sept 2020).
- Seeding: relevant treatments include seeding at 160 g per plot (40 m2) using seed mix (80% Bromopsis erecta, 20% forbs).
- Forbs selected to indicate CG2/3 grassland or typical calcareous grassland species.

### Cut and graze experiment
- Large plot over sparser B. pinnatum cover; 9 plots (20 m x 18 m).
- Treatments (three replicates of each):
  - Autumn cut and graze (treatment 5)
  - Spring cut and graze (treatment 6)
  - Spring and autumn cut and graze (treatment 7)
- Grazing: sheep introduced 3–4 weeks after cutting; around 1300–1400 sheep days per season.

## Data Collection and Measurements
- Baseline vegetation survey: Sept 2019 (before treatments).
- Post-treatment surveys: Aug/Sep 2020, 2021, 2022.
- Survey method:
  - Spray experiment: five 50 cm × 50 cm quadrats per plot (≈1 m apart along a W transect), excluding outer 50 cm to reduce drift risk.
  - Cut and graze: seven quadrats per plot (diamond center of five plus two edge quadrats).
- Recorded data per quadrat:
  - % cover of B. pinnatum
  - % cover of all other vascular plants
  - % bare ground
  - Additional habitat metrics: sward height and various components (bryophytes, thatch, litter, fungi, seedlings)
  - Seedling presence and other descriptive data
- Data collection performed by experienced field ecologists; consistent team across surveys.
- Data recorded in Vegetation_surveys_for_Brachypodium_experiments.csv with standardized fields.

## Data Structure, Metadata and Access
- Core dataset: Vegetation_surveys_for_Brachypodium_experiments.csv.
- Key fields include:
  - Date, Year, Treatment_no, Treatment
  - Plot (Spray: 1–12; Cut & graze: 13–21), Quadrat
  - Unique_ID (Plot_Quadrat_Year)
  - Sward_height
  - Species-level columns for percentage cover
  - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi
  - NA indicates missing data
- Plot layout and relocation:
  - Relocation and precise positioning aided by Leica Zeno 20 RTK dGPS (±3 cm).
- Seed sowing details:
  - Seeds sown September 2020 for the spray experiment; species list and weights provided (e.g., Bromopsis erecta and various forbs).
- Standards and references:
  - Data collection aligned with JNCC Common Standards Monitoring Guidance for Lowland Grassland Habitats (2004).

## Quality Control and Governance
- Data collected by the same experienced ecologists across surveys to ensure consistency.
- Paper data sheets digitized to Excel with anomaly checks.
- Data structured to support clear interpretation and potential public sharing, with explicit metadata and definitions included in the dataset.

## Site Context and Timing
- Location: Martin Down National Nature Reserve.
- Focus: calcareous grasslands at risk from torgrass invasion and management restoration.
- Temporal scope: baseline survey in 2019; post-treatment monitoring through 2022.

## Seed Sowing Details (Table Context)
- September 2020 sowing for the spray experiment included a mix of grasses and forbs (e.g., Bromopsis erecta; Anthyllis vulneraria; Linum catharticum; Lotus corniculatus; etc.), with specified weights per plot.