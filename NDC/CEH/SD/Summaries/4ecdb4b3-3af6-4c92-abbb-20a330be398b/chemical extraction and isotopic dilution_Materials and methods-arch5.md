# Isotopic dilution assay

- Scope and context
  - Describes a study of four UK soils with contrasting metal contamination histories: Kegworth, Chat Moss, Clough Wood, and a sewage processing farm.
  - Aims to quantify metal concentrations (Ni, Cu, Zn, Cd, Pb) via chemical extractions and isotopic dilution to determine isotopically exchangeable metal fractions.

- Data types and site metadata
  - Site locations and coordinates for each soil sample.
  - Soil properties: pH measured in soil-water suspensions; organic matter content estimated by loss on ignition (550°C, 7 h).
  - Sampling depth: 0–20 cm.
  - Sample identifiers, replication status, and NA (not applicable) indicators for missing results.

- Chemical extraction protocol (data provenance and methods)
  - Extractants used to obtain metal fractions: 0.43 M HNO3, 0.43 M CH3COOH, 1 M CaCl2, and 0.05 M Na2H2EDTA (MExt mg/kg reported per extractant).
  - Procedure: three replicates per soil per extractant, suspensions centrifuged, supernatants filtered (<0.22 µm), CaCl2 extracts acidified to 2% HNO3.
  - Total soil metal concentration (MTotal) determined by aggressive digestion (HNO3, HClO4, HF) after agate ball milling.

- Isotopic dilution assay design (data collection and spike management)
  - Enriched stable isotopes used: 62Ni, 65Cu, 70Zn, 108Cd, 204Pb with certified abundances.
  - Custom mixed-isotope spikes created for each soil-extractant combination; spike volumes chosen to raise spike isotope abundance by ~20%.
  - Experimental setup: multiple replicates (six) with and without spikes; two sets of suspensions prepared per metal/extractant type.
  - Spiking protocol: three replicates spiked, followed by extended shaking; post-spike processing includes filtration and preparation for ICP-MS.

- Instrumentation and measurement (data acquisition)
  - Multi-element analysis by quadrupole ICP-MS (X-Series II) with collision cell technology and kinetic energy discrimination (CCT-KED) to reduce interferences.
  - Internal standards used: Sc, Ge, Rh, Ir to correct sensitivity drift.
  - External calibration with multi-element standards.
  - Isotope ratios measured: 62Ni/60Ni, 65Cu/63Cu, 70Zn/66Zn, 108Cd/111Cd, 204Pb/208Pb (and Pb isotopes for mass discrimination checks).
  - Interference management: chlorine interference mitigated using CCT-KED; 204Hg/204Pb isobaric interference corrected via 202Hg measurement; dilution to ensure detector operation in pulse-counting mode when needed.
  - Mass discrimination corrections applied using standards; calibration checks every ~20 samples.

- Data processing and calculation (E value concepts)
  - Calculation targets: isotopically exchangeable metal concentrations in soil suspensions (E Value) and in extracts (E Ext).
  - Based on measured spike and reference isotope abundances from three solutions: spike, spiked soil-solution, and unspiked soil-solution.
  - Key variables include soil mass (W), spike concentration and volume, atomic masses, and measured isotope abundances.
  - Output values include exchangeable metal fractions (E Value and E Ext) expressed in mg/kg.
  - Note: The document provides a formula for E Value / E Ext (Equation 1), with the understanding that some text appears garbled; the approach relies on isotope ratio data to quantify exchangeable metal pools.

- Data quality, flags, and interpretation
  - NA markers indicate non-applicable results for certain metals/extractants or replicates.
  - Replication and spike-solution design enable QA of isotopic measurements and correction for instrumental drift and mass discrimination.
  - Interference corrections and instrumental settings are documented to support reproducibility and cross-lab comparability.

- Data governance and stewardship considerations (implications for data stewards)
  - Rich multi-method dataset requiring detailed metadata: site provenance, soil properties, extraction conditions, isotope spike details, and ICP-MS settings.
  - Critical to capture data lineage: sample handling, replicate structure, spike volumes, timepoints, and all QA steps.
  - Standardization needs: consistent units (mg/kg), clear annotation of extractants, and explicit reporting of non-detects or NA values.
  - Data sharing and interoperability: ensure metadata schemas cover isotopic dilution parameters, calibration curves, MD corrections, interferences corrections, and instrument mode (CCT-KED).
  - Documentation should include calculation methodology for E values, including formulas or code to reproduce E Value and E Ext from isotope data.
  - Potential challenges for governance: integration of inorganic geochemical data across multiple extractants and metals; ensuring consistent data formats and interpretation rules for exchangeable metal pools across datasets.

- End result and usefulness
  - Produces quantitative measures of total and extractable metal pools in soils, with isotopic dilution providing insight into exchangeable metal fractions.
  - Data suitable for meta-analyses of soil contamination, metal mobility, and risk assessment, provided thorough metadata and transparent processing documentation accompany the dataset.