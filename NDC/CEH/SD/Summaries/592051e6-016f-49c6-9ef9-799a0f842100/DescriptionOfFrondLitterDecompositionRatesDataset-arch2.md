# PalmFrondDecompositionRates

- Purpose and scope
  - Documentation of palm frond litter decomposition measured on three oil palm estates in Riau Province, Sumatra, Indonesia, as part of the Biodiversity and Ecosystem Function in Tropical Agriculture project.
  - Data intended to monitor environmental conditions and decomposition processes across mature, replanted, and during ENSO-related drought periods, enabling cross-time and cross-treatment comparisons.

- Experimental design and site description
  - Locations: Ujung Tanjung (UTNE), Kandista (KNDE), and Libo (LIBE) estates.
  - Plot structure: 18 plots in a 50 m x 50 m area per plot, with 3 sampling positions per plot at 45°, 165°, and 285° from north.
  - Time frame: Decomposition measured from 2013 to 2017 (with a reduced protocol in May 2016 during ENSO drought).
  - Plantations: Ujung Tanjung and Kandista are mature/over-mature; Libo plots replanted in 2014–2016.

- Decomposition protocol and sampling regime
  - Litter bags: three bag types to separate invertebrate effects
    - 0.1 mm mesh (exclude visible invertebrates)
    - 2 mm mesh (exclude large invertebrates)
    - 0.1 mm mesh with four 1 cm holes (allow large invertebrates)
  - Procedure: 4 g dried oil palm frond litter placed in each bag type; bags placed on soil surface under litter; collected at 10, 30, 60, and 90 days. Each sampling event replicated three times per plot (one at each position).
  - Reduced protocol (May 2016): one fine mesh bag per corner per plot left for 30 days.
  - Units of measure: grams of dried litter remaining in each bag.

- Data quality control and validation
  - Basic data checks for impossible values (e.g., dates).
  - Approximately 50% of 2016–2017 data entry cross-checked against field sheets; error rate <1%, with corrections logged and traceable.

- Data structure and storage
  - Data stored in three CSV files (thin format; one observation per line):
    - PalmFrondDecompositionRates_2013_2015.csv (mature stands)
    - PalmFrondDecompositionRates_2016_2017.csv (mature stands; during ENSO period)
    - PalmFrondDecompositionRates_replants.csv (replanted stands, Libo)
  - Key fields include: Estate_abbrev, Plot_no, Treatment (reduced, normal, enhanced), Period, Position, Date_set, Time_set, Date_coll, Time_coll, Bag type, Grammes_remaining, dayrain, allnotes, SAFE_distance (Befta core sites; data interpretation caveat), among others.
  - Data format notes: “Thin format” with a single observation per line; extensive metadata documented in the field descriptions.

- Variables and field descriptions (highlights)
  - Estate_abbrev, Plot_no, Triplet, Treatment, Period, Position
  - Date_set, Time_set, Date_coll, Time_coll
  - Bag type, Grammes_remaining
  - dayrain (24-hour rainfall at nearest station)
  - allnotes (field/data-entry observations and data-check notes)
  - SAFE_distance (distance metric related to BEFTA cores; usage notes apply)

- Funding and provenance
  - Project funding reference: NE/P00458X/1
  - Distinct datasets:
    - BEFTA core plots (KNDE and UTNE), 2013–2014
    - BEFTA core plots, 2016–2017 (NERC-funded)
    - Replanted stands (LIBE), 2016–2017 (NERC-funded)

- Plot information and classification
  - Mature stands: multiple plots labeled with C01–F06, etc., and corresponding coordinates and plot identifiers.
  - Replanted stands: plots labeled with a different scheme (E, 1/2, etc.) and corresponding plot identifiers.
  - This classification supports comparisons between mature and replanted stands and across periods.

- Usage notes and considerations
  - Data intended for standardized comparison of decomposition rates over time and across management treatments.
  - BEFTA core data and replanted data may have different timeframes and funding streams; treat period definitions (before/during ENSO) accordingly.
  - The SAFE_distance field should be used with caution due to BEFTA exclosure protocols (data may not be suitable for all analyses).

- Relevance for environmental monitoring
  - Provides a time-series, standardized dataset of litter decomposition as an indicator of ecosystem function, soil process activity, and responses to management and climatic stresses.
  - Designed to be integrated with other environmental datasets and analyses to enhance understanding of tropical agricultural ecosystems.