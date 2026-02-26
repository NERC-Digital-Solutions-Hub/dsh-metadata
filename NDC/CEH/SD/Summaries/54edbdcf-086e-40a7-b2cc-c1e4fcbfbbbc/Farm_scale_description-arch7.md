Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview
- Describes a high-precision study of N2O fluxes and soil properties at Easter Bush Farm Estate (Central Scotland) conducted between autumn 2012 and summer 2013.
- Data cover more than 500 flux measurements across 20 fields, with 457 accompanying soil measurements at flux collar locations.
- Data are organized for GIS-style analysis with spatial coordinates (BNG GPS easting/northing) and rich soil and management descriptors.

## Experimental design
- Site: Easter Bush Farm Estate near Penicuik, Midlothian, UK; run by SRUC and University of Edinburgh.
- Measurement approach: dynamic closed chamber system with a quantum cascade laser gas analyser mounted in a vehicle, enabling mobile measurements.
- Chamber: circular, 39 cm diameter; placed on soil collars inserted 5 cm deep; fluxes measured over a 3-minute period.
- Radius of operation: measurements conducted within a 30 m radius from the vehicle.
- Sampling: four seasonal measurement periods across autumn 2012 to summer 2013.
- Fields: 20 selected fields representing a range of management practices; included arable fodder crops and grazing pastures.

## Data collected
- Flux measurements: N2O fluxes (µg N2O-N m^-2 h^-1) and associated uncertainties (Flux_Error).
- Soil measurements (457 locations): pH; available N (NH4+ and NO3- in g N kg^-1); soil temperature (°C); soil moisture indicators (WFPS, bulk density, porosity, VWC).
- Bulk density and soil moisture: measurements used to derive WFPS and related soil properties.
- Field metadata: Date, Period (season/year), Measurement_ID, Field, Plot type, Plot Description, GPS_E, GPS_N.
- Data file: Farm_Flux_and_Soil with 21 variables describing measurement context, location, soil properties, and flux results.

## Data structure and units
- Key fields (examples):
  - Date: dd/mm/yyyy
  - Period: season and year
  - Measurement_ID: unique id
  - Field, Plot type, Plot Description
  - GPS_E, GPS_N: British National Grid coordinates
  - Soil_T: soil temperature (°C)
  - SMAv: water-filled pore space (WFPS, %)
  - BD_density: bulk density (g cm^-3)
  - BD_Porosity, BD_VWC, BD_WFPS: soil porosity, volumetric water content, and WFPS (dimensionless/%)
  - pH: soil pH
  - NH4N, NO3N: ammonium and nitrate content (g N kg^-1)
  - Tot_C, Tot_N: total carbon and nitrogen (g C or N kg^-1)
  - Flux: N2O flux (µg N2O-N m^-2 h^-1)
  - Flux_Error: 95% CI for flux
- Units are provided for each variable, enabling direct GIS integration and cross-dataset comparisons.

## Data processing and quality control
- Flux calculation: performed with the HMR package in R, which selects among five methods to estimate fluxes from chamber data.
- Quality checks: chamber CO2 response used to detect leaks; data with unstable signals were discarded.
- Data characteristics: due to log-normality and multiple sources, flux and soil variable outliers were retained (no a priori removal of outliers).
- Data interpretation references provided for methods and uncertainty assessment.

## GIS and mapping implications
- Spatially explicit dataset: precise GPS coordinates (BNG) enable mapping of N2O flux hotspots and spatial patterns across fields.
- Rich attribute data: integrates soil chemistry, physical properties, and land management context, supporting correlation analyses and spatial modeling.
- Potential applications: hotspot identification, field-scale emission assessments, and exploring relationships between fluxes and soil properties or management practices.

## Limitations and considerations
- Temporal scope: four seasonal periods within 2012–2013; spatial coverage limited to 20 fields at a single estate.
- Soil sampling: 457 soil measurements out of >500 flux measurements; not all flux points have soil data.
- Storage/analysis timeline: soils frozen soon after sampling and analyzed within two months.
- Data structure is designed for integration with GIS workflows but requires careful handling of units and coordinate reference (BNG).

## References
- Cowan et al. (2014, 2015, 2017) on flux measurement methodology, spatial variability, and hotspot analysis.
- Levy et al. (2011) and Pedersen et al. (2010) on uncertainty quantification and flux estimation methods.
- Rowell (1994) on soil measurement methods.