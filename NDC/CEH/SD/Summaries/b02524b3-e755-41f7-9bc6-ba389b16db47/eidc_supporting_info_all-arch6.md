# Physiological responses of marine phytoplankton to acute and chronic thermal stress.

## Overview
- Describes data supporting the grant Identifying the mechanisms and resource use implications of acclimation to high temperature in marine cyanobacteria (NE/P002374/1) to Richard J. Geider.
- Data comprise physiology-based measurements on four marine phytoplankton: Synechocystis sp. PCC 6803, Synechococcus sp. CCMP 2370, Phaeodactylum tricornutum CCMP 2561, and Emiliana huxleyi CCMP 1516.
- Experimental designs include Ramp (gradual heating), Steady State (acclimated responses at sub-, optimal-, supra-optimal temperatures), and Thermal Performance (responses across temperature and light gradients); omics data are stored in separate depositories.
- Laboratory work conducted 2017–2021 at University of Essex; data collation/quality control completed July 2021.
- This document explains data collection, normalisation, quality control, experimental conditions, methods, and contents of the data files.

## Organisms and culture conditions
- Synechocystis sp. PCC 6803: grown at 30 °C in BG-11 medium with 10 mM TES-KOH (pH 7.5); bubbled with 1% CO2-enriched air; light at ~150 μmol photons m-2 s-1; continuous stirring.
- Synechococcus sp. CCMP 2370: grown in K medium with artificial seawater base, bicarbonate 3 mM; light ~325 μmol photons m-2 s-1; maintained at 26 °C; semi-continuous batch culture setup.
- Phaeodactylum tricornutum CCMP 2561: grown in K medium with silicic acid and 3 mM bicarbonate; light ~325 μmol photons m-2 s-1; 20 °C; semi-continuous culture.
- Emiliana huxleyi CCMP 1516: grown in K medium with artificial seawater base and 3 mM bicarbonate; light ~325 μmol photons m-2 s-1; 20 °C; semi-continuous culture.
- Culturing conditions varied by species to match physiological tolerances and experimental designs.

## Experimental designs

### Ramp experiments
- Objective: characterize transient physiological changes and identify responses to heating rate.
- Synechocystis sp.: gradual heat stress from 30 °C to 46.5 °C at 1.5 °C h-1; sampling hourly across 12 time points; three biological replicates.
- Synechococcus sp.: gradual heating from 27 °C to 32 °C, 1 °C d-1 steps over 6 days; four vessel replicates; sampling during growth to collect physiology and omics data.
- Phaeodactylum tricornutum: heat from 20 °C to 28 °C, sampling hourly for 12 time points; four biological replicates; control at 20 °C.
- General Ramp approach: aligned with species-specific growth rates and tolerances; time-course measurements include transcriptomics, proteomics, metabolomics, and physiology.

### Steady State experiments
- Purpose: characterize acclimated responses to sub-, optimal-, and supra-optimal temperatures for metabolic rates and biochemical composition.
- Species: P. tricornutum, Emiliana huxleyi, and Synechococcus.
- Conditions: steady temperatures corresponding to sub-, opt-, and supra-optimal values (temperature sets per species listed in Table 1); continuous light ~325 ± 25 μmol photons m-2 s-1; cultures inoculated after acclimation and grown to exponential phase before harvesting.
- Measurements focus on photosynthetic and elemental composition (C, N, P) and biochemical composition (protein, carbohydrate, lipid, RNA).

### Thermal Performance experiments
- Design: expose inoculum to a broad temperature gradient (with varying light) to map performance across temperature–light combinations.
- Organisms: Emiliana huxleyi and P. tricornutum.
- Temperature gradients: E. huxleyi (9–27.2 °C) and P. tricornutum (8.6–29.2 °C) with ~1.5 °C intervals; light levels (PPFD) varied to create multiple light treatments.
- For each condition, replicates and extinction events were managed; a culture was considered acclimated after multiple transfers with stable growth, and each growth cycle was treated as an independent biological replicate.

## Measurements and methods

- 4.1 Growth: cell abundances measured by flow cytometry or Chl a fluorescence proxy; specific growth rates derived from ln-transformed abundance or Chl a over time.
- 4.2 POC: particulate organic carbon via filtration, acidification to remove inorganic C, analyzed with Formacs HT; normalization to cells or carbon for C:N and C:P ratios.
- 4.3 PON and POP: total N and P via persulfate digestion and subsequent UV/visible measurements; normalized to cell density or converted to molar ratios.
- 4.4 Chl a: extraction in acetone/DMSO, absorbance-based quantification, normalized to cell density or carbon.
- 4.5 Macromolecular composition: bulk protein, lipids, carbohydrates determined from sequential solvent extraction and colorimetric assays; polysaccharides quantified by anthrone method; data corrected for extraction efficiency and normalized to cell density or carbon.
- 4.6 Fast Repetition Rate fluorometry (FRRf): PSII electron transport kinetics (Fq'/Fm', σ, τ) using FastTracker II (and FastOcean) fluorometers; measurements taken on fresh samples.
- 4.6.1 Fluorescence Light Curves (FLC): light-dependent PSII response using actinic light series; temperature-controlled flow through system.
- 4.7 Oxygen Light Curves (OLC); Membrane Inlet Mass Spectrometry (MIMS): gross and net O2 evolution/uptake across light gradients; 18O2 tracer used; normalization to cells, carbon, Chl a.
- 4.8 PSII Photoinactivation: rate constants of photoinactivation under different PPFDs with and without lincomycin to partition gross vs net inactivation.
- 4.9 Mortality rates: live/dead cell ratios using SYTOX-green staining and flow cytometry.
- 4.10 Flow cytometric characterization: cell size (FSC-A) and pigment content (Chl a, phycoerythrin) by flow cytometry; gating consistent across experiments.

## Data processing, normalization and quality control

- Data collation and quality control completed July 2021.
- Normalization approaches:
  - Cellular metrics normalized to cell density or carbon content (e.g., POC, PON, POP, Chl a per cell, Chl a per carbon).
  - Ratios computed for C:N, C:P, and N:P using molecular conversions.
- Replication and sampling:
  - Ramp experiments: three biological replicates for Synechocystis; four replicates for Synechococcus and P. tricornutum ramp; time-series data across multiple time points.
  - Steady State: four biological replicates per condition per species.
  - Thermal Performance: multiple replicates with extensive matrix of temperature/light conditions; independent biological replicates for each growth cycle.
- Data quality indicators:
  - Consistent gating and instrument settings for flow cytometry.
  - Timepoint alignment to experimental treatments and temperature blocks.
  - Standardized measurement protocols across species and experiments.

## Data files and metadata

- The dataset comprises eighteen (18) CSV files with a consistent column-naming schema described in Table 4.
- Representative file types include:
  - P_tricornutum_mortality_data.csv
  - P_tricornutum_steady_state_data.csv
  - E_huxleyi_steady_state_data.csv
  - Synechococcus_steady_state_data.csv
  - P_tricornutum_photoinhibition_lincomycin_data.csv
  - P_tricornutum_oxygen_evolution_MIMS_data.csv
  - P_tricornutum_FLC_data.csv
  - E_huxleyi_SS_FLC_data.csv
  - Synechococcus_SS_FLC_data.csv
  - Synechocystis_ramp_data.csv
  - Synechocystis_ramp_FLC_data.csv
  - P_tricornutum_ramp_data.csv
  - P_tricornutum_ramp_FLC_data.csv
  - Synechococcus_ramp_data.csv
  - Synechococcus_ramp_FLC_data.csv
  - P_tricornutum_thermal_performance_data.csv
  - E_huxleyi_thermal_performance_data.csv
  - E_huxleyi_TPC_FLC_data.csv
- Columns and units are described in Table 4; common columns include Time (h), Stock Temperature, Biological Replicate, Sample ID, Gradient Temperature, Temperature, Growth/Assay PPFD, Light Level annotation, Lincomycin, Saq (FLC step), Medium, Growth Rate (d-1), Mortality Rate (d-1), Cell mL-1, Median FSC-A, Median FL3-A, Chl a per cell, Chl a per carbon, POC, PON, POP, C:N, C:P, N:P, Carbohydrate cell-1, Lipid cell-1, Protein cell-1, Fv/Fm, and related FRRf-derived metrics.

## Data usability and reuse

- The dataset provides a comprehensive, multi-species, multi-condition view of thermal responses, enabling cross-species comparisons of growth, photosynthesis, elemental composition, and photophysiology under acute and acclimated conditions.
- Data are organised for self-service analysis with standardized metadata and column headings, facilitating integration with omics data in separate repositories.
- The accompanying methodological detail supports reproducibility and quantitative re-analysis of thermal sensitivity and acclimation strategies in marine phytoplankton.