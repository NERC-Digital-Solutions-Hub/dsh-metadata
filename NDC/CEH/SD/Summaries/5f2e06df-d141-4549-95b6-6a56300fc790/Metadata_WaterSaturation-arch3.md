# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

## Overview
- Dataset of daily water-saturation profiles along vertical soil columns (0 to 10 m deep) for six sites near the Namoi River, from two locations: Old Mollee and Yarral East.
- Sites are at two locations with varying distances from the river: Old Mollee (50 m, 140 m, 320 m) and Yarral East (40 m, 110 m, 290 m).
- Generated using the HaughFlow model to simulate subsurface hydrology in hydraulically connected floodplains, coupling vadose and phreatic zone dynamics.

## Data and Modelling Details
- Acquisition method: HaughFlow model (Evans et al., 2018), which solves the 1D vertical Richards equation for vertical moisture transport (vadose zone) and the 1D lateral Boussinesq equation for lateral saturated flow (phreatic zone); two-way coupling between zones.
- Implementation: Fortran90 with a tri-diagonal solver, predictor-corrector temporal discretisation, and centered finite differences for spatial discretisation.
- Inputs: river stage levels, climate parameters, and soil properties to determine lateral inputs, vertical inputs, and flow speed.
- Outputs: time series of soil-water profiles at chosen distances and depths; stored originally in unformatted files and converted to formatted files for ease of use.
- Grid/domain: 944 grid points across 10 m depth at half-grid intervals.
- Data relation: Outputs correspond to figures in Evans et al. (2018).

## Site, Timeframe and Data Structure
- Study sites: Old Mollee (50 m, 140 m, 320 m from river) and Yarral East (40 m, 110 m, 290 m from river).
- Coordinates (latitude, longitude in decimal degrees; elevation in metres AHD):
  - Old Mollee 50 m: -30.254, 149.681 (202.25)
  - Old Mollee 140 m: -30.254, 149.682 (204.37)
  - Old Mollee 320 m: -30.254, 149.684 (203.82)
  - Yarral East 40 m: -30.237, 149.671 (202.98)
  - Yarral East 110 m: -30.236, 149.671 (202.84)
  - Yarral East 290 m: -30.234, 149.671 (202.02)
- Time frames:
  - Old Mollee Figure 6 datasets: 01 July 2011 to 30 June 2015.
  - Yarral East Figure 6 datasets: 01 Jan 2013 to 30 June 2015.
  - Old Mollee Figure 7 dataset (alternative climate inputs): 01 Jan 2004 to 31 Dec 2016.
- Output specifics: daily outputs; depth from surface; depth grid characteristics as described above.

## Calibration and Validation
- Calibration: Model outputs calibrated against water-table levels at Yarral East 290 m for the year 2013.
- Resulting soil properties (calibration): saturated hydraulic conductivity = 5.756 m/day; drainage = 0.01568 m/day.
- See Evans et al. (2018) for fuller methodological details on calibration and hydrological modelling.

## Access, Format and References
- Data format: outputs originally in unformatted files; reformatted versions provided for ease of use.
- Documentation and methodology reference: Evans, C.M., Dritschel, D.G., and Singer, M.B., 2018, "Modelling subsurface hydrology in floodplains," Water Resources Research.
- Project context: data modelled as part of a PhD project funded by the Natural Environment Research Council (NERC) and the National Trust.