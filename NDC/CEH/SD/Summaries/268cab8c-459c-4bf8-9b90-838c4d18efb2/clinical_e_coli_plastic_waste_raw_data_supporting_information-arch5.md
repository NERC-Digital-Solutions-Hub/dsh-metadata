# Data on the persistence, virulence and survival of clinically relevant strains of Escherichia coli on plastic waste

- Purpose and scope
  - Study of the ability of clinically relevant Escherichia coli pathotypes to colonise, persist on plastic waste, and assess antimicrobial resistance and virulence.
  - Data generated under environmentally relevant conditions to support understanding of the “plastisphere.”
  - Funded to meet UKRI NERC grant requirements; experiments conducted January–June 2023 in Scotland, UK.

- Data producers and provenance
  - Responsible collector/analyst: Michael Ormsby.
  - Data collected under controlled laboratory conditions with standard calibration and QA procedures (replication, statistical analysis, instrument calibration).
  - Data checked for anomalies; missing data indicated as “ND.”

- Data scope and contents
  - Total of 8 CSV files, each addressing a different aspect of the study:
    1) Luciferase_expression_WT_and_lux_transformed_strains.csv
       - Comparison of luciferase expression between wild-type and lux-transformed E. coli strains.
       - Units: relative luminescent units (RU).
    2) Growth_curves_WT_and_lux_transformed_strains.csv
       - Growth (OD600) over time for WT and lux-transformed strains.
       - Units: OD600nm.
    3) Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv
       - Persistence levels on plastic and cotton over time.
       - Units: CFU counts; time in days.
    4) Virulence_in_Galleria_mellonella_model.csv
       - Virulence outcomes assessed in Galleria mellonella survival assays.
       - Units: % survival over 72 hours; time in hours.
    5) Properties_of_surface_water_used_in_each_replicate_tank.csv
       - Surface water characteristics used to generate natural biofilms.
       - Units: turbidity, electrical conductivity (μS), pH, etc.
    6) Inocula_used_in_frames.csv
       - Concentrations of E. coli used as inocula for cotton and plastic frames.
       - Units: CFU (per inoculum).
    7) Inocula_used_in_galleria_challenge.csv
       - Inoculation concentrations for Galleria mellonella challenges.
       - Units: CFU.
    8) Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv
       - MICs for erythromycin against isolates from plastic.
       - Units: mg/mL; data across two-fold serial dilutions.
  - Data coverage includes:
    - Strains: wild-type and lux-transformed E. coli isolates.
    - Materials: cotton and HDPE plastic.
    - Timepoints: 7, 14, 21, 28 days after inoculation (DAI).
    - Virulence challenge: Galleria mellonella survival up to 72 hours post-injection.
  - File-level and column-level metadata describe variables (e.g., Strain, Material, Time) and units.

- Experimental design and data collection
  - Experimental setup
    - E. coli strains inoculated onto cotton and HDPE in nutrient-rich and surface water environments.
    - Sampling at 7, 14, 21, and 28 DAI; parallel Galleria virulence challenges.
  - Measurements and thresholds
    - Persistence: confirmed when OD600 > 0.5 and luciferase expression > 1000 RU.
    - Galleria virulence: larvae injected with ~5×10^4 to 5×10^5 CFU; survival recorded for 72 h.
  - Virulence assays
    - Groups of 10 larvae per experiment; controls included PBS injections.
    - Glycerol stocks stored at -80°C for later analysis.
  - MIC testing
    - MICs determined using two-fold serial dilutions of erythromycin (16 mg/mL to 0.25 mg/mL).
    - OD600 measured after overnight incubation; MIC defined as lowest concentration inhibiting ≥50% growth.
    - Three independent replicates; results reported as mean ± standard error.
  - Instrumentation and calibration
    - Plate reader and standard lab equipment calibrated per routine protocols.
    - Inocula and challenge preparations prepared under standardized conditions.

- Data structure and metadata details
  - Each CSV file contains descriptive headers and column metadata (e.g., Strain, Material, Time, Replicate, Concentration, Survival, Optical_density, Luciferase_expression, etc.).
  - Key units across files:
    - Time: days (persistence), hours (virulence exposure), hours (survival assessment).
    - Growth: OD600nm.
    - Persistence: CFU.
    - Luciferase_expression: relative units (RU).
    - MIC: mg/mL.
    - pH, turbidity, conductivity (for surface water properties).
  - Data completeness indicators
    - ND marks missing data points.
    - Data were checked for anomalous values; biological triplicates used for replication.

- Completeness and data quality
  - Experimental design employed biological triplicates; multiple replicates per condition.
  - Data quality control included replication, ANOVA, and Tukey post-hoc analyses in the analysis workflow.
  - Completeness status noted via explicit ND entries where applicable.

- Governance, licensing and access considerations
  - Dataset describes data provenance, collection methods, and file-level descriptions to enable reuse and portfolioing into data portals.
  - No licensing terms are specified in the document; provenance and responsible party are provided for stewardship and future data sharing.

- Reuse potential and relevance for Data Stewards
  - Provides a well-structured, multi-file dataset with explicit variable descriptions, units, and QA steps suitable for ingestion into data catalogs.
  - Demonstrates how to document complex, multi-environment microbiology data (persistence, virulence, resistance) for discoverability and reuse.
  - Highlights challenges typical to data stewardship in multidisciplinary experiments (heterogeneous data formats, metadata alignment across files, missing data handling).