# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Overview and aims
- Document describes a dataset and its structure for assessing soil biological activity using the bait lamina test in the Chornobyl Exclusion Zone (CZ) after the 2016 Red Forest wildfire.
- Aims align with monitoring framework goals: identifying environmental health measures to scrutinise policy, evaluate decisions, and inform future actions.
- Study design spans three sampling occasions: September 2016, March 2017, and September 2017, with data on soil properties, radiation exposure, and biotic activity.

## Data files and schema (data governance, metadata, and QA)
- Core data files included:
  - Bait_Lamina_Summary.csv: per-plot summaries and metadata.
  - Reader_1_Bait_Lamina_September_2016.csv; Reader_2_Bait_Lamina_September_2016.csv; Reader_1_Bait_Lamina_March_2017.csv; Reader_2_Bait_Lamina_March_2017.csv; Reader_1_Bait_Lamina_September_2017.csv; Reader_2_Bait_Lamina_September_2017.csv: raw bite observations from two readers.
- Column headings explained (Table 1 and Table 2 style descriptions):
  - Plot identifiers (site, plot), location coordinates (latitude/longitude), burn status, ambient dose rate, soil dry matter (DM), LOI, pH, and date-related fields for each deployment and collection event.
  - Bait lamina-specific fields: bait lamina number (1–16 and abrasion strips), top/middle/bottom hole bite indicators for each reader, including “Missing” if a strip was not retrieved.
  - Derived fields: Total_Bites, Bites_Per_Day, Date_Out, Date_Of_Collection, Days_Deployed, and holes grouped by aperture sets (1–4, 5–8, 9–12, 13–16, etc.) and overall subscores (e.g., Total_Bites_September_2016).
- Data quality and governance features:
  - Two readers read strips blind to site/plot to reduce bias.
  - Abbreviation of missing data with explicit markers.
  - Documentation notes provenance, methodology, and measurement standards (ISO 18311:2016; Allen 1974; Harrison & Bocock 1981).
  - Datasets linked to prior and subsequent studies; public sharing considerations addressed; data provenance and dataset origins described.

## Study sites and sampling design
- 23 study sites located within the CZ, established after the July 2016 wildfire (Red Forest burn ~80%).
- Three 1x1 m plots per site with similar vegetation cover; plots at each site within ~30 m of one another.
- Sampling occasions affected by flooding; not all sites used in every occasion (Sept 2016, Mar 2017, Sept 2017).
- Site-level data include GPS coordinates, vegetative cover descriptions, burn extent, and ambient soil dose rates measured at the soil surface.

## Bait lamina methodology
- Bait lamina strips: approx. 155x6x1 mm PVC with sixteen 5 mm-spaced apertures starting 10 cm from the tip; top 70 mm of the strip unperforated.
- Bait composition: 70% cellulose, 25% ground wheat bran, 5% active charcoal.
- Field application following ISO 18311:2016:
  - Strips inserted in a 4x4 grid per plot; top aperture slightly below soil surface.
  - An abrasion set (additional strips) inserted/withdrawn in Sep 2016 to check for abrasion effects.
- Reading protocol:
  - Strips cleaned and read visually on an iPad with a light-table app.
  - Scoring: pierced (1) or unpierced (0) per aperture; “Missing” used where strips were not retrieved.
  - Reading performed blind by two readers (Reader 1 and Reader 2).
- Data outputs include per-strip bite statuses and aggregated bite totals per plot, per time point, and per aperture grouping.

## Soil properties and ancillary measurements
- Soil sampling and analysis:
  - At each plot: five 10 cm deep soil cores (2.5 cm diameter) collected, bulked, and homogenised.
  - Sub-samples processed for:
    - Soil dry matter (DM) via oven-drying to estimate DM percentage.
    - Loss on Ignition (LOI) following Harrison & Bocock (1981) to estimate organic content.
    - pH determined using standard methods (Allen 1974).
- Temporal coverage:
  - DM measured in September 2016, March 2017, and September 2017.
  - pH and LOI measured in September 2016 and September 2017.
- Ambient dose rate:
  - Measured at plots in September 2016 using an ATOMEX AT6130 radiometer.

## Data handling, timing, and limitations
- Deployment and collection timing:
  - Strips deployed primarily in April 2016; sampling at three key time points (Sept 2016, Mar 2017, Sept 2017).
  - Some data records note flooding or plot-specific issues affecting deployment/collection windows.
- Data transformations and derived metrics:
  - Calculations include Bites Per Day (Total Bites / Days Deployed) and site/plot-level aggregations.
- Limitations for monitoring/framework use:
  - Data gaps due to environmental events (flooding) and missing strips.
  - Potential data quality issues from missing apertures and need for careful metadata to verify suitability for policy evaluation.
  - Metadata completeness (e.g., precise burn extent, organic matter context) necessary for alignment with broader monitoring programs.

## Context, references, and funding
- Standards and methods cited:
  - ISO 18311:2016 (bait-lamina test methodology).
  - Allen, 1974 (soil chemical analysis methods).
  - Harrison & Bocock, 1981 (LOI and bulk density estimation).
  - Kratz, 1998 (bait-lamina test overview).
- Related works:
  - Data and findings related to Chernobyl soil activity published in Beresford et al. 2022 and Barnett et al. 2021; data deposited in the NERC Environmental Information Data Centre (EDS).
- Funding:
  - REDFIRE project funded by the Natural Environment Research Council (NERC) under Urgency Grant NE/P015212/1.