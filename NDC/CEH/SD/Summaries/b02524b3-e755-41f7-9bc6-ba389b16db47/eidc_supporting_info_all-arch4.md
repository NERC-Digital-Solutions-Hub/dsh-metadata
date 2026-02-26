# Physiological responses of marine phytoplankton to acute and chronic thermal stress

## Overview
- Data support the grant Identifying the mechanisms and resource use implications of acclimation to high temperature in marine cyanobacteria (NE/P002374/1) to Richard J. Geider.
- Four taxa studied: Synechocystis sp. PCC 6803; Synechococcus sp. CCMP 2370; Phaeodactylum tricornutum CCMP 2561; Emiliana huxleyi CCMP 1516.
- Experimental designs include: Ramp (gradual heating), Steady State (acclimated to sub/optimal/supra temperatures), and Thermal Performance (response across thermal gradients with varying light).
- Omics data collected but stored in separate depositories; laboratory work conducted 2017–2021; data collation/quality control completed July 2021.
- Data description plus methods detail collection, normalization, and quality control; datasets comprise 18 CSV files describing various physiological measurements.

## Data scope and contents
- Physiological measurements include:
  - Growth and cell abundances (via flow cytometry or chlorophyll a proxy) and calculated specific growth rates.
  - Particulate organic carbon/nitrogen/phosphorus (POC, PON, POP) and C:N, C:P, N:P molar ratios.
  - Chlorophyll a concentrations and macromolecular composition (protein, carbohydrate, lipid); polysaccharides; lipid quantification.
  - FRRf-based measurements of photosystem II electron transport (Fq'/Fm', sigma, tau); fluorescence light curves (FLC).
  - Oxygen evolution/consumption via membrane inlet mass spectrometry (MIMS) with 18O2; oxygen light curves (OLC) across light gradients.
  - PSII photoinactivation rates (with and without lincomycin) and associated rate constants.
  - Mortality rates via SYTOX green staining and flow cytometry.
  - Flow cytometric cell-characterization (size proxies via FSC-A; pigment content via chlorophyll a and phycoerythrin channels).
- Data normalization and units are specified (e.g., per cell, per mL, fg cell-1 for Chl a, mg/L, etc.), with several metrics converted to molar or carbon-based scales as appropriate.

## Experimental design details by species
- Culturing conditions (temperatures, media, light) are specified for each species:
  - Synechocystis sp. PCC 6803: optimal 30°C in BG-11 with 1% CO2; 150 µmol photons m-2 s-1 light.
  - Synechococcus sp. CCMP 2370: 26°C in K medium with artificial seawater base; 325±25 µmol photons m-2 s-1 light.
  - Phaeodactylum tricornutum CCMP 2561: 20°C in K medium with silicic acid; 325±25 µmol photons m-2 s-1 light.
  - Emiliana huxleyi CCMP 1516: 20°C in K medium with silicic acid; 325±25 µmol photons m-2 s-1 light.
- Ramp experiments:
  - Species-specific heating regimes (e.g., 1.5 °C h-1 for Synechocystis; 1 °C d-1 for Synechococcus; rapid step to 28–46.5 °C depending on species).
  - Hourly sampling across a time-series with three biological replicates per condition.
- Steady State experiments:
  - Temperature sets at suboptimal, optimal, and supra-optimal values per species (Table 1 defines exact temps).
  - After >10 generations of acclimation, four replicates per condition; exponential-growth cultures sampled for physiological and omics measurements.
- Thermal Performance experiments:
  - Temperature and light gradient matrices (multiple temperatures with varying light intensities) conducted in separate runs (approx. one year apart) for each species.
  - Large matrix: e.g., dozens of light-temperature combinations; multiple biological replicates; extensive measurements (growth, FRRf, OLC, FLC, etc.).

## Data structure and access
- Dataset comprises 18 CSV files, each with descriptive file names (e.g., P_tricornutum_mortality_data.csv, P_tricornutum_steady_state_data.csv, E_huxleyi_SS_FLC_data.csv, Synechococcus_SS_FLC_data.csv, ramp and thermal_performance data files, etc.).
- Column headings standardized across files with metadata fields such as:
  - Time (h), Biological Replicate, Sample ID, Stock Temperature, Gradient Temperature, Temperature, Growth/Assay PPFD, Light Level, Lincomycin ( Plus/Minus ), and numerous measured variables (rates, concentrations, Fv/Fm, etc.).
- Derived metrics included:
  - Growth Rate (d-1), Mortality Rate (d-1), POC, PON, POP, C:N, C:P, N:P, Chl a per cell or per carbon, MACROs (protein, lipid, carbohydrate per cell), FRRf-derived parameters, O2 evolution/uptake (per cell, per carbon, per Chl a).
- Replication and time-series:
  - Each ramp/steady-state/thermal-perf experiment includes multiple biological replicates; time-series data capture dynamic responses to temperature shifts.
- Data quality and provenance:
  - Normalization procedures described; gating strategies for flow cytometry; instrument-specific settings noted; omics data stored separately, requiring cross-referencing for integrative analyses.
- Documentation and schemas:
  - Column definitions and units described in Table 4 (data dictionaries) and Table 3 (file descriptions); consistent nomenclature across datasets.

## Data quality, provenance, and governance
- Data produced under controlled laboratory conditions with detailed culturing and measurement protocols; final quality control completed July 2021.
- Omics datasets are stored separately from the main physiological dataset.
- Primary publication/documentation provides extensive methods, references, and data dictionaries to facilitate reuse, validation, and cross-study comparisons.

## Potential uses for data leaders
- Cross-species comparisons of thermal acclimation mechanisms and resource-use strategies under acute and chronic heat stress.
- Integration of physiological metrics (growth, photosynthesis, macromolecular composition) with pigment and nutrient dynamics to model phytoplankton responses to warming.
- Support for climate-change biology studies, including predictions of community- and ecosystem-level responses to temperature increases.
- Baseline data for meta-analyses and for benchmarking data-management practices in laboratory-generated environmental datasets.