# Experimental design / sampling regime

- Location and scope
  - Research conducted on three oil palm estates in Riau Province, Sumatra, Indonesia, owned by Pt Ivo Mas Tunggal: Ujung Tanjung (UTNE), Kandista (KNDE), and Libo (LIBE).
  - 18 plots established in 2013 as part of the Biodiversity and Ecosystem Function in Tropical Agriculture project (BEFTA).
  - Estate history: UTNE and KNDE plots planted 1987–1992 (mature/over-mature); LIBE plots replanted in 2014.
  - Plot layout: each 50 x 50 m, with 50 m between plots and access tracks on three sides, ~1000 m to the fourth track; sampling positions at 45°, 165°, and 285° from compass north.

- Experimental design
  - 6 decomposition measurements conducted from 2013 to 2017, including a drought-related reduced protocol in May 2016 (ENSO event).
  - Standard protocol: four grams of dried Elaeis guineensis frond litter placed in each of three bag types to manipulate invertebrate access:
    - 0.1 mm mesh ( excludes all invertebrates visible to the naked eye)
    - 2 mm mesh ( excludes large invertebrates)
    - 0.1 mm mesh with four 1 cm holes (allows large invertebrates)
  - Replication and timing: 4 bags of each type per sampling position, total 12 bags per replication; three replicates per plot.
  - Sampling schedule: bags retrieved after 10, 30, 60, and 90 days.
  - May 2016 reduced protocol: one fine-mesh bag at two randomly chosen corners per plot, left for 30 days.

- Data and measurements
  - Target variable: grams of dried litter remaining in each bag.
  - Environmental context captured: daily rainfall (dayrain) for the 24 hours preceding collection.
  - Additional observations: miscellaneous field or data-entry notes (allnotes); distance-related measure (SAFE_distance) for BEFTA cores from 2016 onward (note: data with values in this field should be used with caution).

- Data organization and storage
  - Three CSV files, in thin format (one observation per line):
    - PalmFrondDecompositionRates_2013_2015.csv (mature plantations, pre-ENSO period)
    - PalmFrondDecompositionRates_2016_2017.csv (mature plantations, during ENSO)
    - PalmFrondDecompositionRates_replants.csv (replanted stands)
  - Key fields (sample): Estate_abbrev, Triplet/Plot_no, Treatment, Period, Position, Date_set/Time_set, Date_coll/Time_coll, Bag type, Grammes_remaining, dayrain, allnotes, SAFE_distance.
  - Plot identifiers and coordinates: plots identified by three-character codes (e.g., C01, D28) and accompanying coordinates are provided for mature and replanted stands.
  - Provenance: BEFTA core plots (KNDE and UTNE) from 2013–2014 and 2016–2017; replanted stands (LIBE) from 2016–2017; funding NE/P00458X/1 and NERC.

- Quality control and provenance
  - Basic data checks for plausibility (e.g., dates).
  - 50% of 2016–2017 data entries error-checked against field sheets; error rate <1%; corrections recorded with the dataset.
  - Changes to data are tracked and retained with the dataset.

- GIS and data usage context
  - Spatially explicit design enables mapping of decomposition rates across estates, plots, treatments, and sampling times.
  - Distinct datasets allow comparison between mature and replanted stands, as well as assessment of treatment effects and temporal dynamics.
  - Caution advised with SAFE_distance data due to BEFTA exclosure-related context (potential non-use for some analyses).