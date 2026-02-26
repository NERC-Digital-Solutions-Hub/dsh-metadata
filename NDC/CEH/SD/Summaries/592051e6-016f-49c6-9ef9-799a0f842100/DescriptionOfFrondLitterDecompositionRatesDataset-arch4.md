# Experimental design / sampling regime

- Study location and scope
  - Three estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) owned by Pt Ivo Mas Tunggal.
  - 18 plots established in 2013 as part of a larger vegetation management experiment; plots classified as mature/over-mature for UJ and Kandista, replanted in 2014 for Libo.
  - Experimental area 50 x 50 m per plot, with three edge sampling positions at 45°, 165°, 285°.

- Decomposition measurement design
  - Six measurements of litter decomposition from 2013–2017, including a reduced protocol in May 2016 during ENSO drought.
  - Standard protocol: 4 g dried oil palm frond litter in each of three bag types (0.1 mm, 2 mm, and 0.1 mm with four 1 cm holes).
  - Each bag type replicated four times per plot (12 bags total), placed on the soil surface under the litter layer.
  - Sampling time points: 10, 30, 60, 90 days; one bag of each type removed at each time point; three replicates per plot per position.
  - Reduced protocol (May 2016): one fine-mesh bag per plot corner, left for 30 days.

- Data collected and units
  - Primary variable: grams of dried frond litter remaining in each bag after retrieval.

- Data format and storage
  - Three separate CSV files in thin format:
    - PalmFrondDecompositionRates_2013_2015.csv (mature stands; pre-ENSO period)
    - PalmFrondDecompositionRates_2016_2017.csv (mature stands; during ENSO period)
    - PalmFrondDecompositionRates_replants.csv (replanted stands)
  - Key metadata fields include: Estate_abbrev, Plot_no, Triplet, Treatment, Period, Position, Date_set, Time_set, Date_coll, Time_coll, Bag type, Grammes_remaining, dayrain, allnotes, SAFE_distance.

- Data governance, quality control, and provenance
  - Basic data checks for impossible values; 50% of 2016–2017 data entry cross-checked against field sheets with <1% error rate; all changes logged with dataset.
  - Data provenance linked to BEFTA core plots (2013–2014 and 2016–2017) and replanted stands (LIBE, 2016–2017); funded by BEFTA/NERC (NE/P00458X/1).

- Metadata and descriptions
  - Dataset is organized to support analysis by estate, plot, treatment, sampling period, and bag type.
  - Contains fields enabling traceability of sample timing, location within plots, rainfall context (dayrain), and observational notes.
  - Some fields (e.g., SAFE_distance) relate to exclosure experiments (ant poison) and should be treated accordingly in analyses.

- Practical context for use
  - Designed for analysis of decomposition rates across different sites, planting histories, and exposure conditions, with replication across plots and sampling positions.
  - Geographic coordinates and plot identifiers are included to support spatial analyses and linkage to other datasets within the BEFTA framework.