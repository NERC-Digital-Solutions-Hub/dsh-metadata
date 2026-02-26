# Experimental design / sampling regime

- Study location and context
  - Conducted on three oil-palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal): Ujung Tanjung, Kandista, Libo.
  - Part of a larger BEFTA project on vegetation management; plots established in 2013–2014 (mature stands) and replanted in 2014–2016; comparisons between mature and replanted stands.
  - Experimental area: 50 x 50 m plots, with three sampling positions per plot (at 45°, 165°, and 285° from compass north).

- Experimental design
  - 18 plots across the estates as part of a larger vegetation-management experiment.
  - Predation measured in 2014 (mature stands) and 2016–2017 (mature and replanted stands).
  - Treatments arranged as a factorial design: cage vs uncaged (vertebrate exclusion) and canopy vs ground exposure.
  - Exclusion apparatus designed to allow invertebrates access but restrict vertebrates (e.g., rat traps with fronds).
  - Sampling involves three palm sets per plot chosen by random numbers; each palm used for predation tests.

- Predation assay and units
  - Predation measured using six freshly-killed mealworms glued to trimmed oil palm fronds.
  - Outcome: number of mealworms remaining after about 24 hours.
  - Basic units for testing include vertical stratum (crown vs edge) via placement of exclosure and non-exclosure treatments on different parts of the palm.

- Data collection and timing
  - Field deployment of mealworms occurred at specified dates with associated start and end times.
  - Measurements include date/time fields: Date_set, Time_set (larvae placement) and Date_coll, Time_coll (larvae counts).

- Data fields and metadata (format and structure)
  - Stored as three CSV files in thin format (one observation per line):
    - MealwormPredationRates_2013_2014.csv
    - MealwormPredationRates_2016_2017.csv
    - MealwormPredationRates_replants.csv
  - Key fields include:
    - Estate_abbrev and Plot_no to identify location and plot; Triplet to identify the three-plots set; Palm for palm identifier; Treatment describing management since Feb 2014.
    - Period and Date_set/Time_set for sampling periods.
    - Date_coll/Time_coll for the count time.
    - wormtreat describing the six mealworms’ treatment combinations (Remain_top_nocage, Remain_top_cage, Remain_base_nocage, Remain_base_cage).
    - worms_remaining (numeric) as the main outcome (0–6).
    - Ants characteristic and Ants Quantity (optional; field observations regarding ant presence).
    - All_notes for field or data-entry observations, including any data-checking changes.
    - dayrain ( rainfall for the 24-hour period) and distance (distance to the palm from an ant-exclosure area; used to exclude certain palms from analyses after May 2016).
  - Data structure details:
    - “Triplet” and palm numbering help identify data points within plot clusters.
    - Replanted plots (LIBE) use non-unique palm numbers; replanted data include specific positional identifiers (R1, R2, R3).

- Quality control and provenance
  - Basic data integrity checks performed (logical value checks, date formats, consistent palm/plot identifiers).
  - 50% of data entry cross-checked against original field sheets; error rate <1%; corrections documented with audit trail.
  - All changes tracked and accompany the dataset (All_notes field) to preserve provenance.

- Miscellaneous and funding
  - Three data files correspond to BEFTA core plots (KNDE and UTNE) 2013–2014 and 2016–2017, plus replanted stands (LIBE) 2016–2017.
  - Funded under NE/P00458X/1 and NERC-supported periods (El Niño period data in 2016–2017).

- Considerations for data governance and reuse (Data Steward perspective)
  - Clear, consistent naming and thin-format CSV structure facilitate interoperability and reuse by data users.
  - Rich metadata within the dataset (dates, times, treatments, palm identifiers, sampling periods) supports traceability and reproducibility.
  - Documentation of data collection methods, treatment definitions, and field procedures essential for proper interpretation.
  - Exclusion rules (e.g., distance to ant exclosures) and replanted plot idiosyncrasies (non-unique palm numbers) should be captured in metadata to avoid misinterpretation.
  - Availability of multiple datasets across time periods with explicit funding sources aids provenance and data governance.
  - Potential use issues for data stewards include ensuring timely data updates, handling multiple systems/formats, and reconciling palm identifiers across mature vs replanted plots.