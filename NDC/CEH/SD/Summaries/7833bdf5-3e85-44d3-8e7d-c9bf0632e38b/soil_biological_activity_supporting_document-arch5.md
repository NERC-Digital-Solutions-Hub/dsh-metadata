# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Overview
- Study of soil biological activity after the 2016 Red Forest wildfire in the Chornobyl Exclusion Zone (CZ) using bait lamina tests.
- Sampling at 23 study sites across three time points: September 2016, March 2017, and September 2017 (some plots affected by flooding limited data collection).
- Data include site and plot descriptions, bait lamina bite readings by two blind readers, and soil properties (dry matter, loss on ignition, pH) and ambient radiation levels.
- Documentation aligns with ISO 18311:2016 bait-lamina methodology; dataset described with extensive column-level metadata to enable reuse.

## Data files included
- Bait_Lamina_Summary.csv
- Reader_1_Bait_Lamina_September_2016.csv
- Reader_1_Bait_Lamina_March_2017.csv
- Reader_2_Bait_Lamina_September_2016.csv
- Reader_2_Bait_Lamina_March_2017.csv
- Reader_2_Bait_Lamina_September_2017.csv
- Reader_1_Bait_Lamina_September_2017.csv
- An overview of sites (detailed in Bait_Lamina_Summary.csv) and descriptions of bait lamina, soil dry matter (DM), Loss on Ignition (LOI) and pH measurements
- Table 1: Column heading explanations for Bait_Lamina_Summary.csv
- Table 2: Column heading explanations for reader files

## Study design and sampling
- 23 study sites within the Chornobyl Exclusion Zone, investigated after the 2016 wildfire in the Red Forest (approximately 80% burned).
- At each site, three 1x1 m plots with similar vegetation cover were identified (plots coded like 1.1, 1.2, 1.3, etc.).
- Data collection occurred on three sampling occasions (Sept 2016, Mar 2017, Sept 2017); not all sites used at every occasion due to flooding.
- Ambient soil dose rates were measured at plots in Sept 2016.

## Bait lamina methodology
- Bait lamina strips: ~155x6x1 mm PVC with 16 apertures (5 mm apart) starting 10 cm from the bottom; bait composition: 70% cellulose, 25% ground wheat bran, 5% active charcoal.
- Strips inserted in a 4x4 grid per plot; top aperture just below soil surface.
- Abrasion checks: some additional strips inserted/withdrawn in Sept 2016 to check abrasion effects.
- Reading: strips read blind by two readers (Reader 1 and Reader 2) using an iPad/tablet; scores: pierced (1) or unpierced (0); “Missing” used if a strip was not retrieved.
- Data handling: abrasion strips labeled separately; results from each reader combined per hole and per strip.

## Measured variables
- Bait lamina readings: per strip, per reader; includes 16 holes per strip (holes 1–16) with top and bottom hole designations.
- Bites data: Totals and bites per day calculated for various time frames (e.g., Total_Bites_September_2016, Bites_Per_Day_September_2016, etc., and similarly for March 2017 and September 2017).
- Site and plot metadata: Plot, Plot_Location, GPS coordinates (latitude/longitude in WGS84), burn history, and field notes.
- Soil and environmental measurements: ambient dose rate (µSv/h) at Sept 2016, soil percent dry matter (DM), soil Loss on Ignition (LOI), and soil pH measured at specified times (DM, LOI, pH across Sept 2016, Sept 2017).
- Data structure specifics: for each reader file, Replicate_no identifies 16 bait lamina strips per plot; abrasion strips included in Sept 2016 data.

## Data structure and column descriptions
- Bait_Lamina_Summary.csv: high-level plot/site descriptors, environmental context (burn level, ambient dose rate, DM, LOI, pH), and timing-related fields (dates deployed/collected, etc.).
- Reader_X_Bait_Lamina_YYYY.csv: per-reader bite data for each sampling event; columns include Reader, Plot, Replicate_no, Bait_lamina_no, and 16 hole readings (holes 1_top_hole through 16_bottom_hole) with values 1 (pierced), 0 (unpierced), or Missing.
- Columns include specific codes for borehole status, date fields, and derived metrics (e.g., Total_Bites, Bites_Per_Day).

## Data quality and provenance
- Two independent blind readers per plot per sampling occasion to ensure unbiased assessment.
- Use of ISO 2016 bait-lamina protocol to standardize methodology across sites and times.
- Documentation provides detailed definitions for each column, unit descriptions, and data coding (including Missing values).
- References to previous related datasets and publications for context (e.g., Barnett et al. 2021; Beresford et al. 2022; ISO 18311:2016; prior bait-lamina datasets).
- Funding: REDFIRE project (NERC Urgency grant NE/P015212/1).

## Spatial and temporal coverage
- Temporal: three sampling occasions – September 2016, March 2017, September 2017.
- Spatial: 23 study sites within the Chornobyl Exclusion Zone; plots per site with precise GPS coordinates (WGS84, decimal degrees) provided in the dataset.

## Limitations and context
- Some sites not used on all sampling occasions due to flooding; this affects data completeness across time points.
- Missing values used where strips were not retrieved or data could not be collected.
- Some data fields are not measured at all time points (e.g., certain environmental variables measured only in Sept 2016 and Sept 2017).

## Uses and governance
- Rich, well-documented dataset suitable for secondary analysis of soil invertebrate feeding activity in relation to fire impact, radiation exposure, and soil properties.
- Supported by detailed metadata, standardized measurement protocols, and access to both raw reader data and summary metrics.
- Relevant for researchers and data stewards aiming to store, share, and reuse large, multi-temporal ecological datasets with clear data provenance.
- Related outputs (publications and datasets) provide analytical context and validation for reuse.