# Experimental design / sampling regime

- Location and scope
  - Three oil palm estates in Riau Province, Sumatra, Indonesia, owned by Pt Ivo Mas Tunggal: Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE).
  - Estates include mature stands (UTNE, KNDE) planted 1987–1992 and replanted Libo in 2014; part of the Biodiversity and Ecosystem Function in Tropical Agriculture project (BEFTA).
  - 18 plots established in 2013 as part of a larger vegetation management experiment.

- Experimental layout
  - Plots are 50 x 50 m with spacing from tracks (approximately 50 m on three sides and ~1000 m on the fourth side).
  - Each palm numbered; three sampling positions per plot at 45°, 165°, and 285° from north.

- Decomposition protocol
  - Standard protocol: four grams of dried oil palm frond litter placed in each of three bag types
    - 0.1 mm mesh: excludes all invertebrates visible to the naked eye
    - 2 mm mesh: excludes large invertebrates (e.g., cockroaches)
    - 0.1 mm mesh with four 1 cm holes: allows large invertebrates
  - Bag sets: four of each type per plot (12 bags total) placed on soil surface under litter.
  - Sampling: bags retrieved at 10, 30, 60, and 90 days; three replicates per plot, one per sampling position.
  - Reduced protocol (May 2016, ENSO drought): one fine mesh bag per plot corner, left for 30 days.

- Measurements and units
  - Primary data: grams of dried frond litter remaining in each bag over time.

- Quality control
  - Basic data checks (e.g., dates).
  - 50% of 2016–2017 data entry error-checked against field sheets; error rate < 1%; corrections recorded with dataset.

- Data storage and structure
  - Three CSV files in thin format:
    - PalmFrondDecompositionRates_2013_2015.csv (mature stands)
    - PalmFrondDecompositionRates_2016_2017.csv (mature stands)
    - PalmFrondDecompositionRates_replants.csv (replanted Libo estate)
  - Key fields include: Estate_abbrev, Triplet, Plot_no, Treatment (reduced, normal, enhanced), Period, Position, Date_set/time, Date_coll/time, Bag type, Grammes_remaining, dayrain, allnotes, SAFE_distance (BEFTA exclosure proximity data; flagged as questionable for use), and data provenance notes.

- Data provenance and funding
  - BEFTA core plots funded 2013–2014 and 2016–2017; replanted plots funded by NERC.
  - BEFTA and NERC references: project funding NE/P00458X/1 and related NERC support.

- Additional metadata and context
  - Detailed plot identifiers and coordinates provided for mature and replanted plots, enabling spatial analysis and replication.
  - Data capture includes field notes and observations (allnotes) and weather-related rainfall data (dayrain) to contextualize decomposition rates.