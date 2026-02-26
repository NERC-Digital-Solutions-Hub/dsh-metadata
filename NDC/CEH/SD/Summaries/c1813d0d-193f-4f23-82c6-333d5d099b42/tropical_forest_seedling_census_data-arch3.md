# Danum Valley Seedling Census

- A field study comparing forest regeneration in an unlogged primary forest (Danum Valley Conservation Area, DVCA) and a nearby selectively logged forest (Ulu Segama Forest Reserve, USFR).
- Conducted during a mast fruiting event, with four census rounds from Sep 2019 to Mar 2021.

## Study Context and Aim

- Objective: generate environmental health and forest regeneration indicators to inform monitoring, policy scrutiny, and future decisions.
- Location context: DVCA (438 km2 of lowland dipterocarp and lower montane forest) adjacent to a large logging concession; USFR previously logged (1981–1993) with a trial of Reduced Impact Logging in 1993.
- Management regimes: primary forest (DVCA) vs logged forest with either natural regeneration or active restoration within USFR plots.
- Data use: counts of fruits and seedlings by species and plot to assess regeneration dynamics across forest types and restoration treatments.

## Study Site Details

- Climate: mean annual rainfall ≈ 2305 mm; mean daily temperature ≈ 25.8°C.
- Logging history: intense historical logging in USFR; variation in intensity across coupes; some restoration activities included (tree planting, liana cutting) and natural recovery elsewhere.
- Restoration context: Innoprise-FACE Foundation Rainforest Rehabilitation Project included silvicultural interventions in a subset of coupes.

## Seedling Plots and Field Inventory

- Plot design: seedling plots of 1 m2 established in both DVCA primary forest and USFR logged forest during Sep–Oct 2019.
- Plot counts: 87 plots in DVCA; 96 plots in USFR (52 actively restored, 44 naturally regenerating).
- Data collection: four census rounds to count fruits and new seedlings; species-level identification in the field; unidentified taxa grouped as morphospecies.
- Taxonomic scope: counts recorded by plant family and species.

## Data File and Structure

- Primary data file: Danum_Valley_Seedling_Census.csv
- Key columns:
  - Forest and Management: classification as primary vs logged forest; natural regeneration vs active restoration.
  - Seedling.Plot: unique plot identifier (1 m2 plots).
  - Family and Species: plant family and species names; morphospecies kept when unidentified.
  - Date.1 to Date.4 and Count.1 to Count.4: dates of each census and corresponding counts of individuals (seedlings; fruits noted during mast event as part of the census activity).
- Data granularity: counts by species (or morphospecies) per plot per census.
- Contextual notes: field-based identification and four sequential censuses provide temporal resolution around a mast fruiting event and subsequent regeneration.

## Temporal and Spatial Coverage

- Temporal: four census rounds between Sep 2019 and Mar 2021.
- Spatial: comparisons between DVCA primary forest plots and USFR plots (both restored and naturally regenerating regimes).

## Implications for Monitoring and Management

- Provides a structured, species- and plot-level dataset to evaluate:
  - Regeneration rates across forest types and restoration treatments.
  - Species composition changes over time in primary vs logged contexts.
  - Effects of restoration activities on seedling recruitment and early forest recovery.
- Supports monitoring frameworks by offering explicit metadata (forest type, management regime, plot identifiers, species, dates, and counts) to enable transparent analysis and reporting.

## Data Governance and Access Considerations

- Metadata explicitness enhances data usability and reuse (clear column definitions and census timing).
- The dataset aligns with broader restoration and biodiversity monitoring initiatives (ForestGEO, INDFORSUS).
- Breaches or barriers to data sharing and standardization highlighted in monitoring framework contexts (open access, metadata completeness, data transformation needs, and governance) are relevant to ensuring this dataset remains usable and comparable across studies and over time.