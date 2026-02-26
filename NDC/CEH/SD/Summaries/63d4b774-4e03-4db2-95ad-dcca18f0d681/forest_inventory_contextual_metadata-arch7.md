# Tree census in permanent forest plots across the Amazon Basin

## Overview
- Dataset of Diameter at Breast Height (DBH) for 8,729 trees across 29 RAINFOR forest plots in the Brazilian Amazon (Acre, Mato Grosso, Pará).
- Plot types: terra-firme, nonflooded lowland forests.
- Measurements collected between 2017 and 2019.
- Data file: tree_data.csv with DBH values in millimetres (mm) and geographic coordinates.

## Data collection and protocol
- Plots were established in prior field campaigns; plot sizes range from 0.25 ha to 1 ha.
- Trees tagged in the field; DBH measured with a measuring tape.
- New recruits (DBH > 100 mm) assigned a new tag; dead trees recorded with cause of death and decomposition stage.
- For living trees, tree state was noted.
- All fieldwork conducted following the RAINFOR protocol (detailed at forestplots.net).

## Data structure and contents
- CSV columns included: Plot_number, Tree_ID, Tag_No, DBH, Latitude, Longitude.
- Additional observations (e.g., tree state, cause of death, decomposition) captured per field protocol (not all necessarily in the CSV). Coordinates enable GIS mapping.

## Data processing and quality control
- Field data digitised and uploaded to ForestPlots.net, enabling integration with historical censuses for long-term forest dynamics.
- DBH values were quality-checked individually; corrective actions applied as needed following ForestPlots.net quality protocols.

## Data provenance and access
- Collected under the project Do past fires explain current carbon dynamics of Amazonian forests, with support from multiple funders (NERC, CAPES, Royal Society, CNPq, PPBio, FATE, FAPESP, and others).
- Primary data storage and access via ForestPlots.net; dataset referenced in Biological Conservation 2021 (taking the pulse of Earth's tropical forests).

## GIS relevance and applications
- Enables map-based visualization of tree sizes and their spatial distribution across Amazon plots.
- Can be combined with other spatial datasets (e.g., carbon dynamics, species distributions) for enhanced environmental analyses.
- Useful for examining spatial structure and long-term forest dynamics in terra-firme forests of the Amazon.

## Notes and considerations for users
- Plot size variation (0.25–1 ha) may affect comparability across plots; consider normalization when aggregating.
- Temporal scope is 2017–2019; the dataset supports historical analyses but is not a continuous time series beyond that window.
- Data quality relies on precise geolocation and adherence to the documented field protocols.