# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

- Purpose and scope
  - Provides modeled daily water saturation profiles for six sites near the Namoi River to support understanding of subsurface hydrology in floodplain environments.
  - Water saturation is presented as a proportion of pore space (0 to 1) with high precision (7 decimals) across depths up to 10 m.

- Data description
  - Six sites across two locations: Old Mollee (50 m, 140 m, 320 m) and Yarral East (40 m, 110 m, 290 m) from the river.
  - Vertical profiles span from the soil surface to 10 m depth.
  - Time series provided daily; depth measured from the surface.
  - Outputs are stored as modeled time series with 944 grid points across 10 m depth at half-grid intervals (as per Evans et al., 2018).

- Sites, coordinates, and frame
  - Old Mollee: 50 m (-30.254, 149.681, 202.25 m AHD), 140 m (-30.254, 149.682, 204.37 m AHD), 320 m (-30.254, 149.684, 203.82 m AHD).
  - Yarral East: 40 m (-30.237, 149.671, 202.98 m AHD), 110 m (-30.236, 149.671, 202.84 m AHD), 290 m (-30.234, 149.671, 202.02 m AHD).
  - Dataset relates to figures from Evans et al. (2018) and includes different time frames per site and figure.

- Model and methodology
  - Generated with the HaughFlow model (Evans et al., 2018) to predict water movement in vadose and phreatic zones of hydraulically connected floodplains.
  - Governing equations: 1D vertical Richards equation for vertical moisture transport; 1D lateral Boussinesq equation for lateral saturated flow; coupled bidirectionally between vadose and phreatic zones.
  - Implementation: Fortran90 with tri-diagonal solver, predictor-corrector temporal discretisation, and centered finite differences spatially.
  - Inputs: river stage levels, climate parameters, and soil properties to determine lateral and vertical inputs and flow speed.

- Outputs and format
  - Daily outputs of water saturation versus depth for each site and depth grid; formatted for ease of use (original outputs in unformatted files, converted to formatted CSV equivalents named Figure6a_..., Figure7b_...).
  - Depth scale: 0 to 10 m; grid points reflect half-grid spacing within the domain.

- Calibration and validation
  - Calibrated against water table levels at Yarral East 290 m for the year 2013.
  - Calibrated soil properties: saturated hydraulic conductivity = 5.756 m/day; drainage = 0.01568 m/day.

- Time frame
  - Old Mollee Figure 6 datasets: 01 July 2011 to 30 June 2015.
  - Yarral East Figure 6 datasets: 01 January 2013 to 30 June 2015.
  - Old Mollee Figure 7 dataset (alternative climate inputs): 01 January 2004 to 31 December 2016.

- Data context and usage
  - Data describe modeled subsurface hydrology suitable for monitoring environmental conditions and informing policy performance related to floodplain hydrology.
  - The dataset accompanies Evans, C.M., Dritschel, D.G., and Singer, M.B. (2018) on modelling subsurface hydrology in floodplains and supports related PhD work funded by NERC and the National Trust.

- Access and stewardship considerations
  - Outputs are standardized, clearly annotated, and linked to specific site locations and time periods, supporting reproducibility and comparison across sites.
  - Reflects a data-management approach aligned with enabling broader access to underlying model inputs and outputs for monitoring and policy analysis.