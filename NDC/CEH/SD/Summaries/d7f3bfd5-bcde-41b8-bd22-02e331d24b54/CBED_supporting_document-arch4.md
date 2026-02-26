# Concentration Based Estimated Deposition (CBED)

## Overview
- Produces 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Uses measured concentrations of gases/particulate matter in air and ions in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs are annual values provided as rolling 3-year means, designed to assess critical load exceedances with ecosystem-specific assumptions.

## Data inputs and sources
- Site-based measurements from the UKEAP network.
- An annual precipitation map from the UK Meteorological Office.
- Gas and particulate matter concentration maps; habitat-specific deposition velocities.
- For oxidised nitrogen dry deposition: interpolation of rural sites plus PCM model data for NO2; nitric acid from interpolation; ammonia from FRAME model and UKEAP measurements.
- Wet deposition components include direct cloud droplet deposition (occult) and precipitation deposition; separation of anthropogenic vs total components via sea-salt ion ratios.
- Orographic enhancement factors based on upland precipitation observations (e.g., Great Dun Fell, Holme Moss).

## Methodology (processing steps)
- Interpolate site measurements to generate UK-wide concentration maps.
- Combine gas/PM concentration maps with deposition velocities to estimate dry deposition for five land cover categories: forest, moorland, grassland, arable, urban.
- Weight deposition by the proportion of land cover types within each 5x5 km grid to produce grid-square deposition values.
- For critical loads, apply deposition values of moorland to non-woodland habitats and forest values to woodland habitats.
- Wet deposition accounts for deposition from precipitation and occult deposition to vegetation; separate components using ion ratios relative to sea water.
- Include an orographic enhancement factor for upland precipitation to refine wet deposition estimates.
- Averaging: deposition values can vary inter-annually; CBED uses a 3-year mean to smooth fluctuations.
- Outputs are provided as rolling 3-year means; ecosystem-specific options include:
  - Moorland/short vegetation everywhere
  - Forest/woodland everywhere
  - Grid-average values

## Outputs and data structure
- Data are calculated annually but delivered as rolling 3-year means.
- Units: deposition values expressed as keq ha⁻¹ year⁻¹; convertible to kg of S, N, or Ca/ha/year via specified multipliers:
  - Oxidised/reduced nitrogen deposition: keq ha⁻¹ year⁻¹ × 14 = kg N ha⁻¹ year⁻¹
  - Sulphur deposition: keq ha⁻¹ year⁻¹ × 16 = kg S ha⁻¹ year⁻¹
  - Base cation deposition (Ca+Mg): keq ha⁻¹ year⁻¹ × 20 = kg Ca ha⁻¹ year⁻¹
- Dataset fields (examples):
  - Forest deposition: nox_f (oxidised nitrogen), nhx_f (reduced nitrogen), nms_f (non-marine sulphur), nm_ca_mg_f (non-marine base cations)
  - Moorland deposition: nox_m, nhx_m, nms_m, nm_ca_mg_m
  - Grid-average deposition: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga
  - Spatial identifiers: easting, northing (centre of 5x5 km grid squares)

## Quality control and governance
- CBED methods align with government QA practices and have undergone extensive peer review and inter-comparison (e.g., Defra model inter-comparison with Carslaw 2011).
- Documentation, version control, and central code storage procedures are followed.
- Mass balance checks are routinely performed and results are compared to previous years.
- Deposition estimates have been published in peer-reviewed literature and overseen by senior responsible officers.

## Practical considerations for Data Leaders
- Data system view: CBED provides a comprehensive, model-based deposition dataset that integrates multiple data streams (air concentrations, precipitation, land cover, deposition velocities).
- Data availability and discoverability: Data are associated with Defra/UK-air resources and CEH hosted information; interoperability with other pollutant datasets is supported by standardized units and documented fields.
- User needs and iteration: The 3-year rolling means smooth inter-annual variability, offering stable inputs for policy assessment and regulatory analyses.
- Data gaps and coordination: The approach combines site measurements with modelling to address data gaps (e.g., urban and woodland deposition estimates) but relies on multiple models and sources that require coordination across networks and institutions.
- Metadata and documentation: Clear field definitions, units, and conversion factors are provided to support discoverability and correct use across analyses.

## Resource references
- Pollutant deposition information: http://www.pollutantdeposition.ceh.ac.uk/ukeap
- UK Air Defra network information: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap