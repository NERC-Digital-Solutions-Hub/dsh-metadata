# Persistence of Salmonella Typhimurium on Plastic Waste under UV Exposure and Associated Virulence in Galleria mellonella

## Scope and Objective
- Investigates persistence of a clinically relevant Salmonella Typhimurium strain on plastic waste (PE) and glass under UV exposure.
- Assesses virulence using Galleria mellonella larvae, including post-recovery virulence from surfaces.
- Aims to support understanding of environmental survival and pathogenic potential in plastisphere-like conditions.

## Datasets Included
- Persistence_Salmonella_UV_exposure.csv
  - Persistence levels of S. Typhimurium on plastic and glass under UV exposure, including dry and submerged conditions and surrounding water.
- Concentration_killing_curve_Galleria_control.csv
  - Virulence data for wild-type S. Typhimurium D23580 in Galleria mellonella infection model.
- Virulence_in_Galleria_mellonella_model.csv
  - Virulence data for S. Typhimurium D23580 recovered from PE and Glass in Galleria mellonella.
- Temperature_logger_data.csv
  - Temperature measurements taken throughout the study.
- Linear_decline_analysis.csv
  - Die-off characteristics (k values, D-values, RSquared, gradients) derived from linear decline analyses.

## Data Content and Variables
- Material: Plastic (PE) or Glass
- Condition: Dry, Submerged, or water
- UV: UV-exposed or No_UV
- Time: Days (for persistence and die-off analyses)
- Concentration: CFU/ml (bacterial counts; also inocula concentrations)
- Survival: Percentage survival of Galleria mellonella larvae
- Replicate: Replicate identifier
- Temperature: Recorded temperatures (from logger)
- Statistical metrics: RSquared, Gradient, K (day^-1), D-value (days)

## Experimental Design and Sampling
- Inoculation of Salmonella onto materials in nutrient-rich and surface water environments.
- Photoperiod: 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness.
- Sampling timepoints: 1, 2, 3, 6, 8, 10, 14, 21 days after inoculation (DAI).
- Galleria mellonella assay: Minimum infectious dose determined; larvae challenged with dilution series of S. Typhimurium, survival monitored for 72 h.
- Post-recovery virulence: 21-day samples recovered from materials injected into larvae to assess pathogenicity at exact concentrations.
- Replication: Biological triplicate experiments; PBS negative controls.

## Quality Control and Validation
- Replication of experiments (biological triplicates).
- Statistical analyses: ANOVA, Holm-Šídák post-hoc tests; linear regression for die-off rates.
- Confirmatory PCR for strain verification (ttr gene targeted).
- Controlled experimental conditions (temperature, material consistency).
- Calibration: Instrumentation for enumeration (plate reader) and PCR thermocycler calibrated per standard protocols.
- Completeness checks: Data reviewed for anomalies; missing data recorded as ND.

## Data Structure and Accessibility
- Data are organized into five CSV files, each corresponding to different aspects of the study (persistence, virulence, temperature, decline analysis).
- Column headers describe factors such as strain, material, condition, UV exposure, time, replication, and outcome measures (Concentration, Survival, RSquared, Gradient, K, D-value).
- Locations and dates:
  - Collected in Scotland, UK.
  - Experimental work conducted February to August 2024.

## Instrumentation and Calibration
- Photoperiod apparatus with white light and UV-B sources delivering an environmental UV index of 8.
- PVC frames to hold glass jars with samples; lights suspended ~30 cm from samples.
- Temperature logging with i-Button data loggers; calibrations performed under standard protocols.
- Microbiological enumeration with plate-based assays (LB-chloramphenicol) and PCR validation for strain identity.

## Temporal and Spatial Context for GIS Reuse
- Temporal data: Time-series measurements of persistence and die-off across multiple days (1–21 DAI) and virulence assessments at defined timepoints.
- Spatial relevance: While the data are laboratory-derived, they include surface types (Plastic PE and Glass) and exposure conditions (Dry, Submerged, Water) that can be mapped to real-world surfaces or environments (e.g., plastic waste streams, glass surfaces in aquatic settings) when combined with contextual spatial layers.
- Potential GIS products:
  - Spatiotemporal maps of predicted bacterial persistence or die-off under different surface materials and UV exposure scenarios.
  - Risk projections integrating environmental UV exposure, surface type, and temperature profiles.
  - Linkable datasets for plastisphere studies, enabling integration with environmental plastics distributions and water quality layers.

## Practical Use and Integration
- The CSVs provide structured, repeatable data suitable for GIS-friendly analyses and visualization.
- Data can be joined with metadata on surface types and environmental conditions to produce map-based insights on persistence risk and virulence potential.
- Statistical outputs (k values, D-values, RSquared) support modeling of bacterial decline across different materials and UV regimes for risk assessment.

## Responsible Access and Contact
- Principal responsible: Michael Ormsby (data collection and interpretation).
- Data support and references available within the dataset documentation and associated published works cited in the references.

## References (Context)
- Related studies on persistence and pathogenicity of environmental microbes on plastics and waste surfaces, including plastisphere dynamics and UV resilience, underpin the dataset and analytical approaches.