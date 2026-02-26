# Radial growth in stems in human-modified forests of Eastern Amazonia

## Overview
- Dataset describing radial growth of stems in 20 Amazonian forest plots (250 x 10 m each) across a prior disturbance gradient.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots each).
- Measurements collected from December 2014 to September 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Study design and sampling
- 20 plots across a disturbance gradient to assess how prior human impact influences stem growth.
- In each plot, trees and palms stratified into five DBH size classes: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm.
- At least 50 dendrometer bands per plot, distributed evenly across size classes (10 bands per class), plus bands on all lianas ≥10 cm DBH.
- Dendrometers installed 10 cm above the DBH point of measure; bands marked after one month to stabilize, with first measurement 5 months after marking.
- Monthly measurements thereafter; damaged bands replaced and reinstalled; dead stems removed and replaced with a new band on another tree in the same size class.
- Negative growth observed (due to trunk water loss) is recorded as part of measurements and not corrected.

## Measurements and data collection protocol
- Timeframe: December 2014 – September 2018.
- Convert monthly dendrometer readings into radial growth (mm) per individual per month.
- Data management practices include re-installation of bands after damage and documentation of re-installations (Tree_tag and Life form data maintained).
- Notes and field observations recorded monthly (OBS-Dec14) alongside monthly growth (mm-Dec14, etc.).

## Location, coordinates, and data structure
- Geographic coordinates provided for each sampled plot (latitude and longitude per plot/transect), covering multiple microcatchments within the study area in Eastern Amazonia.
- Data are stored in a comma-separated value file: RadialGrowthOfStems.csv.
- Key columns and meanings:
  - Catchment, Transect, Plot: plot identifiers within microcatchments.
  - Rainfor: plot code according to the ForestPlots database.
  - Forest: disturbance class prior to the 2015–16 El Niño.
  - Fire_ElNino: whether the plot burned during the 2015–16 El Niño.
  - Tree_tag: identifier for each individual with a dendrometer band.
  - Tree_code: unique code combining bacia, plot, and tree tag.
  - DBH: diameter at breast height measured in 2014.
  - Life form: tree (A), liana (C), or palm (P).
  - Re-installed: whether the dendrometer was reinstalled during the study.
  - Data-Dec14 and subsequent month columns (e.g., mm-Dec14): radial growth in millimeters for each month.
  - OBS-Dec14 and subsequent months: field notes for each monthly measurement.

## Data governance and accessibility considerations
- The dataset emphasizes standardized data collection and explicit metadata (column headers, units, and timing), enabling comparability across plots and time.
- Detailed documentation of methods (installation, stabilization period, monthly measurement schedule, handling of damage) supports transparency and reproducibility.
- Data are linked to a major environmental monitoring program, illustrating a model for policy-relevant environmental health monitoring and long-term data stewardship.