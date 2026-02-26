# Data on the survival of human pathogens bound to microplastics during transfer through the freshwater-marine continuum

## Overview
- Dataset documenting survival of human pathogens (Escherichia coli, Enterococcus faecalis, Pseudomonas aeruginosa) bound to microplastics during transfer through the freshwater–marine continuum.
- Two mesocosm experiments conducted at the University of Stirling, Scotland, April–June 2022.
- Purpose aligned with UKRI NERC grants examining microbial hitchhikers on marine plastics.
- Contains 14 CSV files detailing background and experimental conditions, CFU counts, biofilm measurements, and sand analysis.

## Study design and data collection
- Setting: Mesocosm experiments at University of Stirling, Scotland.
- Experiments:
  - Experiment 1: Direct discharge of WWTP effluent with microplastic (polyethylene) or glass beads into freshwater or seawater. Sites: three locations in the Forth Catchment (Dunblane, Bridge of Allan, Kirkaldy). Tanks: 30 cages per tank, 12 L volume, 15 °C, 30 rpm. Sampling days: 1, 2, 3, 4, 5, 6, 7, 9, 12, 17, 22, 27.
  - Experiment 2: Downstream transport simulation to beach environments. Four sites (Dunblane, Bridge of Allan, Torryburn, Kirkaldy). WWTP effluent inoculated, then cages moved sequentially through river water, estuary water, seawater, and beach sand. Biofilm assessed with crystal violet; 40 particles per cage; sand sampling (40 g); temperature 15 °C.
- Inoculation: Bacterial suspensions prepared to target concentrations; initial CFU per mL documented for each species.
- Replication: Multiple cages per replicate; sampling across timepoints; n=4 replicates in applicable setups.

## Data collected and formats
- Data files (14 CSVs) cover:
  - BackgroundWaterCharacteristics_Mesocosm1
  - ExperimentWaterCharacteristics_Mesocosm1
  - InitialBacteriaAdded_Mesocosm1
  - WaterCFU_Mesocosm1
  - PlasticCFU_Mesocosm1
  - GlassCFU_Mesocosm1
  - BackgroundWaterCharacteristics_Mesocosm2
  - InitialBacteriaAdded_Mesocosm2
  - CrystalViolet_Plastic_Mesocosm2
  - CrystalViolet_Glass_Mesocosm2
  - SandDryWeight_Mesocosm2
  - BackgroundCFU_Mesocosm2
  - PlasticCFU_Mesocosm2
  - GlassCFU_Mesocosm2
- Key variables:
  - Water characteristics: pH, electrical conductivity (EC), turbidity, salinity, temperature
  - Bacteria: E. coli, E. faecalis, P. aeruginosa; CFU counts in water (per 100 ml) and on plastic/glass materials (various dilution factors)
  - Biofilm on plastics/glass: crystal violet absorbance at 550 nm
  - Sand: dry weight before/after drying; percentage change
- Methods:
  - Bacterial enumeration via membrane filtration and selective media (MLGA for E. coli; PA for P. aeruginosa; SB for E. faecalis)
  - Crystal violet biofilm assay for microplastics and glass (Experiment 2)
  - Sand CFU analysis by PBS suspension and filtration
- Notes on data values:
  - Terminology such as TMTC (too many to count), NR (no reading), NP (no plate at this dilution) used in the datasets
  - Data include multiple dilution factors (e.g., CFU_DF0, CFU_DF10, CFU_DF100, etc.)

## Sampling, quality assurance, and completeness
- Data collection timeframe:
  - Experiment 1: sampling across 12 timepoints up to day 27 (June 2022)
  - Experiment 2: sampling aligned with downstream sequence across tanks
- Data completeness: No data missing; datasets checked for anomalous values and upper/lower limits
- Data provenance: Collected from four sites within the Forth Catchment; controlled mesocosm conditions; detailed procedural descriptions accompany the files

## Data governance and stewardship
- Metadata-rich dataset with explicit variable descriptions and units per file
- Clear documentation of experimental setup, sampling regimes, and analytical methods
- Data intended for sharing and reuse; linked to publicly describable methods and results
- Principal data collector: Rebecca Metcalf
- Grants supporting the work: UKRI NERC NE/S005196/1 and NE/V005847/1

## Relevance for monitoring frameworks
- Demonstrates end-to-end data lifecycle for environmental health monitoring:
  - Clear aims tied to policy-relevant questions (pathogen hitchhiking on plastics across aquatic environments)
  - Structured, replicated experimental design across multiple environmental contexts
  - Comprehensive metadata, standardized QA, and transparent methods to enable replication and longitudinal monitoring
  - Data governance considerations (open data readiness, metadata completeness, clear data provenance)
- Provides a framework for designingMonitoring datasets that integrate biological, chemical, and physical measurements across coupled environments (freshwater to marine) with explicit data handling and sharing practices.