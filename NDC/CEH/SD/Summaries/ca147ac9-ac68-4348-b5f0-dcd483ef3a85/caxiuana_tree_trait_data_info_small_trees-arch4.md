# Supporting information for Traits data from juvenile trees exposed to a 50% reducing in canopy throughfall at the Caxiuanã drought experiment, Brazil, August to September 2017

## Context and Aim
- Describes trait data from a drought-manipulation experiment (through-fall exclusion, TFE) in eastern Amazonia, with a control plot for comparison.
- Aims to quantify how juvenile tropical forest trees adjust hydraulic and photosynthetic traits under 50% reduction in canopy throughfall.
- Experimental setup includes two 1-ha plots (TFE vs control) with drought structure present since 2002.

## Experimental Design and Sampling
- Location: Caxiuanã, eastern Amazonia (approx. 1°43' S, 51°27' W).
- Plots: 1 ha TFE (through-fall exclusion) and 1 ha control without drought structure.
- Sampling period: September–October 2017 (peak dry season).
- Sampled trees: 76 individuals across the most common genera (43 in control, 33 in TFE); aimed to cover multiple size classes (1 cm to 10 cm DBH).
- Species and plot-level context recorded to enable cross-plot comparisons.

## Traits Measured (17 traits)
- Plot membership (Control or Drought/TFE) and species identification.
- DBH (cm).
- Vcmax (μmol CO2 m^-2 s^-1): maximum carboxylation capacity.
- Jmax (μmol CO2 m^-2 s^-1): maximum electron transport capacity.
- Rleaf (μmol CO2 m^-2 s^-1): leaf dark respiration.
- Min gs (mmol CO2 m^-2 s^-1): minimum stomatal conductance.
- LMA (g m^-2): leaf mass per area.
- Nleaf (g g^-1): leaf nitrogen content.
- Pleaf (g g^-1): leaf phosphorus content.
- Thickness (mm): leaf thickness.
- ρ (g cm^-3): branch wood density.
- Ψpd (MPa): pre-dawn leaf water potential.
- Ψmd (MPa): midday leaf water potential.
- P50 (MPa): xylem pressure at 50% loss of conductivity.
- P88 (MPa): xylem pressure at 88% loss of conductivity.
- Ksmax (mol H2O m^-1 MPa^-1 s^-1 m^-2): maximum lumen conductance.
- PLC (%): percentage loss of conductivity.
- LA:SA: leaf area to sapwood area ratio.

## Sampling Methodology and Measurements
- Branch-based sampling: three branches per tree sampled on three separate time slots during the day.
  - Branch 1 (0430–0630): Ψpd, rehydration, then P50 via pneumatic method.
  - Branch 2 (1000–1200): A–Ci curve (Vcmax, Jmax) and leaf gas exchange (Rleaf, gs), plus dried leaves for Pleaf, Nleaf, LMA.
  - Branch 3 (1300–1400): Ψmd; PLC and Ksmax; LA:SA measured via leaf area and sapwood area.
- Measurement sequence designed to capture hydraulic and photosynthetic traits under near-peak dry-season conditions.

## Data Processing and Quality Control
- Data quality controls included removing values where curve fitting failed or measurements could not be fitted to the expected equations (e.g., P50, P88, Ksmax, PLC, Vcmax, Jmax).
- Such removed values are labeled as NA in the data.
- Remaining data were checked to ensure values fall within ranges reported in related studies.
- NA also used for missing data due to damaged samples or inability to collect certain measurements.

## Metadata and Documentation
- Detailed methodology for trait collection is documented in:
  - Bartholomew et al. 2020 (plant hydraulics and trait methods).
  - Giles et al. 2022 (understorey vs canopy tree hydraulic trait responses).
  - Pereira et al. 2016; Pereira & Mazzafera 2012; Schneider et al. 2012 (methods and instrumentation references).
- The document serves as supporting information for the dataset and points to primary methodological sources for variable-specific procedures.

## Data Availability and Structure (Implied)
- Data are provided as trait measurements associated with individual trees on two plots, with per-trait values and units as listed.
- Where measurements could not be obtained or curves could not be fitted, values are NA.
- Table 1 (accompanying description) enumerates all traits, their descriptions, and units to aid discoverability and reuse.

## Implications for Data Leaders
- Demonstrates end-to-end data governance: clear experimental design, per-tree sampling, multi-trait measurement, and explicit QC rules.
- Emphasizes the importance of detailed metadata (plot, species, DBH, trait definitions, units) to enable cross-study integration and reuse in mixed-data environments.
- Highlights common data access challenges in ecological data (fragmented sources, measurement-specific QC, NA handling).
- Illustrates how to document measurement protocols and reference foundational methodological sources to support data discoverability and trust.
- Provides a concrete example of preparing a multi-trait dataset from a manipulated environmental experiment, useful for planning data products that support user needs and future analyses.