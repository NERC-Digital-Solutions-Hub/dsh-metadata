# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

## Overview
- Longitudinal study of soil CO2 fluxes, soil carbon content and fractions, and decomposition under different land-management treatments in two sites within Manu National Park, Peru.
- Factorial design: burnt vs not burnt, grazed vs not grazed, in adjacent unburnt areas, with fencing to exclude cattle in some plots.
- Data collected from July 2011 to July 2012 across multiple measurements and depths, organized into five datasets.

## Study Area and Experimental Design
- Location: Manu National Park, Peru; two sites:
  - Wayqecha (burnt in 2003)
  - Acjanaco (burnt in 2005)
- Site arrangement: adjacent unburnt areas within 200 m, each split into 2 x 2 m subplots.
- Treatments (2x2 factorial): burnt/not burnt x grazed/not grazed.
- Sample layout: each site contained four plots per treatment combination with four permanent PVC chamber bases per plot for CO2 flux measurements.

## Data Collection Methods
- CO2 flux measurements:
  - Static chamber method with Vaisala CARBOCAP CO2 probe and temperature sensor.
  - Measurements every 30 seconds for 3 minutes, morning and afternoon, monthly interval (July 2011 – July 2012).
  - Environmental data: air temperature, atmospheric pressure; time of day recorded.
  - Flux calculations performed in R (HMR package) using time vs headspace CO2 concentration.
- Soil sampling:
  - 50 g samples at depths: 0-5, 5-10, 10-20, 20-30 cm (shallow soils where bedrock encountered).
  - Six replicates per depth per site.
  - Samples air-dried, sieved (2 mm), shipped to University of St Andrews for analyses.
- Decomposition experiment:
  - 18 birch wood sticks placed in mesh bags at 10 cm depth; bags retrieved every two months.
  - Mass loss used to calculate decomposition rate via linear regression over time.

## Analytical Methods
- Bulk density:
  - Undisturbed soil cores (30 cm3) collected; dried at 105 °C for 48 h; bulk density computed as dry mass per core volume.
- Soil fractionation (organic carbon fractions):
  - Sieve and density separation using sodium polytungstate (NaPT) to yield free light fraction (free LF), occluded light fraction (OLF), and heavy fraction (HF).
  - Fractions separated, dried at 100 °C, weighed, ground, and prepared for C and isotope analyses.
  - Recovery of carbon density fractions ~96%.
- Carbon analysis:
  - Bulk soils ground and analyzed via EA-IRMS (Finnegan Delta plus XP) at University of St Andrews.

## Data Output and Structure
- Data records organized into five CSV spreadsheets:
  - Peruvian_Andes_CO2_Raw.csv
    - Columns include: Sequence, Code, Site, Grazing, Burning, Burn year, Replicate, Month, Time of day, Sampling time, Time (mins), CO2 concentration (ppm)
  - Peruvian_Andes_CO2_Fluxes.csv
    - Columns include: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Month, Season, Time of day, Pressure (atm), Chamber temp. (°C), Chamber temp. (K), Mole (HMR) (n=PV/RT), CO2 Flux (HMR) (µL/m2/min), CO2 Flux (µmol/m2/s), CO2 Flux (g C m-2 d-1), CO2 Flux (Mg C ha-1 yr-1)
  - Peruvian_Andes_Soil_C.csv
    - Columns include: Sequence, Code, Site, Replicate, Burning, Grazing, Burn year, Soil depth (cm), C (%), Bulk density (g cm-3), SOC (Mg C ha-1)
  - Peruvian_Andes_Soil_Decomposition.csv
    - Columns include: Sequence, Code, Site, Burning, Grazing, Burn year, Replicate, Date, Initial average stick weight (g), Stick weight after collection (g), Dry weight remaining (%)
  - Peruvian_Andes_Soil_C_Fractions.csv
    - Columns include: Sequence, Code, Site, Soil depth (cm), Replicate, Grazing, Burning, Fraction, Fraction C (%), Fraction weight (g), C in the fraction (g), Total C (LF + OLF + HF) (g), Fraction of total C (%), Mass of soil recovered (%)
- Coding scheme examples:
  - Site: A = Acjanaco, W = Wayqecha
  - Grazing: NG = Not grazed, G = Grazed
  - Burning: B = Burnt, NB = Not burnt
  - Time: Morn = morning, Aft = Afternoon
  - Month/Period: 1 = July 2012, 5cm = soil depth, HF = Heavy fraction, LF = Free light fraction, OLF = Occluded light fraction

## Key Variables and Units
- CO2 concentration: ppm
- CO2 flux: µL/m2/min, µmol/m2/s, g C m-2 d-1, Mg C ha-1 yr-1
- Soil carbon content: C (%), SOC (Mg C ha-1)
- Bulk density: g cm-3
- Decomposition: dry weight remaining (%)
- Fractions: % and mass of C in Free LF, Occluded LF, and Heavy fraction

## GIS and Data Integration Considerations
- Spatial context: two sites within Manu National Park, with precise coordinates provided in text; adjacent unburnt plots within 200 m, enabling fine-scale spatial comparisons.
- Temporal resolution: measurements span July 2011 – July 2012 with repeated measurements (morning/afternoon; every two months for CO2 fluxes).
- Data interoperability: five structured CSV datasets with clearly defined fields and coding scheme, suitable for GIS attribute joins and spatial analyses with associated plot locations.
- Data quality and provenance: detailed methodological notes on collection and analysis methods; replication design and fractionation procedures support reproducibility and data cleaning.
- Potential GIS use: map-based visualization of CO2 fluxes and soil C across treatments and depths; spatial modelling of carbon dynamics under land management; integration with environmental layers (soil type, topography, climate) for spatial risk and impact assessments.