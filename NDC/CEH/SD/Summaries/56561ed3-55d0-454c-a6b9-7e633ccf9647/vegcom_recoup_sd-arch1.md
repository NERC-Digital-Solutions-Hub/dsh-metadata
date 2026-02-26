# RECOUP-Moor Vegetation Community data: Methodology

## Overview
- Study location: Stalybridge estate, Saddleworth Moor (blan ket bog near Manchester, UK). A wildfire on June 24, 2018 burned 18 km2 and removed surface vegetation.
- Vegetation context: Dominated by Calluna vulgaris and Eriophorum vaginatum.
- Aim: Track recovery of the vascular plant community and seed-bank composition after fire, comparing shallow vs deep burn severity and including an unburned reference site.

## Study design and field methods
- Plot layout: 10 plots, each 10 m x 10 m. Five plots experienced a shallower burn (S1-5) and five deeper burns (D1-5); all plots had surface vegetation removed exposing bare peat.
- Vegetation surveys: 1 m x 1 m point quadrats with 1 cm intervals, conducted twice per plot at random positions; results combined to yield a single community assessment per plot at each survey time.
- Seed-bank sampling: soil peat samples collected from three random locations within each plot. For seed-bank analyses, samples were taken from two depths per plot: 0–5 cm (top) and 5–10 cm (bottom). An unburned reference site (<2 km away) was sampled using the same procedure (R1-5).
- Reference to post-fire comparison: Each plot’s post-fire soil samples were complemented by a reference sample set to enable comparison of seed-bank and vegetation responses.

## Laboratory processing and germination experiment
- Storage and treatment: Samples transported to the University of Southampton and stored at approximately 5°C for 21 days, followed by frost treatment at -20°C for 48 hours.
- Seedling emergence experiment: Samples mixed with about 1 L of horticultural peat and spread on trays in a greenhouse. Seedlings that emerged were identified and removed. The experiment ran for 12 weeks or until no new seedlings emerged.
- Normalization: Seed-bank results were adjusted to account for variations in initial soil weight, with each sample equivalent to 1 L of extracted peat soil. Seed-bank values are normalized to 1 L; vegetation abundances remain unadjusted (raw abundances reported separately).

## Variables and data structure
- Plot identifiers: Plot_number; Plot_ID (S1-5 = shallow burn, D1-5 = deep burn, R1-5 = unburned/reference)
- Survey type: Survey (Veg for vegetation surveys, SB for seed-bank surveys)
- Soil layer: Soil_layer (T = top 0–5 cm, B = bottom 5–10 cm; seed-bank only)
- Sample grouping: Sample_group (Reference or Post-Fire)
- Weight control: Weight_soil (g) for seed-bank samples
- Date: Date of sampling
- Species data: Species_Latin (Latin species name); Abundance (total individuals per sample)
- Data notes: Seed-bank Abundance is normalized to 1 L of soil; Raw_Abundance is unstandardized; Vegetation abundances are unchanged

## Species list
- Betula pubescens — Moor birch
- Calluna vulgaris — Common heather
- Epilobium angustifolium — Rosebay willowherb/Fireweed
- Epilobium hirsutum — Great willowherb
- Erica tetralix — Bog heather
- Eriophorum vaginatum — Hare's-tail cottongrass
- Festuca rubra — Red fescue
- Holcus lanatus — Yorkshire fog
- Juncus bufonius — Toad rush
- Juncus effuses — Soft rush
- Rumex acetosa — Common Sorrel
- Vaccinium myrtillus — European blueberry