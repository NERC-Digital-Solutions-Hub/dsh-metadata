# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

## Overview
- Documentation accompanying a field study in Manu National Park, Peru, detailing terminology, location, experimental design, collection and analytical methods, data units, and data file structure for soil carbon, CO2 flux, and decomposition measurements across land-management treatments.

## Experimental design and study system
- Location: Manu National Park, Peru.
- Sites: Two burnt areas (Wayqecha, burned in 2003; Acjanaco, burned in 2005) with adjacent unburnt areas within 200 m.
- Plot layout: Each site subdivided into two subplots with fencing introduced 2 years before sampling to exclude cattle grazing; the other subplot unfenced.
- Treatments (factorial 2x2): Burnt vs Not burnt crossed with Grazed vs Not grazed.
- Objective alignment: Compare soil CO2 flux, soil carbon pools, and decomposition under different land-management scenarios and burning histories.

## Data collection methods

### CO2 flux measurements
- Setup: Four permanent PVC chamber bases per plot (diameter 20 cm, height 10 cm).
- Sampling schedule: Morning and afternoon measurements every two months from July 2011 to July 2012.
- Instrumentation: Static flux chamber with Vaisala CARBOCAP CO2 probe and temperature sensor inside a 20 cm tall chamber with a gas-tight lid.
- Procedure: CO2 accumulation measured every 30 seconds for 3 minutes; concurrent air temperature and atmospheric pressure recorded.
- Calculation: Flux rates derived in R (R Core Team 2012) using the HMR package by fitting linear/non-linear regression of headspace CO2 concentration (ppm) vs time.
- Data outputs: CO2 concentrations and derived CO2 fluxes per collar, with accompanying environmental measurements.

### Soil sampling
- Timing: July 2012.
- Protocol: 50 g soil samples collected with six replicates per site at depths 0–5, 5–10, 10–20, and 20–30 cm; exact depths sometimes shallower due to bedrock.
- Processing: Air-dried and sieved (2 mm) before shipping to the University of St Andrews for analyses.

### Decomposition experiment
- Setup: Eight groups of three 2 cm-hole mesh bags containing birch sticks, buried at 10 cm depth (18 bags per site, collected every two months).
- Measurements: Initial and final dry weight of sticks to compute mass loss and decomposition rate (via slope of mass loss over time).

## Analytical methods

### Bulk density
- Method: Undisturbed soil cores (30 cm^3) collected from 0–10, 10–20, and 20–30 cm depths; dried at 105 °C for 48 h to calculate oven-dry mass per core volume.

### Soil fractionation and carbon analysis
- Fractionation: Sodium polytungstate density fractionation to separate soil carbon into:
  - Free light fraction (free LF)
  - Occluded light fraction (OLF)
  - Heavy fraction (HF)
- Process: Sieve soil (15 g), density separation with NaPT, sequential rinsing and processing to isolate fractions; fractions dried and ground for analysis.
- Recovery: Reported overall soil C density fraction recovery of 96%.
- Carbon analysis: Ground soils analyzed for carbon content with an EA-IRMS system (Finnegan Delta plus XP connected to elemental analyzer) at University of St Andrews.

## Data units and data structure

### Units
- Decomposition: percent remaining (dry weight)
- CO2 concentration: ppm
- Carbon content: percent C
- Soil organic carbon (SOC): Mg C ha^-1
- CO2 flux: various units including μmol, μL, g C m^-2 d^-1, Mg C ha^-1 yr^-1, etc.
- Fractions: percent C per fraction and fraction weights (g)

### Data files and structure
- Five spreadsheets comprising the dataset:
  - Peruvian_Andes_CO2_Raw.csv
  - Peruvian_Andes_CO2_Fluxes.csv
  - Peruvian_Andes_Soil_C.csv
  - Peruvian_Andes_Soil_Decomposition.csv
  - Peruvian_Andes_Soil_C_Fractions.csv
- Key column details:
  - CO2_Raw: Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)
  - CO2_Fluxes: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure (atm), Chamber temp. (°C), Chamber temp. (K), Mole (HMR) (n=PV/RT), CO2 Flux (HMR) (uL/m^2/min), CO2 Flux (μmol/m^2/s), CO2 Flux (g C m^-2 d^-1), CO2 Flux (Mg C ha^-1 yr^-1)
  - Soil_C: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth (cm), C (%), Bulk density (g cm^-3), SOC (Mg C ha^-1)
  - Soil_Decomposition: Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial average stick weight (g), Stick weight after collection (g), Dry weight remaining (%)
  - Soil_C_Fractions: Sequence, Code, Site, Soil depth (cm), Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight (g), C in fraction (g), Total C (LF+OLF+HF) (g), Fraction of total C (%), Mass of soil recovered (%)
- Coding conventions (examples):
  - A = Acjanaco, W = Wayqecha
  - NG = Not grazed, G = Grazed
  - B = Burnt, NB = Not burnt
  - Morn/Aft = Morning/Afternoon
  - 1–4 = Replicate
  - Depths labeled as 5cm, etc.
- Data organization emphasizes explicit treatment codes, site identifiers, timing, and replication to support cross-treatment comparisons.

## Data quality and use notes
- Methodological details provided to enable reproducibility and cross-study comparability, including sampling cadence, chamber setup, and fractionation protocol.
- The dataset supports analyses of how burning, grazing, and their interaction influence soil CO2 flux, SOC distribution among fractions, and decomposition rates over a one-year period.
- Limitations acknowledged where depth access was restricted by bedrock, impacting uniform sampling at deeper horizons.