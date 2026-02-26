# Experimental protocol

## Overview
- Laboratory study with 44 adult zebra finches (breeding group) to examine effects of light exposure on physiology.
- Three treatment groups in separate rooms: DARK (control natural photoperiod), PLAN (partial artificial light at night; 7am–4pm and 9pm–2am), FLAN (dim light at night; 9am–4pm and 7pm–9am).
- Group sizes: DARK 13, PLAN 15, FLAN 16.
- Each room contains four cages (2m x 1m x 0.5m); birds housed 2–5 per cage with males and females separated.
- Standard lighting: broad-spectrum white LEDs (400–700 nm) at 1.5 lux perching level; daytime light 400 lux. Lights timed with weekly checks.
- Diet: dry finch seed mix and ad libitum water.

## Experimental design and data collection timeline
- Acclimatisation period with adjusted photoperiod (9 hours light, 15 hours dark; lights on 7am–4pm).
- Blood sampling at two main timepoints: start (September) and end (January).
- End-of-study circadian sampling: two blood samples per bird at different times of day (1am, 6am, 1pm, 8pm). Half the birds sampled at each timepoint; each bird sampled twice across the study with breaks.
- Weighing: birds weighed at each sampling attempt.

## Measurements and assays
- Glucose:
  - Measured from a drop of blood using Exactive EQ real-time glucose test.
- Relative Telomere Length (RTL):
  - DNA extracted from red blood cells (Puregene kit).
  - DNA quantified (Nanodrop), diluted to 1.25 ng/µl, stored at -80°C.
  - RTL measured by real-time qPCR (T/S ratio) using Tel1b/Tel2b primers and RAG-1 as single-copy control.
  - Reactions run in triplicate; plates randomized by cage and treatment.
  - Standard curves (6-point) included on each plate; inter-run calibrators used for normalization (QBASE software).
  - qPCR efficiency: ~99.2% (telomere) and ~104.1% (RAG-1).
- Oxidative stress markers:
  - Malondialdehyde (MDA) in plasma measured by HPLC following a TBARS-like protocol with BHT protection, thiobarbituric acid reaction, organic extraction, and fluorescence detection.
  - Oxidative capacity (OXY) measured with OXY-Adsorbent test (Diacron) in triplicate; diluted plasma with HOCl challenge; read at 505 nm; results in µmol HOCl/mL.
  - Inter-plate coefficient of variation around 9.35% (N=20).
  
## Quality control and data validation
- Post-assay data organized in CSV files; checked for inconsistencies and typos.
- Assays validated by repeatability checks; ensure measurements fall within acceptable ranges.

## Data structure and metadata
- Rows: individual birds; columns: sample identifiers and measured values.
- Key fields:
  - Bird_ID: unique identifier for each bird.
  - Cage: cage location within the room.
  - Treatment: DARK, PLAN, or FLAN.
  - Timepoint: T1 (start), T2 (midpoint), T3 (end); at T3, time-of-day specification (1 AM, 6 AM, 1 PM, 8 PM).
  - Date: exact sampling date.
  - Experiment_timepoint: same as Timepoint but without end-of-day detail.
  - Sex: M or F.
  - Weight: body weight in grams.
  - Glucose: whole-blood glucose (mg/dL).
  - Telomere_plate: qPCR plate identifier for RTL measurement.
  - Telomere_length: RTL value (T/S ratio).
  - OXY_plate: plate identifier for OXY measurement.
  - OXY: plasma anti-oxidant capacity (µmol HOCl/mL).
  - MDA: plasma malondialdehyde (µM).
- Primer and assay details provided for traceability (Telomere and RAG-1 primers, qPCR cycling profiles, standard curve details).

## Practical notes for GIS-specialist framing
- Although not geographic, the dataset contains spatially interpretable context (Room, Cage) that can enable spatial visualization of treatment effects within the lab layout if mapped.
- Data are multi-domain (physiology, time, treatment), suitable for time-series and multivariate GIS-friendly dashboards when combined with spatial metadata (cage coordinates, room layout).
- Units and measurement protocols are explicitly defined, enabling consistent data integration and reproducibility across datasets or studies.
- The design supports cross-sectional and longitudinal analyses of treatment effects on circadian biology and oxidative stress markers.