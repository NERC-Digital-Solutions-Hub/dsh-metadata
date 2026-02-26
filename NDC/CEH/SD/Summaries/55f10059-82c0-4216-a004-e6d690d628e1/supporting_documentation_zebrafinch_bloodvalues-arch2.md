# Experimental protocol

- Purpose and scope
  - Document a standardized, data-rich protocol to assess physiological responses in zebra finches under different light exposure regimes, enabling consistent environmental health monitoring and cross-study data integration.

- Experimental design
  - Subjects: 44 adult zebra finches bred together.
  - Acclimatisation: 9 hours light / 15 hours darkness (lights on 7:00–16:00).
  - Groups and timing (Sept 21, 2022 – Jan 23, 2023):
    - DARK: natural photoperiod; lights 7:00–16:00; sample size 13.
    - PLAN: partial artificial light at night during dark photoperiod; lights 7:00–16:00 and 21:00–02:00; sample size 15.
    - FLAN: dim light at night throughout dark photoperiod; lights 9:00–16:00 and 19:00–09:00; sample size 16.
  - Housing: separate rooms per treatment; four cages per room; 2–5 birds per cage; sex-separated per cage.
  - Environment: broad-spectrum white LEDs (400–700 nm) at 1.5 lux at perch during night; daytime ~400 lux at perch.

- Sampling schedule and measurements
  - Timepoints: start (September) and end (January) of the experiment; weight measured at each sampling.
  - Blood handling: brachial venipuncture, 75 µL capillary tubes, cold storage on wet ice; plasma and red blood cells separated by centrifugation within 4 hours; stored at -80°C.
  - End-of-study circadian sampling: two additional blood draws per bird at different times (1 AM, 6 AM, 1 PM, 8 PM); half the birds sampled at each timepoint so each bird sampled twice with a break in between.

- Glucose measurements
  - Method: Exactive EQ real-time blood glucose test.
  - Timing: at start and end sampling attempts for all birds.

- Relative telomere length (RTL) measurements
  - DNA extraction: Puregene kit from red blood cells.
  - Quantification: Nanodrop; diluted to 1.25 ng/µL; stored at -80°C.
  - RTL assay: real-time qPCR (T/S ratio; Telomere repeats vs control gene RAG-1).
  - Primers: Tel1b/Tel2b for telomeres; RAG-1 primers provided.
  - Reactions: triplicate per sample; plate randomization by cage and treatment.
  - Quality controls: six-point standard curve per plate; inter-run calibrators; non-template controls.
  - Data analysis: QBASE software; RTL = T/S normalized relative quantity; report plate-level efficiency (telomere ~99.2% ± 2.3%; RAG-1 ~104.1% ± 1.9%).

- Oxidative stress and lipid peroxidation markers
  - MDA (malondialdehyde)
    - Method: HPLC with thiobarbituric acid (TBA) reaction; BHT antioxidant added; fluorescence detection.
    - Column, mobile phase, and detection specifics provided; calibrated with 1,1,3,3-tetrathoxypropane.
  - OXY (antioxidant capacity)
    - Method: OXY-Adsorbent test following manufacturer protocol with modifications.
    - Sample prep: plasma diluted 1:100; HOCl challenge; plate incubation; chromogen addition; read at 505 nm.
    - Output: umol HOCl per mL; repeatability and inter-plate variability reported (R2 ~0.57; CV ~9.35%).

- Data quality control
  - Post-assay data management: CSV files; consistency checks for typos and inconsistencies.
  - Assay validation: repeatability checks within acceptable ranges.
  - Data structure: each row corresponds to an individual bird’s blood parameter; columns include identifiers, treatment, timepoint, sex, date, weight, glucose, RTL, OXY, MDA, and plate identifiers.

- Data structure and metadata
  - Core fields:
    - Bird_ID (unique), Cage, Treatment (DARK, PLAN, FLAN), Timepoint (T1, T2, T3 with end-time-of-day detail), Date, Experiment_timepoint, Sex (M/F), Weight (g).
    - Glucose (mg/dL); Telomere_plate; Telomere_length (RTL); OXY_plate; OXY (umol HClO/mL); MDA (uM).
  - Plate and assay metadata: plate identifiers for RTL and OXY; standard curve details; inter-run calibrators; non-template controls.

- Outputs and potential uses
  - Standardized dataset enabling comparison of physiological responses to different lighting regimes.
  - Multi-parameter profile including metabolic (glucose), cellular aging (RTL), and oxidative stress/antioxidant capacity (MDA, OXY).
  - Data suitable for environmental health monitoring applications related to light exposure, circadian disruption, and welfare indicators, with a structure that supports integration with other datasets.

- Relevance to environmental monitoring challenges
  - Demonstrates how to increase data value through standardized collection across timepoints and treatments.
  - Emphasizes accessibility and traceability of underlying data via detailed metadata and plate-level assay documentation.