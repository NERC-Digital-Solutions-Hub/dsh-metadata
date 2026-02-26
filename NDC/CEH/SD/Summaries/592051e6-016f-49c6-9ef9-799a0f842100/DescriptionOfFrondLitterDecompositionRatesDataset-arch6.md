# Experimental design / sampling regime

- Objective and scope
  - Study of decomposition rates of oil palm frond litter across three estates in Riau Province, Sumatra, Indonesia.
  - Part of the Biodiversity and Ecosystem Function in Tropical Agriculture project; data used to understand litter decomposition under different management and environmental conditions.
  - Data collected 2013–2017, including a reduced protocol during an ENSO-related drought in May 2016.

- Study sites and plot layout
  - Estates: Pt Ivo Mas Tunggal – Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE).
  - Libo plots replanted in 2014; UTNE and KNDE plots considered mature/over-mature.
  - Experimental area: 50 x 50 m plots with 50 m distance to access tracks on three sides and ~1000 m to the fourth side.
  - Each palm numbered; three sampling positions per plot at compass bearings 45°, 165°, and 285°.

- Experimental design and sampling regime
  - 18 plots established in 2013 as part of a larger vegetation management experiment.
  - Litter decomposition measured six times between 2013 and 2017.
  - Standard protocol: three bag types, each with four grams of dried oil palm frond litter, placed on soil surface under litter.
    - Bag types:
      - 0.1 mm mesh: excludes all invertebrates visible to the naked eye.
      - 2 mm mesh: excludes large invertebrates (e.g., cockroaches).
      - 0.1 mm mesh with four 1 cm holes: allows large invertebrates to access litter.
  - Replication: four bags of each type per plot, total of 12 bags per replicate; located at three sampling positions.
  - Time points for sampling: 10, 30, 60, and 90 days.
  - Data collection in May 2016 (reduced protocol): one fine-mesh bag per corner (two random corners per plot) left for 30 days.

- Measurements and data recorded
  - Primary response: grams of dried frond litter remaining in each bag.
  - Additional data: daily rainfall (dayrain; 24-hour period 8am–8am) from the nearest station; field observations and notes (allnotes).
  - Special variable: SAFE_distance (BEFTA cores, 2016 onward) indicating proximity (within 20 m) to anti-poison exclosures; data flagged as potentially unusable if present.
  - Date/time fields for placement (Date_set, Time_set) and collection (Date_coll, Time_coll).

- Data quality and management
  - Basic quality checks for impossible values (e.g., dates).
  - 50% data entry cross-check against original field sheets for 2016–2017 data; error rate <1% with corrections recorded.

- Data format and files
  - Three separate CSV files, stored in thin format (one observation per line):
    - PalmFrondDecompositionRates_2013_2015.csv (mature stands)
    - PalmFrondDecompositionRates_2016_2017.csv (mature stands; during ENSO period)
    - PalmFrondDecompositionRates_replants.csv (replanted Libo stands)
  - Common columns and descriptions include:
    - Estate_abbrev (UTNE, KNDE, LIBE), Plot_no (e.g., C01, C10, D28), Triplet (plot triplet), Treatment (reduced, normal, enhanced)
    - Period (discrete sampling periods), Position (sampling compass bearing), Date_set/Time_set, Date_coll/Time_coll
    - Bag type (mesh category), Grammes_remaining (numeric), dayrain (numeric)
    - allnotes (observations), SAFE_distance (numeric; BEFTA cores)
  - Data provenance:
    - BEFTA core plots (KNDE and UTNE) 2013–2014
    - BEFTA core plots 2016–2017 funded by NERC
    - Replanted stands (LIBE) 2016–2017 funded by NERC

- Plot details and coordinates
  - Mature plots: listed coordinate-like entries and plot identifiers (e.g., C10, C11, D28, F04, G07–G16) to assist geolocational analysis.
  - Replanted plots: coded references (e.g., E, 1 = N; E, 2 = Plot) with associated coordinates and plot mappings (e.g., C18, D19, E22, etc.).

- Funding and project context
  - BEFTA project reference: NE/P00458X/1
  - NERC funding for the 2016–2017 data collection and replanted stands

- Practical notes for data users
  - Data suitability caution: SAFE_distance indicates potential issues for data near ant poison exclosures; consider excluding those observations for certain analyses.
  - Outputs are designed to support self-service analyses (e.g., decomposition rates by bag type, period, and treatment) and to facilitate combining with environmental covariates such as rainfall.