# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

- Purpose and scope
  - Describes bulk elemental and stable isotope composition of organic matter from terrestrial, intertidal, and marine environments across the UK (2016–2021).
  - Aims to constrain organic carbon sources (terrestrial vs marine) using isotope data in conjunction with isotope mixing models.
  - Sample set includes 491 samples from soils, peat, living/dead biomass, saltmarsh, seagrass, mudflat, macroalgae, zooplankton, finfish aquaculture waste, and analytical standards.

- Dataset content and variables
  - Observed variables: δ13C_org (‰), δ15N (‰), OC content (%), N content (%), C/N ratio, N/C ratio.
  - Sample classes and contexts span terrestrial, intertidal, and marine environments.
  - Geographic and location annotations cover multiple coastal catchments around the UK; coordinates provided to delineate observation extent.
  - File formats: .csv for the primary data resource; metadata descriptions for other related datasets.

- Sampling, preparation, and analysis
  - Samples collected across varied UK environments to maximize organic matter diversity.
  - Storage and pre-analysis handling: samples stored at -20°C; oven-dried at 40°C for 72 hours; milled to a fine powder.
  - Stable isotope analysis: ~12 mg processed sediment in tin capsules for C and N; an additional 12 mg in silver capsules for carbonate removal via acid fumigation; analysis performed with EA-IRMS.
  - Calibration and quality control: isotopic values quality-checked through repeat analysis of standard reference material (B2151) with known C and N values; lab practices aligned with University of St Andrews standards.
  - Data quality notes: explicit QA procedures described for isotopic analyses; some fields indicate NA (not available) where data are not applicable or not reported.

- Location and geography
  - Geographic extent: United Kingdom; specific coordinate pairs indicate a defined observation boundary.
  - Nations represented: Scotland, England, Wales.
  - Location descriptions emphasize sampling from coastal catchments to capture wide diversity of organic matter.

- Data governance and metadata considerations for data stewards
  - Metadata clarity: explicit description of sampling, preparation, instrumentation, calibration, and QC procedures.
  - Data format and units: isotopes reported in per mil (‰); OC/N percentages and ratios clearly labeled; consistent with standard geochemical reporting.
  - Provenance and reproducibility: documented analytical workflow and reference standards (e.g., B2151) support traceability.
  - Documentation of dataset scope and limitations: NA entries indicate where data were not collected or not reported; users should interpret missing values appropriately.
  - Related dataset: Aboveground_Biomass_Carbon_UK.csv provides a structured taxonomy of sample_id and sample_class across a broad set of terrestrial, aquatic, and coastal biota, with consistent textual field formats.

- File structure and key metadata fields
  - UK_geochemistry_of_OM_sources.csv: main variables include delta_13Corg_per_mil, delta_15N_per_mil, OC_perc, N_perc, CN, NC, with geographic and sampling context details.
  - Aboveground_Biomass_Carbon_UK.csv: metadata sections list sample_id and sample_class for a wide range of vegetation and aquatic samples; detailed sample descriptions are provided to support classification.

- References and methodological notes
  - Harris, D., Horwáth, W.R. and Van Kessel, C. (2001): Acid fumigation method to remove carbonates prior to total OC or C-13 analysis.
  - Rodwell, J.S. (2000): National vegetation classification framework referenced for sample context.

- Practical considerations for reuse
  - Enables isotope-informed source apportionment of UK organic matter across multiple ecosystems.
  - Suitable for integration with isotope mixing models and cross-dataset comparisons within geochemistry and environmental science projects.
  - Users should account for NA fields and ensure alignment of units and metadata with their own data standards.