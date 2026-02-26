# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

## Overview
- Describes the supplementary materials accompanying the manuscript “Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling” by Chrapkiewicz et al. (submitted; preprint available).
- Provides the SourceApp code snapshot and related data used to perform inverse-model source apportionment in a river network.
- Builds on prior convex-optimisation source apportionment work and employs downstream conservative mixing plus measured concentrations to infer source locations and concentrations.

## Data and Units
- Chemical concentration units: nanograms per litre (ng/L).
- Data sources include:
  - Synthetic and real concentration data used for inversion, with origins in Barron and colleagues and Egli et al. (2023).
  - Publicly available data in the Data directory to reproduce results (e.g., ICL London Dataset 2019–2021; LIDAR-based DTM; Thames drainage network).
- Recorded outputs include observed vs. predicted concentrations at sampling sites, regularisation plots, and calculated subcatchment source concentrations with associated uncertainties.
- Figures depict:
  - Observed vs. predicted concentrations at sample sites.
  - 1:1 plots and regularisation (data misfit vs. model roughness) for different lambda values.
  - Calculated subcatchment source concentrations and uncertainties.

## Methods (Conceptual)
- Source apportionment uses:
  - Waterway network topology.
  - A simple downstream conservative mixing model.
  - Inversion to estimate source locations and concentrations from measured concentrations.
- Methodology builds on refined convex-optimisation approaches for efficient source apportionment of tracers and pollutants.
- A synthetic data inversion, ANOVA, and uncertainty assessments are performed to evaluate robustness.

## Quality Control
- Synthetic data inversion used to test the method.
- Analysis of Variance (ANOVA) and uncertainty assessment conducted.
- Details and justification referenced in the accompanying documentation and cited papers.

## Repository Structure and Content
- Top-level: mwe.yaml configuration for installation.
- Data/ directory: contains raw and auxiliary data necessary to reproduce results:
  - ICL_London_Dataset2019-2021.csv
  - LIDAR_Composite_10m_DTM_2022_521500_540000_151500_179500.tif
  - Thames_d8.nc (drainage network)
- Figures/apportionment/: multiple PNGs for each chemical (e.g., Acetamiprid, Cocaine, Tramadol, etc.) with standard panels (observed vs. predicted, 1:1, regularisation, subcatchment concentrations, uncertainty).
- Examples/: minimal working example (MWE) with mwe.py.
- Data and figures are organized to support reproducibility of the results described in the manuscript.

## Installation and Running
- Prerequisites: Unix-like environment and Anaconda.
- Steps:
  - Clone the repository (or use included SourceApp).
  - Create and activate a conda environment from mwe.yaml (e.g., my_env=mwe).
  - Install required packages:
    - autocatchments (from GitHub) in editable mode.
    - faster-unmixer (with submodules) in editable mode.
  - Run the MWE:
    - cd SourceApp/examples
    - python mwe.py
  - Review generated PNG outputs to view results.
- Notes:
  - The repository is a snapshot designed to reproduce the study results; updates are available in the upstream SourceApp repository.

## Citing and References
- If used in research, cite:
  - Chrapkiewicz, Kajetan; Lipp, Alex; Barron, Leon Patrick; Barnes, Richard; Roberts, Gareth (2024), “Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling”. Science of the Total Environment. Preprint available at SSRN.
- Related references:
  - Egli et al. (2023), A One-Health environmental risk assessment of contaminants of emerging concern in London's waterways throughout the SARS-CoV-2 pandemic.
  - Barnes & Lipp (2024), Using convex optimisation to efficiently apportion tracer and pollutant sources from point concentration observations.
  - Lipp et al. (2020, 2021), Source region geochemistry and river sediment mixture modelling studies.

## Practical Relevance for Analysts Monitoring the Environment
- Provides a data-driven, reproducible workflow to apportion chemical sources along an urban river.
- Demonstrates how to:
  - Integrate network topology with measured concentrations for source inference.
  - Use convex-optimisation techniques to efficiently estimate source locations and strengths.
  - Produce standardized outputs (observed vs predicted, regularisation diagnostics, subcatchment source estimates, uncertainties) suitable for monitoring reports and policy evaluation.
- Emphasizes quality control and uncertainty assessment to support decision-making and transparency in environmental health assessments.

## Limitations and Considerations for Use
- The materials represent a snapshot requiring specific dependencies and data; ongoing updates may be required for new datasets.
- Installation involves multiple external packages and submodules; users must follow the specified steps to ensure compatibility.
- The methodology assumes downstream conservative mixing and network topology accuracy; real-world deviations could affect source attribution.