# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

## Overview
- Dataset of mathematically modelled water saturation along vertical soil profiles at six sites near the Namoi River, south-eastern Australia.
- Sites split between two locations: Old Mollee and Yarral East, at varying distances from the river.

## Data Acquisition and Modelling
- Generated using the HaughFlow model (Evans et al., 2018), which predicts water movement in vadose and phreatic zones of hydraulically connected floodplains.
- Based on 1D vertical Richards equation (vadose zone) and 1D lateral Boussinesq equation (phreatic zone); two-way coupling enables water exchange between zones.
- Model coded in Fortran90 with a tri-diagonal solver and predictor-corrector temporal discretisation; centered finite differences for spatial discretisation.
- Inputs: river stage levels, climate parameters, and soil properties to determine lateral inputs, vertical inputs, and water flow speed.
- Outputs: time series of soil-water profiles at chosen distances from the river and down to specified depths; outputs stored in unformatted files and converted to formatted files for usability.

## Data Description
- Data comprise modeled vertical soil-water saturation profiles, with depths from the surface down to 10 m.
- Six sites at two locations:
  - Old Mollee: 50 m, 140 m, 320 m from the river
  - Yarral East: 40 m, 110 m, 290 m from the river
- Distances are embedded in the file names (e.g., OldMollee50m).
- Depths: 0–10 m; water saturation ranges from 0 to 1, reported to 7 decimals.
- Time series: daily outputs; depth grid uses 944 points across 10 m depth at half-grid intervals.
- Site coordinates (latitude, longitude, and elevation) provided for each location.

## Timeframe
- Old Mollee datasets (Figure 6): 01 July 2011 to 30 June 2015.
- Yarral East datasets (Figure 6): 01 January 2013 to 30 June 2015.
- Old Mollee Figure 7 dataset (alternative climate inputs): 01 January 2004 to 31 December 2016.

## Calibration and Validation
- Calibrated against water table levels at Yarral East 290 m for the year 2013.
- Calibrated soil properties include:
  - Saturated hydraulic conductivity: 5.756 m/day
  - Drainage: 0.01568 m/day
- Further methodological details provided in Evans, C.M., Dritschel, D.G., and Singer, M.B. (2018), Modelling subsurface hydrology in floodplains (Water Resources Research).

## Provenance and Metadata
- Data accompany a published study documenting the modeling approach and site descriptions (Evans et al., 2018).
- Part of a PhD project funded by the Natural Environment Research Council and the National Trust.

## Access and Use Considerations
- Outputs are model-generated data; users should consider the underlying assumptions of HaughFlow, the calibrated parameters, and the climate inputs used.
- Metadata includes precise site locations, depths, timeframes, and file naming conventions to aid discovery and reuse.