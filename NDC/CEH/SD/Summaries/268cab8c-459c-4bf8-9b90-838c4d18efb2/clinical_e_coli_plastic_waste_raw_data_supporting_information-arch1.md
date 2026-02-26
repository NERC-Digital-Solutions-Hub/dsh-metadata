# Collection/Generation Methods

- Study aim and scope
  - Investigates persistence, virulence, and survival of clinically relevant E. coli strains on plastic waste (cotton and HDPE) under environmentally relevant conditions, including antimicrobial resistance and virulence assessments.

- Experimental design
  - Inoculation of E. coli strains onto cotton and plastic surfaces in nutrient-rich and surface water environments.
  - Sampling at 7, 14, 21, and 28 days after inoculation (DAI).
  - Galleria mellonella larva virulence assays conducted by challenging larvae with recovered bacteria; survival monitored for 72 hours.
  - Biological triplicates used; experiments calibrated with standard laboratory controls.

- Measurements and outcomes
  - Persistence: measured by OD600 nm and luciferase expression thresholds to confirm persistence.
  - Growth: includes growth curves for wild-type and lux-transformed strains (OD600).
  - Virulence: larval survival after Galleria mellonella challenge (percentage survival).
  - Antimicrobial resistance: minimum inhibitory concentrations (MICs) for erythromycin against isolates.
  - Inocula and challenge concentrations recorded for both frame inocula and Galleria challenges.
  - Associated water properties and inoculation details captured for each replicate.

- Data files and structure
  - 8 CSV files, each corresponding to a specific experimental variable:
    - Luciferase_expression_WT_and_lux_transformed_strains.csv: comparison of luciferase expression between wild-type and lux-transformed strains.
    - Growth_curves_WT_and_lux_transformed_strains.csv: comparison of growth rates between WT and lux-transformed strains.
    - Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv: persistence levels on plastic vs. cotton.
    - Virulence_in_Galleria_mellonella_model.csv: virulence outcomes post-recovery from surfaces.
    - Properties_of_surface_water_used_in_each_replicate_tank.csv: surface water properties used to generate biofilms.
    - Inocula_used_in_frames.csv: inocula concentrations for cotton and plastic frames.
    - Inocula_used_in_Galleria_challenge.csv: inocula concentrations for Galleria challenges.
    - Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv: MICs for erythromycin.
  - Data columns include strain, material, time (days or hours), replicates, concentration (CFU), luciferase expression (relative units), OD readings, survival percentages, turbidity, conductivity, pH, and antibiotic concentrations.

- Location and timeframe
  - Scotland, UK; experiments conducted January–June 2023.

- Data collection and processing details
  - Persistence sampling: seven, 14, 21, 28 DAI; squares removed aseptically, processed in LB with erythromycin, incubated, and evaluated via OD600 and luciferase thresholds.
  - MIC procedure: colonies grown in LB, tested across two-fold erythromycin dilutions, MIC defined as lowest concentration inhibiting 50% growth.
  - Galleria mellonella virulence assay: larvae injected with defined CFU, incubated at 37 °C, survival tracked for 72 h; multiple inoculum levels used depending on isolate.
  - Inocula and challenge preparations mirrored for comparability with the initial frame inocula.
  - Instrumentation calibration: plate reader calibrated per standard protocols.

- Data quality and completeness
  - Data checked for anomalies; missing data recorded as ND (not determined).

- Analysis and provenance
  - Analytical methods referenced: ANOVA and Tukey’s post-hoc tests for treatment and survival analyses.
  - Primary responsibility for data collection and interpretation: Michael Ormsby.

- Data provenance and accessibility notes
  - Dataset comprises clearly described CSV files with consistent variable naming; metadata embedded in the file descriptions and column headers.