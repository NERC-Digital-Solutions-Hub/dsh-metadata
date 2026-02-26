# Dataset Description (Soil_Nutrients)

## Overview
- Describes soil nutrient availability across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Sampling conducted March–April 2016 as part of the NERC-funded BALI project.

## Sampling design
- 9 one-hectare plots across 3 sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified design: each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 3 subplots sampled per plot.
- Within each subplot, 4 pairs of PRS™ ion exchange membranes buried to ~10 cm for 2 weeks, then eluted with 0.5 M HCl.
- Membranes from each location pooled and analyzed.
- Analyses:
  - NO3- and NH4+ measured colorimetrically via automated flow injection analysis (FIA).
  - All other elements analyzed by ICP-OES.
- Results reported as supply rates per 10 cm² (area of membrane) over 14 days (µg/10 cm²/14 days).

## Data structure and metadata
- 21 data columns: Identifier, Site, Land_Use, Plot_Name, Subplot, NO3_N, NH4_N, Total_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd.
- Metadata definitions include:
  - Identifier: unique sample identifier (text).
  - Site: geographical site (text).
  - Land_Use: unlogged forest, logged forest, or oil palm plantation (text).
  - Plot_Name: name of the 1 Ha plot (text).
  - Subplot: subplot number within each plot (numeric).
  - Nutrient columns: concentration values for each element, with units as µg/10 cm²/14 days.
- Method Detection Limits (MDLs) provided for each element; data are reported as measured even when below MDL; zeros indicate non-detectable levels.

## Measurements and detection limits
- NO3_N, NH4_N: analyzed by FIA.
- Other elements (Total_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd): analyzed by ICP-OES.
- MDL values listed for each element; non-detects recorded as zeros.

## Data quality, provenance, and references
- Data collected under Riutta et al. 2018; metadata and methodological references include:
  - Qian, P. & J. J. Schoenau (2002) on ion exchange resins (Practical applications).
  - Riutta et al. (2018) on logging disturbance effects in Bornean tropical forests.
  - Western Ag (provider of PRS membranes) website.

## Data governance and sharing considerations
- Ensure consistent units and formatting across the dataset (µg/10 cm²/14 days; text fields for Site and Land_Use).
- Maintain explicit metadata mappings to support discoverability and interoperability.
- Document sampling design and measurement methods to enable reproducibility and proper interpretation.
- Record and communicate any data availability limitations or embargoes; clearly state MDLs and how non-detects are handled.
- Consider updates and versioning if future datasets from the same study are released; ensure portal-ready formats and proper citations.

## Limitations and cautions
- Temporal scope limited to a two-week burial period in 2016; cross-site comparisons may be affected by sampling window and environmental conditions.
- Use context from referenced studies (Riutta et al. 2018) for interpretation of land-use effects and disturbance impacts.
- Large dataset size and potential transfer considerations noted for large-scale sharing.

## References
- Qian, P. & J. J. Schoenau (2002). Practical applications of ion exchange resins in agricultural and environmental soil research. Canadian Journal of Soil Science, 82, 9-21.
- Riutta, T. et al. (2018). Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology.
- Western Ag (www.westernag.ca).