# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Overview
- Datasets describe soil biological activity in the Chornobyl Exclusion Zone after a severe wildfire in July 2016.
- Sampling occurred at 23 study sites across three time points: September 2016, March 2017, and September 2017 (some plots with flooding limiting data collection on certain occasions).
- Primary method: bait lamina test to assess soil invertebrate feeding activity, complemented by soil physicochemical measurements (dry matter, LOI, pH) and ambient radiation dose rate.
- Data support focus: provides detailed metadata, standardized column definitions, and multi-source data to enable re-use and cross-plot comparisons.

## Data files included
- Bait_Lamina_Summary.csv: site and plot-level metadata, plot coordinates, burn history, ambient dose rate, soil DM, LOI, pH, and bait lamina deployment data summaries.
- Reader_1_Bait_Lamina_September_2016.csv; Reader_1_Bait_Lamina_March_2017.csv; Reader_1_Bait_Lamina_September_2017.csv: Reader 1 observations for bait lamina strips by plot and strip (16 strips per plot, with abrasion strips in 2016).
- Reader_2_Bait_Lamina_September_2016.csv; Reader_2_Bait_Lamina_March_2017.csv; Reader_2_Bait_Lamina_September_2017.csv: Reader 2 observations mirroring Reader 1 structure.
- Each Reader file includes: study plot, replicate number (1–16, plus abrasion strips in 2016), bait_lamina_no, hole-by-hole pierced/unpierced coding (1 or 0; “Missing” for lost strips).

## Study design and sites
- 23 study sites within the Chornobyl Exclusion Zone, located after a July 2016 wildfire in the Red Forest (~80% burnt).
- At each site, three 1x1 m plots with similar vegetation cover were surveyed (plots labeled e.g., 1.1, 1.2, 1.3, etc.).
- GPS coordinates (WGS84) provided for all plots; site descriptions of vegetation and burn extent included.
- Ambient dose rate measured at plots in September 2016 using a radiometer; not all sites used on all sampling occasions due to flooding.

## Bait lamina data collection and scoring
- Bait lamina strips: PVC strips (~155x6x1 mm) with 16 apertures arranged in a 4x4 grid, deployed with the top aperture just below the soil surface.
- Bait composition: 70% cellulose, 25% finely ground wheat bran, 5% active charcoal.
- Deployment: strips inserted at each plot in a 4x4 grid; one additional abrasion strip deployed/withdrawn in September 2016 to check for abrasion effects.
- Reading procedure: strips visually assessed after gentle cleaning, using an iPad with a light-table app; two readers conducted blind scoring.
- Scoring: each aperture scored as pierced (1) or unpierced (0); “Missing” used if a strip was not retrieved or lost.
- Output includes both aperture-level data (per strip) and aggregated metrics such as total bites and bites per day, across time points.

## Soil physicochemical measurements
- Soil samples collected from five 10 cm deep cores per plot (bulk, then homogenized).
- Measurements:
  - Soil dry matter (DM) estimated by oven-drying subsamples.
  - Loss on Ignition (LOI) determined to assess organic matter content.
  - Soil pH measured for September 2016 and September 2017.
- Note: DM measured at Sep 2016, Mar 2017, and Sep 2017; LOI and pH measured at Sep 2016 and Sep 2017.

## Data processing and outputs
- Bait lamina data include calculated summaries such as:
  - Total_Bites across all apertures per strip/deployment period.
  - Bites_Per_Day = Total_Bites / Days_Deployed.
  - Bites per aperture and per hole group (top 4, holes 1–4; 5–8; 9–12; 13–16; and aggregated 1–8, 9–16).
- The Bait_Lamina_Summary.csv provides plot-level and site-level context for use in cross-site analyses and replication of results.

## Data quality, limitations, and notes
- Two readers read each strip blind to reduce observer bias.
- Some plots were flooded, resulting in missing data for certain time points.
- “Missing” values are used where strips were not retrieved, and certain fields are not measured at all time points.
- Documentation includes explicit column definitions (Table 1 and Table 2 style descriptions) to support data interpretation and harmonization with other datasets.
- ISO 18311:2016 methodology referenced for bait lamina field procedures; LOI and DM/pH methods follow cited standard procedures.

## Usage notes and references
- Data intended to support analyses of post-fire soil biological activity in relation to environmental context (burn extent, soil properties) and ambient radiation exposure.
- Related publications:
  - Beresford et al. 2022: current ionising radiation doses in the Chernobyl Exclusion Zone and soil biological activity.
  - Barnett et al. 2021; 2022 data-related publications providing context and prior dataset comparisons.
  - ISO 2016 standard for bait lamina testing (ISO 18311:2016).
- Funding: REDFIRE project, Natural Environment Research Council (NE/P015212/1).