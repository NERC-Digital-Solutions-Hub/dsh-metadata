# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

- Location and design
  - Study area: Manu National Park, Peru
  - Sites: two burnt sites (Wayqecha 2003; Acjanaco 2005) with adjacent unburnt areas within ~200 m
  - Plot layout: each site split into two subplots with or without fencing; four treatment combinations: burnt/grazed, burnt/not grazed, not burnt/grazed, not burnt/not grazed

- Measurements and sampling schedule
  - Soil CO2 fluxes: four permanent PVC chamber bases per plot; measurements morning and afternoon every two months from July 2011 to July 2012
  - CO2 flux methodology: static flux chambers with Vaisala CARBOCAP CO2 probe and temperature sensor; data collected every 30 seconds for 3 minutes
  - Additional measurements: air temperature, atmospheric pressure, and plot metadata (time of day, sampling time)
  - Soil sampling: 50 g samples, six replicates per depth (0–5, 5–10, 10–20, 20–30 cm); many plots shallow to bedrock
  - Decomposition experiment: five birch sticks per bag at 10 cm depth; buried July 2011; retrieved every two months; mass loss used to estimate decomposition rate

- Analytical methods
  - CO2 flux calculation: R 3.0.2 with HMR package; linear or non-linear regression of headspace CO2 vs time
  - Bulk density: undisturbed cores (30 cm3), dried at 105 °C, density = oven-dry mass / core volume
  - Soil fractionation: NaPT density separation into free LF, occluded LF, and heavy fraction; sequential rinsing and centrifugation; fractions dried and ground for analysis
  - Carbon analysis: soil C content via EA-IRMS at University of St Andrews
  - Recovery: soil C density fractions recovered at 96%

- Data attributes and units
  - CO2 concentration: ppm
  - C content: %, SOC: Mg C ha^-1
  - CO2 flux: uL m^-2 min^-1, umol m^-2 s^-1, g C m^-2 d^-1, Mg C ha^-1 yr^-1
  - Fraction metrics: fraction C (%), fraction weight (g), mass recovery percentage
  - Depth and bulk properties: soil depth (cm), bulk density (g cm^-3)
  - Decomposition: dry weight remaining (%)

- Data structure: five spreadsheets
  - Peruvian_Andes_CO2_Raw.csv
    - Columns include: Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)
  - Peruvian_Andes_CO2_Fluxes.csv
    - Columns include: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure (atm), Chamber temp. (°C), Chamber temp. (K), Mole (HMR) (n=PV/RT), CO2 Flux (HMR) (µL/m^2/min), CO2 Flux (µmol/m^2/s), CO2 Flux (g C m^-2 d^-1), CO2 Flux (Mg C ha^-1 yr^-1)
  - Peruvian_Andes_Soil_C.csv
    - Columns include: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth (cm), C (%), Bulk density (g cm^-3), SOC (Mg C ha^-1)
  - Peruvian_Andes_Soil_Decomposition.csv
    - Columns include: Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial average stick weight (g), Stick weight after collection (g), Dry weight remaining (%)
  - Peruvian_Andes_Soil_C_Fractions.csv
    - Columns include: Sequence, Code, Site, Soil depth (cm), Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight (g), C in fraction (g), Total C (LF + OLF + HF) (g), Fraction of total C (%), Mass of soil recovered (%)
  - Codes and abbreviations
    - Site: A = Acjanaco, W = Wayqecha
    - Grazing: NG = Not grazed, G = Grazed
    - Burn: B = Burnt, NB = Not burnt
    - Timing: Morn = morning, Aft = Afternoon
    - Replicates: 1–4
    - Depths: 5cm, etc.
  
- Coding scheme and terminology
  - Key terms: CO2, SOC, NaPT (density fractionation), LF (free light fraction), OLF (occluded light fraction), HF (heavy fraction)
  - Purpose of the data: enable analysis of how burning and grazing affect soil CO2 fluxes, carbon stocks, fractionation, and decomposition across depths and over a year

- Data quality and considerations for use
  - Replication: multiple plots per treatment with four chamber bases per plot
  - Temporal coverage: July 2011 to July 2012 for flux measurements
  - Depth coverage: primarily 0–30 cm, with some shallow soils limiting deeper sampling
  - Data processing: standardized flux calculations; fractionation and C analyses follow established lab protocols; 96% recovery for C fractions
  - Potential data use: assess impacts of land management on soil carbon dynamics, compare site responses to burning and grazing, integrate CO2 flux data with SOC pools and decomposition rates for holistic soil Carbon budgeting

- Practical notes for integration and exploration
  - The five CSV files are designed for cross-linking via common keys (Site, Burn/Grazing, Burn year, Replicate, Depth)
  - Unit consistency is maintained across fluxes and carbon metrics, enabling comparative analyses and modeling
  - The dataset supports self-contained analyses of CO2 flux dynamics, soil carbon stocks, decomposition rates, and carbon fraction partitioning under different land-management scenarios

- Timeline
  - Measurements conducted over one year (July 2011–July 2012) with ancillary sampling and processing conducted around July 2011 as the initiation of decomposition trials

- Accessibility
  - Data are organized into clearly named CSV files with explicit column definitions to aid data discovery, cleaning, and reuse for broader analyses of soil carbon under land management in tropical montane grasslands