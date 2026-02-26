# Soil biological activity in the Chornobyl Exclusion Zone, Ukraine in September 2016, March 2017 and September 2017 following a severe wildfire in July 2016

- Purpose of the dataset: assess soil biological activity after the 2016 Red Forest wildfire using bait lamina strips, across multiple sites and time points to identify patterns and potential environmental drivers.

## Data files and structure

- Data files described:
  - Bait_Lamina_Summary.csv: site/plot level summaries with environmental context and aggregated bait lamina results.
  - Reader_1_Bait_Lamina_September_2016.csv, Reader_2_Bait_Lamina_September_2016.csv
  - Reader_1_Bait_Lamina_March_2017.csv, Reader_2_Bait_Lamina_March_2017.csv
  - Reader_1_Bait_Lamina_September_2017.csv, Reader_2_Bait_Lamina_September_2017.csv
- Column guidance:
  - Table 1: explains site, plot, location, burn level, ambient dose rate, soil DM, LOI, pH, and bait lamina outputs across Sep 2016, Mar 2017, Sep 2017.
  - Table 2: explains Reader-specific columns (Reader 1 and 2), bait lamina strip identifiers, replicate pattern, and per-hole piercing data (1 = pierced, 0 = unpierced; “Missing” when not retrieved).
- Data structure notes:
  - Three 1x1 m plots per site (e.g., 1.1, 1.2, 1.3) with a 4x4 grid of 16 bait lamina strips per plot.
  - Additional abrasion strips included at each plot in Sep 2016 to verify abrasion effects.
  - Blind reads by two readers per strip.

## Study sites and sampling timeline

- 23 study sites located within the Chornobyl Exclusion Zone.
- Sampling occasions:
  - September 2016
  - March 2017
  - September 2017
- Context: sites were surveyed after a severe wildfire in July 2016 (Red Forest; ~80% burnt). Flooding affected some plots, so not all sites were used on all occasions.
- Environmental context captured per plot:
  - Ambient dose rate at soil surface (µSv/h)
  - Vegetation cover descriptions
  - Burn extent per plot (No burn, partial burn, full burn)

## Bait lamina method

- Bait lamina strips: PVC, ~155x6x1 mm with 16 apertures (5 mm apart) starting ~10 cm from the lower end.
- Bait composition: 70% cellulose, 25% finely ground wheat bran, 5% active charcoal.
- Field procedure:
  - Strips inserted in a 4x4 grid per plot, top aperture just below soil surface.
  - In Sep 2016, extra strips were inserted/withdrawn to check for abrasion effects.
  - Strips read by two independent readers using an iPad/tablet with a light-table app.

## Measurements and variables

- Bait lamina feeding activity:
  - Piercing data collected per hole (1 = pierced, 0 = unpierced); readers 1 and 2 recorded independently.
  - For each strip, holes grouped into four sets (top 4, 5–8, 9–12, 13–16) and also by overall 1–8 and 9–16 as applicable.
  - Outputs include per-hole scores and aggregated totals (e.g., Total_Bites per strip set, Bites_Per_Day).
  - Data include periods of deployment and retrieval dates, with notes on missing data or flooding.
- Time-specific bait lamina metrics (per site/plot and time point):
  - Total_Bites_September_2016, Total_Bites_March_2017, Total_Bites_September_2017
  - Bites_Per_Day for each period (where applicable)
- Ambient environmental measurements:
  - Ambient_Dose_Rate_September_2016 (µSv/h)
  - Ambient_Dose_Rate_March_2017 (µSv/h)
  - (Note: some periods may be missing measurements)
- Soil and substrate properties:
  - Soil_%_DM (percent dry matter) for Sep 2016, Mar 2017, Sep 2017
  - Soil_pH for Sep 2016 and Sep 2017
  - Soil_%_LOI (loss on ignition) for Sep 2016 and Sep 2017
- Administrative and data-quality details:
  - Plot_location coordinates (GPS WGS84)
  - Previous vegetation context (e.g., Previous_Pine_Plantation)
  - Burn level at sampling (Plot_Burn_Level_September_2016)
  - Site and plot field notes and remarks

## Data collection and processing

- Sampling and analysis workflow:
  - Three plots per site selected with similar vegetation cover.
  - Bait lamina strips deployed and read blind by two independent readers.
  - Post-deployment processing includes cleaning, visual assessment, and digital capture of readings.
- Data assurance:
  - Two readers per strip reduce subjective bias.
  - Abrasion controls included via abrasion strips; missing data flagged clearly.
- Data handling and traceability:
  - Datasets include explicit documentation of variables, units, methodologies, and sampling dates to enable reproducible analyses.
  - Datasets are linked to standard references and previous related work (2005, 2016, and earlier bait lamina studies).

## Data quality, limitations, and context for analysis

- Key limitations:
  - Flooding caused data loss and incomplete site coverage across time points.
  - Some sites were not used in all sampling occasions.
- Data richness:
  - Rich, multi-temporal, site-level data enabling correlations between soil biotic activity (bait lamina bites) and environmental variables (dose rate, soil DM/LOI/pH, burn extent).
  - Data support modeling of post-wildfire impacts on soil invertebrate/feeding activity and potential drivers.

## References and funding

- References:
  - ISO 18311:2016 standard for bait lamina testing
  - Foundational methodological sources (Kratz 1998; Allen 1974) and prior bait-lamina studies (Barnett et al., Beresford et al.)
- Funding:
  - REDFIRE project, Natural Environment Research Council (NE/NERC) Urgency grant NE/P015212/1

- Overall use case for analysts:
  - Enables identifying correlations and drivers of soil biological activity after wildfire.
  - Supports development of predictive insights by integrating biological activity with environmental context and radiological exposure data.