# Experimental protocol

- Overview
  - 44 adult zebra finches brought to the University of Glasgow for acclimatisation under a photoperiod of 9 hours light and 15 hours dark (lights on 7:00–16:00).
  - From Sept 21, 2022 to Jan 23, 2023, birds were assigned to three treatment groups in separate rooms to avoid interference.

- Treatment groups and lighting
  - DARK: Control group, natural photoperiod; lights on 7:00–16:00; 13 birds.
  - PLAN: Partial artificial light at night during the dark period; lights on 7:00–16:00 and 21:00–02:00; 15 birds.
  - FLAN: Dim light at night throughout the dark period; lights on 9:00–16:00 and 19:00–09:00; 16 birds.
  - Room and housing: Each treatment in a separate room with four cages (2 m x 1 m x 0.5 m), 2–5 birds per cage, mixed sexes housed separately; two broad-spectrum LED lights per cage (400–700 nm) standardized to 1.5 lux at perch; 400 lux daytime illumination at ceiling; weekly timer checks.
  - Diet: Dry finch seed mix and water ad libitum.

- Sampling schedule
  - Timepoints: Start (September) and end (January) of the experiment.
  - End-of-study sampling: Each bird blood-sampled twice at different times of day (1:00, 6:00, 13:00, 20:00). Half the birds sampled at each timepoint to ensure each bird is sampled twice with a break in between.

- Measurements and assays
  - Glucose
    - Method: Drops of blood measured with Exactive EQ real-time blood glucose test.
    - Timepoints: Start and end of the experiment.
  - Relative Telomere Length (RTL)
    - DNA extraction: Puregene kit; quantified (Nanodrop-8000); diluted to 1.25 ng/µL; stored at -80°C.
    - RTL measurement: Real-time qPCR (T/S ratio) with Telomere primers Tel1b/Tel2b and RAG-1 primers (control gene).
    - Primer details and optimization: Tests across multiple concentrations; triplicate reactions; standard curves on each plate; inter-run calibrators used.
    - Data processing: QBASE software; RTL reported as calibrated T/S ratio; assay efficiencies ~99.2% (telomere) and ~104.1% (RAG-1).
  - Oxidative stress markers
    - MDA (malondialdehyde): Measured in plasma by HPLC after reaction with TBA/BHT; fluorescence detection; external standard (TEP) for calibration.
    - OXY (antioxidant capacity): Measured with OXY-Adsorbent test; plasma diluted and incubated with HOCl, followed by chromogen; read at 505 nm; results in umol HOCl/mL.
    - Replicates and quality: All samples run in triplicate; inter-plate coefficient of variation ~9.35%; repeatability and quality controls documented.
  - Quality control
    - Post-assay data organized as CSVs; checks for inconsistencies; repeatability of telomere length and oxidative stress assays validated within acceptable ranges.

- Data structure and metadata
  - Data format: Rows represent individual bird blood parameter values; columns include sample identifiers and measured values.
  - Key metadata fields and units:
    - Bird_ID: unique identifier for each bird
    - Cage: cage location
    - Treatment: DARK, PLAN, or FLAN
    - Timepoint: T1 (start), T2 (midpoint), T3 (end); end includes time-of-day (1 AM, 6 AM, 1 PM, 8 PM)
    - Date: exact sampling date
    - Experiment_timepoint: same as Timepoint without end-day time specification
    - Sex: M or F
    - Weight: grams
    - Glucose: mg/dL
    - Telomere_plate: qPCR plate identifier for RTL
    - Telomere_length: RTL value (T/S ratio)
    - OXY_plate: plate identifier for OXY
    - OXY: antioxidant capacity (µmol)
    - MDA: malondialdehyde concentration (µmol)

- Analytic opportunities (from data structure)
  - Assess effects of light treatment on RTL, glucose, MDA, and OXY across timepoints.
  - Explore circadian patterns in glucose and any treatment-by-time interactions.
  - Integrate measurements to examine links between photoperiod exposure, oxidative stress, and telomere dynamics.