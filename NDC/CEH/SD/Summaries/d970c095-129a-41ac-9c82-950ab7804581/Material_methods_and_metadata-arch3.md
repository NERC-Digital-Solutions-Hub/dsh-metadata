# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Overview
- Document detailing methods, sampling, and metadata for a UK LTLS study on denitrification and greenhouse gas (GHG) emissions in natural and semi-natural terrestrial ecosystems.
- Two catchments: Conwy (N Wales) and Ribble-Wyre (NW England); focus on N, C, and P fluxes between soil, water, and air under climate perturbations.
- Study period: monthly gas flux measurements from Apr 2013 to Oct 2014 (17 months), with some sampling months skipped (Nov 2013, Jan 2014).

## Study design and sites
- Study sites categorized by land-use types across catchments:
  - Conwy: C-PB peat bog, C-UG unimproved grassland, C-IG improved grassland, C-MW mixed woodland.
  - Ribble-Wyre: R-UG unimproved grassland, R-IG improved grassland, R-HL heathland, R-DW deciduous woodland.
- Site-specific soil types and conditions described; variations in altitude, rainfall, grazing/fertilization regimes.
- Sampling framework: five plots per site, 40 plots per monthly campaign; each plot with a soil collar for gas flux measurements.
- Replication and site categorization used in prior analyses to group sites into land-use types (organic soils, IG, SIG, MW, DW).

## Gas flux measurement and denitrification assessment
- Gas fluxes measured monthly using static chambers placed on soil collars (approx. 0–15 cm depth adjustments for some plots).
- 15N tracer methodology:
  - Labelled K15NO3 applied in plots to trace denitrification-derived N2O production.
  - 15N tracer injected via grid with multiple injections; tracer solution moisture adjusted to match soil water content.
  - Chamber headspace sampled at 0, 1, and 2 hours after enclosure for gas concentrations.
- Analytical workflow:
  - CFIRMS used for 15N-N2 and 15N-N2O (in-house continuous flow isotope ratio mass spectrometer).
  - GC-μECD for total N2O, GC-FID for CH4 and CO2.
  - Determination of fluxes using linear regression of concentration vs time, with adjustments to standard temperature/pressure.
  - Minimum detectable concentration differences (MDCD) and fluxes calculated; only values above MDCD used; others treated as zero flux.
- Denitrification attribution:
  - DN2O flux derived from CF-IRMS data; TN2O flux from incubations extended to 20 hours when needed to align with DN2O.
  - Rules applied for cases with negative TN2O, zero TN2O, or DN2OTN2O discrepancies to assign denitrification-derived N2O.
  - In some samples, when DN2O exceeded TN2O by up to 10%, the entire N2O flux assigned to denitrification.
- Temporal aggregation:
  - Annual GHG fluxes computed by interpolating monthly measurements; 100-year horizon GWP calculated for N2O and CH4 (298 and 34 multipliers, respectively).
- Additional soil sampling:
  - Five composite soil samples (0–10 cm) collected near plots after gas sampling for later analyses.

## Data, units and outputs
- Key data files (examples of variables):
  - Denitrification_data_N20.csv: N2 flux, N2O flux (μg N m^-2 h^-1)
  - GHG_data_CH4.csv: CH4 flux (μg N m^-2 h^-1)
  - GHG_data_CO2.csv: CO2 flux (mg C m^-2 h^-1)
  - GHG_data_DN20TN2O.csv: DN2O/TN2O ratio (%)
  - GHG_data_N2O.csv: Total N2O flux (μg N m^-2 h^-1)
  - Soil_properties_*: various soil metrics (nitrate, TDN, NH4-N, bulk density, C/N, DOC, moisture, OM, pH, temperature, WFPS)
- Units indicators and labels clarified (e.g., μg N2O-N m^-2 h^-1, mg CO2-C m^-2 h^-1, g/cm^3 for bulk density).
- Sampling dates span Apr 2013–Oct 2014 with specific months omitted (e.g., Nov 2013, Jan 2014).
- Location references and maps provided (Conwy and Ribble catchments) with grid references and links.

## Metadata and documentation standards
- Detailed replicate/location metadata for each site:
  - Catchment, Land use Type, Latitude (degrees, minutes, decimal), Longitude (degrees, minutes, decimal)
  - X_BNG and Y_BNG coordinates; Grid Reference
  - Replicate identifiers (e.g., C-ML, C-RG, R-ML, etc.)
- Sampling date records accompany site metadata.
- Map links included for geographic context:
  - Conwy Map Link
  - Ribble Map Link
- Note: Empty cells indicate missing data due to sampling or analytical failure.

## Relevance for monitoring frameworks
- Demonstrates a comprehensive workflow integrating field sampling, isotopic tracing, and multi-gas analysis to quantify denitrification and GHG fluxes across diverse land uses.
- Emphasizes the importance of:
  - Rigorous, standardized metadata and site descriptors to enable cross-site comparability.
  - Clear definitions and handling rules for flux calculation, detection limits (MDCD), and attribution of N2O sources.
  - Transparent data outputs with explicit units and data file structures to support data governance and re-use.
- Highlights management of data gaps and complex data processing requirements (e.g., DN2O/TN2O calculations, 20-hour incubations where needed) essential for robust monitoring frameworks.