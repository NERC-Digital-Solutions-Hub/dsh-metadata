What has been recorded and what form does the data take?

- Aim and scope
  - Study of clinically relevant human pathogenic Escherichia coli’s ability to colonise and persist on plastic waste, including antimicrobial resistance and virulence assessment.
  - Supports UKRI-NERC grants on microbial hitchhikers of marine plastics and related SPACES project.

- Study location and timeframe
  - Scotland, UK.
  - Experiments conducted January–June 2023.

- Experimental design at a glance
  - Persistence experiments: E. coli strains inoculated onto cotton and HDPE plastic; sampling at 7, 14, 21, 28 days.
  - Virulence assessment: Galleria mellonella larvae challenged after recovery from frames; survival tracked for 72 hours.
  - Antimicrobial resistance: Minimum inhibitory concentrations (MICs) for erythromycin determined.
  - Data collected across multiple replicates and conditions with controlled lab parameters.

- Data collection methods and key procedures
  - Persistence measurements: Recover inoculated material, culture in LB with erythromycin, incubate, and determine persistence by OD600 (>0.5) and luciferase expression (>1000 RFU).
  - MIC determination: Serial dilutions of erythromycin (16 mg/mL to 0.25 mg/mL); measure growth by OD600; MIC is the lowest concentration inhibiting ~50% growth.
  - Galleria mellonella virulence: Inoculate larvae with bacterial suspensions, monitor survival over 72 h; include PBS controls and initial frame inoculum for comparison.
  - Data collection environment: Laboratory-grade equipment (96-well plates, incubators); Galleria larvae sourced locally; storage of glycerol stocks at -80°C.
  - Calibration and quality: Instrument calibration per standard protocols; experiments run in biological triplicate; predefined thresholds for persistence and virulence.

- Data outputs and structure
  - 8 CSV data files, each corresponding to a specific experimental aspect:
    1) Luciferase_expression_WT_and_lux_transformed_strains.csv — luciferase expression comparisons between wild-type and lux-transformed strains.
    2) Growth_curves_WT_and_lux_transformed_strains.csv — growth rate comparisons (OD600) between WT and lux-transformed strains.
    3) Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv — persistence levels on plastic vs. cotton.
    4) Virulence_in_Galleria_mellonella_model.csv — virulence outcomes after recovery and challenge.
    5) Properties_of_surface_water_used_in_each_replicate_tank.csv — surface water properties for biofilm generation.
    6) Inocula_used_in_frames.csv — initial inocula concentrations per frame for cotton/plastic.
    7) Inocula_used_in_galleria_challenge.csv — inocula concentrations for Galleria challenge.
    8) Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv — MICs for WT and lux strains.
  - Each file includes variables such as strain, material, time (days or hours), replication, and corresponding measurements (luciferase units, OD600, CFU, survival percentage, etc.). Units are specified within each file's headers.

- Variables and units (highlights)
  - Bacterial strain, material (cotton or plastic), time (days or hours), replication identifier.
  - Persistence: CFU-like measures via culture and thresholds (OD600 and luciferase).
  - Growth: Optical density at 600 nm (OD600).
  - Luciferase expression: Relative units (RU).
  - Virulence: Larval survival percentage.
  - MIC: Concentration of erythromycin (mg/mL).
  - Water properties: Turbidity, electrical conductivity (µS), pH, etc.
  - Inocula: Concentration of bacteria (CFU).

- Data quality, completeness and provenance
  - Data checked for anomalies; missing data marked as "ND".
  - Experiments conducted in biological triplicate.
  - Responsible for collection and interpretation: Michael Ormsby.

- Data governance and metadata considerations
  - Data include methodological details enabling replication and verification.
  - Metadata cover experimental design, materials, timepoints, and units; data governance considerations evident in QC and replication.

- How this supports monitoring frameworks (relevance for the archetype)
  - Provides concrete, policy-relevant environmental health indicators: microbial persistence on manipulated waste materials, antimicrobial resistance profiles, and virulence potential.
  - Demonstrates end-to-end data handling from collection to analysis (QA, transformation, reporting), aligning with monitoring framework practices.
  - Highlights data structure, file-level documentation, and the need for metadata and data accessibility (ND handling, open sharing considerations) relevant to governance and data sharing in monitoring programs.