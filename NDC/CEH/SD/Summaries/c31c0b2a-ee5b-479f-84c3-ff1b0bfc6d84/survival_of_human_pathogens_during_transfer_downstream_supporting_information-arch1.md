# Survival of human pathogens bound to microplastics during transfer through the freshwater-marine continuum

## Overview
- A dataset from mesocosm experiments investigating the survival of human pathogens (E. coli, E. faecalis, P. aeruginosa) on microplastics and glass during transfer through freshwater to marine environments.
- Aims to understand pathogen fate on microplastics and potential downstream transport along the freshwater–marine continuum.
- Linked to UKRI NERC grants on microbial hitchhikers of marine plastics.

## Study design and setting
- Location: University of Stirling, Scotland.
- Timeframe: Experiments conducted April and June 2022.
- Experimental setup: Two mesocosm experiments using plastic beads (polyethylene) and glass beads (control), inoculated with target bacteria.
- Organisms: Escherichia coli, Enterococcus faecalis, and Pseudomonas aeruginosa.
- Materials: 2 mm beads (plastic and glass) housed in stainless cages within 30 L tanks (12 L working volume per tank); incubated at 15 °C with gentle shaking.

## Experiment 1 (Direct discharge from WWTP into freshwater or seawater)
- Objective: simulate direct discharge of microplastics from WWTPs into freshwater or seawater.
- Procedures:
  - WWTP effluent collected from three Forth Catchment sites (Dunblane, Bridge of Allan, Kirkcaldy) on 4–6 June 2022.
  - Background water characteristics measured; beads loaded with 100 microplastic or 100 glass particles per cage.
  - Bacteria prepared in exponential phase, inoculated into WWTP effluent; final concentrations determined by plating.
  - After 48 h, cages transferred to replicate tanks containing freshwater or seawater; 30 cages per tank.
  - Sampling at days 1, 2, 3, 4, 5, 6, 7, 9, 12, 17, 22, 27; one cage per material per tank per timepoint.
  - Processing: wash 100 particles per cage, enumerate CFU on selective media (MLGA for E. coli, PA for P. aeruginosa, SB for E. faecalis).
- Outputs: Bacterial concentrations on plastic and glass over time (CFU per 100 ml washes, per timepoint).

## Experiment 2 (Downstream transport to beach environments)
- Objective: simulate downstream transport from WWTP effluent to beach environments (river water → estuary → seawater → beach sand).
- Procedures:
  - Water and sand samples collected from four sites (Dunblane, Bridge of Allan, Torryburn, Kirkcaldy) on 12–16 April 2022.
  - Similar mesocosm setup; initial WWTP effluent inoculated to achieve target concentrations (final levels specified).
  - Cages moved through sequential tanks: river water, estuary water, seawater, then beach sand.
  - Beach sand treatment: particles emptied onto sand (40 g) in Petri dish; incubated at 15 °C.
  - Measurements:
    - Biofilm on particles assessed by crystal violet staining; absorbance at 550 nm after dye extraction.
    - Bacteria quantified as in Experiment 1 (CFU via washing, filtration, and selective media).
    - For sand: CFU quantified from sand suspensions (10 g sand in 10 ml PBS) and clarified via filtration.
- Outputs: Time-resolved biofilm formation on plastics and glass; CFU counts in water and sand across downstream sequence.

## Data collected and formats
- Focus: survival and biofilm formation of pathogens on microplastics vs glass, through freshwater to marine contexts.
- Data formats: 14 CSV files covering:
  - Background water characteristics and experimental water characteristics (mesocosm 1 and mesocosm 2).
  - Initial bacteria added to mesocosms.
  - Bacterial concentrations in water (WaterCFU_Mesocosm1; BackgroundCFU_Mesocosm2).
  - Bacterial concentrations on plastics (PlasticCFU_Mesocosm1; PlasticCFU_Mesocosm2) and on glass (GlassCFU_Mesocosm1; GlassCFU_Mesocosm2).
  - Crystal violet biofilm measurements on plastic and glass in mesocosm 2.
  - Sand dry weight measurements (SandDryWeight_Mesocosm2).

## Key methods and units
- CFU measurements:
  - Water phase: CFU per 100 ml.
  - Plastic/glass phase: CFU at multiple dilution factors (e.g., CFU_DF0, CFU_DF10, CFU_DF100, etc.); Total_CFU accounts for dilution.
- Biofilm measurements:
  - Crystal violet absorbance at 550 nm; sample-specific details (absorbance values with material type, time, rep, and water type).
- Biofilm and CFU sampling cadence:
  - Experiment 1: multiple timepoints up to day 27.
  - Experiment 2: timepoints aligned with downstream sequence (hours to days, with sanding step for beach environment).
- Physical and water quality measurements:
  - pH, electrical conductivity (EC in mS), turbidity (NTU), salinity (% or %), and temperature (°C) recorded for background and experimental waters.

## Completeness and provenance
- Data completeness: Checked for anomalous values; no missing data reported.
- Responsible data collector/handler: Rebecca Metcalf.
- Completeness note: Detailed metadata included for each file; datasets designed to be discoverable with metadata.

## Data dictionary and accessibility
- Data files (14 CSVs) cover:
  - Background and experiment water characteristics (mesocosm 1 and 2).
  - Initial bacterial inocula and subsequent CFU counts in water, plastic, and glass.
  - Biofilm (crystal violet) measurements on plastics and glass (mesocosm 2).
  - Sand dry weight measurements (mesocosm 2).
- Each file includes variables describing material type, time or date, replicate, dilution factors, and relevant measurement units to enable reproducibility and modeling.

## Relevance for analysis and modeling
- Enables analysis of:
  - Survival dynamics of pathogens on microplastics vs glass over time.
  - Impact of water type and downstream sequence on pathogen fate.
  - Relationship between biofilm formation and CFU persistence on different materials.
- Provides data suitable for correlations, trend analysis, and predictive modeling of pathogen transport and persistence in the plastics-plume context.