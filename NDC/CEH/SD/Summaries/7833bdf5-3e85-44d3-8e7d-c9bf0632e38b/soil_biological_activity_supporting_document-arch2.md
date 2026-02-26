# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

## Purpose and use
- Provides multi-temporal data to monitor soil biological activity after a major wildfire in the Chernobyl Exclusion Zone.
- Aims to support assessment of environmental health and policy-relevant performance over time by standardising data collection and reporting.

## Study design and sampling framework
- 23 study sites within the Chornobyl Exclusion Zone, surveyed across three sampling occasions: September 2016, March 2017, and September 2017.
- At each site, three 1x1 m plots with similar vegetation cover selected (plots labeled 1.1, 1.2, 1.3, etc.).
- Several plots were not used at all times due to flooding.

## Bait lamina method and data collection
- Bait lamina strips: PVC strips (~155x6x1 mm) with sixteen 5 mm-spaced apertures, filled with a bait mixture (70% cellulose, 25% finely ground wheat bran, 5% active charcoal).
- Deployment: strips inserted in a 4x4 grid per plot; top aperture just below soil surface.
- Reading: two independent readers (Reader 1 and Reader 2) blind to site/plot assessed bait consumption as pierced (1) or unpierced (0) per aperture; an additional abrasion strip was included at each plot in Sept 2016 to check for abrasion effects.
- Outputs: per-plot, per-strip bite data (1/0) and aggregated bite metrics such as total bites and bites per day; data stored in multiple CSVs with detailed column descriptions.

## Data files and structure
- Bait_Lamina_Summary.csv: site/plot level metadata including plot location, burn history, ambient radiation dose, soil dry matter (DM), pH, LOI, and bite metrics across sampling periods.
- Reader_1_Bait_Lamina_September_2016.csv; Reader_2_Bait_Lamina_September_2016.csv
- Reader_1_Bait_Lamina_March_2017.csv; Reader_2_Bait_Lamina_March_2017.csv
- Reader_1_Bait_Lamina_September_2017.csv; Reader_2_Bait_Lamina_September_2017.csv
- Each Reader file contains per-strip (1–16) scores across plots, with identifiers for Replicate_no and Bait_lamina_no and notes on missing data.
- Table 1 (column descriptions for Bait_Lamina_Summary.csv) and Table 2 (column descriptions for all Reader files) provide detailed variable explanations, including coordinates (GPS, WGS84), burn level, ambient dose rate, soil DM, pH, LOI, and bite counts per aperture and per period.

## Site context and environmental measurements
- Study sites located within the Chernobyl Exclusion Zone; burn occurred in the Red Forest during July 2016, affecting about 80% of the forest area.
- Ambient dose rate measured at plots in September 2016 using an ATOMEX AT6130 radiometer.
- Soil properties measured in specific periods: soil percent dry matter (DM), pH, and loss on ignition (LOI) were quantified; DM measured Sept 2016, Mar 2017, and Sept 2017; pH and LOI measured Sept 2016 and Sept 2017.

## Methodological standards and QA
- Field protocol broadly follows ISO 18311:2016 (Soil quality – Test method for effects of soil contaminants on feeding activity of soil-dwelling organisms – Bait-lamina test).
- Strips read by two independent, blinded observers to ensure objectivity; data entry relies on standardised coding (pierced/unpierced; Missing) for consistency.
- Historical data referenced for context (2005 and April 2016) and related datasets cited for broader temporal coverage.

## Data quality, limitations, and accessibility
- Some plots excluded in certain periods due to flooding, affecting temporal completeness.
- Abrasion checks implemented in Sept 2016 to validate data integrity.
- Data are designed for cross-site and multi-temporal analyses, enabling integration with other environmental datasets to enhance value.

## Expected uses and relevance for environmental monitoring
- Enables assessment of soil biological activity responses to wildfire and potential interactions with ambient radiation across multiple times and locations.
- Standardised data and metadata support replication, trend analyses, and comparisons over time, contributing to monitoring and policy evaluation of ecosystem recovery in contaminated landscapes.
- Datasets can be combined with other site-level environmental measurements (e.g., DM, LOI, pH, dose rate) to build more comprehensive environmental health indicators.

## Funding and provenance
- Data collection conducted under the REDFIRE project, funded by the Natural Environment Research Council (NERC Urgency grant NE/P015212/1).