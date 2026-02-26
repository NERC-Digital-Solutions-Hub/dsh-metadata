# Soil organic matter fractions

- Analyzes soil organic matter (SOM) fractions to understand turnover and stabilization mechanisms.
- Four traditional fractions described (DOC, LF, OF, MAOM); in this study, DOC and OF were discarded, focus is on Free Light fraction (LF) and Mineral-Associated OM (MAOM) with OF inferred by mass balance.
- Data derived from UKCEH Countryside Survey, a long-running national soil and vegetation monitoring program.

## Data context and purpose

- Countryside Survey provides a national-scale audit of soil and vegetation change in the UK, enabling comparisons from 2019 onward with historic surveys.
- UK-SCAPE national capability program funds rolling monitoring from 2019 to 2023 to map stock and change in GB soils, co-located with vegetation assessments.
- Rolling design: 500 one-km squares across Great Britain per five-year cycle; 100 squares sampled annually; exclusion of highly urban or ocean-dominated squares.
- Sampling is designed to capture multi-metric ecosystem data in a single snapshot, enabling integration across soil and vegetation datasets.

## Data collection and lab methods

- Sample collection:
  - Within each 1-km square, up to 5 randomly dispersed locations with vegetation plots.
  - Topsoil samples collected with a 15 cm core from locations co-incident with vegetation surveys.
  - 100 archived soil samples (2 mm sieved, air-dried) used for SOM density fractionation in spring 2022.
- Laboratory measurements:
  - Density fractionation using sodium polytungstate (SPT) to separate LF and MAOM; OF separated via sequence of centrifugation, sonication, and re-suspension steps.
  - Loss-on-Ignition (LOI) via thermogravimetric analysis (TGA) to quantify hygroscopic water, SOM, and CaCO3 across multiple temperature steps (25–1000°C).
  - Total carbon and nitrogen measured on LF, MAOM, and a subsample of archived soil using an Elementar analyzer (SOP3102, UKAS-accredited).
  - Calculations include correction for hygroscopic water content and correction for calcite-C content in SOC and MAOM-C.
- Quality control:
  - Two internal standards per batch, 10% replicated samples for accuracy and precision.
  - Detailed stepwise corrections and mass balance equations used to derive carbon and nitrogen contents for LF, MAOM, OF, and POM.
  - OF and POM fractions derived from corrected totals; OF-C and OF-N set to zero if negative due to measurement uncertainty.

## Data structure and contents

- Dataset characteristics:
  - 13 columns, 101 rows; NA entries indicate metrics not analysed for that sample.
  - Key fields: Year, SQ_ID; LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg; LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg; SOC_gperg; TN_gperg; SOM_gperg.
  - SOC = total soil carbon corrected for calcite-C; SOM = soil organic matter measured by LOI (SOM_gperg).
- Fractions and calculations:
  - LF-C and MAOM-C derived from fraction masses and carbon concentrations; MAOM-C corrected for inorganic carbon; POM-C and POM-N computed from corrected LF and OF contributions.
  - OF-C and OF-N derived by mass balance (SOC minus LF minus MAOM); if negative due to measurement uncertainty, set to zero before deriving POM-C/N.
- Data lineage:
  - Samples drawn from UKCEH Countryside Survey (2019–2020) with LOI/TGA and density fractionation performed on archived samples; results published and archived (Bentley et al. 2023a, 2023b; method details in Reinsch et al. 2024).

## Data provenance, governance, and availability

- Context: UK-SCAPE program funded by Natural Environment Research Council; rolling five-year sampling cycle aligned with national soil health monitoring.
- Data platform and access:
  - Topsoil physico-chemical properties from UKCEH Countryside Survey (GB, 2018–2019 and 2020) published and archived in NERC EDS Environmental Information Data Centre.
  - Data designed to support national-scale assessments of soil status and dynamics, co-located with vegetation data.
- References for methodology and data:
  - Key methodological sources include Bentely et al. (2023a, 2023b), Reinsch et al. (2024), and foundational SOM fractionation and soil carbon literature (Gärdenäs et al., Golchin et al., Six et al., Sohi et al., etc.).

## Implications for data strategy and Data Leaders

- Data discoverability and usability:
  - Clearly structured, provenance-rich dataset with explicit units, fraction definitions, and correction steps supports reuse and modeling of soil carbon dynamics.
  - Data are part of a rolling, repeatable monitoring framework enabling temporal trend analyses and cross-cycle comparisons.
- Data quality and standards:
  - Adherence to UKAS-accredited SOPs, internal standards, and replication enhances reliability; explicit documentation of corrections (hygroscopic water, calcite-C) improves reproducibility.
- Integration and coordination:
  - Data align with a broader national soil health program (UK-SCAPE) and are co-located with vegetation data, supporting holistic ecosystem assessments.
- Strategic considerations:
  - For data programs, maintain detailed metadata on fractionation methods, corrections, and QC procedures; ensure ongoing calibration of OF via mass balance as cycles evolve.
  - Address potential data gaps (e.g., fractions not analysed in all samples) through clear NA handling and documentation to guide analysis and interpretation.