# Experimental protocol

- Purpose and scope
  - Investigates how different night-time light exposure regimes affect physiological measures in zebra finches, including circadian glucose variation, relative telomere length, and oxidative stress markers.

- Experimental design and housing
  - Subjects: 44 adult zebra finches, acclimatized to 9 hours light / 15 hours dark.
  - Timeline: September 21, 2022 to January 23, 2023.
  - Treatments (3 groups, separate rooms): 
    - DARK: natural photoperiod (lights on 07:00–16:00). Sample size 13.
    - PLAN: partial artificial light at night (07:00–16:00 and 21:00–02:00). Sample size 15.
    - FLAN: dim light at night (09:00–16:00 and 19:00–09:00). Sample size 16.
  - Housing: each treatment in its own room with four cages (2 m x 1 m x 0.5 m), 2–5 birds per cage, sex-separated; cages laid out to prevent cross-treatment interference.
  - Lighting specifics: broad-spectrum white LEDs (400–700 nm) tuned to 1.5 lux at perch during the night; ceiling fixtures provide ~400 lux at perch during the day; timers checked weekly.
  - Data and welfare: birds provided with dry seed mix and ad libitum water.

- Sampling strategy
  - Primary timepoints: beginning (Sept) and end (Jan) of the experiment; two sampling events per bird per timepoint for baseline and final measures.
  - End-of-study circadian sampling: at 1 AM, 6 AM, 1 PM, and 8 PM; half the birds sampled at each timepoint to ensure each bird sampled twice with a rest period between sampling efforts.
  - Blood collection: brachial vein, 75 µL capillary tubes, samples kept cold, centrifuged within four hours, plasma and RBC stored at -80°C; body weight recorded at each sampling.

- Measured variables and methods
  - Glucose
    - Method: Exactive EQ real-time blood glucose test.
    - Sampling: taken at start and end of the experiment.
  - Relative Telomere Length (RTL)
    - DNA extraction: Puregene kit from RBCs.
    - Quantification: qPCR with telomere primers Tel1b/Tel2b and single-copy gene RAG-1 as control.
    - Data processing: triplicate reactions per sample; standard curve with six dilutions; analysis via QBASE to compute RTL as T/S relative to reference sample, with inter-plate calibration.
    - Quality metrics: amplification efficiencies (telomere ~99.2% ± 2.3%; RAG-1 ~104.1% ± 1.9%).
  - Malondialdehyde (MDA) in plasma
    - Method: HPLC after reaction with thiobarbituric acid (TBA) and butylated hydroxytoluene (BHT); fluorescence detection.
    - Column and conditions: C18 column, MeOH/buffer mobile phase, detection at 515 nm/553 nm.
  - Oxidative capacity (OXY) in plasma
    - Method: OXY-Adsorbent test; samples diluted and exposed to hypochlorous acid, then chromogen developed and read at 505 nm.
    - Replicates: measurements performed in triplicate.
    - Output: units of μmol of HOCl per mL; repeatability and inter-plate CV reported.

- Data quality control
  - Post-assay data handling: exported to CSV; checks for inconsistencies or typos.
  - Assay validation: repeatability assessed to ensure measurements fall within acceptable ranges.

- Data structure and metadata
  - Data layout: rows represent individual birds with a mix of identifiers and measured values; columns include sample identifiers and morphological or blood values.
  - Metadata fields and values
    - Bird_ID: unique identifier for each bird.
    - Cage: cage identifier.
    - Treatment: DARK, PLAN, or FLAN.
    - Timepoint: T1 (start), T2 (midpoint), T3 (end); T3 includes time-of-day (1 AM, 6 AM, 1 PM, 8 PM).
    - Date: exact sampling date.
    - Experiment_timepoint: timepoint without time-of-day for end samples.
    - Sex: M or F.
    - Weight: body weight (grams).
    - Glucose: blood glucose (mg/dL).
    - Telomere_plate: qPCR plate for RTL measurement.
    - Telomere_length: RTL value.
    - OXY_plate: plate for OXY measurement.
    - OXY: antioxidant capacity (μmol/L or given unit).
    - MDA: malondialdehyde concentration (μM).
  - Procedural details documented
    - Primer sequences for Telomere and RAG-1 assays.
    - Thermal profiles for RTL and telomere assays.
    - Plate calibration with standards and golden samples to ensure cross-plate comparability.
    - Randomized sample distribution across plates to mitigate plate effects.

- Relevance to monitoring frameworks
  - Demonstrates a multi-parameter environmental health monitoring approach, linking exposure (light regime) to physiological endpoints (glucose circadian rhythm, RTL, oxidative stress markers).
  - Highlights importance of standardized protocols, calibration across plates, and comprehensive metadata for traceability and comparability across time and groups.
  - Illustrates practical data governance needs: data organization, reproducibility through explicit protocols, and metadata richness to enable validation and future decision-making.
  - Reflects challenges identified for monitoring frameworks: ensuring data quality, metadata completeness, avoiding data silos, and facilitating transparent sharing of underlying data and methods.