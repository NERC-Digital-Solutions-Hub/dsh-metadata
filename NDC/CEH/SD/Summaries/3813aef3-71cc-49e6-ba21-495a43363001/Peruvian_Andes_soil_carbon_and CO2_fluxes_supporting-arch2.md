# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

## Overview
- A year-long study in Manu National Park, Peru, comparing two burnt sites (2003 and 2005) with adjacent unburnt areas and two grazing treatments (fenced to exclude cattle vs unfenced).
- Factorial design: burnt vs not burnt x grazed vs not grazed.
- Aims aligned with environmental monitoring: document soil CO2 fluxes, soil carbon fractions, decomposition, and related soil properties using standardized methods.

## Study design and locations
- Sites: Wayqecha (burnt 2003) and Acjanaco (burnt 2005), with adjacent unburnt areas within 200 m.
- Plot layout: each site split into two subplots with fencing status (fenced vs unfenced), forming four treatment combinations per site.
- Objective: assess how land management and burning history influence soil carbon dynamics and decomposition processes.

## Data collection methods

### Soil surface CO2 flux measurements
- Four permanent PVC chamber bases per plot (diameter 20 cm, height 10 cm) deployed randomly.
- Measurements conducted morning and afternoon every two months from July 2011 to July 2012.
- Method: static flux chamber with a Vaisala CARBOCAP CO2 probe and temperature sensor inside a sealed chamber; CO2 accumulation sampled every 30 seconds for 3 minutes.
- Additional measurements: air temperature and atmospheric pressure recorded.
- Data processing: CO2 flux calculated in R 3.0.2 using the HMR package by regressing headspace CO2 concentration (ppm) against time; fit type selected by best fit (linear or nonlinear).

### Soil sampling for carbon and fractions
- Soil samples (50 g) collected in July 2012, at depths 0–5, 5–10, 10–20, and 20–30 cm; 6 replicates per plot.
- Samples air-dried, sieved to 2 mm, then shipped to University of St Andrews for analyses.

### Decomposition measurements
- Litter bags: five birch sticks per bag, each with 2 cm air-access holes.
- 18 bags buried at 10 cm depth in groups of six; three bags collected every two months starting July 2011.
- Mass loss measured to estimate decomposition rate via slope of mass loss over time.

## Analytical methods

### Bulk density
- Undisturbed soil cores (30 cm3) collected from 0–10, 10–20, and 20–30 cm horizons.
- Cores dried at 105 °C for 48 hours; bulk density calculated as oven-dried mass divided by core volume.

### Soil fractionation (density fractionation)
- Sub-sample (15 g) treated to correct for moisture; soil material sieved to 2 mm to remove roots and large organic material.
- Sodium polytungstate density separation (1.85 g/mL) used to separate:
  - Free light fraction (free LF)
  - Occluded light fraction (OLF)
  - Heavy fraction (HF)
- Fractions processed, rinsed, and further treated to remove NaPT; fractions oven-dried at 100 °C, weighed, and ground for analyses.
- Recovery of C density fractions reported as 96%.

### Carbon analysis
- Soil samples ground and homogenised; C analyzed at University of St Andrews with a Finnegan Delta plus XP mass spectrometer coupled to an EA-IRMS.

## Data structure and content

### Datasets (five spreadsheets)
- Peruvian_Andes_CO2_Raw.csv
- Peruvian_Andes_CO2_Fluxes.csv
- Peruvian_Andes_Soil_C.csv
- Peruvian_Andes_Soil_Decomposition.csv
- Peruvian_Andes_Soil_C_Fractions.csv

### Key column themes
- CO2 raw: Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)
- CO2 fluxes: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure, Chamber temp. (°C), Chamber temp. (K), Mole (HMR) (n=PV/RT), CO2 Flux (HMR) (μL/m2/min), CO2 Flux (μmol/m2/s), CO2 Flux (g C m-2 d-1), CO2 Flux (Mg C ha-1 yr-1)
- Soil C: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth (cm), C (%), Bulk density (g cm-3), SOC (Mg C ha-1)
- Decomposition: Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial average stick weight (g), Stick weight after collection (g), Dry weight remaining (%)
- C Fractions: Sequence, Code, Site, Soil depth (cm), Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight (g), C in the fraction (g), Total C (LF + OLF + HF) (g), Fraction of total C (%), Mass of soil recovered (%)

### Coding conventions
- Site: A = Acjanaco, W = Wayqecha
- Grazing: NG = Not grazed, G = Grazed
- Burning: B = Burnt, NB = Not burnt
- Time designations: Morn = morning, Aft = Afternoon
- Sampling periods: July/2012 (A), Sep/2012 (B), Nov/2012 (C), Jan/2012 (D), Mar/2012 (E), May/2012 (F)
- Depths and fractions: 5cm depth; HF = Heavy fraction; LF = Free light fraction; OLF = Occluded light fraction

## Data management and sharing
- Data are organized into standardized spreadsheets with explicit variable definitions and coding schemes to enable reproducibility and cross-study comparisons.
- Outputs include standardized formats suitable for integration with other environmental monitoring datasets and for upload to data portals.

## Relevance for environmental monitoring and analysis
- Provides a standardized dataset to assess how burning history and grazing management affect soil CO2 fluxes, soil carbon pools, and decomposition processes over a year.
- Uses established, replicable methods (static chamber CO2 flux, NaPT density fractionation, EA-IRMS carbon analysis) enabling comparability with other soil C studies.
- Facilitates data quality and transparency by detailing collection, processing, and data-structure conventions, supporting broader environmental health and policy monitoring objectives.

## Practical takeaways for analysts
- Use standardized methods and explicit data schemas to ensure comparability across monitoring programs.
- Consider integrating these soil CO2 flux and carbon fraction datasets with other environmental indicators to enhance data value and policy relevance.
- Ensure underlying data accessibility by maintaining clear metadata, coding conventions, and complete dataset documentation to enable reuse and secondary analyses.