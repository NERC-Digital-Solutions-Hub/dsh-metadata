# Experimental design / sampling regime

- Study location: three oil palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal) — Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE).
- Timeframe and plots: 18 plots established in 2013 as part of the Biodiversity and Ecosystem Function in Tropical Agriculture project; plots include mature (Ujung Tanjung, Kandista) and replanted (Libo, 2014) stands.
- Plot layout: 50 x 50 m experimental area per plot, with ~50 m separation to access tracks on three sides and ~1000 m to the fourth side; each palm numbered; three sampling positions per plot at compass bearings 45°, 165°, and 285°.
- Experimental design for predation: measured predation three times in 2014 for mature palms; six times in 2016–2017 for both mature and replanted palms.
- Predation testing units and setup: six freshly-killed mealworms glued to trimmed oil palm frond segments (~10 cm of leaflet); applied in factorial combinations of exclusion (caged vs uncaged) and stratum (canopy vs ground). Vertebrates excluded by protected cages; rat traps used as part of the exclusion design.
- Randomization and sampling: three treatment sets per plot, palms chosen by random-number generator; field exposure ~24 hours per sampling event.
- Basic unit and response: primary response is worms remaining out of six at assessment; half-worms counted as part of the data.

## Nature and units of recorded values

- Primary measure: worms_remaining (0–6) per observation.
- Supporting variables include:
  - Estate_abbrev (KNDE, UTNE, LIBE)
  - Plot_no (e.g., C01, C10, etc.)
  - Treatment (reduced, normal, enhanced since Feb 2014)
  - Palm (palms identified by three-digit numbers or replanted conventions)
  - Period (discrete sampling period)
  - Date_set/Time_set (when larvae were placed)
  - Date_coll/Time_coll (when remaining larvae were counted)
  - wormtreat (assignment of six mealworms to specific exposure setups: Remain_top_nocage, Remain_top_cage, Remain_base_nocage, Remain_base_cage)
  - Ants characteristic/Ants Quantity (notes on ant presence when many)
  - All_notes (field observations, data-check notes; includes data-check updates from 2018)
  - dayrain (rainfall in the 24 hours prior to observation)
  - distance (only in 2016–2017 data; distance to palm from ant-exclosure area)
- Exclusion and stratum details: whether measures were taken at canopy vs ground, cage vs no cage, and the corresponding treatment combinations.

## Quality control

- Performed basic data checks for impossible values, date ranges, correct palm/plot identifiers, and formatting.
- 50% of data entries cross-checked against original field sheets; error rate <1%; corrections recorded with audit trail.

## Format of stored data

- Three CSV files:
  - MealwormPredationRates_2013_2014.csv (BEFTA core plots, mature stands)
  - MealwormPredationRates_2016_2017.csv (BEFTA core plots, mature stands, NERC-funded period)
  - MealwormPredationRates_replants.csv (replanted stands, Libo estate, 2016–2017)
- Data structure: thin format; each row is a single observation.
- Key fields described above (Estate_abbrev, Plot_no, Treatment, Palm, Period, Date_set/Time_set, Date_coll/Time_coll, wormtreat, worms_remaining, Ants Quantity, All_notes, dayrain, distance).

## Miscellaneous

- Funding reference: NE/P00458X/1.
- File purpose: three datasets corresponding to BEFTA core plots (2013–2014 and 2016–2017) and replanted stands (2016–2017); includes metadata for analysis and interpretation.

## Plots in mature stands

- Details linking estate codes to plot identifiers and coordinates are provided; example mappings show plot identifiers (e.g., C10, C11, F04) and associated numerical descriptors for spatial positioning.

## Plots in replanted stands

- Similar listing of plots with codes (e.g., C18, D19, E22) and spatial descriptors for replanted plots; data allow comparisons between mature and replanted stands in predation rates.