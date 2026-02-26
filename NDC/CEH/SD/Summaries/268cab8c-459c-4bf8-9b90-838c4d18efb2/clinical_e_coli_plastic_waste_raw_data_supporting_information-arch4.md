# Data on persistence, virulence, and survival of clinically relevant E. coli on plastic waste

## Overview
- Study objective: Assess the ability of clinically relevant pathogenic E. coli to adhere to and persist on plastic waste under environmentally relevant conditions, including antimicrobial resistance and virulence.
- Location and timeframe: Scotland, UK; January–June 2023.
- Data assets: 8 CSV files covering luciferase expression, growth, persistence on plastic/cotton, virulence in Galleria mellonella, surface water properties, inocula, and MICs.
- Primary data owners: Collected and interpreted by Michael Ormsby; aligned with NERC grant requirements.

## Data assets and their contents
- Luciferase_expression_WT_and_lux_transformed_strains.csv
  - Content: Comparison of luciferase expression between wild-type and lux-transformed E. coli strains.
  - Key columns: Strain, Replicate, WT luciferase expression (relative units), Lux luciferase expression (relative units).
- Growth_curves_WT_and_lux_transformed_strains.csv
  - Content: Growth rates of wild-type and lux-transformed strains.
  - Key columns: Strain, Replicate, Time (Hours), WT OD600, Lux OD600.
- Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv
  - Content: Persistence levels on plastic and cotton over time.
  - Key columns: Strain, Material, Time (Days), Replicate, CFU/ml (or equivalent persistence metric).
- Virulence_in_Galleria_mellonella_model.csv
  - Content: Virulence outcomes after recovery from frames, assessed by larval survival.
  - Key columns: Strain, Replicate, Time, Survival (%), (controls noted).
- Properties_of_surface_water_used_in_each_replicate_tank.csv
  - Content: Water properties used to generate natural biofilms; context for environmental conditions.
  - Key columns: Tank, Turbidity, Electrical_conductivity (μS), pH.
- Inocula_used_in_frames.csv
  - Content: Inoculum concentrations for frames (cotton/plastic).
  - Key columns: Strain, Replicate, Material, Concentration (CFU).
- Inocula_used_in_galleria_challenge.csv
  - Content: Inoculum concentrations for Galleria mellonella challenges.
  - Key columns: Strain, Replicate, Concentration (CFU).
- Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv
  - Content: MICs for erythromycin against E. coli isolates.
  - Key columns: Strain, Replicate, Concentration (mg/ml), Optical_density (for MIC readout).

## Data collection context and design
- Experimental design: E. coli strains inoculated onto cotton and HDPE plastic; sampling at 7, 14, 21, and 28 days post-inoculation (DAI). Galleria mellonella virulence assessed after persistence on materials; MICs determined for resistance profiling.
- Sampling and analysis: Persistence determined by OD600 and luciferase thresholds; virulence assessed via larval survival over 72 hours; MICs determined by two-fold serial dilutions and OD600 readouts.
- Replication and calibration: Biological triplicates; standard laboratory calibration for plate reader and associated instruments; controls included for each assay.

## Data structure and metadata
- Data are organized into separate CSV files, each representing a different experimental variable or assay.
- Column headers describe factors (strain, material, time, replicate, etc.) with units documented where applicable.
- Completeness: Missing data are recorded as 'ND'; data were checked for anomalous values and within expected upper/lower bounds.

## Quality control and data completeness
- Quality assurance: Replication (biological triplicates), ANOVA and post-hoc tests described for analysis; controlled conditions (temperature, material consistency) maintained.
- Completeness notes: ND used to flag missing data; some data may be absent in certain records as part of QC.

## Provenance, responsibilities, and governance
- Primary data collector/interpreter: Michael Ormsby.
- Relevance to funding: UKRI NERC grants for plastics-massociated microbial research (e.g., NE/S005196/1; NE/V005847/1).
- Data stewardship: Clearly described experimental methods, variables, and file-level metadata to support reproducibility and reuse.

## Data usage considerations and limitations
- Context: Lab-based study focused on plastic/cotton surfaces; environmental relevance considered but not field-collected ambient samples.
- Limitations for reuse: Limited to the eight CSV files described; variability in environmental conditions beyond documented parameters may affect generalizability.
- Data discoverability: Metadata provided within file headers and accompanying descriptions; standardized variable naming supports cross-study comparability.

## How this supports data strategy for data leaders
- Data assets map to end-to-end data lifecycle: clear data generation methods, structured data files, and detailed metadata support discoverability and reuse.
- Emphasis on data quality and provenance, with defined replication and calibration protocols.
- Potential for integration with broader datasets (e.g., environmental microbiology, antimicrobial resistance) to inform policy and impact assessments.
- Highlights governance needs: consistent metadata standards, documented stewardship, and explicit data provenance to enable cross-network collaboration.