# Physiological responses of marine phytoplankton to acute and chronic thermal stress.

- This dataset supports the research grant "Identifying the mechanisms and resource use implications of acclimation to high temperature in marine cyanobacteria" (NE/P002374/1) led by Richard J. Geider.
- Focus: physiology-based measurements of four marine phytoplankton species under thermal stress to understand acclimation mechanisms, resource use, and responses across time scales.
- Location and timeframe: Laboratory work at the University of Essex, School of Life Sciences (Colchester Campus) between March 2017 and February 2021; data collated and quality controlled by July 2021.
- Data scope: Includes multiple experimental designs (Ramp, Steady State, Thermal Performance) and incorporates omics data in separate depositories.

- Species and strains studied
  - Synechocystis sp. (PCC 6803)
  - Synechococcus sp. (CCMP 2370; WH8102 alias)
  - Phaeodactylum tricornutum (CCMP 2561; CCAP 1055/1)
  - Emiliana huxleyi (CCMP 1516)

- Culturing conditions (key points)
  - Synechocystis: BG-11 medium, TES-KOH buffer, ~30 °C optimum, 150 µmol photons m-2 s-1, 1% CO2-enriched air
  - Synechococcus: K medium with artificial seawater base, 3 mM bicarbonate, ~26 °C, 325 ± 25 µmol photons m-2 s-1
  - P. tricornutum: K medium with silicic acid, ~20 °C, 325 ± 25 µmol photons m-2 s-1
  - E. huxleyi: K medium with silicic acid, ~20 °C, 325 ± 25 µmol photons m-2 s-1
  - All cultures were under continuous light and routinely mixed; vessel volumes ranged from 50 mL to 6 L depending on experiment.

- Experimental designs
  - Ramp experiments
    - Objective: characterize transient physiological changes during gradually increasing (sub-lethal) temperatures.
    - Species-specific ramp protocols with hourly or daily sampling and biological replicates.
    - Measurements span growth, photophysiology, biochemical composition, and omics.
  - Steady State experiments
    - Objective: acclimated, balanced-growth responses to suboptimal, optimal, and supra-optimal temperatures.
    - Temperature triplets per species (sub, opt, supra) with exponential-growth inoculations and 4 replicates.
    - Measurements include photosynthetic electron transfer, O2 evolution/uptake, and biomass composition.
  - Thermal Performance experiments
    - Objective: responses across a temperature gradient combined with varying light levels.
    - Temperature and light gradients applied to inoculated cultures; extensive sampling for physiological responses and photophysiology.
    - Separate experiments for each species conducted about a year apart but using similar designs.

- Measurements and methods (summary)
  - Growth and cell abundance
    - Flow cytometry for live cell counts; chlorophyll a as biomass proxy via fluorometry.
    - Specific growth rates from log-linear fits to time-series data.
  - Particulate Organic Carbon (POC) and Nitrogen/Phosphorus (PON/POP)
    - Filtration, acid digestion, and TOC analysis; POC normalized per cell or per carbon basis; PON/POP via persulfate digestion and UV/visible measurements; data normalized to cell density.
  - Chlorophyll a (Chl a)
    - Acetone/DMSO extraction and spectrophotometric quantification; normalization to cell density or carbon.
  - Macromolecular composition
    - Bulk protein, lipid, carbohydrate analyses via sequential extraction and colorimetric assays; polysaccharides quantified colorimetrically; results normalized to cell density.
  - FRRf and FLC (Photosystem II physiology)
    - FRRf to obtain Fq'/Fm', PSII cross-section (σ), and QA re-oxidation (τ); FLCs with increasing light to parameterize light response of electron transport.
  - Oxygen production/consumption (MIMS)
    - 18O2 technique to derive gross and net O2 evolution/uptake across light levels; data normalized to cell, carbon, or Chl a.
  - PSII photoinactivation
    - Rates determined under multiple PPFDs with and without lincomycin to separate gross vs net photoinactivation.
  - Mortality
    - SYTOX green staining to quantify live/dead cells; used to infer mortality rates in culture tubes.
  - Flow cytometric cell characterization
    - Size proxy (FSC-A) and pigment content (Chl a, phycoerythrin) via flow cytometry.
  - Replication and treatment design
    - Ramp experiments: three biological replicates per condition; each species-level ramp conducted separately.
    - Steady State: 4 biological replicates per temperature condition.
    - Thermal Performance: multiple temperature/light combinations with replicate tubes per combination.

- Data content and structure
  - Dataset comprises eighteen CSV files detailing:
    - Mortality data for Phaeodactylum tricornutum
    - Steady-state physiological measurements for P. tricornutum, E. huxleyi, and Synechococcus
    - Photoinhibition (lincomycin) data for P. tricornutum
    - Oxygen evolution data (MIMS) for P. tricornutum
    - FLC data for P. tricornutum, E. huxleyi, and Synechococcus
    - Ramp experiment datasets for Synechocystis, P. tricornutum, and their associated FLC
    - Thermal performance datasets for P. tricornutum and E. huxleyi
    - Corresponding descriptive columns and units
  - Data file naming reflects species, experiment type, and measurement type (e.g., P_tricornutum_steady_state_data.csv, E_huxleyi_SS_FLC_data.csv, etc.)
  - Data dictionary and column headings
    - Includes Time, Biological Replicate, Sample ID, Temperature (stock and assay), Growth Rate, Mortality Rate, cell counts, POC, PON, POP, Chl a, macromolecular contents, FRRf outputs (Fv/Fm, FLC-derived metrics), O2 rates (O2 evolution/uptake/net), LP/POLNE ratios (C:N, C:P, N:P), and flow cytometry metrics (Median FSC-A, Median FL3-A, etc.)
  - Units and metadata
    - Temperature in °C; PPFD in µmol photons m-2 s-1; Time in hours; growth rates in d-1; concentrations in fg cell-1 or pg cell-1 where appropriate; FRRf and OLC-derived units as specified in the tables.

- Data provenance and accessibility
  - Methods and normalisation procedures are documented (Sections 4.1–4.10) to enable reproducibility and cross-study comparability.
  - Omics datasets are stored in separate repositories, with physio-chemical measurements consolidated in the CSVs described here.
  - References and methodological sources are provided to support measurement techniques (e.g., FRRf, MIMS, pigment and macromolecule assays, etc.).

- Relevance for monitoring framework authors
  - Provides a multi-species, multi-metric baseline of phytoplankton responses to acute and chronic thermal stress, enabling:
    - Benchmarking of thermal sensitivity and acclimation across key phytoplankton groups.
    - Evaluation of data quality, metadata richness, and reproducibility requirements for environmental monitoring datasets.
    - Cross-metric integration (growth, stoichiometry, photophysiology, and mortality) to inform policy-relevant indicators of ecosystem health under warming scenarios.
  - Demonstrates structured experimental design, standardized measurement protocols, and clear data documentation suitable for informing monitoring frameworks and data governance practices.