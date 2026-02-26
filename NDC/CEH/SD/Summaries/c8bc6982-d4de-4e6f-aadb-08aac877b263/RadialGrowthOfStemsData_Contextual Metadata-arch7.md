# Radial growth in stems in human-modified forests of Eastern Amazonia

- Overview
  - Dataset: RadialGrowthOfStemsData.csv with measurements of litterfall and radial growth from 20 Amazonian forest plots (each 250 x 10 m).
  - Plots span a gradient of prior human disturbance: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
  - Data collection timeframe: December 2014 to September 2018.
  - Context: Part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

- Data collection methods
  - Each plot stratified into five DBH size classes (1019.99 cm, 20-29.99 cm, 30-39.99 cm, 40-49.99 cm, ≥50 cm).
  - At least 50 dendrometer bands per plot (10 per size class); bands also installed on all lianas ≥10 cm DBH.
  - Dendrometers installed 10 cm above DBH; a one-month settle period before marking the zero line; first measurement 5 months after marking; then monthly measurements.
  - If bands were damaged, replacements followed by proper re-installation; if a stem died, the band was removed and a new one installed on another tree in the same size class.
  - Negative growth (stem shrinkage) can occur due to bark water loss; no correction applied, as positive growth includes water accumulation.

- Spatial information
  - Plot coordinates are provided (lat/long) for 20 plots, labeled with codes such as 112_12, 112_8, 129_10, etc.
  - Latitudes range around -2.57 to -3.31, longitudes around -54.65 to -55.01 (within the Eastern Amazonia region).
  - Coordinates enable GIS mapping of plot locations and integration with other spatial datasets.

- Data structure and key fields
  - File name: RadialGrowthOfStems.csv
  - Core columns (sampled fields):
    - Catchment: microcatchment (~5,000 ha) containing each plot
    - Transect: plot number within each bacia
    - Plot: unique plot code (bacia + transect)
    - Rainfor: plot code per ForestPlots database
    - Forest: disturbance class before the 2015-16 El Niño
    - Fire_ElNino: whether the plot burned during the 2015-16 El Niño
    - Tree_tag: individual dendrometer band identifier
    - Tree_code: unique code for each individual (bacia_plot_treeTag)
    - DBH: diameter at breast height (2014)
    - Life form: A = tree, C = liana, P = palm
    - Re-installed: whether dendrometer band was re-installed during the study
    - Data-Dec14: month of data (e.g., Dec14)
    - mm-Dec14: radial growth in mm for that month
    - OBS-Dec14: field notes for that month
  - Temporal coverage: monthly measurements from Dec 2014 through Sep 2018 (Data-Jan15, Data-Feb15, etc., with corresponding mm-<Month> and OBS-<Month> fields).

- Interpretation and usage notes for GIS
  - Suitable for map-based visualization of radial growth trends across disturbance classes and over time.
  - Can be integrated with canopy disturbance, fire history, and land-use datasets to explore spatial patterns in growth responses.
  - Data quality considerations: monthly sensor/field notes, band maintenance, and re-installations may affect time-series continuity; negative growth is data-meaningful (water loss) and not corrected.
  - The dataset provides detailed per-tree growth measurements linked to plot-level disturbance context, enabling fine-grained GIS analyses and cross-dataset comparisons.