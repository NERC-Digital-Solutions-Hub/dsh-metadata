# Data on the persistence, virulence and antimicrobial characteristics of Escherichia coli on plastic waste

## Overview
- A study to assess the ability of clinically relevant E. coli pathotypes to colonise and persist on plastic waste (cotton and HDPE) under environmentally relevant conditions.
- Also evaluates antimicrobial resistance (MIC) and virulence in a Galleria mellonella model.
- Data collected in Scotland, UK, from January to June 2023 to support UKRI NERC grants on microbial hitchhikers of marine plastics and related projects.
- Data provided as 8 CSV files, covering luciferase expression, growth, persistence, virulence, water properties, inocula, and MICs.

## Data collection and experimental design
- Materials and setup:
  - Inoculation of E. coli strains onto cotton and plastic surfaces.
  - Environments included nutrient-rich conditions and surface water contexts.
- Sampling and timepoints:
  - Persistence measured at 7, 14, 21, and 28 days after inoculation (DAI).
  - Galleria mellonella virulence assessed by 72-hour survival following larval challenge.
- Analytical approach:
  - Biological triplicates with replication.
  - Statistical analyses included ANOVA and Tukey’s post-hoc tests.
  - Instrumentation calibration performed according to standard protocols.
- Data quality:
  - Rigorous QC with replication, controlled conditions, and explicit thresholds for persistence.

## Data files and contents
- Luciferase_expression_WT_and_lux_transformed_strains.csv
  - Compare luciferase expression between wild-type and lux-transformed E. coli strains.
- Growth_curves_WT_and_lux_transformed_strains.csv
  - Compare growth rates (OD600) between wild-type and lux-transformed strains.
- Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv
  - Persistence levels on plastic vs. cotton for the strains.
- Virulence_in_Galleria_mellonella_model.csv
  - Virulence outcomes (larval survival) after recovery from surfaces.
- Properties_of_surface_water_used_in_each_replicate_tank.csv
  - Surface water characteristics (e.g., turbidity, conductivity, pH) used to generate biofilms.
- Inocula_used_in_frames.csv
  - Concentrations of E. coli used as frame inocula for cotton/plastic.
- Inocula_used_in_galleria_challenge.csv
  - Inocula concentrations for Galleria mellonella challenges.
- Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv
  - MICs for erythromycin against isolates, via two-fold dilution series.

## Key variables and units
- Strain: Bacterial strain identity.
- Material: Cotton or plastic (HDPE) surfaces.
- Time: Time since inoculation (days for persistence; hours for growth/virulence assays).
- Replicate: Experimental replicate identifier.
- Luciferase_expression (WT and lux-transformed): Relative units (RU).
- Growth (WT and Lux): Optical density at 600 nm (OD600).
- Persistence: Levels of persistence on plastic and cotton.
- Survival: Galleria mellonella survival percentage.
- Inocula: CFU concentrations for frame inocula and Galleria challenges.
- MIC: Minimum inhibitory concentrations (mg/mL) of erythromycin.
- Water properties: Turbidity, electrical conductivity (microsiemens), pH.

## Data collection location and period
- Collected in Scotland, UK.
- Experiments conducted from January to June 2023.

## Quality control and data integrity
- Replication: Biological triplicate experiments.
- Validation criteria for persistence: OD600 > 0.5 and luciferase expression > 1000 RFU.
- MICs determined through two-fold serial dilutions with appropriate positive/negative controls.
- Data completeness: Missing data flagged as ND (not detected).

## Responsible parties
- Data collection and interpretation led by Michael Ormsby.

## Potential GIS-relevant interpretations and data product ideas
- Although the data are laboratory-based, they include time-series measurements across materials (cotton vs plastic) and environments, which could be translated into map-like, interactive data products:
  - Spatialized, time-enabled dashboards showing persistence probability by material type and timepoint.
  - Layered views combining persistence data with surface water properties to explore environmental risk factors.
  - Attribute tables linking strains and virulence outcomes to surface type for policy or public-facing risk communication.
- To enable GIS integration, align data with a geospatial framework by assigning each experimental frame/tank a spatial identifier, then present persistence and virulence as map layers with temporal animation.