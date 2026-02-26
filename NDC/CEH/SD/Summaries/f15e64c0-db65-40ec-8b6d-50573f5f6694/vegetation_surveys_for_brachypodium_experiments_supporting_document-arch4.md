# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

## Purpose and context
- Investigates strategies to control tor-grass Brachypodium pinnatum in calcareous grasslands at Martin Down NNature Reserve.
- Part of two experimental trials: (1) herbicide spraying with reseeding vs not, and (2) cut and graze to reduce dense/sparse cover dynamics.
- References: Ridding et al. (under review) Practical strategies for the control of tor-grass and restoration of calcareous grassland.

## Experimental design

- Herbicide spraying experiment
  - Three blocks over dense B. pinnatum patches; each block has four plots (8 m × 5 m).
  - Treatments (randomized within blocks): 
    1) spray and reseed; 2) spray and no reseed; 3) spray twice and reseed; 4) spray twice and no reseed.
  - Herbicide: Roundup Biactive glyphosate (360 g l-1) first spray on 19 Sep 2019; second spray (if applicable) on 23 Jun 2020 with Rodeo glyphosate; both at 5 l ha-1 where applicable.
  - Post-spray management: cut and removal of dead material in Apr 2020; subsequent cut in Sep 2020; reseeding on relevant treatments.
  - Seeding: 160 g per plot, seed mix 80% Bromopsis erecta and 20% forbs (selected for calcareous grassland indicators).

- Cut and graze experiment
  - One large plot over sparser B. pinnatum cover, subdivided into nine plots (20 m × 18 m); three replicates of three treatments.
  - Treatments: autumn cut and graze; spring cut and graze; spring and autumn cut and graze.
  - Management: autumn cut in early Sep with sheep grazing started 3–4 weeks later; spring cut in Apr with 3–4 weeks until grazing; grazing around 1,300–1,400 sheep days per plot.

- Seed management
  - Common ragwort (Senecio jacobaea) cut in July 2021 to reduce seeding.

## Data collection and timing

- Baseline survey: early Sep 2019 (before treatments).
- Post-treatment surveys: Aug/Sep 2020, 2021, 2022.
- Sampling design per plot:
  - Spray experiment: five 50 cm × 50 cm quadrats per plot, approx. 1 m apart along a W-shaped transect; outer 50 cm avoided to minimize drift.
  - Cut and graze experiment: seven quadrats per plot arranged in a central diamond (five quadrats) plus two edge quadrats.
- Metrics recorded per quadrat:
  - Percentage cover of B. pinnatum, all other vascular plants, bare ground.
  - Additional attributes: sward height, bryophytes, litter, thatch, fungi, seedlings; and seedling presence for young vegetation.
  - Species-level data captured as percentage cover per taxon; NA indicates missing data.
- Data collection quality: performed by the same experienced ecologists across all surveys; paper forms digitized into Excel with anomaly checks.

## Data structure and units

- Data file: Vegetation_surveys_for_Brachypodium_experiments.csv.
- Key columns and definitions:
  - Date (survey date), Year (survey year, 2019–2022), Treatment_no (numeric treatment code), Treatment (treatment name), Plot (plot number), Quadrat (quadrats within each plot), Unique_ID (Plot_Quadrat_Year), Sward_height (cm).
  - Species columns: Achillea_millefolium, Viola_riviniana, Bryophyte (and other taxa) with corresponding percentage cover per quadrat.
  - Bare_ground, Thatch, Seedling, Litter, Fungi (percentage cover or presence) and NA for missing data.
- Data granularity: percent cover metrics at quadrat level; height in centimeters; multi-year longitudinal dataset aligned to treatment and plot structure.

## Data quality, governance, and provenance

- Provenance: linked to two experimental trials designed to test management strategies for B. pinnatum at Martin Down NNR.
- Data integrity: same ecologists conducted surveys across years; data sheets digitized and checked for anomalies.
- Metadata emphasis: includes detailed treatment mapping (numbers and names), plot and quadrat identifiers, sampling geometry, and seed mix composition.
- Standards and references: aligns with JNCC Common Standards Monitoring Guidance for Lowland Grassland Habitats (JNCC, 2004).

## Additional context and uses for data leaders

- Enables evaluation of long-term effects of herbicide vs. cutting strategies on B. pinnatum and associated calcareous grassland communities.
- Provides a structured framework for tracking data lineage, experimental treatments, spatial relocation (via dGPS), and multi-year vegetation responses.
- Useful for cross-study comparisons, restoration planning, and informing policy or management decisions by analyzing treatment efficacy, species responses, and changes in community composition over time.