# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Overview
- Dataset describing soil biological activity in the Chornobyl Exclusion Zone following the July 2016 Red Forest wildfire.
- Measurements taken at 23 study sites across three sampling occasions: September 2016, March 2017, and September 2017 (flooding affected availability at some sites/dates).
- Core components include bait lamina feeding activity data, site and plot descriptions, and soil physico-chemical measurements (dry matter, LOI, pH).
- Data intended for GIS-based visualization and analysis of spatial patterns in soil biological activity in a post-wildfire, post-accident context.

## Data files and structure
- The file provides column headings/definitions for:
  - Bait_Lamina_Summary.csv
  - Reader_1_Bait_Lamina_September_2016.csv
  - Reader_1_Bait_Lamina_March_2017.csv
  - Reader_2_Bait_Lamina_September_2016.csv
  - Reader_2_Bait_Lamina_March_2017.csv
  - Reader_2_Bait_Lamina_September_2017.csv
- Also includes an overview of sites and details on bait lamina, soil dry matter (DM), Loss on Ignition (LOI), and soil pH.
- Data descriptions cover plot-level information (locations, burn status, dose rate) and bait lamina readings collected by two blind readers.

## Study sites and field context
- 23 study sites located within the Chornobyl Exclusion Zone, established after the 2016 Red Forest wildfire (≈80% burn extent).
- Not all sites used on all sampling occasions due to flooding.
- Each site has GPS coordinates (WGS84) and vegetation cover descriptions; ambient soil surface dose rates were estimated in September 2016.
- Site-level details are provided in Bait_Lamina_Summary.csv.

## Bait lamina method and data collection
- Bait lamina strips: approx. 155x6x1 mm PVC with sixteen 5 mm-interval apertures, filled with a bait mixture (70% cellulose, 25% ground wheat bran, 5% active charcoal).
- Field procedure (ISO 18311:2016) involved inserting strips into ground in a 4x4 grid per plot (three 1x1 m plots per site); top aperture placed just below soil surface.
- Some additional strips (and abrasion strips) were inserted/withdrawn in September 2016 to check for abrasion effects.
- Post-deployment, strips were read visually on an iPad with a light-table app; each strip was read blind by two readers (Reader 1 and Reader 2).
- Scoring: each aperture scored as pierced (1) or unpierced (0). “Missing” used if a strip was not retrieved or lost.
- Data capture includes per-strip readings for each plot: bait lamina number, replicate number (1–16), and per-aperature pierced/unpierced data.
- Abrasion strips are labeled separately in the readers’ CSVs.

## Bait lamina data structure and metrics
- Data include per-plot, per-strip, per-reader bite observations across sampling campaigns.
- Bites are aggregated into:
  - Total_Bites for each campaign (September 2016, March 2017, September 2017).
  - Bites_Per_Day calculated as Total_Bites divided by Days_Deployed.
- Site/Plot identifiers follow a 1.x, 2.x, etc. scheme for site and plot numbers.
- Key dates:
  - Date_Out (when bait lamina were inserted)
  - Date_Of_Collection (when retrieved)
  - Days_Deployed (duration of deployment)
- Separate columns track bites in subsets of apertures (top 1-4, 5-8, 9-12, 13-16) and combined groups (1-8, 9-16).
- Data include potential Flooded status notes when plots were inaccessible.

## Soil physical-chemical measurements
- Soil dry matter (DM) determined from five cores per plot (bulk sample) to estimate DM content.
- Loss on Ignition (LOI) measured to assess soil organic/inorganic content.
- Soil pH measured at specified campaigns (September 2016 and September 2017).
- Measurements follow established methods (Allen 1974; Harrison & Bocock 1981; ISO 2016).

## Data quality, provenance, and references
- Two independent readers assess each bait lamina strip to reduce observer bias.
- Abrasion control strips deployed to verify non-dietary abrasion effects.
- Data are part of the REDFIRE project and linked to related datasets and papers:
  - Beresford et al. 2022 (current ionising radiation doses and soil activity)
  - Barnett et al. 2021 (soil biological activity in 2005 and 2016)
  - Related data descriptors in EIDC with DOIs provided in the documentation.
- ISO 18311:2016 standard followed for bait lamina methodology.

## GIS relevance and potential applications
- The dataset provides geo-referenced plots with precise coordinates, burn status, ambient dose rates, and soil properties, enabling:
  - Spatial analysis of soil biological activity across fire-affected and radiation contexts.
  - Visualization of AP aperture piercing data as raster or point-based maps.
  - Integration with other environmental layers (vegetation cover, soil properties, radiological exposure) for risk assessment and ecological modelling.

## References and funding
- Funding: REDFIRE project, Natural Environment Research Council (NE/P015212/1).
- Key references:
  - ISO 18311:2016 (bait-lamina test)
  - Allen, S.E. 1974 (soil chemical analysis)
  - Harrison & Bocock 1981 (LOI/bulk density)
  - Kratz 1998 (bait-lamina test overview)
  - Beresford et al. 2022; Barnett et al. 2021 (dataset context and related findings)