# Experimental protocol

- Objective and design
  - Study involving 44 adult zebra finches to assess effects of different light treatments on physiological and molecular parameters.
  - Acclimatisation photoperiod: 9 hours light / 15 hours dark (lights on 07:00–16:00).
  - Treatments (coded): DARK (control, natural photoperiod), PLAN (partial artificial light at night), FLAN (dim light at night).
  - Group sizes: DARK = 13, PLAN = 15, FLAN = 16.
  - Each treatment conducted in separate rooms with independent cage layouts to prevent interference.

- Housing and lighting specifics
  - Each room contains four cages (2 m x 1 m x 0.5 m); 2–5 birds per cage; males and females housed separately.
  - Treatment lighting: broad spectrum white LEDs (400–700 nm) at 1.5 lux at perch level.
  - Daytime illumination: ceiling lights at 400 lux at perch level.
  - Lighting schedules per group:
    - DARK: lights on 07:00–16:00; then 15 hours darkness.
    - PLAN: lights on 07:00–16:00 and 21:00–02:00.
    - FLAN: lights on 09:00–16:00 and 19:00–09:00.
  - Birds had ad libitum access to dry finch seed mix and water.

- Sampling timeline and procedures
  - Two main sampling points: start (September) and end (January) of the experiment.
  - Blood collection from the brachial vein into 75 µL capillary tubes; samples kept cold on wet ice.
  - Post-collection processing: centrifuge within four hours to separate plasma from red blood cells; store at -80°C.
  - Each bird weighed at each sampling attempt.
  - End-of-study circadian sampling: two additional blood samples per bird at different times: 01:00, 06:00, 13:00, and 20:00. Half of the birds sampled at each timepoint to ensure every bird contributes two samples with a break between samplings.

- Measurements and analytical methods
  - Glucose
    - Measured at start and end using Exactive EQ real-time blood glucose test.
  - Relative Telomere Length (RTL)
    - DNA extracted from red blood cells with Puregene kit; concentration/quality via Nanodrop; diluted to 1.25 ng/µL; stored at -80°C.
    - RTL determined by real-time qPCR (T/S ratio) using Tel1b/Tel2b primers with RAG-1 as single-copy control.
    - Primer optimization across concentrations (50–500 nM).
    - qPCR profile: telomere: 15 min at 95°C; 27 cycles (95°C 15 s, 58°C 30 s, 72°C 30 s); RAG-1: 15 min at 95°C; 40 cycles (95°C 15 s, 60°C 30 s).
    - Reactions run in triplicate; plate randomization by cage and treatment; include 6-point standard curve; two golden samples per plate.
    - Data analysis with QBASE to compute RTL (T/S), correcting for plate efficiency and inter-run variation using calibrators.
    - Reported mean qPCR efficiency: telomere ~99.2% (±2.3%), RAG-1 ~104.1% (±1.9%).
  - Plasma MDA (lipid peroxidation)
    - MDA quantified by HPLC with TBARS; protocol includes BHT, thiobarbituric acid, and phosphoric acid reagents; fluorescence detection.
    - Chromatography details: Agilent 1200 series, C18 column, MeOH/buffer mobile phase (40:60), flow 1 mL/min, detection at 515 nm.
    - Calibration with external 1,1,3,3-tetraethoxypropane (TEP) standard.
  - Plasma OXY (antioxidant capacity)
    - Measured with OXY-Adsorbent assay; triplicate measurements.
    - Procedure includes plasma dilution, HOCl challenge, and chromogen addition; read at 505 nm.
    - Results express as µmol HOCl/mL; reported repeatability (R² = 0.57, N=20) and inter-plate CV (9.35%).

- Quality control and data integrity
  - Post-assay data organized into CSV files; checked for inconsistencies and typos.
  - Assay repeatability validated to acceptable ranges.
  - Data structure: rows = individual birds’ blood parameter values; columns = sample identifiers (bird ID, cage, treatment, date, sex) and measured variables (weight, glucose, RTL, OXY, MDA).

- Data structure and metadata (variables and units)
  - Bird_ID: unique identifier for each bird.
  - Cage: cage identifier.
  - Treatment: DARK, PLAN, or FLAN.
  - Timepoint: T1 (start), T2 (midpoint), T3 (end); at T3, time of day specifics (1 AM, 6 AM, 1 PM, 8 PM) are recorded.
  - Date: exact sampling date.
  - Experiment_timepoint: same as Timepoint but without time-of-day detail at end.
  - Sex: M or F.
  - Weight: body weight in grams.
  - Glucose: whole-blood glucose (mg/dL).
  - Telomere_plate: qPCR plate identifier for RTL measurement.
  - Telomere_length: RTL relative to control gene (T/S ratio).
  - OXY_plate: plate identifier for OXY measurement.
  - OXY: plasma antioxidant capacity (µmol HOCl/mL).
  - MDA: plasma malondialdehyde concentration (units as used in assay, typically µM).

- Notes for data management and governance (relevant to data leaders)
  - Comprehensive linking of samples to treatment groups, cages, and timepoints supports traceability and reproducibility.
  - Detailed metadata (primers, qPCR conditions, plate IDs, standard curves) enhances data discoverability and cross-study comparability.
  - Data quality controls include triplicate assays, inter-run calibration, and standardized storage conditions, which support reliable analyses across datasets and time.