# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Overview
- Dataset represents aboveground woody biomass (tC/ha) for three study areas in Mozambique: Mabalane, Gurue, and Maruppa.
- Each study area has three GeoTIFF layers corresponding to years 2007, 2010, and 2014.
- NoData value is -18; negative biomass values can occur due to noise.
- Individual yearly layers can be extracted for year-specific analyses.

## Data structure and formats
- Three separate GeoTIFF layers per study area (one per year).
- Pixel resolution: 15 m.
- Each pixel value reflects biomass density in tonnes of carbon per hectare.
- Biomass estimates are converted from sigma0 as described in the methods (not local to the study region).

## Methods and processing
- Processing lineage follows Ryan et al. 2012 and 2014, updated for ALOS PALSAR 2.
- Data sources: three ALOS PALSAR scenes per year (2007, 2010, 2014) using HV backscatter in power units.
- Acquisition timing: late dry season, from two tracks.
- Processing steps:
  - Calibration, terrain correction, and despeckling (3x3 GammaMAP) in SNAP v2.0.
  - Export to 15 m pixel size.
  - Scene georeferencing to a mosaic, pansharpened Landsat 8 base image (Sept 2014) using ENVI v4.8.
  - Georeferencing done with manually selected tie points distributed around each image.
- Tie-point accuracy (RMS errors) summarized for multiple acquisitions (values range roughly from 0.6 to 1.9 pixels; number of tie points from ~24 to 75 depending on scene).

## Biomass conversion and scope
- Biomass layer values are sigma0 converted to carbon density (tC/ha) using the Ryan 2012 equation.
- Conversion based on Central/Northern Mozambique data; not local to these sites; accuracy should be corroborated with plot data.

## Limitations and data quality
- Biomass estimates may be inaccurate in flooded/wet areas; mask these regions, as well as urban areas.
- Noise in the data may warrant increasing pixel size (e.g., 30 m or 60 m) to improve robustness.
- Detailed accuracy estimates are provided in Ryan et al. (2012).

## Usage considerations
- Each yearly layer can be used independently for temporal analyses of biomass.
- Ensure masking of problematic areas (flooded, urban) and consider resampling if noise is an issue.
- Properly acknowledge data sources and providers when using the datasets.

## Data sources and acknowledgments
- ALOS PALSAR data provided by JAXA and ESA.
- ESPA acknowledgment required separately.

## Additional notes
- Georeferencing should be performed for each scene prior to mosaicking; coregistration was not essential in this workflow.
- ALOS-2 generally offers better positional accuracy than ALOS-1 for this processing.

## References
- Ryan, C. M., et al. 2012. Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery. Glob. Chang. Biol.
- Ryan, C. M., Berry, N. J., & Joshi, N. 2014. Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique. Appl. Geogr.