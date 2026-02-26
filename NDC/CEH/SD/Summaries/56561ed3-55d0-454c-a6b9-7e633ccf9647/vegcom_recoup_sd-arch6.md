# RECOUP-Moor Vegetation Community data: Methodology

## Field Site
- Stalybridge estate, Saddleworth Moor (Manchester, UK): blanket bog dominated by Calluna vulgaris and Eriophorum vaginatum.
- June 24, 2018: wildfire affected 18 km2, causing large-scale surface vegetation removal.

## Methods
- Experimental design: 10 plots established in Oct 2018 at the post-fire site, each 10 m x 10 m.
  - 5 plots with shallow (less severe) burn (S1–S5) and 5 with deep (more severe) burn (D1–D5).
  - A neighbouring unburned reference site (<2 km away) sampled with 5 plots (R1–R5) using the same procedure.
- Vegetation surveys:
  - 1 m x 1 m point quadrats with 1 cm intervals.
  - Two surveys per plot at random positions; results combined to produce one overall community per plot per survey time.
- Soil seed-bank sampling:
  - Peat samples taken from three random locations within each plot.
  - Each sample: ~5 cm diameter, 10 cm deep; combined to yield 0–5 cm (top) and 5–10 cm (bottom) depth samples per plot.
  - Reference site sampled with the same procedure (n = 5).
- Seed-bank processing (laboratory):
  - Samples transported to the University of Southampton; stored at ~5°C for 21 days.
  - Frost treatment at −20°C for 48 hours.
  - Mixed with ~1 L horticultural peat; spread on trays in a greenhouse.
  - Seedlings identified and removed; maintained for 12 weeks or until no new seedlings emerged.
  - Seed-bank counts adjusted for initial soil weight; each sample equates to 1 L of extracted peat soil.
  - Post-processing: seed-bank abundances standardized by soil weight; vegetation abundances left unstandardized.
- Outputs and potential use:
  - Data suitable for analyzing post-fire recovery, comparing burn severities (shallow vs deep) and reference conditions.
  - Supports generation of community composition profiles and seed-bank germination results for data products and dashboards.

## Variable Key (data structure)
- Plot_number / Plot_ID: identifies plot and burn type (S1–5, D1–5 for post-fire; R1–5 for reference).
- Survey: Abundance data from seed-bank (SB) or vegetation (Veg) surveys.
- Soil_layer: Top (T) or bottom (B) soil layer (seed-bank only).
- Sample_group: Reference or Post-Fire grouping.
- Weight_soil: Weight of extracted peat soil (g) (seed-bank only).
- Date: Date of sampling.
- Species_Latin: Latin species name.
- Abundance: Total individuals per sample (seed-bank tissue adjusted per 1 L of soil).
- Seed-bank / Raw_Abundance: Seed-bank abundances adjusted by soil weight; raw abundance is total per sample (not weight-adjusted).

## Species List (representative taxa)
- Betula pubescens (Moor birch)
- Calluna vulgaris (Common heather)
- Epilobium angustifolium (Rosebay willowherb/Fireweed)
- Epilobium hirsutum (Great willowherb)
- Erica tetralix (Bog heather)
- Eriophorum vaginatum (Hare's-tail cottongrass)
- Festuca rubra (Red fescue)
- Holcus lanatus (Yorkshire fog)
- Juncus bufonius (Toad rush)
- Juncus effusus (Soft rush)
- Rumex acetosa (Common sorrel)
- Vaccinium myrtillus (European blueberry)

(Note: The dataset encompasses both post-fire vegetation abundances and seed-bank germination data across multiple plots and depths, enabling comparative analyses of recovery dynamics and seed-bank contributions.)