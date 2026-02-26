# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

## Overview
- A dataset of daily vertical soil water saturation profiles (0–1) for six sites near the Namoi River, SE Australia.
- Generated with the HaughFlow model to predict vadose and phreatic zone moisture dynamics in hydraulically connected floodplains.
- Sites split between Old Mollee and Yarral East, at distances of 50/140/320 m and 40/110/290 m from the river, respectively.
- Outputs cover vertical profiles from the surface to 10 m depth, across 944 grid points, with values provided to seven decimal places.

## Data and modeling approach
- Model: HaughFlow (Evans et al., 2018) using 1D vertical Richards equation (vadose zone) and 1D lateral Boussinesq equation (phreatic zone); two-way coupling allows water exchange between zones.
- Implementation: Fortran90 with a tri-diagonal solver and predictor-corrector time stepping; centered finite differences for space.
- Inputs: river stage levels, climate parameters, and soil properties to determine lateral/vertical inputs and flow speed.
- Outputs: time series of soil-water profiles at chosen distances and depths; stored as unformatted files and converted to formatted CSVs for usability.
- Data products: daily saturation values at each depth, enabling trend detection and cross-site comparisons.

## Data description and structure
- Depth convention: depth measured from the soil surface; output depths implied by the first row of data; units are metres.
- Saturation convention: fraction of pore space saturated (0 to 1), recorded with seven decimal precision.
- Time frame:
  - Old Mollee: Figure 6 datasets run 01 July 2011 – 30 June 2015.
  - Yarral East: Figure 6 datasets run 01 Jan 2013 – 30 June 2015.
  - Old Mollee Figure 7 dataset uses alternative climate inputs, running 01 Jan 2004 – 31 Dec 2016.
- File naming: metadata maps to figures in Evans et al. (2018) (Figure 6a–f; Figure 7b).
- Site coordinates and elevation (relative to Australian Height Datum) provided for each location.

## Site details
- Old Mollee: distances 50 m, 140 m, 320 m; coordinates around -30.254 to -30.254 latitude, 149.681 to 149.684 longitude.
- Yarral East: distances 40 m, 110 m, 290 m; coordinates around -30.237 to -30.234 latitude, 149.671 longitude.
- Elevations provided in metres above datum (e.g., ~202–204 m).

## Calibration and validation
- Calibration against water table levels at Yarral East 290 m for 2013.
- Derived soil properties: saturated hydraulic conductivity ≈ 5.756 m/day; drainage ≈ 0.01568 m/day.

## Metadata and usage notes
- Depth grid: 944 points spanning 0–10 m depth at half-grid intervals.
- Data are model outputs; suitable for assessing vertical moisture dynamics, comparing saturation across distances, and informing hydrological analyses of floodplain systems.
- Data prepared to support self-serve exploration, with formatted outputs to ease use in dashboards, charts, and reports.
- Reference for methodology and broader study: Evans, C.M.; Dritschel, D.G.; and Singer, M.B. (2018), Water Resources Research; PhD-funded study by NERC and National Trust.