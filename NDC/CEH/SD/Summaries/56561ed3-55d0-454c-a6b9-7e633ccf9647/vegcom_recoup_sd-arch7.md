# RECOUP-Moor Vegetation Community data: Methodology

## Overview for GIS Specialists
- Document describes field-based collection of post-fire vegetation and seed-bank data on a blanket bog near Manchester (Saddleworth Moor), with 10 plots (10 m x 10 m).
- Data include vegetation surveys, soil seed-bank sampling (depths 0–5 cm and 5–10 cm), and a reference unburned site within 2 km.
- Data are designed to enable map-based analyses of post-fire recovery, seed-bank versus vegetation dynamics, and burn-severity effects.

## Field Site
- Location: Stalybridge estate on Saddleworth Moor, a blanket bog near Manchester, UK.
- Pre-fire vegetation dominated by Calluna vulgaris and Eriophorum vaginatum.
- Fire: June 24, 2018; burn affected approx. 18 km2 and caused large-scale surface vegetation loss.

## Methods
- Plot design: 10 plots (10 m x 10 m); 5 plots with shallow burn (S1–S5) and 5 plots with deep burn (D1–D5). A neighboring unburned reference site (R1–R5) within 2 km sampled similarly.
- Vegetation surveys: 1 m x 1 m point quadrats with 1 cm interval measurements; two surveys per plot at random positions; results combined to yield one overall vegetation community per plot per survey time.
- Seed-bank sampling: peat samples collected at three random locations per plot, 0–5 cm (top) and 5–10 cm (bottom). Three samples per plot aggregated to one seed-bank sample per depth. Seed-bank sampling replicated at the reference site using the same procedure.
- Storage and treatment: samples stored at ~5°C for 21 days, frost-treated at -20°C for 48 hours, then mixed with ~1 L horticultural peat and placed on trays in a greenhouse. Seedlings emerged were identified and removed; the process lasted 12 weeks.
- Data processing: total species counts adjusted to account for initial soil weight variations; seed-bank data standardized to 1 L of extracted peat soil; vegetation abundances left unstandardized.

## Variable Key (Data Structure)
- Plot_number / Plot_ID: Distinguishes plots and replicates; S1–S5 = shallow burn, D1–D5 = deep burn, R1–R5 = unburned/reference.
- Survey: Indicates whether data come from seed-bank (SB) or vegetation surveys (Veg).
- Soil_layer: Top soil layer (T) or bottom soil layer (B) for seed-bank data.
- Sample_group: Reference or Post-Fire grouping (seed-bank only).
- Weight_soil: Weight of extracted peat soil (g) for seed-bank samples.
- Date: Sampling date.
- Species_Latin: Latin species name.
- Abundance: Total individuals per sample (seed-bank data adjusted for weight; vegetation data unchanged).
- Seed-bank / Raw_Abundance: Seed-bank values relative to 1 L of soil; raw counts not standardized by weight (vegetation data not standardized by weight).

## Species List (Representative taxa included in the study)
- Betula pubescens – Moor birch
- Calluna vulgaris – Common heather
- Epilobium angustifolium – Rosebay willowherb / Fireweed
- Epilobium hirsutum – Great willowherb
- Erica tetralix – Bog heather
- Eriophorum vaginatum – Hare's-tail cottongrass
- Festuca rubra – Red fescue
- Holcus lanatus – Yorkshire fog
- Juncus bufonius – Toad rush
- Juncus effusus – Soft rush
- Rumex acetosa – Common sorrel
- Vaccinium myrtillus – European blueberry

## GIS-Relevant Considerations
- Spatial units: 10 plots provide a discrete framework for mapping burn severity and post-fire recovery at a fine scale.
- Data layers: vegetation community composition (per plot), seed-bank composition by depth (top vs bottom), and burn-status (shallow, deep, reference).
- Temporal aspects: multiple survey times per plot allow potential time-series mapping of recovery trajectories (subject to available time-stamped data).
- Data integration: seeds vs. standing vegetation enable analysis of lag effects and potential reseeding from the seed bank; data normalized to 1 L for seed-bank facilitates comparability across plots.
- Quality and standards: explicit data fields (Plot_ID, Survey, Soil_layer, Date, Abundance) support consistency and GIS compatibility; note potential data gaps due to sample weights and replication limited to 10 plots.

## Data Provenance and Usage Notes
- Fieldwork conducted October 2018 for plot establishment; post-fire conditions reflect a near-initial recovery stage following the 2018 fire.
- Samples stored and processed at the University of Southampton; detailed laboratory treatment and seedling emergence protocol described.
- The dataset enables comparing post-fire vegetation with an unburned reference and to examine how seed-bank depth and burn severity influence recovery.