# Overview

- Purpose and scope
  - A dataset from a continuous trial of a decentralised low-maintenance drinking water treatment system (DWTS) in the UK, conducted Nov 2019–Feb 2020.
  - Focus on the NINJA drinking water treatment platform (NINJA-DWTP) integrating PAqua 1000D-2 with ECAS biocidal dosing and ultrafiltration, to provide biologically safe drinking water.
  - Part of a UK-India Water Quality project aimed at sensing, monitoring and improving water quality in India.
  - Demonstrates long-term continuous operation of the modular off-grid DWTP and provides baseline data for system performance and water quality.

- Data components and structure
  - Four CSV files included:
    - 1_DWTS_operational-parameters.csv: 11 columns; 5-minute operational telemetry from Grundfos Remote Management (e.g., Date_Time, Flow_min/Flow_max/Flow_average, TMP_average, ORP_min/Max/average, FCl_min/Max/Average).
    - 2_DWTS_RawWater_data-summary.csv: 85 columns; raw water sample results from three locations (RW, HT, PW); includes microbiological (coliforms, E. coli, C. perfringens, Enterococci, counts), pH, colour, turbidity, EC, hardness, alkalinity, TOC, SO4, PO4, Cl, Si, NH4, NO2, NO3, F, CN, FOG, metals, pesticides/PAHs, and more; DWI limits and methods documented.
    - 3_DWTS_HeaderTank_data-summary.csv: 77 columns; similar parameter set for header tank samples.
    - 4_DWTS_Potable_data-summary.csv: 85 columns; potable water samples.
  - Detailed parameter mapping, units, limits, and standard methods are provided (e.g., methods like 3303 for microbiology, 3406 for pH, 3404 for turbidity, 2550 series for various chemistries).

- Sampling regime and context
  - Raw water sourced from a modified artificial water body near UWE, Bristol.
  - Field trial duration: 11 weeks, with weekly sampling (two weeks lost to university closure).
  - Three sampling locations per trial: raw water (RW), header tank (HT) after pre-filtration, and potable water (PW) from the pipeline to the potable storage tank.
  - Samples analysed by Wessex Water Scientific Centre (UKAS-accredited) following ISO 17025 standards; microbiological analyses conducted within 24 hours of collection.
  - Key regulatory parameters aligned with Drinking Water Inspectorate (DWI) 2010 standards; multiple chemical and biological indicators included, with specified DWI limits.

- System description and telemetry
  - DWTP configuration includes PAqua WPU, pre-dosing with PAqualtye, 50 µm pre-filter, 0.02 µm UF membranes, backwashing, and inline free chlorine/ORP monitoring.
  - Ancillary pretreatment to improve influent quality: two series settlement tanks and Turbidex 5 µm prefilters.
  - Telemetry via Grundfos Remote Management (pump and TMP monitoring) and inline sensors (s::can) for remote diagnostics.

- Data quality and completeness
  - Data completeness varies by file; file 1 (operational parameters) contains essential telemetry, while some LAB-derived parameters may be incomplete or missing for certain samples (NA values noted).
  - Some parameters are measured less frequently (e.g., extended metals, hydrocarbons) or only for subsets of samples.
  - Data documentation includes explicit sampling plans and parameter lists (Tables and Appendix references) to support interpretability and reuse.

- Governance and reuse considerations for Data Stewards
  - Rich metadata: clear file naming, column headings, parameter definitions, units, measurement methods, and regulatory limits (DWI) documented.
  - Provenance: UKAS laboratory analyses, standardized methods, and regulatory baselines; traceability to sampling events and telemetry.
  - Discoverability and interoperability: four structured CSV files with consistent parameter mappings across(raw, header tank, potable) data; suitable for linking operational telemetry with water quality outcomes.
  - Usage notes: suitable for evaluating treatment performance, disinfection efficacy, compliance with drinking water standards, and cross-linking with system operational data for governance and auditing.

- Challenges and considerations from a Data Steward perspective
  - Aligning diverse data sources (telemetry vs. lab analyses) and varying sampling regimes across locations.
  - Ensuring metadata completeness for long-term discoverability, especially regarding method codes, DWI limits, and unit conventions.
  - Managing incomplete data and documenting gaps to preserve dataset usability.

- References
  - Clayton, G.E., Thorn, R.M.S., Reynolds, D.M., 2019. Development of a novel off-grid drinking water production system integrating electrochemically activated solutions and ultrafiltration membranes. J. Water Process Eng.
  - Drinking Water Inspectorate, 2010. The Water Supply (Water Quality) Regulations 2010.