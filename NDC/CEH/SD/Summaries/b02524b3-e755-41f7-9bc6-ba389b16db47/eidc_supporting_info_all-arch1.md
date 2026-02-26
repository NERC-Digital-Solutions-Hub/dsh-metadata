# Physiological responses of marine phytoplankton to acute and chronic thermal stress.

- Overview of the dataset
  - Physiology-based measurements on four marine phytoplankton: Synechocystis sp. PCC 6803, Synechococcus sp. CCMP 2370, Phaeodactylum tricornutum CCMP 2561, and Emiliana huxleyi CCMP 1516.
  - Experimental designs to probe thermal responses: ramp (gradual heating), steady-state (acclimated to sub-, optimal-, supra-optimal temps), and thermal performance across gradients.
  - Includes omics data (genomics/transcriptomics/proteomics/metabolomics) in separate depositories.
  - Conducted at the University of Essex, School of Life Sciences, Colchester Campus, between March 2017 and February 2021; data collation and quality control completed July 2021.
  - Aimed at describing how temperature affects physiology, with potential for correlations, models, and predictions of acclimation and thermal stress responses.

- Organisms and culture conditions
  - Synechocystis sp. PCC 6803: optimal growth at 30°C in BG-11 medium with 1% CO2-enriched air; continuous illumination ~150 µmol photons m-2 s-1.
  - Synechococcus sp. CCMP 2370: grown in K medium with artificial seawater base, 3 mM bicarbonate; constant 26°C and ~325 µmol photons m-2 s-1.
  - Phaeodactylum tricornutum CCMP 2561: K medium with silicic acid, bicarbonate 3 mM; ~20°C, ~325 µmol photons m-2 s-1.
  - Emiliana huxleyi CCMP 1516: K medium with silicic acid, bicarbonate 3 mM; ~20°C, ~325 µmol photons m-2 s-1.
  - Cultures maintained under semi-continuous or continuous growth in sterile bottles with controlled light and temperature; detailed parameters provided per species.

- Experimental designs
  - Ramp experiments
    - Goal: characterize transient physiological changes during heating; sampling every hour to form time-series data.
    - Synechocystis: stepwise heating at 1.5°C h-1 from 30°C to 46.5°C; three biological replicates.
    - Synechococcus: gradual heating at ~1°C per day up to 32°C; four replicates; cells maintained and diluted as needed; sampling and physiology/'omics' analyses.
    - P. tricornutum: heat to 28°C (from 20°C) with hourly sampling; four independent biological replicates; biomass maintained by staged media replacements.
  - Steady State experiments
    - Purpose: characterize acclimated metabolic and biochemical responses at sub-optimal, optimal, and supra-optimal temperatures.
    - Species and temperature sets vary (Table 1): examples include P. tricornutum (sub 10°C, opt 20°C, supra 26.5°C), E. huxleyi (sub 10°C, opt 23°C, supra 26°C), Synechococcus CCMP2370 (sub 19°C, opt 26.5°C, supra 32°C).
    - Replicates: n = 4 per condition; after ≥4 generations post-inoculation, cultures harvested for measurements.
  - Thermal Performance experiments
    - Purpose: assess physiological and photophysiological responses across a temperature gradient under different light regimes.
    - Experimental setup involved inoculum into multiple tubes placed along temperature gradients (9–27.2°C for E. huxleyi; 8.6–29.2°C for P. tricornutum) with combinations of light intensities.
    - Temperature acclimation prior to gradient exposure; detailed light conditions varied by species.
    - Multiple biological replicates; data collected on growth and a suite of physiological measurements.

- Measurements and methods (selected)
  - Growth and biomass
    - Cell abundances measured by flow cytometry or chlorophyll a fluorescence; specific growth rates derived from log-linear fits over time.
  - Particulate organic carbon and nitrogen/phosphorus
    - POC, PON, POP quantified from filtered samples; inorganic carbon removed for TOC; results normalized to cell density or carbon, yielding C:N, C:P ratios.
  - Chlorophyll a
    - Extraction-based pigment quantification; results reported per cell or per carbon.
  - Macromolecular composition
    - Bulk protein, carbohydrate, lipid analysis via solvent extraction and colorimetric assays; polysaccharides quantified by anthrone method; proteins via BCA; lipids via sulfo-phospho-vanillin method.
  - Photosynthetic performance
    - FRRf: measures PSII electron transport kinetics; outputs include Fq'/Fm', PSII cross section, and QA re-oxidation kinetics (τ).
    - Fluorescence Light Curves (FLC): light-dependent PSII responses at varying PPFD.
    - Oxygen Light Curves (OLC) with Membrane Inlet Mass Spectrometry (MIMS): 18O2 technique to derive gross and net O2 evolution/uptake across light gradients.
  - Photoinactivation
    - PSII inactivation rates under different light intensities and with/without lincomycin to separate gross vs. net inactivation.
  - Mortality
    - Live/dead cell quantification using SYTOX green staining and flow cytometry to estimate mortality rates.
  - Flow cytometry profiling
    - Cell size (FSC), chlorophyll and phycoerythrin content (FL3, FL2) used to characterize populations and assay consistency.
  - Omics
    - Transcriptomics, proteomics, metabolomics described as part of ramp experiments; files reside in separate depositories.

- Datasets and data structure
  - Total of 18 CSV data files described with file names and contents (Table 3).
  - Datasets cover:
    - Mortality data for Phaeodactylum tricornutum.
    - Steady-state physiological measurements for P. tricornutum, Emiliana huxleyi, and Synechococcus.
    - Photoinhibition (lincomycin) data for P. tricornutum.
    - Oxygen evolution data (MIMS) for P. tricornutum.
    - FLC data for P. tricornutum, E. huxleyi, and Synechococcus.
    - Ramp and ramp-related data (including FLC) for Synechocystis, P. tricornutum, and Synechococcus.
    - Thermal performance data for P. tricornutum and E. huxleyi.
  - Column headings are standardized across files; Table 4 details units and meanings for fields such as Time, Temperature, Growth Rate, Mortality Rate, Cell mL-1, Chl a, C:N, C:P, N:P, various per-cell metrics, and FRRf-derived parameters.
  - Data replication: multiple biological replicates per condition; ramp experiments include time-series data; steady-state experiments include replicate cultures after acclimation.

- Data quality, normalization, and usage
  - Normalization approaches described per measurement (e.g., per cell, per carbon, per protein, etc.).
  - Measurements taken with consistent instrumentation settings within each experiment; methods for each metric are detailed (4.1–4.10).
  - Omics data are housed separately but linked by experimental design; data quality control and documentation provided (finalized 2021).
  - Intended uses include identifying correlations between temperature, photosynthetic performance, macromolecular composition, and mortality; developing predictive insights into thermal acclimation and stress responses in marine phytoplankton.

- Access and references
  - Data generated under NE/P002374/1 grant to Richard J. Geider; full methodological details, species-specific conditions, and measurement protocols are documented.
  - Primary references for methods and context are listed, including culture media formulations, chlorophyll equations, and previous phytoplankton thermal physiology work.

- Note on data scope
  - The dataset focuses on physiology-driven responses to acute and chronic thermal stress across diverse phytoplankton taxa, with rich time-series and multi-parameter measurements suitable for data-driven analysis and model development.

- Purpose for analysts
  - Suitable for exploring correlations between temperature exposure and growth, photosynthetic efficiency, elemental stoichiometry, and mortality.
  - Supports development of predictive models for acclimation and thermal stress outcomes, and cross-species comparisons of thermal tolerance mechanisms.