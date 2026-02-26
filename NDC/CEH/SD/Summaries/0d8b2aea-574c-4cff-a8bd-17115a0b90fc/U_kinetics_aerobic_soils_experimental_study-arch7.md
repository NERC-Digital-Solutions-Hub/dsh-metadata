# Measurements of soluble, chemically exchangeable and isotopically exchangeable UO2^2+ concentrations in soils following laboratory contamination and 619-day incubation

## Dataset scope and purpose
- Measurements of soluble, chemically exchangeable, and isotopically exchangeable UO2^2+ concentrations in 20 soils from central England.
- Soils were contaminated with UO2^2+ and incubated in the laboratory for 619 days to study kinetics of UVI transformations and binding strength in aerobic soils.
- Data support models of long-term UVI mobility and bioavailability under temperate, aerobic soil conditions.

## Spatial and contextual information
- Twenty topsoil samples (0–15 cm) collected across central England from diverse land uses (arable, grassland, moorland, woodland).
- For each soil: location coordinates (latitude/longitude), land use, organic carbon content, and pH.
- Sub-sampling within ~5 m^2 grids to form composite ~3 kg field-moist soil samples.

## Soil sampling and characterization
- Soil properties recorded prior to contamination:
  - Organic carbon content (various percent ranges, e.g., from ~1.7% to ~38.6%)
  - Soil pH (ranging from acidic to near-neutral/alkaline in the dataset)
  - Land use category (arable, grassland, moorland, woodland)
- Specific soil identifiers (e.g., CO-A, EV-A, NP-A, SR-A, WK-A, WS-A, BH-G, DY-G, etc.) with corresponding coordinates and properties.

## U addition and incubation setup
- Contamination: soils mixed with a U(VI)O2^2+ solution to 5000 µg UVI per kg dry soil.
- Microcosms: soils distributed into three bottles per soil, with gas-exchange lids and dark incubation at 10.0 ± 1.0 °C for 619 days.
- Incubation conducted Nov 2014 – Aug 2016 at the University of Nottingham.

## U fractionation and isotopic measurements
- Fractionation protocol (per sampling time):
  - Soluble U: extracted with 0.01 M KNO3 (approximate soil pore water ionic strength).
  - Chemically exchangeable U: extracted with 1 M Mg(NO3)2 (to target electrostatically adsorbed U on Fe/Mn oxides).
  - Labile U: extracted after equilibration with Mg solutions and prepared for isotopic exchange measurements.
  - Isotopically exchangeable U: measured via isotopic exchange using spikes of 233U and 236U.
- Analytical techniques:
  - Concentrations determined by ICP-MS (iCAP-Q) with Ir internal standard.
  - Isotopic exchange quantified by tracking 233U, 236U, and 238U to derive the isotopically exchangeable pool.
- Data outputs (per soil/timepoint):
  - U in soluble fraction (µg U kg^-1 dry soil)
  - U in chemically exchangeable fraction (µg U kg^-1 DW)
  - U in labile fraction (µg U kg^-1 DW)
  - U in isotopically exchangeable fraction (µg U kg^-1 DW)

## Data structure and variables (for GIS use)
- Spatial attributes per soil:
  - Soil ID, land use, latitude, longitude, pH, organic carbon (%)
- Temporal and fractionation attributes:
  - incubation_days since contamination
  - soluble_U_µg_kg
  - exch_U_µg_kg
  - labile_U_µg_kg
  - isotopically_exchangeable_U_µg_kg
- Methods and references:
  - Extraction methods (0.01 M KNO3, 1 M Mg(NO3)2 with 233U and 236U)
  - Instrumentation (iCAP-Q ICP-MS) and internal standard (Ir)
  - Isotopic correction using 233U/236U spike
- Data context:
  - Tables describe the extracts and calculations; specific values are provided as µg U per kg dry soil.

## Potential GIS applications and visualizations
- Spatial distribution maps of U fractions across soils to identify patterns related to land use, pH, and organic carbon.
- Multivariate maps showing correlations between U fractionation and soil properties (pH, organic C) for risk assessment.
- Time-series visualizations (per soil) of soluble, exchangeable, labile, and isotopically exchangeable U fractions to study kinetics.
- Integration with environmental risk models to predict long-term mobility and bioavailability of UVI under temperate conditions.

## Data quality, limitations, and considerations
- Laboratory incubation under controlled conditions (10 °C, darkness) may limit direct extrapolation to field scenarios.
- Only 20 soils from central England; regional representativeness may be limited.
- Data density depends on sampling schedule (incubation days) and may require interpolation for temporal analysis.
- Units and reference frames: ensure consistent units (µg U kg^-1 DW) and coordinate system (likely WGS84) when mapping.

## Additional notes for interpretation
- The dataset is designed to quantify kinetic transformations and binding strength of UVI in aerobic soils, informing models of long-term mobility in groundwater-saturated environments.
- Isotopic tracing enables differentiation between readily exchangeable U and more persistent bound forms, crucial for understanding potential plant uptake and mobility pathways.