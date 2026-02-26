# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

- This dataset, collected by the UK Centre for Ecology & Hydrology (UKCEH) in 2018 under a BBSRC-funded project, aims to evidence how pasture-fed livestock practices affect grassland parameters, including sward composition and soil quality.
- Scope: 56 farms across Britain (Pasture Fed Livestock Association members; certification status varies), sampled May–September 2018.
- Data types: vegetation surveys, soil analyses, and field-management data from a single 200 m2 plot per field, designed for comparability with the Countryside Survey (CS) methods.

## Experimental Design and Data Collection

- Farms recruited via the Pasture Fed Livestock Association (PFLA); certification status among farms ranged from fully certified to members only.
- Field work involved on-site visits by surveyors and the use of CS-like vegetation and soil sampling protocols for cross-study comparability.
- Plot sampling:
  - Large 200 m2 plot per field; pre-visit location mapping validated on-site when possible.
  - Vegetation: species presence, cover (nested plots), and vegetation height categories; data captured with electronic devices.
  - Soils: one 15 cm depth soil core per plot for a suite of analyses.
  - Field management: on-site farmer-provided data via a bespoke questionnaire (grazing, inputs, sward longevity, etc.).

## Data Structure and Key Variables

- Four CSV data sheets (anonymised farm sites):
  - SEEGSLIP_PLOTS_2018.csv: top-level plot attributes (site code, plot type, survey dates, habitat classifications, presence of trees/shade, slope/aspect, soil sampling indicators, OS grid reference).
  - SEEGSLIP_SPECIES_2018.csv: vegetation species data per plot (species name, cover by nest, total cover, nest level, etc.).
  - SEEGSLIP_SOIL_2018.csv: soil properties per plot (dry content, conductivity, total carbon and nitrogen, LOI, total phosphorus, Olsen P, pH in water and CaCl2, bulk density, particle-size fractions, aggregate stability, CaCO3).
  - SEEGSLIP_FIELD_MGT.csv: field management and farm practices (PFLA membership/certification duration, pasture type, grazing patterns, fertiliser usage, organic and lime inputs, herbicide use, stocking density, cuts and timing, etc.).
- Anonymisation: farms assigned numeric/site codes to protect landowner confidentiality.
- Units and methods reflect Countryside Survey standards where applicable to enable cross-study comparisons.
- References to established protocols and calibration standards are included (e.g., CS soil manuals, LOI method, particle-size analysis standards).

## Data Quality, Standardisation, and Provenance

- Quality control for soil analyses:
  - Loss-on-ignition (LOI) with QC using internal standards; LOI data used to derive soil carbon concentration with a validated formula.
  - SOC and N measured via UKAS-accredited SOP3102 using an elemental analyzer; in-house reference materials included in each batch.
  - Phosphorus measurements (TOT_P and Olsen P) with duplicate samples and matrix blanks for QC.
  - pH (water and CaCl2), EC, and bulk density with internal standards for QC and batch-repeats when standards deviate.
  - PSD determined by laser diffraction with cross-checks against sieve data and standard soils; high organic matter can affect LD results.
  - Aggregate stability assessed with wet sieving and NaOH treatment; results expressed as a percentage.
  - CaCO3 content determined by thermogravimetric analysis.
- Vegetation data quality: species identification aligned with established taxonomies; nested plot covers and percent cover recorded to facilitate aggregation to plot level.
- Data integrity: multiple QC steps and cross-referencing with Countryside Survey methods to ensure comparability and reliability.

## Data Access, Metadata, and Provenance

- Data provided as four CSV sheets with detailed field descriptions and data dictionaries embedded in the dataset structure.
- Farm-level data are anonymised; site codes and plot IDs enable traceability within the anonymised framework.
- The methodology links to published CS and related soil/vegetation measurement protocols, supporting reproducibility and integration with other UK grassland datasets.

## Governance, Stewardship, and Compliance for Data Stewards

- Governance fit:
  - Data governance aligned with large dataset practices: clear data schema, standardised variables, and documented measurement methods.
  - Anonymisation ensures confidentiality while preserving useful linkage via site codes.
  - Cross-compatibility emphasis with the Countryside Survey enables broader reuse and comparative analyses.
- Stewardship considerations:
  - Maintain and update metadata to reflect any re-analyses or re-processing of soil/vegetation data.
  - Monitor for updates or corrections to measurement protocols or reference standards.
  - Plan for long-term storage and accessibility, including version control and data lineage documentation.
- Sharing and reuse:
  - Data are suitable for analyses of pasture management effects on soil carbon, nutrient status, soil physical properties, and vegetation structure/diversity.
  - Enables assessments of certification-related practices (PFLA) on grassland health and soil health indicators.
  - Potential to integrate with models of carbon storage, soil fertility, and biodiversity in managed grasslands.

## Practical Uses and Integration

- Benchmarking pasture-fed systems against Countryside Survey baselines for soil and vegetation parameters.
- Investigating relationships between management practices (grazing, fertiliser types/timing, lime, organic amendments) and soil properties (SOC, N, P, pH, bulk density, moisture, microbial habitats).
- Supporting certification programs (PFLA) with quantitative evidence on soil quality and sward characteristics.
- Contributing to data harmonisation efforts for UK grassland datasets and informing land-management policy and advisory services.

## Challenges and Considerations for Data Stewards

- Incomplete or evolving user needs beyond standard CS-type analyses; ensure clear documentation of variables and potential caveats.
- Timeliness and completeness of data submission from farmers/mappers; maintain processes to chase missing information while preserving data integrity.
- Interoperability across diverse data collection systems and field formats; continue to document data standards and provide guidance tooling.
- Managing large, high-resolution soil datasets and maintaining long-term accessibility and compatibility with future analytical methods.