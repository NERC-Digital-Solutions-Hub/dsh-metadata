# Mealworm Predation Rates on Oil Palm in Sumatra, Indonesia

- Purpose and scope
  - Dataset describing predation rates on oil palm leaves using mealworms as prey, collected on three estates in Riau Province, Sumatra (Ujung Tanjung, Kandista, Libo) as part of the BEFTA project.
  - Time periods include mature stands (2013–2014 and 2016–2017) and replanted stands (Libo, 2016–2017).
  - Experimental design comprises 18 plots within a 50 x 50 m area per estate, with sampling across canopy vs ground, cage vs uncaged, and vertical strata, to test predation under different conditions.

- Study setting and experimental design
  - Estates: UTNE (Ujung Tanjung), KNDE (Kandista), LIBE (Libo); Libo replanted in 2014, UTNE/KNDE mature or over-mature.
  - Plots: 50 x 50 m, with 50 m separation from access tracks on three sides and ~1000 m from the fourth.
  - Sampling positions on each palm: edge of plot at 45°, 165°, 285° from north.
  - Predation tests: six freshly killed mealworms glued to trimmed oil palm frond; duration ~24 hours.
  - Treatments: caged vs uncaged; canopy vs ground; applied in factorial combinations; vertebrate exclusion tested with rat traps in cages.
  - Randomization: palm-level selection by random-number generator; three treatment sets per plot.

- Data collected and main outputs
  - Primary metric: number of mealworms remaining after exposure; half-worm counts noted when applicable.
  - Additional observations: ant presence/quantity; rainfall (dayrain) from nearest station; distance to ant exclosures (2016–2017 dataset only).
  - Metadata: treatment type, palm identifier, plot triplet, plot number, estate, sampling period, and timestamps for placement and collection.

- Data quality control and provenance
  - Basic data checks for impossible values and formatting; 50% data entry checked against field sheets with <1% error rate; all changes documented with a data-tracking record.
  - Data are stored with clear provenance, including field sheets and data-check notes.

- Data format and storage
  - Three thin-format CSV files:
    - MealwormPredationRates_2013_2014.csv (BEFTA core plots, mature stands)
    - MealwormPredationRates_2016_2017.csv (BEFTA core plots, mature stands, NERC-funded)
    - MealwormPredationRates_replants.csv (replanted stands, Libo, 2016–2017, NERC-funded)
  - Key fields (examples): Estate_abbrev, Triplet, Plot_no, Treatment, Palm, Period, Date_set, Time_set, Date_coll, Time_coll, wormtreat, worms_remaining, Ants_Characteristic, Ants_Quantity, All_notes, dayrain, distance (where applicable).
  - Format notes: data stored in a single observation per line; includes extensive metadata to enable robust analysis and cross-dataset integration.

- Miscellaneous and governance
  - Project funding reference: NE/P00458X/1.
  - Data provenance split across BEFTA core plots (KNDE, UTNE) and replanted plots (LIBE), with separate funding streams (BEFTA and NERC).

- Implications for environmental monitoring
  - Provides standardized, temporally segmented data suitable for monitoring predation pressure and its environmental correlates across mature and replanted oil palm stands.
  - Facilitates cross-plot and cross-period comparisons and integration with other BEFTA/NERC datasets.
  - Emphasizes data quality assurance and clear metadata to support reuse, sharing, and policy-relevant analyses.
  - Highlights ongoing challenges and opportunities for data value enhancement and broader data accessibility by linking with related environmental datasets.