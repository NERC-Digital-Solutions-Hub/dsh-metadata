# Soil organic matter fractions

## GIS-focused overview
- Provides UK-wide, 1-km resolution data on soil organic matter (SOM) density fractions and associated carbon and nitrogen contents, enabling map-based visualization of soil health, carbon stocks, and temporal change.
- Based on the UK Countryside Survey rolling programme (2019–2023), with annual sampling across 100 of 500 randomly selected 1-km2 squares, stratified by landscape characteristics.
- Data suitable for integrating with vegetation and other environmental layers to support policy, land management, and public-interest visualizations.

## Survey design and sampling framework
- Rolling survey: 500 x 1-km2 squares over a five-year cycle; 100 squares sampled per year; aims to detect change while accommodating climate variability.
- Exclusions: squares with >75% urban land or >90% sea.
- Within each square: up to 5 randomly dispersed locations for topsoil sampling, coordinated with vegetation X-Plots.
- Sample processing: archived soil samples (2 mm sieve, air-dried) used for SOM density fractionation; LOI, hygroscopic water, and CaCO3 measured via thermogravimetric analysis (TGA).

## Laboratory methods and fractionation workflow
- SOM density fractions considered: dissolved organic carbon (DOC), free light fraction (LF), occluded particulate fraction (OF), and mineral-associated OM (MAOM); in this study, DOC and OF were discarded; LF and MAOM analyzed, with OF derived by mass balance.
- Density fractionation: sodium polytungstate solution (1.8 g/cm3) used to separate LF (light fraction) and MAOM (mineral-associated) from archived soil; OF obtained after aggregate disruption and centrifugation steps.
- Carbon and nitrogen analyses: total C and N measured on LF and MAOM fractions and archived soil using a Vario-Ele elemental analyzer; SOC computed as total C minus calcite-C; LF-C and MAOM-C calculated from carbon concentrations and fraction masses; OF-C and OF-N derived by mass balance.
- POM concept: POM-C and POM-N calculated as LF-C + OF-C and LF-N + OF-N, respectively.
- Corrections and quality control: hygroscopic water content corrections applied to relevant fractions; calcite-C correction applied to MAOM-C and SOC; negative OF-C or OF-N values set to zero due to measurement uncertainty; internal standards and 10% replicated samples used to assess accuracy; calcite recovery targeted at 95–100%.

## Calculations and data corrections
- SOM fractionation details: LOI measured via TGA; SOM content calculated from LOI steps; hygroscopic moisture fraction computed from weight losses; CaCO3 content derived from weight changes between temperature steps with a correction factor (2.27) and applied to calcite-C calculations.
- Fraction masses and carbon/nitrogen concentrations used to compute:
  - LF-C, MAOM-C
  - OF-C, OF-N (via residuals)
  - POM-C, POM-N (LF + OF)
  - SOC (calcite-corrected total C minus calcite-C)
  - Total soil nitrogen (TN)
- Data are corrected for hygroscopic water across LF, MAOM, total SOC; OF and POM fractions inherit their corrections via mass balances.

## Data fields and structure
- Dataset: 13 columns, 101 rows.
- Key fields (examples): Year, SQ_ID; LF_C_gperg; MAOM_C_gperg; OF_C_gperg; POM_C_gperg; LF_N_gperg; MAOM_N_gperg; OF_N_gperg; POM_N_gperg; SOC_gperg; TN_gperg; SOM_gperg.
- Not all metrics are available for every sample (NA indicates not analysed); dataset aligns with SOP3102 UKAS-accredited methods.

## Data provenance, accessibility, and support
- Source: UKCEH Countryside Survey, Great Britain; rolling programme initiated 2019, supported by UK-SCAPE (NERC) and AI4SoilHealth (funding details in document).
- Data products generated to enable stock and change maps for GB soils, co-located with vegetation assessments, and designed for integration into GIS workflows.
- Full methodological details and validation are described in Reinsch et al. (2024); related topsoil properties for 2018–2019 and 2020 datasets published (Bentley et al., 2023a, 2023b).

## Applications and implications for GIS specialists
- Enables spatial mapping of SOM density fractions (LF, MAOM, OF, POM) and associated C/N stocks across GB soils at 1-km resolution.
- Facilitates time-series analysis and change detection through the rolling survey design (annual square sampling).
- Supports linkage with vegetation data and landscape classifications to explore drivers of soil carbon dynamics.
- Useful for policy planning, land management, climate research, and public communication about soil health and carbon cycling.

## References (selected)
- Reinsch et al. 2024 (method details for SOM density fractionation)
- Bentley et al. 2023a, 2023b (topsoil physico-chemical properties, GB 2018–2019 and 2020)
- UK-SCAPE/NERC programme and related Countryside Survey methodology (Emmett et al. 2010; Reynolds et al. 2013; Keith et al. 2020)