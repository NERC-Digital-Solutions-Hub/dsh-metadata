# Dataset Description (Soil_Nutrients)

## Overview
- Describes soil nutrient availability across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Sampling occurred March–April 2016 as part of the NERC-funded BALI project.
- Data file Soil_Nutrients.csv includes 21 columns detailing sample identifiers, location, land use, plot details, and concentrations of multiple nutrients/elements.
- Results are reported as supply rates per 10 cm2 over a 14-day burial period (µg/10 cm2/14 days).

## Sampling design and methods
- Study design: 9 one-hectare plots across 3 sites representing the three land-use types (Danum Valley Conservation Area, Maliau Basin Conservation Area, SAFE project).
- Approach: stratified sampling with each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 3 subplots sampled per plot.
- Within each subplot: 4 pairs of PRS™ ion exchange membranes (one pair = 1 cation & 1 anion) placed vertically to ~10 cm depth at 3 locations per subplot.
- Burial duration: membranes left in situ for 2 weeks, then retrieved, rinsed, and shipped for analysis.
- Analysis: pooled four probe pairs per location, eluted with 0.5 M HCl for 1 hour.
  - NO3- and NH4+ measured colorimetrically via automated flow injection analysis (FIA).
  - All other elements measured using ICP-OES.
- Data reported as supply rates per 10 cm2 area over the burial period.

## Variables and measurements
- Primary data columns: 
  - Identifier, Site, Land_Use, Plot_Name, Subplot
  - NO3_N, NH4_N, Total_N
  - Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd
- Units: µg/10 cm2 / 14 days for all nutrient concentrations (except Total_N is the sum of NO3_N and NH4_N for the same pool); metadata specifies units accordingly.
- Land_use categories: Unlogged tropical forest, Logged tropical forest, Oil palm plantation.
- MDL (Method Detection Limits) provided for each element; zeros denote non-detectable concentrations.

## Metadata and data structure
- Metadata fields:
  - Identifier: Unique sample identifier
  - Site: Geographical area/site
  - Land_Use: Land use category
  - Plot_Name: Name of the 1 Ha plot
  - Subplot: Subplot number within each plot
  - Each nutrient/element field has a corresponding unit/description in the metadata
- Data handling notes:
  - Data are reported as measured even if below the MDL.
  - Zeros indicate non-detectable concentrations.

## Method detection limits (MDL)
- MDL values provided for each element (e.g., NO3_N, NH4_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd).
- Example MDLs (per 1 = MDL micrograms/10 cm2/14 days): NO3_N = 2, NH4_N = 2, Ca = 2, Mg = 4, K = 4, P = 0.2, Fe = 0.4, Mn = 0.2, Cu = 0.2, Zn = 0.2, B = 0.2, S = 2, Pb = 0.2, Al = 0.4, Cd = 0.2.

## References
- Qian, P. & J. J. Schoenau (2002) Practical applications of ion exchange resins in agricultural and environmental soil research. Canadian Journal of Soil Science, 82, 9-21.
- Riutta, T. et al. (2018) Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology, 0.
- Western Ag (www.westernag.ca) for PRS ion exchange membranes.