# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Overview
- Dataset representing aboveground woody biomass (tC/ha) for three study areas in Mozambique: Mabalane, Gurue, and Maruppa.
- Each area contains three GeoTIFF layers corresponding to years 2007, 2010, and 2014, enabling year-specific analyses.
- -18 indicates no data; occasional negative values may occur due to noise.

## Data structure
- Three spectral layers per area, stacked as:
  - Band 1 = 2007
  - Band 2 = 2010
  - Band 3 = 2014
- Biomass values expressed as carbon density (tC/ha) derived from sigma0; the conversion uses a central/northern Mozambique-based equation (not locally calibrated).
- Individual layers can be extracted for analyses focused on a single year.

## Methods and quality control
- Based on established methods (Ryan et al. 2012; Ryan et al. 2014) updated for PALSAR-2.
- Data sources: three ALOS PALSAR scenes per year (2007, 2010, 2014) capturing HV backscatter in power units.
- Preprocessing:
  - Late dry-season acquisitions from two tracks.
  - Calibration, terrain correction, and despeckling with a 3x3 GammaMAP filter.
  - Output at 15 m pixel size.
  - Scene georeferenced to a mosaicked, pansharpened Landsat 8 base (Sept 2014) using manual tie points.
- Georeferencing accuracy:
  - Reported RMS errors (in pixels) vary by scene; typical mean RMS errors range from ~0.6 to ~1.9 pixels; max RMS up to ~1.9–1.7 pixels depending on year/scene.
  - Tie points per scene range from 24 to 75.
- Coregistration note: coregistration attempts had limited effect; ALOS-2 generally provides better location accuracy than ALOS-1.

## Biomass estimation and caveats
- Biomass values convert sigma0 to carbon density using Ryan et al. (2012) equations; not locally validated with plot data in this study.
- Accuracy caveats:
  - Estimates may be biased in flooded/wet areas; such areas should be masked.
  - Urban areas should be masked as well.
  - Local calibration against plot data recommended to assess map accuracy.
- Recommendations to users:
  - Consider increasing pixel size (e.g., 30–60 m) to suppress noise.
  - Cross-check biomass estimates against independent plot data where possible.

## Data usage notes and acknowledgments
- Data provenance and acknowledgments:
  - ALOS PALSAR data provided by JAXA and ESA under specific agreements; ESPA acknowledgment required.
  - JAXA: 4th Research Agreement for ALOS-2; PI No. 1152.
  - ESA: Category-1 Proposals 7493 and 18624; ESPA acknowledgment separately.
- Core methodological references:
  - Ryan, C. M. et al. 2012; Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery.
  - Ryan, C. M., Berry, N. J. & Joshi, N. 2014; Quantifying causes of deforestation and degradation and creating REDD+ baselines.

## Additional notes
- -18 data points indicate missing data in the biomass layers.
- The study emphasizes transparency of methodology and calls for corroboration with plot data to assess accuracy.