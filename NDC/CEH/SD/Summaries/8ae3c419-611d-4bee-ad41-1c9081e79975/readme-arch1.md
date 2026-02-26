# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

- Purpose
  - Presents supplementary material for the manuscript on apportioning sources of chemicals of emerging concern along an urban river using inverse modelling.
  - Describes data, methods, quality controls, and repository structure to reproduce and extend the results.

- Methods and modelling approach
  - Source apportionment uses river network topology and a downstream conservative mixing model to invert for source locations and concentrations from measured concentrations.
  - Builds on efficient convex-optimisation approaches previously developed for sediment source apportionment.
  - Principal developers: K. Chrapkiewicz (code) with A. Lipp; extends prior work by Lipp, Barnes, Roberts, and collaborators.
  - Outputs focus on identifying where chemicals originate and their concentrations along subcatchments.

- Nature and units of data
  - Chemical concentrations are recorded in ng/L.
  - Inversion data drawn from Egli et al. (2023/2022) datasets and related sources.

- Quality control and uncertainty
  - Includes a synthetic data inversion test to assess performance.
  - An Analysis of Variance (ANOVA) and uncertainty assessment are performed.
  - Additional methodological details provided in supporting documentation and cited papers.

- Repository structure and contents
  - Data directory contains publicly available datasets to reproduce results (e.g., ICL_London_Dataset2019-2021.csv, LIDAR DTM, Thames drainage network).
  - Figures/apportionment includes multiple chemicals with standardized plots (observed vs. predicted, 1:1 plots, regularisation vs data misfit vs model roughness, subcatchment concentrations, and uncertainty).
  - examples directory provides a Minimal Working Example (MWE) with mwe.py.
  - Top level includes mwe.yaml (installation config).
  - Data and example files are organized to support replication of the analyses and visualizations.

- Installation and running the Minimal Working Example (MWE)
  - Prerequisites: Unix-like environment and Anaconda.
  - Steps:
    - Clone the repository (or use included SourceApp).
    - Create and activate a conda environment using the provided mwe.yaml (e.g., conda env create --name mwe --file=mwe.yaml; conda activate mwe).
    - Install dependencies:
      - autocatchments (clone and pip install -e .
      - faster-unmixer (clone with submodules and pip install -e .)
    - Run the MWE:
      - cd SourceApp/examples
      - python mwe.py
  - Output: generated PNG figures illustrating observed vs predicted concentrations and other diagnostic plots.

- Data provenance and reproducibility
  - The repository provides a Data directory with raw datasets (publicly available) to reproduce results.
  - Acknowledges the upstream data sources (e.g., Egli et al. 2023/2022) and the associated methodological papers for the optimisation approach.

- Citing and references
  - Primary citation for use: Chrapkiewicz, Kajetan; Lipp, Alex; Barron, Leon Patrick; Barnes, Richard; Roberts, Gareth (2024), "Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling". Science of the Total Environment. Preprint available.
  - Related references cited in the supplementary material:
    - Egli et al. (2023) on environmental risk assessment of contaminants in London’s waterways during SARS-CoV-2.
    - Barnes & Lipp (2024) on convex optimisation for source apportionment.
    - Lipp et al. (2020, 2021) on source region geochemistry and unmixing downstream observations.