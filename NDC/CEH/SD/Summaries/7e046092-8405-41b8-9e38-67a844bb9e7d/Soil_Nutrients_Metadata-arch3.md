# Dataset Description (Soil_Nutrients)

## Overview
- Describes soil nutrient availability across three land-use types in Sabah, Malaysia: unlogged tropical forest, logged tropical forest, and oil palm plantation.
- Collected March–April 2016 as part of the NERC-funded BALI project.
- Data captured as nutrient supply rates per 10 cm2 over a 14-day burial period using ion exchange membranes, analyzed for multiple elements.

## Sampling Design and Methods
- 9 one-hectare plots across 3 sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project.
- Stratified sampling: each 1-ha plot subdivided into 25 subplots; 3 subplots randomly selected for sampling.
- Within each subplot location, 4 pairs of PRS ion exchange membranes (one pair for cations, one for anions) buried to ~10 cm for 2 weeks.
- Membrane pairs from each location pooled prior to elution; eluted with 0.5 M HCl for 1 hour.
- Analyses:
  - Nitrate (NO3-) and ammonium (NH4+) by colorimetric methods with automated flow injection analysis (FIA).
  - All other elements by inductively coupled plasma – optical emission spectroscopy (ICP-OES).
- Results reported as supply rates per 10 cm2 (area of membrane available for ion exchange) over 14 days (µg/10 cm2/14 days).

## Dataset Structure and Metadata
- 21 columns including:
  - Identifier (Unique Sample Identifier)
  - Site (geographical area/site)
  - Land_Use (Unlogged, Logged, Oil palm plantation)
  - Plot_Name (1-ha plot name)
  - Subplot (subplot number)
  - NO3_N, NH4_N, Total_N (and other nutrient elements: Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd)
- Units:
  - All nutrient concentrations expressed as µg/10 cm2/14 days.
  - Total_N is the sum of NO3_N and NH4_N.
- Metadata details provided for each field (descriptions and units/formats).

## Measurements, Units, and Detection Limits
- Method Detection Limits (MDL) provided for each element.
- Data are reported as measured even when below MDL; zeros indicate non-detectable levels.
- MDL values listed for NO3_N, NH4_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd (values vary by element).

## Land Use, Sites, and Context
- Land-use categories: Unlogged tropical forest, Logged tropical forest, Oil palm plantation.
- Sites include DVCA, MBCA, and SAFE project in Sabah, representing a gradient of disturbance and management.

## Data Quality, Governance, and Use for Monitoring
- Metadata-rich dataset enabling traceability and comparability across land-use types and sites.
- Standardized sampling and analytical methods support monitoring and evaluation of nutrient availability under different management regimes.
- Availability of MDLs facilitates assessment of data reliability and detection capability in policy-relevant analyses.

## References
- Qian, P. & J. J. Schoenau (2002). Practical applications of ion exchange resins in agricultural and environmental soil research. Canadian Journal of Soil Science, 82, 9-21.
- Riutta, T. et al. (2018). Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology, 0.
- Western Ag (supplier of PRS ion exchange membranes): www.westernag.ca

## Notes for Policy and Monitoring Implications
- Provides a replicable framework for assessing nutrient availability across land-use changes, informing decisions on forest conservation vs. agricultural expansion.
- Demonstrates integration of field sampling, laboratory analyses, and metadata standards to support transparent, data-driven environmental health monitoring.