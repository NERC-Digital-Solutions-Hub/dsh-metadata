# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

- Purpose and scope
  - Assess soil CO2 fluxes, soil organic carbon (SOC), and decomposition under different land-management practices in Puna grasslands.
  - Compare burnt vs. not burnt and grazed vs. not grazed conditions using a paired-site design.

- Location and experimental design
  - Manu National Park, Peru with two sites: Wayqecha (burnt in 2003) and Acjanaco (burnt in 2005).
  - For each site: adjacent unburnt area within 200 m, each split into two subplots with and without grazing exclusion (fenced 2 years prior).
  - Factorial treatment: burnt/not burnt × grazed/not grazed, yielding four treatments.
  - Plot setup: 2 m × 2 m subplots; four permanent PVC chamber bases per plot.
  - Sampling period: July 2011 to July 2012; measurements in morning and afternoon, every two months.

- Data collection methods
  - Soil CO2 fluxes
    - Static flux chamber technique with a Vaisala CARBOCAP CO2 probe and temperature sensor inside a 20 cm tall chamber.
    - Measurements: CO2 accumulation every 30 seconds for 3 minutes; simultaneous air temperature and atmospheric pressure recorded.
    - Calculations: CO2 fluxes derived by fitting headspace concentration vs. time; regression type chosen by fit (linear or non-linear) using R 3.0.2 and the HMR package.
  - Soil sampling
    - 50 g soil samples collected in July 2012 with six replicates across depths (0–5, 5–10, 10–20, 20–30 cm); shallow soils limited by bedrock.
    - Samples air-dried, sieved (2 mm), then shipped for analysis.
  - Decomposition experiment
    - Birch wood sticks (five per bag) buried at 10 cm depth in each plot; bags collected every two months.
    - Mass loss tracked to estimate decomposition rate via time–mass loss slope.
  - Bulk density and soil fractionation
    - Bulk density: undisturbed cores (30 cm3) taken from 0–10, 10–20, 20–30 cm; dried at 105 °C for 48 h.
    - Soil fractionation: density-based separation using sodium polytungstate to obtain free light fraction (free LF), occluded light fraction (OLF), and heavy fraction (HF); fractions dried, ground, and prepared for C analysis.
  - Carbon analysis
    - Total carbon analyzed by milling soils and measuring with a Finnegan Delta plus XP mass spectrometer coupled to an elemental analyser (EA-IRMS).

- Data handling and units
  - Recorded units include: CO2 concentration (ppm), CO2 fluxes (various units), SOC (Mg C ha-1), decomposition (% dry weight remaining), fraction C (%), and other related metrics.
  - Bulk density and C densities calculated from dry masses and core volumes; fractionation recovery reported as 96%.

- Data structure and datasets
  - Five datasets provided:
    - Peruvian_Andes_CO2_Raw.csv
    - Peruvian_Andes_CO2_Fluxes.csv
    - Peruvian_Andes_Soil_C.csv
    - Peruvian_Andes_Soil_Decomposition.csv
    - Peruvian_Andes_Soil_C_Fractions.csv

- Data contents and column structure
  - CO2_Raw.csv: 12 columns (e.g., Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)).
  - CO2_Fluxes.csv: 18 columns (e.g., Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure, Chamber temp, Mole, CO2 Flux (various units)).
  - Soil_C.csv: 11 columns (e.g., Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth, C (%), Bulk density, SOC (Mg C ha-1)).
  - Soil_Decomposition.csv: 11 columns (e.g., Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial weight, Final weight, Dry weight remaining).
  - Soil_C_Fractions.csv: 14 columns (e.g., Sequence, Code, Site, Soil depth, Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight, C in fraction, Total C, Fraction of total C, Mass recovered).
  - Codes used in labels: A/W for Acjanaco/Wayqecha; NG/G for Not grazed/Grazed; B/NB for Burnt/Not burnt; Morn/Aft for sampling times; 1–4 replicates; 5cm for depth; HF/LF/OLF for heavy, free light, occluded light fractions.

- Data governance and accessibility notes
  - Data compiled with explicit metadata in column headers and structured datasets to facilitate reuse for monitoring and policy evaluation.
  - Recovery of C density fractions reported at 96%, indicating high methodological rigor in fractionation and analysis.