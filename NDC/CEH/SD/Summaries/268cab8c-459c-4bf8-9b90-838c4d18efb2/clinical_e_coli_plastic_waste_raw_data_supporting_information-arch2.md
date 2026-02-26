# Data collected for a study looking at the ability of clinically relevant pathotypes of Escherichia coli to colonise and persist on plastic waste. Additionally, antimicrobial resistance and virulence were assessed.

## Overview
- Purpose: Assess persistence, virulence, and antimicrobial resistance of clinically relevant E. coli pathotypes on plastic waste and cotton under environmentally relevant conditions.
- Scope: Includes persistence on materials, growth dynamics, virulence in a Galleria mellonella model, surface-water properties, and antibiotic resistance.

## What was recorded (data files and content)
- Luciferase_expression_WT_and_lux_transformed_strains.csv: Comparison of luciferase expression between wild-type and lux-transformed E. coli strains.
- Growth_curves_WT_and_lux_transformed_strains.csv: Growth rate comparisons (OD600) between wild-type and lux-transformed strains.
- Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv: Levels of persistence on plastic and cotton over time.
- Virulence_in_Galleria_mellonella_model.csv: Virulence outcomes (larval survival) after exposure to recovered strains.
- Properties_of_surface_water_used_in_each_replicate_tank.csv: Physical/chemical properties of surface water used to generate biofilms.
- Inocula_used_in_frames.csv: Concentrations of E. coli used to inoculate cotton/plastic frames.
- Inocula_used_in_galleria_challenge.csv: Concentrations of E. coli used for Galleria mellonella challenges.
- Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv: MICs for erythromycin against isolates.

## Where and when data were collected
- Location: Scotland, United Kingdom.
- Timeframe: January to June 2023.

## How data were collected
- Persistence: Inoculated cotton and plastic frames; sampled at 7, 14, 21, 28 days after inoculation (DAI). Frames processed aseptically; bacteria cultured in LB with erythromycin and analyzed by OD600 and luciferase expression.
- MICs: Isolates tested in 96-well plates across two-fold erythromycin dilutions; MIC determined as lowest concentration inhibiting 50% of growth relative to antibiotic-free control.
- Galleria mellonella virulence: Recovered samples grown, prepared, and microinjected into larvae; survival followed for 72 h; experiments in biological triplicate.
- Controls: Positive/negative controls included; initial frame inoculum used for reference in virulence assays.
- Calibration: Instrumentation (plate reader) calibrated per standard lab protocols.

## Experimental design and sampling regime
- Inoculation: E. coli strains inoculated onto cotton and plastic in nutrient-rich and surface water environments.
- Timepoints: 7, 14, 21, 28 DAI for persistence measurements.
- Virulence assay: Galleria mellonella challenge with defined CFU per larva; survival recorded over 72 h.
- Replication: Biological triplicate experiments.

## Data quality and completeness
- Quality controls: Replication, ANOVA, and Tukey post-hoc analyses planned for treatment effects and survival outcomes.
- Completeness: Data checked for anomalous values; missing data marked as "ND" (not detected).
- Calibration and standardization: Standard laboratory procedures used; plate reader and other instruments calibrated.
- Data structure: Data organized into separate CSVs with clear headers and units; key factors (strain, material, time, replicate) documented.

## Data structure and units (as described in the dataset)
- Persistent data: Time (Days), Material (cotton/plastic), Strain, Replicate, Persistence (CFU or related measure) with units as described per file.
- Growth data: Time (Hours or Days), Strain, Material, WT (OD600), Lux (OD600) with units in OD600.
- Luciferase data: Time (Hours), Strain, Material, WT (Luciferase RU), Lux (Luciferase RU).
- Virulence data: Time-related survival percentages; Strain; Replicate; Material; Inoculum details.
- MIC data: Strains, Concentration (mg/mL), OD readings; MIC values per isolate.
- Water properties: Turbidity, Electrical conductivity (µS), pH (dimensionless or specified units).
- Inocula: Concentration (CFU) per frame or per Galleria challenge; Material (cotton/plastic or Wild-type). 

## Responsible party and provenance
- Responsible for collection and interpretation: Michael Ormsby.
- Completeness and integrity: Data checked for upper/lower limits; ND used where data were unavailable.

## Relevance for environmental monitoring
- Provides a standardized, multi-faceted dataset on microbial hitchhikers associated with plastic waste under environmentally relevant conditions.
- Enables monitoring of environmental health indicators related to pathogenic E. coli persistence, virulence potential, and antibiotic resistance in relation to plastic and natural biofilm contexts.
- Data are organized in a way that supports time-series analysis and cross-comparison across materials, strains, and virulence outcomes, aligning with environmental monitoring and policy performance review over time.