# Experimental protocol

- Study design and timeline
  - 44 adult zebra finches brought to University of Glasgow; acclimatisation with 9h light/15h dark.
  - 21 Sep 2022 – 23 Jan 2023: birds allocated to three treatments in separate rooms:
    - DARK: natural photoperiod, lights 7:00–16:00, 0 dark period exposure to night light; n=13.
    - PLAN: partial artificial light at night (7:00–16:00; 21:00–02:00); n=15.
    - FLAN: dim light at night throughout dark period (09:00–04:00; 19:00–09:00); n=16.
  - Each room organized with four cages (2m x 1m x 0.5m), birds housed 2–5 per cage with sex separation; standard 1.5 lux at perch; 400 lux daytime; overhead LED lighting.

- Data collection time points
  - Blood sampling at two main timepoints: start (Sept) and end (Jan).
  - Additional circadian sampling at end: two timepoints per bird chosen from 1 AM, 6 AM, 1 PM, 8 PM; half birds sampled at each timepoint so each bird sampled twice with a break.

- Measurements and assays
  - Glucose
    - Measured from a blood drop using Exactive EQ real-time glucose test.
  - Relative telomere length (RTL)
    - DNA extracted from red blood cells; quantified and diluted to 1.25 ng/µL; stored at -80°C.
    - RTL measured by qPCR (T/S ratio; telomere repeats to RAG-1 control gene).
    - Primer sets: Tel1b/Tel2b for telomere; RAG-1 primers provided.
    - Reactions run in triplicate; plate randomization by cage and treatment; included standard curves (6-point) and golden samples to monitor consistency.
    - Data analyzed with QBASE to compute RTL, accounting for amplification efficiency and inter-run variation.
  - Oxidative stress: MDA and OXY
    - MDA: measured in plasma by HPLC following TBARS protocol with BHT protection; details include derivatization, column type, mobile phase, and fluorescence detection.
    - OXY: measured with OXY-Adsorbent test; diluted plasma, reaction with HOCl, chromogen, read at 505 nm; triplicate wells; reported as µmol HOCl/mL.
  - Body weight
    - Birds weighed at sampling attempts using a spring balance.

- Sample handling and storage
  - Blood samples collected via brachial vein into 75 µL capillaries; plasma separated by centrifugation within four hours; samples stored at -80°C.
  - Weights recorded at each sampling event.

- Quality control and data management
  - Data organized as CSV files; checks for inconsistencies or typos.
  - Assay repeatability verified and within acceptable ranges; use of inter-run calibrators and standard curves for RTL normalization.
  - Quality measures include reported PCR efficiencies (telomere ~99.2% average; RAG-1 ~104.1%), and plate-to-plate variability checks.
  - Data structure: rows = individual birds’ measurements; columns include Bird_ID, Cage, Treatment, Timepoint, Date, Experiment_timepoint, Sex, Weight, Glucose, Telomere_plate, Telomere_length, OXY_plate, OXY, MDA.
  - Metadata details outline variable meanings, coding for treatments (DARK, PLAN, FLAN), timepoint designations (T1, T2, T3; with T3 including time of day), sex (M/F), and units (e.g., Glucose mg/dL; RTL, OXY and MDA in specified units).