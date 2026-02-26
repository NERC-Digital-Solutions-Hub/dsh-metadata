# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

- Purpose: Present barium concentration and stable isotope (δ138Ba) measurements from controlled laboratory batch experiments and Himalayan river samples to understand adsorption-desorption fractionation and validate lab results with field data.

## Overview of Methods and Scope

- Analyzed barium concentrations by ICP-OES (Agilent 5100) and isotope abundances by TIMS (Thermo Fisher Triton Plus) using a double-spike approach to correct mass-dependent fractionation.
- Isotope ratios (δ138/134Ba) referenced to NIST 3104a.
- All analyses conducted in clean lab facilities at University of Cambridge.
- Field samples collected from the Saptakoshi and Sunkoshi rivers in Nepal as part of the PRESSurE project; field work complemented by a complimentary dataset.

## Laboratory Experiments

- Riverine Series: designed to quantify Ba isotope fractionation during adsorption-desorption with common environmental minerals and river/groundwater waters.
  - Partitioning Subseries: varying adsorbent concentration at fixed reaction duration (2000 min) to balance dissolved and adsorbed Ba masses for isotope measurements.
  - Kinetic Subseries: fixed adsorbent concentrations, varying reaction duration from minutes to about a month to assess time dependence of fractionation.
- Estuarine Series: quantify desorption of Ba from river-derived suspended sediment into seawater; clay minerals equilibrated with river-mature water analogue then exposed to seawater, with half experiments re-equilibrated with river water.
- Post-Reaction Processes: after separation, adsorbed Ba displaced from mineral surfaces for analysis; both dissolved and adsorbed phases measured for Ba concentrations and isotopic compositions.

## Himalayan River Sediment and Water Samples

- Sample set: 12 river-water samples from Sunkoshi and Saptakoshi rivers, collected over multiple seasons under PRESSurE project.
- Sampling approach: daily sampling at selected stations during pre-monsoon and monsoon; twice weekly during post-monsoon and dry season; integrated water-column samples (first meter) collected as 6 x 500 mL sub-samples per location.
- Processing: in-field separation of sediment and water via 0.22 µm filtration; sediment washed, oven-dried at 40°C, and weighed; adsorbed cations displaced from sediment using NH4Cl or CoHex, with subsequent filtration and handling to maximize desorption.
- Concentrations and isotopes of Ba measured using the same methods as laboratory samples (ICP-OES for Ba, TIMS for isotopes).

## Analytical Methods

- Displacement of pre-existing adsorbed Ba: repeated NH4Cl leaching to desorb exchangeable Ba, followed by washing.
- Mineral-Water Reactions: controlled mixing of waters with mineral adsorbents; mixing conditions adjusted (shaking, ultrasonication) based on duration; separation by centrifugation and filtration.
- Extraction of Adsorbed Phase: displacement of Ba from adsorbent after water-adsorbent separation; samples stored at 5°C prior to analysis.
- Determination of Element Concentrations: Ba quantified by ICP-OES with matrix-matched calibration; TIMS used for isotope measurements with double-spike correction; standard references for accuracy and precision.
- Barium Isotope Measurements: multi-step sample processing including acid digestion, co-precipitation (for seawater), ion-exchange chromatography, re-dissolution, oxidation, and TIMS loading on Re filaments; procedural blanks and long-term standards used to ensure accuracy (uncertainties: ~0.03 ‰ for isotopic measurements).

## Data Structure and Accessibility

- Two CSV data files included:
  - BaIsoExperimentData.csv: laboratory experiment data with fields for experiment ID, series/subseries, water type, adsorbent details, masses, reaction duration, pretreatment, Ba concentrations (dissolved and adsorbed), and d138Ba for both phases.
  - BaIsoNepalRivers.csv: field data for river samples with date, river, sampling location, suspended sediment concentration, discharge, Ba concentrations (dissolved and adsorbed), and d138Ba for both phases.
- Data fields and units are documented (e.g., Ba concentrations in µmol/L, d138Ba in ‰; masses in g or mg as specified).
- Field samples labelled with NA for inapplicable fields and NM where measured data is unavailable.
- Reference datasets and related studies cited for methodology and context (Foster et al. 2004; Hsieh & Henderson 2017; Knight et al. 2024; Rudge et al. 2009).

## Data Quality, Uncertainty, and Documentation

- Uncertainties:
  - ICP-OES Ba concentration: ~7% (2σ).
  - TIMS Ba concentration: ~2% (2σ).
  - Isotopic measurements: minimum ~0.03 ‰ (2σ) using long-term standards.
- Procedural blanks for TIMS processing are low (0.07 ± 0.06 ng, µ ± 2σ, n=6), contributing less than 1% of processed sample mass.
- Analyses performed with careful sample handling to minimize NH4Cl interference and matrix effects; cross-checks with standard reference materials (NIST 3104a, NBS 127) over multiple years.

## References and Related Resources

- Foundational methodological references for Ba isotopes and analyses, including double spike TIMS approaches and Ba proxies in geochemical systems.
- Related dataset: PRESSurE River Chemistry Time Series (Nepal) dataset (Knight et al., 2024).
- Methodological resources for Ba isotope analysis and dispersion corrections (e.g., Hsieh & Henderson, 2017; Rudge et al., 2009).

Note: The document provides comprehensive procedural detail to enable replication and reuse of both laboratory and field Ba isotope data, with explicit data structures to facilitate data integration and analysis.