# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

## Purpose and Scope
- Provides materials accompanying the manuscript on apportioning sources of chemicals of emerging concern along an urban river using inverse modelling.
- Represents a snapshot of the SourceApp repository to enable reproducibility of results.
- Documents collection, generation, and usage of data and code developed during a six-month NERC Exploring the Frontiers project.

## Methods and Modelling Approach
- Uses waterway network topology and a simple downstream conservative mixing model to invert for source locations and concentrations.
- Builds on efficient convex optimisation techniques previously developed for sediment source apportionment.
- Principal developers: K. Chrapkiewicz (code), A. Lipp; builds on earlier work by Lipp, Barnes, Roberts.

## Data and Units
- Chemical concentrations are recorded in ng/L.
- Inverted data were generated from measurements reported by L. Barron and colleagues (Egli et al., 2023).

## Quality Control and Validation
- Includes a synthetic data inversion test.
- Analyses include an Analysis of Variance (ANOVA) and an assessment of uncertainties.
- Additional methodological details and results are provided in the supporting documentation and cited papers.

## Repository Structure and Data Management
- Data directory contains publicly available data sufficient to reproduce results.
- Key files:
  - ICL_London_Dataset2019-2021.csv (raw dataset of chemicals from Egli et al., 2022)
  - LIDAR_Composite_10m_DTM_2022_521500_540000_151500_179500.tif (DEM for drainage network)
  - Thames_d8.nc (digital drainage network)
- Figures/apportionment contains multiple chemical figures (e.g., Acetamiprid, Cocaine, Tramadol, etc.) with consistent panels (observed vs predicted, 1:1 plots, regularisation, subcatchment concentrations, and uncertainties).
- Examples/mwe.py provides a minimal working example; top-level mwe.yaml is the installation configuration.
- The directory also includes a working example (MWE) under SourceApp/examples.

## Installation and Reproduction
- Requires Unix-like environment and Anaconda.
- Steps:
  - Clone the repository (SourceApp) and optionally use the included copy.
  - Create and activate a conda environment from mwe.yaml (e.g., my_env=mwe).
  - Install dependencies: autocatchments (pip install -e .) and faster-unmixer (pip install -e) with submodules.
  - Run the Minimum Working Example: navigate to SourceApp/examples and execute python mwe.py; view generated PNGs.
- The workflow is designed to be reproducible with the provided data and configuration.

## Citing and References
- If used, cite: Chrapkiewicz, Kajetan et al. (2024) “Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling” (Science of the Total Environment). Preprint available at SSRN.
- Related references include Egli et al. (2023); Barnes & Lipp (2024); Lipp et al. (2020, 2021).

## Data Leadership Takeaways
- Emphasizes reproducibility through a clearly organized data and code structure, with publicly available data sufficient to reproduce results.
- Demonstrates data lineage from raw measurements to processed concentrations and downstream source apportionment results.
- Supports data governance best practices: explicit data sources, metadata context (file names and purposes), and a modular workflow that can be audited and reused.
- Underlines collaboration potential across data communities by building on established optimisation methods and providing a transparent, extensible framework for source apportionment in environmental data.