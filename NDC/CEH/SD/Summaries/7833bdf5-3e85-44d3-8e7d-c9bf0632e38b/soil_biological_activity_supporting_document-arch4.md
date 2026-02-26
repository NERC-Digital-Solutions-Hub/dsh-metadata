# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Overview
- Dataset documenting soil biological activity after the 2016 Red Forest wildfire in the Chornobyl Exclusion Zone.
- Measurements taken at 23 study sites across three timepoints: September 2016, March 2017, and September 2017.
- Core components include bait lamina feeding activity (two independent readers), ambient soil conditions (DM, LOI, pH), and ambient dose rate.
- Field methods aligned with ISO 18311:2016 bait-lamina testing; data compiled to assess spatial and temporal patterns in soil fauna activity and potential links to burn severity and radiation exposure.
- Data collected as part of the REDFIRE project (NERC).

## Data files included
- Bait_Lamina_Summary.csv
  - Per-plot, per-site overview including location, burn history, ambient dose rate, soil DM, LOI, pH, deployment/collection dates, and bite metrics (e.g., Total_Bites, Bites_Per_Day, Days_Deployed).
- Reader_1_Bait_Lamina_September_2016.csv and Reader_2_Bait_Lamina_September_2016.csv
- Reader_1_Bait_Lamina_March_2017.csv and Reader_2_Bait_Lamina_March_2017.csv
- Reader_1_Bait_Lamina_September_2017.csv and Reader_2_Bait_Lamina_September_2017.csv
  - Each reader file contains per-plot, per-bait-lamina-strip data: replicate (1–16), bait_lamina_no, and aperture outcomes (1_top_hole through 16_bottom_hole) with values 1 (pierced), 0 (unpierced), or Missing.
- Abrasion strips data (embedded within Sept 2016 reader files)
- Tables 1 and 2 (descriptions of all column headings) are included to explain the dataset structure.

## Study sites and timing
- 23 sites located within the Chornobyl Exclusion Zone, sampled after a severe July 2016 wildfire that affected roughly 80% of the Red Forest.
- At each site, three 1x1 m plots with similar vegetation were identified (plot identifiers like 1.1, 1.2, 1.3, etc.).
- Sampling occasions: September 2016, March 2017, September 2017; some sites were not sampled at all timepoints due to flooding.
- Site metadata includes GPS coordinates (WGS84), vegetation description, burn extent, and ambient soil radiation measurements.

## Bait lamina method
- Bait lamina strips: ~155 x 6 x 1 mm PVC with 16 apertures (5 mm spacing), upper region void of apertures; bait composition: 70% cellulose, 25% finely ground wheat bran, 5% active charcoal.
- Insertion: strips deployed in a 4x4 grid per plot; top aperture just below soil surface; abrasion-control strips inserted/withdrawn in Sep 2016 to check damage from abrasion.
- Reading: strips read visually on an iPad with a light-table app; two readers conducted blind assessments to determine whether apertures were pierced (evidence of soil organism feeding) or unpierced.
- Data timing: deployment began around April 2016; primary reads occurred in September 2016, with follow-ups in March 2017 and September 2017.
- Data recorded include per-aperture piercing status, with separate tallies for apertures 1–4, 5–8, 9–12, and 13–16, plus totals and bite-per-day metrics (when applicable).

## Soil measurements and environmental context
- Soil dry matter (DM): determined by oven-drying sub-samples from five 10 cm soil cores per plot (bulk together for a DM estimate).
- Loss on Ignition (LOI): determined from sub-samples to estimate organic matter/soil combustion loss.
- Soil pH: measured on samples collected at designated times (pH data available for Sept 2016 and Sept 2017).
- Ambient dose rate: measured at plots in Sept 2016 using a MKS-01R radiometer.
- Sampling protocol included five cores per plot (corners and center) to provide representative subsamples.

## Data structure, metadata, and quality
- Column headings are exhaustively defined in Table 1 (Bait_Lamina_Summary.csv) and Table 2 (Reader_1/Reader_2 files).
- Geographic coordinates provided for all plots; dates recorded in DD/MM/YYYY format; units specified in accompanying descriptions.
- Data quality measures:
  - Bait lamina readings conducted blind by two readers to reduce bias.
  - Abrasion control strips included to check for non-biological abrasion effects.
  - Missing aperture data recorded as Missing.
  - ISO 18311:2016 standard followed for bait-lamina testing and interpretation.
- The dataset is part of a broader temporal series with prior data from 2005 and April 2016 documented in related works.

## References and context
- Methodology and prior datasets referenced in accompanying documentation (Barnett et al., 2021; Beresford et al., 2022).
- ISO standard: ISO 18311:2016, Soil quality - Bait-lamina test.
- Key methodological references: Kratz 1998; Allen 1974; Harrison & Bocock 1981.

## Funding and purpose
- REDFIRE project funded by the Natural Environment Research Council (NERC) Urgency grant NE/P015212/1.
- Data intended to support analyses of spatial and temporal patterns in soil biological activity in relation to fire impact and environmental conditions in the Chernobyl Exclusion Zone.