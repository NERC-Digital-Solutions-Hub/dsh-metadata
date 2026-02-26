# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Overview
- Dataset of aboveground woody biomass maps for three Mozambican study areas: Mabalane, Gurue, and Maruppa.
- Contains three GeoTIFF layers corresponding to years 2007, 2010, and 2014.
- Each pixel stores biomass in tonnes of carbon per hectare (tC/ha); -18.00000 indicates no data.
- Negative biomass values may occur due to noise.
- Layers can be extracted individually for year-specific analyses.

## Data Structure
- Three stacked GeoTIFF layers per site: band 1 = 2007, band 2 = 2010, band 3 = 2014.
- Biomass values derived from the corresponding layer; can be used to compare changes over time.

## Methods & Quality Control
- Method follows Ryan et al. (2012, 2014), updated to handle PALSAR-2 data.
- Built from three ALOS PALSAR scenes per year (2007, 2010, 2014) using HV backscatter in power units.
- Late dry-season imagery; scenes calibrated, terrain-corrected, and despeckled (3x3 GammaMAP) in SNAP v2.0; exported at 15 m resolution.
- Each scene georeferenced to a mosaicked Landsat 8 image (Sept 2014) using ENVI v4.8 with manually selected tie points.
- Accuracy assessment provided as RMS errors per tie point set (varies by image and year; ranges roughly from ~0.6 to ~1.9 pixels with 24–75 tie points across different scenes).
- Biomass layer values are converted from sigma0 to carbon density using the Ryan et al. (2012) equation (based on data from central/northern Mozambique, not locally validated).

## Accuracy, Limits, and Validation
- Local validation needed: conversion to carbon density not locally calibrated; corroboration with plot data recommended to estimate map accuracy.
- Biomass estimates are unreliable in flooded/wet areas; these areas should be masked.
- Urban areas should also be masked; consider increasing pixel size (e.g., 30–60 m) to reduce noise.
- Accuracy estimates are documented in Ryan et al. (2012); users should reference these for context.

## Usage, Reuse, and Provenance
- Acknowledgements required: JAXA and ESA provided the ALOS PALSAR data; ESPA acknowledgment also appropriate.
- If used, cite the dataset alongside Ryan et al. (2012) and Ryan et al. (2014) for methodology and context.
- Data structure supports year-by-year analyses of biomass change and can inform deforestation/forest degradation assessments at local scales.

## Notes for Data Leaders
- Provides a clear data lineage: satellite data → processing chain → georeferencing to Landsat mosaic → biomass conversion.
- Explicit quality control steps and limitations enable informed decision-making about where the data are applicable.
- Highlights data gaps and requirements for validation, guiding planning for data gathering, standards alignment, and potential collaboration to improve local calibration.
- Suitable for integration into wider analyses of forest biomass dynamics across networks, with explicit caveats and recommended refinements. 

## References
- Ryan, C. M. et al. Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery. Glob. Chang. Biol. 18, 243-257 (2012).
- Ryan, C. M., Berry, N. J. & Joshi, N. Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique. Appl. Geogr. 53, 45-54 (2014).