# Concentration Based Estimated Deposition (CBED)

## Overview
- Produces 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations across the UK.
- Uses site measurements from the UKEAP network, interpolated to UK concentration maps; combines gas/PM deposition with habitat-specific deposition velocities to produce deposition by land cover (forest, moorland, arable, urban, grassland).

## Deposition components and data sources
- Dry deposition: combines gas and particulate matter deposition with habitat-specific deposition velocities; distributed across 5 land cover categories and aggregated to grid squares.
  - Gas/PM deposition includes SO2, NO2/NO3, HNO3, NH3, and sulphate, nitrate, ammonium, calcium, magnesium.
- Wet deposition: derived from precipitation data and direct deposition to vegetation (occult deposition); includes sulphate, ammonium, nitrate, calcium, magnesium, and hydrogen ion.
- Anthropogenic vs total separation: for sulphur and calcium, separation uses sea-salt ratios.
- Spatial interpolation and modelling inputs:
  - Oxidised nitrogen: NO2/NO3 concentrations via interpolation from rural measurements plus PCM model for NO2.
  - Ammonia: combination of FRAME model and UKEAP measurements.
  - Wet deposition includes orographic enhancement for upland regions (seeder-feeder effect).

## Temporal structure
- Calculations are annual but provided as rolling 3-year means to smooth inter-annual variability.
- Outputs are ecosystem-specific and grid-averaged, with two primary ecosystem assumptions.

## Ecosystem and data outputs
- Two ecosystem-specific value sets:
  - Moorland/short vegetation everywhere
  - Forest everywhere
- Grid-average values also provided as 3-year rolling means.
- Outputs are provided for deposition in keq ha⁻¹ year⁻¹ and can be converted to kg S ha⁻¹ year⁻¹ or kg N ha⁻¹ year⁻¹ using provided factors.

## Data structure and GIS-focused format
- 3-year mean, 5x5 km UK grid, with three ecosystem contexts:
  - Forest/woodland (f)
  - Moorland (m)
  - Grid average (ga)
- Fields (examples):
  - easting, northing (metres) for each grid square center
  - nox_f, nhx_f, nms_f, nm_ca_mg_f (forest deposition; keq ha⁻¹ year⁻¹)
  - nox_m, nhx_m, nms_m, nm_ca_mg_m (moorland deposition; keq ha⁻¹ year⁻¹)
  - nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga (grid-average deposition; keq ha⁻¹ year⁻¹)

## Quality control and validation
- Methods aligned with Government QA practices; extensive peer review and participation in Defra model inter-comparison.
- Mass balance checks and version control; results widely published in peer-reviewed literature.
- Method developments reviewed by senior responsible officers.

## Practical notes for GIS use
- Output is map-ready for GIS: 5x5 km gridded deposition surfaces across the UK, with clear forest vs moorland vs grid-average contexts.
- Useful for policy analysis, ecological impact assessments, and critical load exceedance studies.
- Data are expressed in keq ha⁻¹ year⁻¹, with straightforward unit conversions to kg S or N per hectare per year as needed.