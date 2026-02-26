# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Overview
- Dataset of aboveground woody biomass for three Mozambican study areas: Mabalane, Gurue, and Maruppa.
- Contains three GeoTIFF layers representing years 2007, 2010, and 2014.
- Each pixel value is biomass in tonnes of carbon per hectare (tC/ha).
- No-data value is -18.00000; negative values may occur due to noise.
- Layers can be analyzed year-by-year.

## Data Structure
- Band 1: 2007, Band 2: 2010, Band 3: 2014.
- Each pixel: aboveground woody biomass (tC/ha).
- Biomass layer values converted from sigma0 to carbon density using Ryan et al. 2012 equation (not local-specific).
- Note: conversions and results are not fully locally validated; cross-check with plot data recommended.

## Methods and Quality Control
- Method follows Ryan et al. (2012, 2014), updated for PALSAR 2.
- Data sources: three ALOS PALSAR scenes per year (2007, 2010, 2014); HV backscatter in power units.
- Acquisition: late dry season imagery from two tracks.
- Processing: calibrated, terrain-corrected, despeckled (3x3 GammaMAP filter) in SNAP v2.0; output at 15 m pixel size.
- Georeferencing: scenes manually tied to a mosaicked Landsat 8 image (Sept 2014) using ENVI v4.8; reference tie points distributed around the image.
- Accuracy (sampled per scene): RMS errors range ~0.6–1.9 pixels; tie points per scene range 24–75 (see Table 1 in the source).
- Acknowledges data providers: JAXA (ALOS PALSAR) and ESA; ESPA acknowledgment required.

## Data Quality and Limitations
- Biomass estimates may be inaccurate in flooded/wet areas and urban areas; recommended masking.
- Central and northern Mozambique calibration data used; not fully local—validation against plot data advised.
- Negative biomass values can occur due to noise; treat with caution.
- Suggestion to reduce noise by increasing pixel size to 30–60 m where appropriate.

## Usage and Attribution
- If using the data, acknowledge JAXA and ESA for ALOS PALSAR imagery and ESPA as applicable, per the data provider guidance.

## References
- Ryan, C. M. et al. Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery. Glob. Chang. Biol. 2012.
- Ryan, C. M., Berry, N. J. & Joshi, N. Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique. Appl. Geogr. 2014.