# Persistence of Salmonella Typhimurium on Plastic and Glass under UV Exposure and Virulence in Galleria mellonella

## Scope and purpose
- Describes data from a study of a clinically relevant Salmonella Typhimurium strain's ability to colonise and persist on plastic waste ( polyethylene) and glass, withstand UV exposure, and assess virulence using a Galleria mellonella infection model.
- Data support exploration of persistence, die-off rates, virulence, and survival under varied environmental conditions.

## Data collected and timeframe
- Location: Scotland, UK.
- Collection period: February to August 2024.
- Records span persistence on surfaces, UV-exposure effects, virulence in Galleria mellonella, and associated environmental conditions (temperature).

## Experimental design
- Organism: Salmonella Typhimurium strain D23580.
- Materials: Plastic (LDPE) and Glass; surface conditions include dry, submerged, and surrounding water for submerged samples.
- Environment: Defined photoperiod of 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness; frames kept light-tight to prevent external light interference.
- Persistence sampling: 1, 2, 3, 6, 8, 10, 14, and 21 days after inoculation (DAI).
- Virulence assessment: Galleria mellonella larvae challenged with Salmonella concentrations from 10^3 to 10^12 CFU; survival monitored for 72 h.
- Replication: Biological triplicate experiments; negative PBS controls for Galleria assays.
- Recovery and verification: Surfaces rinsed, biofilm disrupted, serial dilutions plated on LB with chloramphenicol; confirmatory PCR for strain verification.

## Data collection and measurements
- Persistence data: Salmonella counts (CFU/ml) on plastic and glass under different conditions and UV exposure.
- UV exposure data: Presence/absence of UV exposure; UV-treated vs. non-UV samples.
- Galleria virulence data: Survival percentages of larvae after challenge.
- Environmental data: Temperature readings recorded hourly via temperature logger.
- Derived metrics: Die-off rates (k, day^-1), decimal reduction times (D-values), regression parameters (S-curve/linear decline) and R-squared values.

## Data structure and files
- Five CSV files:
  - Persistence_Salmonella_UV_exposure.csv — persistence levels on plastic and glass under UV exposure (dry, submerged, and surrounding water).
  - Concentration_killing_curve_Galleria_control.csv — virulence data from Galleria mellonella infection model (control/virulence context).
  - Virulence_in_Galleria_mellonella_model.csv — virulence data for S. Typhimurium recovered from LDPE and glass in Galleria model.
  - Temperature_logger_data.csv — temperature data logged throughout the study.
  - Linear_decline_analysis.csv — die-off rate analysis over time (k, D-values, R^2, gradient).
- Variables (examples): Material (Plastic or Glass), Condition (Dry, Submerged, or Water), UV (UV or No_UV), Time (Days or Hours), Concentration (CFU/ml or inocula), Survival (%), Replicate, R-Squared, Gradient, K (day^-1), D-value (Days).

## Data processing and quality control
- Replicates and biological triplicates used; confirmatory PCR for strain identity.
- Instrument calibration for bacterial enumeration (plate reader) and PCR thermocycler.
- Data checked for anomalies; missing data labeled as ND.

## Data analysis methods
- Die-off modeled with log10-transformed CFU counts and log-linear regression.
- Die-off characteristics derived: k (day^-1) and D-values.
- Statistical comparisons: ANOVA (to assess treatment effects on k), with Holm-Šídák post-hoc tests; two- and three-way ANOVAs for combined effects (strain, temperature, material).
- Regression outputs (R^2, gradient) used to interpret persistence and decline patterns.

## Data completeness and provenance
- Completeness noted with missing data marked as ND.
- Data collected under UKRI-NERC-supported projects: Plastisphere and SPACES initiatives.

## Data provenance and responsibility
- Data collection and interpretation led by Michael Ormsby.
- Documentation includes detailed experimental procedures and references to related work.

## Potential uses and notes
- Enables re-use for meta-analyses on pathogen persistence on abiotic surfaces under UV stress.
- Supports comparisons of persistence across materials (plastic vs. glass) and conditions (dry vs. submerged vs. water).
- Useful for risk assessment related to environmental plastic waste and pathogen transfer potential.

## References
- Ormsby et al. 2023–2024 papers on persistence and pathogenicity of environmental microbes on plastic and related matrices.