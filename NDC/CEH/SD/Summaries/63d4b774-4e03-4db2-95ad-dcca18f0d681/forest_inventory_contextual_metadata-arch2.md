# Tree census in permanent forest plots across the Amazon Basin

- Data theme: Long-term tree census within a network of permanent forest plots in the Brazilian Amazon (RAINFOR), focused on Diameter at Breast Height (DBH) measurements.
- Scope: 8,729 trees across 29 plots in Acre, Mato Grosso, and Pará; terra-firme, nonflooded lowland forests.
- Timeframe: Measurements collected between 2017 and 2019.

## Data Collection & Methods
- Plot details: Forest plots sized 0.25 ha or 1 ha; plots already established from prior campaigns.
- Tree identification: Each tree tagged; new recruits (DBH > 100 mm) receive a new tag; dead trees recorded with cause of death and decomposition stage.
- Measurements: DBH measured with measuring tape; state of living trees documented.
- Standards: Field work follows the RAINFOR protocol; detailed process available at forestplots.net.

## Data Processing & Storage
- Digitisation: Field sheets digitised, error-checked, and uploaded to ForestPlots.net.
- Integration: Data combined with previous censuses to enable long-term forest dynamic analyses.
- Research context: Part of projects investigating past fires and current carbon dynamics in Amazonian forests; supported by multiple grants and institutions.
- Data accessibility: Stored and accessible via ForestPlots.net, promoting reuse and cross-study analyses.

## Data Quality & Units
- Quality control: QC checks conducted per ForestPlots.net protocol; DBH values verified individually with corrective actions as needed.
- Units: DBH reported in millimeters (mm).

## Data Structure & Access
- CSV structure: tree_data.csv
  - Plot_number: plot code
  - Tree_ID: internal tree code for the network
  - Tag_No: field tag identifier
  - DBH: diameter at breast height
  - Latitude: geographic latitude
  - Longitude: geographic longitude

## Relevance for Environmental Monitoring
- Standardized, verifiable dataset supporting environmental health monitoring and policy performance assessment over time.
- Facilitates cross-plot comparisons and data integration with other datasets to increase the value of monitoring data and support broader analyses of Amazonian forest dynamics.

## Funding & Acknowledgments
- Research linked to Do past fires explain current carbon dynamics of Amazonian forests? (NERC NE/N011570/1) and CAPES, Brazil.
- Additional support from Royal Society Global Challenge Award FORAMA, CNPq, PELD projects, PPBio, FATE, and FAPESP.  

## References
- ForestPlots.net et al. Taking the pulse of Earth's tropical forests using networks of highly distributed plots. Biological Conservation 260 (2021) 108849. https://doi.org/10.1016/j.biocon.2020.108849