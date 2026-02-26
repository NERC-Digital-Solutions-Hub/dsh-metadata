# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

- Objective and study scope
  - Document detailing methods and data structures for soil CO2 fluxes, soil carbon (C), decomposition, and soil C fractions across land-management treatments in Puna grasslands of Manu National Park, Peru.

- Sites and experimental design
  - Two burnt sites (Wayqecha 2003; Acjanaco 2005) with adjacent unburnt areas located within 200 m.
  - Each site divided into two subplots with a factorial, 2x2 design: Burnt vs Not burnt and Grazed vs Not grazed.
  - Within each subplot, fencing status (2 years prior to sampling) implemented to exclude cattle grazing in some plots.

- Field measurements and sampling schedule
  - Soil surface CO2 flux measurements:
    - Four permanent PVC chamber bases per plot (diameter 20 cm, height 10 cm).
    - Measurements conducted morning and afternoon at 2-month intervals from July 2011 to July 2012.
    - Static flux chamber method with Vaisala CARBOCAP CO2 probe and temperature sensor inside a 20 cm high chamber with a gas-tight lid.
    - CO2 accumulation recorded every 30 seconds for 3 minutes; concurrent air temperature and atmospheric pressure recorded.
    - Flux rates calculated in R (R 3.0.2) using the HMR package by linear/non-linear regression of headspace CO2 concentration (ppm) versus time.
  - Soil sampling for carbon and fractions:
    - July 2012: 50 g soil samples with six replicates at depths 0–5, 5–10, 10–20, and 20–30 cm (some depths shallower to bedrock; 20–30 cm where possible).
    - Soils air-dried, sieved (2 mm), shipped to University of St Andrews for analyses.
  - Decomposition experiment:
    - Birch sticks placed in mesh bags (five sticks per bag; bags with 2 cm holes for fauna access) at 10 cm depth.
    - 18 bags buried in groups of six per plot; three bags collected every two months from July 2011 onward.
    - Mass loss measured to compute decomposition rate from the slope of mass loss vs time.

- Analytical methods for soil and carbon fractions
  - Bulk density
    - Undisturbed soil cores (30 cm3) collected from 0–10, 10–20, and 20–30 cm depths.
    - Dried at 105 °C for 48 h; bulk density = oven-dry mass / core volume.
  - Soil fractionation (C partitioning)
    - 15 g air-dried soil treated with NaPT density separation to obtain:
      - Free light fraction (free LF)
      - Occluded light fraction (OLF)
      - Heavy fraction (HF)
    - Process involved NaPT soln densities, centrifugation, rinsing, ultrasonic dispersion, and sequential separations to isolate fractions.
    - Fractions dried, weighed, ground; C analysis performed; overall recovery ~96%.
  - Carbon analysis
    - Ground soils analyzed for total C using an EA-IRMS system (Finnegan Delta plus XP) linked to an elemental analyser.

- Data processing and calculations
  - CO2 flux calculations
    - Flux rates derived from chamber headspace CO2 over time via the HMR method in R.
  - Carbon metrics
    - SOC (soil organic carbon) expressed as Mg C ha^-1.
    - C fractions quantified as percentages and g C per fraction; mass balance across LF, OLF, HF.
  - Decomposition
    - Mass loss over time used to derive decomposition rate (slope of mass remaining vs time).

- Data products and structure
  - Five spreadsheets designed to be interoperable and reproducible:
    - Peruvian_Andes_CO2_Raw.csv
      - Columns: Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)
    - Peruvian_Andes_CO2_Fluxes.csv
      - Columns: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure (atm), Chamber temp. (°C), Chamber temp. (K), Mole (HMR) (n=PV/RT), CO2 Flux (HMR) (µL/m2/min), CO2 Flux (µmol/m2/s), CO2 Flux (g C m-2 d-1), CO2 Flux (Mg C ha-1 yr-1)
    - Peruvian_Andes_Soil_C.csv
      - Columns: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth (cm), C (%), Bulk density (g cm^-3), SOC (Mg C ha^-1)
    - Peruvian_Andes_Soil_Decomposition.csv
      - Columns: Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial average stick weight (g), Stick weight after collection (g), Dry weight remaining (%)
    - Peruvian_Andes_Soil_C_Fractions.csv
      - Columns: Sequence, Code, Site, Soil depth (cm), Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight (g), C in the fraction (g), Total C (LF + OLF + HF) (g), Fraction of total C (%), Mass of soil recovered (%)
  - Coding scheme (examples)
    - Site: A = Acjanaco, W = Wayqecha
    - Grazing: NG = Not grazed, G = Grazed
    - Burning: B = Burnt, NB = Not burnt
    - Time: Morn = morning, Aft = Afternoon
    - Month codes and replicate identifiers (e.g., 1–4 replicates)

- Variables, units, and data quality considerations
  - Recorded units include CO2 concentration (ppm), CO2 flux (uL/m2/min; µmol/m2/s; g C m-2 d-1; Mg C ha-1 yr-1), C content (%), SOC (Mg C ha-1), bulk density (g cm-3), and decomposition metrics (% dry weight remaining).
  - Fractionation recovery ~96% indicates high completeness of C recovery across fractions.
  - Data were produced using standardized protocols and analyzed with R (v3.0.2) and the HMR package for flux calculations.
  - Metadata and structured file naming facilitate discoverability and reuse in broader data portals.

- Scope for interpretation and use
  - Enables analysis of how fire (burning), grazing pressure, and their interaction with site (Wayqecha vs Acjanaco) influence soil CO2 efflux, SOC stocks, C partitioning among LF/OLF/HF fractions, and litter decomposition over a year.
  - Provides a comprehensive dataset linking field flux measurements with soil physical properties, carbon content, and organic matter fractions to support models of carbon dynamics under different land-management regimes.