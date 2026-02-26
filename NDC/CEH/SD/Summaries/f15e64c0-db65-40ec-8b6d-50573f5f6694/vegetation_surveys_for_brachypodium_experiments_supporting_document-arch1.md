# Vegetation surveys for experiments investigating Brachypodium pinnatum control at Martin Down National Nature Reserve

## Aims and context
- Calcareous grasslands threatened by tor-grass (Brachypodium pinnatum); this dataset supports two experimental trials to reduce dense B. pinnatum and prevent expansion of sparse cover.
- Related work: Ridding et al. (under review) Practical strategies for the control of tor-grass and restoration of calcareous grassland.

## Experimental design

- Herbicide spraying experiment
  - Three blocks; within each block four plots (8 m x 5 m).
  - Four treatments per block: 1) spray + reseed, 2) spray + no reseed, 3) spray twice + reseed, 4) spray twice + no reseed.
  - Herbicide: Roundup Biactive glyphosate (360 g/L) at 1:67 dilution; first spray 19 Sept 2019.
  - Post-spray management: cut and removal in April 2020; second spray 23 June 2020 with Rodeo glyphosate; cut/removal Sept 2020; reseeding relevant treatments.
  - Seeding: 160 g per plot; seed mix 80% Bromopsis erecta and 20% forbs (Table 2); forbs chosen as indicators of calcareous grassland or typical Martin Down species.
  - Ragwort control: common ragwort cut in July 2021.

- Cut and graze experiment
  - One large plot subdivided into nine plots (20 m x 18 m); three replicates of three treatments.
  - Treatments: 5) autumn cut and graze; 6) spring cut and graze; 7) spring and autumn cut and graze.
  - Grazing: sheep grazing 3–4 weeks after cutting; grazing period around one month (1300–1400 sheep days).

## Data collection and sampling design

- Baseline survey: September 2019 (before treatments) to establish starting conditions.
- Post-treatment surveys: late August/early September 2020, 2021, and 2022.
- Spray experiment sampling: five 50 cm x 50 cm quadrats per plot along a W-shaped transect; quadrats exclude outer 50 cm to limit spray drift.
- Cut and graze sampling: seven quadrats per plot (five in a central diamond, plus two at the edges) due to greater variability in B. pinnatum cover.
- Measurements within each quadrat: percent cover of B. pinnatum, all other vascular plants, bare ground; also recording of sward height, litter, litter integrity, and other vegetation attributes.

## Data collection quality and provenance

- Data collected by experienced field ecologists; the same ecologists conducted all surveys.
- Paper sheets digitised into Excel; data checked for anomalies.
- Data sources and workflows aimed at reproducibility and traceability; datasets intended to be discoverable with metadata.

## Data structure and contents

- Primary dataset: Vegetation_surveys_for_Brachypodium_experiments.csv.
- Key fields:
  - Date, Year, Treatment_no, Treatment
  - Plot (Spray: 1–12; Cut & graze: 13–21), Quadrat (Spray: 1–5; Cut & graze: 1–7)
  - Unique_ID (Plot_Quadrat_Year)
  - Sward_height
  - Species columns (Achillea millefolium, Viola riviniana, etc.) with percentage cover per quadrat
  - Bryophyte, Bare_ground, Thatch, Seedling, Litter, Fungi
  - NA indicates missing data
- Seed and species details (Table 2, seeds sown in September 2020 for the spray experiment) include Bromopsis erecta (major component) and a range of forbs; seed mix and weights per plot (seed rate: total 160 g per plot; 80% B. erecta, 20% forbs).

## Data use and accessibility

- Data intended to support analysis of treatment effects on B. pinnatum and associated vegetation communities over time.
- Data may be uploaded to portals with metadata to enhance discoverability, with transparent data sources and documentation.

## References and additional context

- JNCC (2004). Common Standards Monitoring Guidance for Lowland Grassland Habitats.
- Ridding et al. (under review): Practical strategies for the control of tor-grass and restoration of calcareous grassland.