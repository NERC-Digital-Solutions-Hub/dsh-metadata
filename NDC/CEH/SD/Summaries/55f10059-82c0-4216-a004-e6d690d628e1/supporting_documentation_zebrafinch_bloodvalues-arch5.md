# Experimental protocol

## Aim and study design
- 44 adult zebra finches were acclimated and then split into three treatment groups (DARK, PLAN, FLAN) from September 21, 2022 to January 23, 2023.
- Group sizes: DARK (n=13), PLAN (n=15), FLAN (n=16).
- Treatments were conducted in separate rooms with controlled lighting schedules.
- Objectives include assessing effects of light exposure on circadian glucose rhythms and various molecular/biochemical markers.

## Experimental setup and data collection points
- Housing: four-cage room layouts per treatment, with male and female birds housed separately.
- Lighting: daylight 400 lux; treatment lighting varying by group; electrical timing checked weekly.
- Timepoints for sampling:
  - Start (T1) and end (T3) of the experiment for baseline and outcome measures.
  - End-of-study additional circadian sampling at 1 AM, 6 AM, 1 PM, and 8 PM with half the birds at each timepoint.
- Measurements collected per bird:
  - Weight (at sampling times)
  - Blood samples for glucose, RTL, MDA, and OXY analyses
  - Caged, treatment, and timepoint metadata recorded

## Biological assays and procedures
- Glucose
  - Measured from a drop of whole blood using Exactive EQ real-time glucose test.
- Relative Telomere Length (RTL)
  - DNA extracted from red blood cells using Puregene kit; quantified and stored at -80°C.
  - RTL measured by qPCR as T/S ratio relative to RAG-1 control gene.
  - Primers: Tel1b/Tel2b for telomeres; RAG-1 as single-copy control.
  - Reactions run in triplicate; plates randomized by cage and treatment.
  - Standard curve included on each plate (6-point dilution: 40–1.25 ng).
  - Data analyzed with QBASE to obtain calibrated RTL values; plate efficiency reported (approx. 99.2% for telomeres, ~104% for RAG-1).
- MDA (oxidative stress marker)
  - Plasma MDA measured by HPLC with TBARs assay (BHT inhibition, TBA reaction) and fluorescence detection.
  - Details include HPLC column, mobile phase, detection wavelengths, and external standard (TEP).
- OXY (antioxidant capacity)
  - Measured with OXY-Adsorbent test; samples run in triplicate.
  - Procedure includes dilution, HOCl challenge, chromogen reaction, and plate read at 505 nm.
  - Reported repeatability (R2 around 0.57 across 20 samples) and inter-plate CV (~9.35%).
  
## Quality control and data validation
- Post-assay data consolidated into CSV files; checked for inconsistencies and typographical errors.
- Assays validated via repeatability checks and use of inter-run calibrators (standard curves and golden samples).
- Documentation includes assay efficiencies and cycle thresholds (RTL and RAG-1).

## Data structure, metadata, and provenance
- Data structure: rows represent individual bird blood parameter values; columns include identifiers and measured values.
- Key metadata fields and units:
  - Bird_ID: unique identifier for each bird
  - Cage: cage location
  - Treatment: DARK, PLAN, or FLAN
  - Timepoint: T1 (start), T2 (midpoint), T3 (end)
  - Date: exact sampling date
  - Experiment_timepoint: same as Timepoint but without specific end-of-study time-of-day
  - Sex: M or F
  - Weight: grams
  - Glucose: mg/dL
  - Telomere_plate: qPCR plate identifier for RTL
  - Telomere_length: RTL value (relative)
  - OXY_plate: plate identifier for OXY measurement
  - OXY: antioxidant capacity (umol HOCl/mL)
  - MDA: malondialdehyde concentration (appropriate units)
- Additional protocol details include:
  - Time of day for end-of-study sampling (1 AM, 6 AM, 1 PM, 8 PM)
  - Randomization and plate layout considerations to minimize batch effects
  - Primer and sequence information for replication and audit purposes
  - Storage conditions for samples and derived DNA (e.g., -80°C storage)

## Data governance and stewardship considerations
- The dataset integrates multiple data types (physiological, molecular biology, biochemistry) with comprehensive metadata to enable discoverability and re-use.
- Documentation of laboratory methods, reagents, primers, and standard curves supports reproducibility and auditability.
- Clear linkage between sample identifiers (Bird_ID, Cage, Timepoint, Plate IDs) and measured values supports traceability from sample collection to published results.
- Quality control steps and inter-run calibration are recorded to assess data reliability and comparability across plates and runs.