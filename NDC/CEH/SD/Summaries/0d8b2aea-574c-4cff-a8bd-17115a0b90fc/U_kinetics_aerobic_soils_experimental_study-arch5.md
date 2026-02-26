# Supporting documentation

- Overview of the dataset
  - Measurements of soluble, chemically exchangeable, and isotopically exchangeable UO2^2+ concentrations in soils.
  - Laboratory-incubated microcosms: 20 soils from central England, contaminated with UO2^2+, incubated in the dark at 10 ± 1°C for 619 days.
  - Data collected to quantify kinetics of U(VI) transformations and assess binding strength, aiding models of long-term U(VI) mobility and availability in aerobic soils under temperate conditions.

- Background and Objectives
  - Uranium in soils is relevant for environmental risk assessment post-nuclear fuel use and waste disposal.
  - The study addresses long-term bioavailability of U(VI) in aerobic soils, which is difficult to predict from simple extractions.
  - Outcomes support understanding of U(VI) transformations and soil–water interactions over extended periods.

- Soil sampling and characterisation
  - Twenty topsoil samples (0–15 cm) collected from multiple central England sites; four sub-samples per site combined to ~3 kg composite samples.
  - pH measured with 0.01 M CaCl2 (soil:solution ratio 2.5 L/kg; 30 minutes agitation).
  - Organic carbon determined with a CNS analyzer.
  - Sites include arable, moorland, and woodland with varied pH and organic carbon contents (data provided in Table 1).

- U addition and soil incubation setup
  - Contaminated with 5000 μg U(VI) per kg dry soil using UO2^2+ solution.
  - ~1.5 kg soil per microcosm distributed across three bottles per soil; bottles allow gas exchange but limit water loss.
  - Incubated in darkness at 10.0 ± 1.0°C for 619 days (Nov 2014–Aug 2016).

- Microcosm sampling and uranium fractionation
  - At sampling times, ~4 g soil equilibrated with 20 mL 0.01 M KNO3 for soluble U assessment (μg U kg^-1 DW).
  - For chemical exchangeability, ~2 g soil equilibrated with 20 mL 1 M Mg(NO3)2 containing 6 μg 233UO2^2+ and 6 μg 236UO2^2+ per kg soil; equilibrated 36 h.
  - Isotopically exchangeable (labile) U determined via isotopic exchange using Mg(NO3)2 extracts and tracers, followed by isotopic analysis.
  - Extractions performed, with data reported as μg U kg^-1 DW for each fraction.

- Analyses and calculations
  - Inductively coupled plasma mass spectrometry (ICP-MS) used to measure U in extracts.
  - Internal standard: Ir; instrument setup includes rapid uptake module and specific dwell times for total and isotopic measurements.
  - Isotopic exchangeability (U_E) calculated from 238U in soil suspensions, extractant volumes, soil mass, and an adsorption-related distribution coefficient (K_d^i), following defined equations.
  - For isotopic analysis, monitoring 233U, 236U, and 238U with spike-corrected mass discrimination; data are reported as μg U kg^-1 DW for soluble, exchangeable, and labile fractions.

- Data structure and completeness
  - Table 1 (soil properties): site location, land use, latitude/longitude, organic C (%), and pH.
  - Table 2 (extractions): definitions of each fraction (soluble, exchangeable, labile) and associated extraction conditions.
  - Data are reported for multiple incubation days; some data entries are missing (denoted by '-') in the dataset.

- Relevance and potential uses
  - Enables kinetic modeling of U(VI) transformations and estimation of U binding strength in aerobic soils under temperate conditions.
  - Supports assessments of long-term U mobility and plant bioavailability in soil systems.
  - Useful for cross-site comparisons and for validating soil chemistry/biogeochemistry models with isotope-tracer data.

- Data quality and provenance notes
  - Detailed protocol for sampling, extraction, isotopic tracers, and ICP-MS analysis supports traceability and reproducibility.
  - Internal standards, spikes, and calibration approaches described to correct mass discrimination and ensure data accuracy.
  - Explicit units (μg U kg^-1 DW) and clear fraction definitions aid interpretation and integration with other datasets.

- Data stewardship considerations (for Data Stewards)
  - Metadata to capture: soil_id, site name, land use, coordinates, pH, organic carbon, incubation_day, fraction type, extractant, concentration, units, method, instrument, calibration, QC results, and uncertainties.
  - Data dictionary alignment: standardize variable names for each fraction (soluble, exch_U, labile_U) and for U_E calculations with clear formulas.
  - Provenance: link fractions to specific sampling times and microcosms; maintain traceability from initial contamination to final measurements.
  - Data sharing and reuse: provide access to raw extract data and derived metrics (U_E, K_d) with full methodological context; include Table 1 and Table 2 definitions.
  - Data quality checks: note missing values and reasons; include QA/QC procedures and detection limits where available.
  - Storage and format: store in machine-readable, well-annotated formats (CSV/ISA-Tab or equivalent) with a machine-readable data dictionary and codebook.
  - Compliance with governance: ensure data licensing, usage restrictions (if any), and proper attribution for datasets used in modeling or comparative studies.

- Endnote
  - The study provides a rich, well-documented dataset linking soil properties, controlled U contamination, fractionation methods, and isotopic analyses to elucidate U(VI) behavior in soils over extended incubation.