# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Experimental design / sampling regime
- Location: three estates in Riau Province, Sumatra (Pt Ivo Mas Tunggal): Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE).
- History: estates planted 1987-1995 on mineral soils; Libo replanted in 2014; UTNE and KNDE mature/over-mature; 18 plots established in 2013 within a larger vegetation-management experiment.
- Plot layout: 50 x 50 m plots, with seeds/tests placed at three sampling positions (edge marked at 45°, 165°, 285° from north).
- Granivory measurements:
  - 2014 (mature stands): once.
  - 2016–2017 (mature and replanted): five times.
  - Experimental unit: ten shelled sunflower seeds on a 15 cm paper disc, shielded ~10 cm above soil.
  - Treatments (4 combinations): cage + grease, cage only, grease only, open (no cage, no grease).
  - Exclosures: metal grid traps (35 x 20 x 14 cm) with ≤1 cm holes; exposure ~24 hours per trial.
- Sampling scope: one test per plot per period per position; replicated across three positions.

## Nature and units of recorded values
- Primary metric: seeds remaining out of ten after exposure (decimal values possible, e.g., 3.5).

## Quality control
- Basic data checks for impossible values (e.g., >10 seeds remaining).
- 50% of data entry cross-checked against field sheets; error rate <1%, with corrections documented and traceable.

## Format of stored data
- Three long-format CSV files:
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (mature stands)
  - SunflowerSeedPredationRates_replants.csv (replanted stands)
- Key columns:
  - Estate_abbrev, Plot_no (e.g., C01), Triplet, Treatment (management since Feb 2014: reduced, normal, enhanced), Period (sampling period), Position (compass heading), Date_set, Time_set, Date_coll, Time_coll, seedstreat (remain_cage, remain_open, remain_cage_grease, remain_open_grease), seedsremaining (0–10), dayrain (24 h rainfall at nearest station), allnotes (observations), SAFE_distance (only in BEFTA 2016–2017 data; indicates proximity to ant-poison exclosure; data flagged here may be unreliable).

## Miscellaneous
- Funding reference: NE/P00458X/1.
- Datasets include BEFTA core plots (2016–2017) and replanted plots.

## Plots and spatial context
- Mature stands: plots identified with coordinates and designations (e.g., C10, C11, D28, F04, G07, etc.), illustrating spatial layout within estates.
- Replanted stands: data structured similarly, with entries tying E, plot identifiers, and center coordinates (e.g., E, 1 = N; E, 2 = Plot).