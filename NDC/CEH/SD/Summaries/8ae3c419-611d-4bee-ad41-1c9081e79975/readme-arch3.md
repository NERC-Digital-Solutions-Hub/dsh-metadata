# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

## Overview
- Presents supplementary material for the manuscript on apportioning sources of chemicals of emerging concern along an urban river using inverse modelling.
- Authors: Chrapkiewicz et al.; manuscript submitted to Science of the Total Environment; preprint available.
- Repository is a snapshot of the SourceApp project and supports reproducing results discussed in the paper.
- Core approach: use river network topology and a simple downstream conservative mixing model alongside measured concentrations to invert for source locations and concentrations.
- Builds on convex optimisation source apportionment methods developed by Lipp, Barnes, and colleagues.

## Data, units, and quality control
- Chemical concentrations are recorded in ng/L; inverted data originate from Egli et al. (2023).
- Quality control includes a synthetic data inversion and an Analysis of Variance (ANOVA) with uncertainty assessment.
- Supporting documentation and cited papers provide further methodology and results details.

## Structure of the repository
- Data directory contains publicly available data necessary to reproduce results.
- Examples directory includes a minimal working example (MWE) and instructions.
- Figures/apportionment includes plots for multiple chemicals (e.g., acetamiprid, cocaine, tramadol, azithromycin, diclofenac, etc.), each with panels showing observed vs. predicted concentrations, 1:1 plots, regularisation studies, subcatchment source concentrations, and uncertainties.
- top-level mwe.yaml configuration file for installation.
- Data files include raw datasets (e.g., ICL London dataset 2019–2021), a detailed digital elevation model (LIDAR DEM), and a Thames drainage network (thames_d8.nc).
- Examples include mwe.py (minimum working example).

## Installation and running the minimal example
- Steps (Unix-like environment):
  - Clone the repository: git clone git@github.com:kmch/SourceApp.git (SourceApp is included; updates optional).
  - Create and activate a conda environment from mwe.yaml, e.g., conda env create --name mwe --file=mwe.yaml; conda activate mwe.
  - Ensure Python points to the environment (tested with Python 3.11).
  - Install autocatchments (pip install -e) from the autocatchments GitHub repo.
  - Install faster-unmixer (pip install -e) from its GitHub repository.
  - Run the minimum working example: navigate to SourceApp/examples and execute python mwe.py.
  - Open generated PNG outputs to view results.
- The instructions emphasize reproducibility and environment isolation.

## Data availability and governance considerations
- The repository provides data sufficient to reproduce results; data sharing is openly supported but publicly sharing datasets can be a barrier in some contexts.
- Metadata quality and consistency are important for reuse; the project includes notes on data provenance and data processing steps.

## Reproducibility and references
- Primary citation: Chrapkiewicz, Kajetan; Lipp, Alex; Barron, Leon Patrick; Barnes, Richard; Roberts, Gareth (2024), 'Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling'. Science of the Total Environment. Preprint available at SSRN.
- Related references:
  - Egli et al. (2023), on One-Health environmental risk assessment in London’s waterways.
  - Barnes & Lipp (2024), convex optimisation for source apportionment.
  - Lipp et al. (2020, 2021), source region geochemistry and unmixing downstream sedimentary compositions.

## Relevance to monitoring frameworks
- Demonstrates an end-to-end workflow aligned with monitoring framework aims:
  - Data gathering from diverse sources and generation of downstream mixing-based inverse models.
  - Data quality assurance, transformation, and presentation through reports and visualisations.
  - Transparent sharing of underlying data and reproducible computational steps.
  - Provision for updating models with improved data, metadata, and governance practices.

## Practical considerations for policy and decision support
- Enables identification of chemical sources along a river system, informing targeted monitoring and interventions.
- Uses open data and transparent methods to support evidence-based decisions and accountability.
- Highlights the importance of metadata, data provenance, and governance to ensure data usable for policy analysis and future monitoring planning.

## Limitations and caveats
- Inversion performance relies on simplified mixing assumptions and network topology; uncertainty analyses are necessary and provided.
- The project includes a synthetic data inversion and empirical validation; real-world applicability requires careful interpretation and ongoing data updates.
- Access to comprehensive, high-quality metadata remains a critical factor for verifiability and reuse.