# Soil and gas measurements from Puna grasslands under different land management over one year - Supporting Documentation

## Overview
- A year-long study in Manu National Park, Peru, assessing soil CO2 flux, soil carbon fractions, and decomposition under different land-management regimes (burning and grazing) on two sites with adjacent unburned controls.
- Includes both measurements (gas fluxes, soil chemistry) and decomposition experiments, with detailed analytical approaches and data organization.

## Study Location and Experimental Design
- Sites: Wayqecha (burnt in 2003) and Acjanaco (burnt in 2005), with adjacent unburnt areas within 200 meters.
- Plot layout: Each site split into two subplots (2 x 2 m) under two treatments, forming a full factorial: burnt/not burnt x grazed/not grazed.
- Fire/grazing context: Burn status and grazing status are primary experimental factors; fencing implemented 2 years before sampling to exclude cattle in the fenced plots.
- Timing: CO2 measurements conducted morning and afternoon every two months from July 2011 to July 2012.
- Measurements targeted: soil surface CO2 fluxes, soil carbon content and fractions, bulk density, and decomposition rates.

## Data Collection Methods
- CO2 flux measurements:
  - Four permanent PVC chamber bases per plot (diameter 20 cm, height 10 cm); random deployment.
  - Static flux chamber technique with Vaisala CARBOCAP CO2 probe and internal temperature sensor inside a 20 cm tall chamber with a gas-tight lid.
  - Readings: CO2 accumulation every 30 seconds for 3 minutes; simultaneous air temperature and atmospheric pressure data recorded.
  - Calculation: Fluxes derived in R (R 3.0.2) using headspace CO2 (ppm) vs. time; regression (linear or non-linear) chosen by best fit.
- Soil sampling:
  - 50 g soil samples collected in July 2012 at depths 0–5, 5–10, 10–20, and 20–30 cm; many plots shallow to bedrock, so deeper sampling not always possible.
  - Samples air-dried, sieved to 2 mm, then shipped to the University of St Andrews for analyses.
- Decomposition experiments:
  - Birch sticks (five per bag) buried at 10 cm depth; 18 bags arranged in groups of six per plot.
  - Retrieval every two months; weights measured before burial and after air-drying to calculate mass loss and decomposition rate (from time vs. mass loss regression).

## Analytical Methods
- Bulk density:
  - Undisturbed soil cores (30 cm3) collected from 0–10, 10–20, and 20–30 cm; dried at 105°C for 48 hours; bulk density computed as oven-dried mass divided by core volume.
- Soil fractionation:
  - Subsample (15 g) subjected to density-based separation using sodium polytungstate (NaPT) to obtain:
    - Free light fraction (free LF)
    - Occluded light fraction (OLF)
    - Heavy fraction (HF)
  - Process includes washing, centrifugation, ultrasonication, and sequential rinsing to remove NaPT; fractions dried and weighed; recovery of carbon density fractions ~96%.
- Carbon analysis:
  - Samples ground and homogenized; analyzed for carbon content using a Finnegan Delta plus XP gas source mass spectrometer coupled to an elemental analyzer (EA-IRMS) at St Andrews.
- Units and data transformation:
  - Reported in multiple units (e.g., CO2 concentration in ppm; CO2 flux in μmol/m2/s, g C m−2 d−1, Mg C ha−1 yr−1; SOC in Mg C ha−1; fraction C as %; mass recovery as %).

## Data Structure and Metadata
- Data products (five spreadsheets):
  - Peruvian_Andes_CO2_Raw.csv
  - Peruvian_Andes_CO2_Fluxes.csv
  - Peruvian_Andes_Soil_C.csv
  - Peruvian_Andes_Soil_Decomposition.csv
  - Peruvian_Andes_Soil_C_Fractions.csv
- Key column details and coding:
  - Site codes: A = Acjanaco; W = Wayqecha
  - Grazing: NG = Not grazed; G = Grazed
  - Burn status: B = Burnt; NB = Not burnt
  - Time indicators: Morn = morning; Aft = afternoon
  - Replicates: 1–4
  - Time and sampling indicators use month codes (e.g., A = July 2012) and sequential letters for sampling events
- Example columns:
  - CO2_Raw: sequence, code, site, grazing, burning, burn year, replicate, month, time of day, sampling time, time (mins), CO2 concentration (ppm)
  - CO2_Fluxes: sequence, code, site, replicate, burning, grazing, burn year, month, season, time of day, pressure, chamber temperature, mole, CO2 flux values in multiple units
  - Soil_C: sequence, code, site, replicate, burning, grazing, burn year, soil depth (cm), C (%), bulk density, SOC (Mg C ha−1)
  - Soil_Decomposition: sequence, code, site, burning, grazing, burn year, replicate, date, initial weight, final weight, dry weight remaining (%)
  - Soil_C_Fractions: sequence, code, site, soil depth, replicate, grazing, burning, fraction (HF, LF, OLF), C fraction (%), fraction weight, C in fraction, total C (HF+OLF+LF), fraction of total C, mass of soil recovered
- Data quality notes:
  - Carbon fraction recovery reported at 96%, indicating robust fractionation efficiency.
  - Data intended for cross-comparison across treatments and time, supporting meta-analyses on soil carbon dynamics under land management.

## Data Quality, Provenance, and Accessibility
- Temporal coverage: July 2011–July 2012 for CO2 flux measurements; July 2012 for soil sampling; staggered decomposition measurements over the study period.
- Provenance: Detailed methodological documentation supports traceability of measurements and calculations (e.g., R-based flux calculations, NaPT density fractionation steps, EA-IRMS carbon analysis).
- Data governance considerations for Data Stewards:
  - Rich, multi-faceted dataset requiring careful metadata curation to ensure interoperability (units, fractions, coding schemes).
  - Uses standardized yet complex laboratory methods (density fractionation) that necessitate precise methodological notes for reuse.
  - Large, longitudinal data structure with multiple related files; requires robust data versioning, linking keys, and documentation to maintain discoverability and reusability.
  - Potential integration with other datasets (soil carbon pools, fractions, decomposition) through consistent site codes and depth conventions.