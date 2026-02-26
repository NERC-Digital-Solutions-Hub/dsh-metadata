# Experimental design / sampling regime

- Scope and location
  - Research conducted on three oil palm estates in Riau Province, Sumatra, Indonesia: Ujung Tanjung (UTNE), Kandista (KNDE), and Libo (LIBE) owned by Pt Ivo Mas Tunggal.
  - Established 18 plots in 2013 as part of the Biodiversity and Ecosystem Function in Tropical Agriculture project.
  - Ujung Tanjung and Kandista are mature/over-mature stands; Libo plots replanted in 2014.

- Experimental setup
  - Plot area: 50 x 50 m with ~50 m buffer to access tracks on three sides and ~1000 m to the fourth side.
  - Each palm is numbered; three sampling positions per plot at 45°, 165°, and 285° from compass north.
  - Experimental design uses factorial treatments: cage vs uncaged (predator exclusion) and canopy vs ground (stratum).
  - Additional manipulation includes palm-level treatments (reduced, normal, enhanced) since 2014.
  - Randomized palm selection for each treatment set; three treatment sets per plot.
  - Sampling periods: predation measured in 2014 (mature stands) and 2016-2017 (mature and replanted stands); field exposure ~24 hours per trial.

- Measurements and procedures
  - Basic predation unit: six freshly-killed mealworms glued to trimmed oil palm fronds (~10 cm of each of six leaflets remaining).
  - Exclusion treatment designed to allow invertebrates access but prevent vertebrates (rat traps used to close some access).
  - Exclosure locations: one palm crown, one palm edge; testing vertical stratification (crown vs edge) and access location.
  - Data collected: number of mealworms remaining after exposure (0–6); occasional ant presence noted.

- Nature and units of recorded values
  - Primary: worms_remaining (numeric) – number of mealworms remaining out of six.
  - Additional fields (optional or contextual): ants_quantity (numeric) when applicable; dayrain (numeric) for rainfall in the 24-hour period; distance to ant exclosure for certain analyses.

- Data format and structure
  - Stored as three thin-format CSV files:
    - MealwormPredationRates_2013_2014.csv (BEFTA core plots)
    - MealwormPredationRates_2016_2017.csv (BEFTA core plots, NERC period)
    - MealwormPredationRates_replants.csv (replanted stands, NERC period)
  - Key columns (summarized): Estate_abbrev, Plot_no, Treatment, Palm, Period, Date_set, Time_set, Date_coll, Time_coll, wormtreat, worms_remaining, Ants_Quantity, All_notes, dayrain, distance (where applicable).
  - Data are stored in thin format; each row is a single observation.

- Data quality, validation, and provenance
  - Basic data checks for impossible values and formatting; 50% of data entry cross-checked against original field sheets with error rate <1%.
  - Corrections documented; all changes retained with dataset.

- Miscellaneous and provenance
  - Funding reference: NE/P00458X/1.
  - Data files reflect BEFTA core plots (2013-2014; 2016-2017) and replanted plots (LIBE) with distinctions in funding sources.
  - Exclosure and proximity considerations: distance to ant exclosures may exclude plots within 20 m after May 2016 to avoid confounding effects.

- Relevance for data-driven leadership
  - Demonstrates end-to-end data lifecycle: from experimental design and field data collection to metadata-rich storage and quality control.
  - Provides a structured, queryable dataset across estates, plot treatments, and temporal periods, suitable for cross-site comparisons and meta-analyses on predation dynamics in oil palm systems.
  - Emphasizes the importance of metadata (dates, times, treatments, sampling periods) and data provenance for reproducibility and cross-network collaboration.