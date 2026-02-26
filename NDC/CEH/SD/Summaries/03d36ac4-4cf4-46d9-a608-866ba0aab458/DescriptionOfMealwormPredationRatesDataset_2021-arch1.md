# MealwormPredationRates

## Context and Objective
- Study location: three oil palm estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) owned by Pt Ivo Mas Tunggal.
- Purpose: measure invertebrate predation on oil palm leaves using freshly-killed mealworms as bait, to assess predation rates across different plots, strata, and management regimes.
- Timeframe: data collected in 2013–2014 (mature stands) and 2016–2017 (mature and replanted stands).

## Experimental Design and Sampling
- Experimental setup: 18 plots within a 50 x 50 m area per estate, with six tested positions per palm leaf fragment.
- Treatments (factorial): caged vs uncaged and canopy vs ground exposure; exclusion designed to allow invertebrates but limit vertebrate access.
- Sampling units: six mealworms glued to trimmed palm leaf fronds; one frond per palm sampled.
- Plot randomization: palm selections and treatment assignments randomized per plot.
- Timeline: predation measured three times in mature stands (2014) and six times in both mature and replanted stands (2016–2017).

## Data Collected and Units
- Primary response: worms_remaining, number of mealworms left out of six after exposure (0–6).
- Basic units: observations per exposure event with date and time stamps.
- Spatial and structural factors: canopy (top) vs ground (base) within each palm; vertical stratum tested via dual exclosure placements (one in canopy, one at edge/ground).
- Additional fields (optional or contextual): Ants characteristic and Ants Quantity (not always used); notes documenting data checks and observations.
- Environmental context: dayrain (rainfall over the 24-hour period, from nearest weather station); distance to ant exclosure for certain replanted analyses.

## Data Format and Storage
- Files:
  - MealwormPredationRates_2013_2014.csv (BEFTA core plots)
  - MealwormPredationRates_2016_2017.csv (BEFTA core plots, NERC period)
  - MealwormPredationRates_replants.csv (replanted stands, NERC period)
- Format: thin data format with one observation per line.
- Key columns (examples):
  - Estate_abbrev (KNDE, UTNE, LIBE)
  - Plot_no (e.g., C01, D28)
  - Triplet (plot set identifier)
  - Treatment (reduced, normal, enhanced)
  - Palm (palms on the plot; 3-digit numbers)
  - Period, Date_set, Time_set, Date_coll, Time_coll
  - wormtreat (experimental treatment of the six mealworms)
  - worms_remaining (numeric, 0–6)
  - Ants Quantity (optional)
  - All_notes (field for data checks and observations)
  - dayrain (rainfall in the 24-hour window)
  - distance (distance to palm from ant exclosure, for certain analyses)
- Data provenance: three files correspond to BEFTA core plots (2013–2014; 2016–2017) and replanted plots (2016–2017); funding references NE/P00458X/1 and NERC.

## Quality Control and Data Integrity
- Basic data checks performed for impossible values, date formats, and consistent palm/plot identifiers.
- 50% of data entries re-checked against original field sheets; error rate <1%; corrections tracked with audit trail.

## Miscellaneous and Context
- Background funding and project: BEFTA (Biodiversity and Ecosystem Function in Tropical Agriculture) with contributions from the NE/P00458X/1 reference and NERC funding.
- Plot details: both mature (Ujung Tanjung and Kandista) and replanted (Libo) plots included; plots have labeled coordinates and are organized by estate, plot, and triplet for analysis.

## Potential Analytical Considerations
- Compare predation rates across estates, maturities (mature vs replanted), and sampling periods.
- Analyze effects of vertical stratum (canopy vs ground) and cage exclusion on mealworm predation.
- Integrate covariates such as rainfall (dayrain) and proximity to ant exclosures (distance) to interpret variability.
- Handle data heterogeneity across datasets (2013–2014 vs 2016–2017) and between core vs replanted plots.