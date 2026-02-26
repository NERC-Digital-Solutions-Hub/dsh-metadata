# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Ammonia enhancement experiment conducted in 2021–2022 at Glencorse woodland near Edinburgh to study NH3 effects on vegetation, bryophytes, lichens, and soil.
- Aimed to optimize NH3 release rates and understand lateral and vertical plume movement within the canopy.
- Data collected include high-temporal-resolution NH3 concentrations downwind of the release system, with accompanying wind and inlet measurements.
- Dataset comprises 97,378 measurements across 6 parameters, available as a CSV.

## Study site and experimental setup
- Location: Glencorse woodland, near Edinburgh, UK (coordinates 55.8539°, -3.2151°, altitude 200 m).
- NH3 release system: three 20 m long, 110 mm diameter PVC tubes mounted horizontally at ground clearance heights of 0.5, 1.35, and 2.2 m.
- Release mechanism: NH3 delivered from a stainless steel manifold through a 6.35 mm pipe, using a mass flow controller and solenoid valve; release activated only when wind direction is between 275–345 degrees and wind speeds are within 0.3–10 m/s.
- Sampling downwind: Picarro NH3/H2O analyser located ~10 m downwind of the release system, housed in a temperature-controlled enclosure.

## Measurements and sampling
- Analyser height and sampling: air sampled at four heights above ground (0.5, 1.0, 1.5, and 2.5 m) using a custom sampling system.
- Temporal resolution: NH3 concentrations recorded at 10 Hz; data averaged to 0.016 Hz intervals.
- Inlet and environmental measurements: below-canopy wind speed and direction recorded; inlet conditions and NH3 release status logged.
- Sampling system details: PTFE tubing (25 mm total length) with controlled inlet temperature (~40°C) and purge/flow rates configured to minimise response delays; some lag remains due to adsorption/desorption effects on inlet surfaces.

## Data structure and access
- Data volume: 97,378 measurements across 6 parameters.
- File format: CSV with multiple timestamped fields:
  - Timestamp and related identifiers
  - NH3_status (valve status)
  - NH3_flow (through MFC to manifold)
  - Wind_speed (below-canopy)
  - Wind_direction (below-canopy)
  - NH3_conc (NH3 concentration downwind; ideally one of the instrument readings)
  - Inlet_height (height of the NH3 concentration measurement)
- Instruments referenced: NH3_status (valve), NH3_flow (MFC), NH3_conc (Picarro and NH3/H2O analyser variants), Wind_speed (WXT536 and Vaisala), Wind_direction (WXT536 and Vaisala), Inlet_height (G2123 and Picarro).

## Quality control and limitations
- Quality checks: visual inspection; removal of data affected by instrument malfunction, datalogger issues, or power outages.
- Gap handling: missing values during valve switching filled by linear interpolation.
- Uncertainties: potential lag due to switching between high and low NH3 concentrations; heating could volatilise NH4NO3, contributing a relatively constant background; residual adsorption/desorption effects at inlet lines.

## Spatial and temporal context for GIS applications
- Temporal scale: multi-year campaign periods spanning 2021 and 2022 with multiple sampling blocks (notable dates in September–November 2021 and August–September 2022).
- Spatial context: downwind plume data relative to a controlled release point, with vertical sampling at four heights enabling three-dimensional plume interpretation near the canopy.
- GIS relevance: suitable for mapping NH3 concentration fields, vertical stratification, and wind-driven plume dispersion; integrates with wind fields to model dispersion and deposition patterns; can be combined with other environmental layers to assess ecosystem exposure.

## Data usage and potential applications
- Primary use: mapping and analysing NH3 plume dynamics and concentration distributions around forest ecosystems.
- Possible analyses: correlate NH3 concentrations with wind speed/direction, examine vertical concentration gradients, assess plume spread from multi-height sampling, integrate with vegetation response data.
- Data preparation steps for GIS:
  - Align timestamp formats, convert to spatial coordinates for plume mapping if location data for sampling points are inferred.
  - Merge wind and concentration records, handle any residual temporal misalignment.
  - Consider interpolation or rasterisation for plume surface visualization, accounting for vertical layers.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024; doi:10.1016/j.atmosenv.2023.120325.