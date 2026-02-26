# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Produces 5x5 km resolution gridded data of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Derived from measured concentrations of gases, particulate matter in air, and ions in precipitation collected at the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Site measurements are interpolated to map UK concentrations; wet deposition is mapped using annual precipitation; dry deposition combines gas/PM maps with habitat-specific deposition velocities across five land cover types (forest, moorland, grassland, arable, urban).
- Deposition data are used to assess critical load exceedances, applying moorland values to non-woodland habitats and forest values to woodland habitats.
- Wet deposition accounts for occult deposition (direct cloud droplet deposition) and separates anthropogenic from total components using sea-salt references; includes an orographic enhancement factor for upland regions.
- Annual deposition varies with weather and atmospheric transport; CBED results used as rolling 3-year means to smooth inter-annual variation.

## Data Sources and Modelling
- Gas/PM concentration maps: SO2 (urban-enhanced rural baseline), oxidised nitrogen (NO2/NO3) via interpolation and PCM model, NO2 concentrations from PCM data; ammonia (NH3/NH4) from FRAME model and UKEAP measurements.
- Wet deposition: direct precipitation deposition plus occult deposition to vegetation; separation of non-seasalt components using sea-water ion ratios.
- Orographic enhancement: based on observations from Great Dun Fell and Holme Moss.
- Inter-annual variability: weather, precipitation, and atmospheric circulation influence results; deposition values averaged over three years to reduce variability.

## Data Outputs and Units
- Depositions are expressed as keq ha^-1 year^-1 (kiloequivalents per hectare per year).
- Conversion to kilograms per hectare per year:
  - SO4/SO2 (sulfur): keq × 16 = kg S ha^-1 yr^-1
  - Oxidised/reduced nitrogen: keq × 14 = kg N ha^-1 yr^-1
  - Base cations (Ca+Mg): keq × 20 = kg Ca ha^-1 yr^-1
- Ecosystem-specific outputs:
  - Moorland
  - Forest/woodland
  - Grid average
- Data provided as rolling 3-year means; annual values are averaged over the 3-year window.

## Data Structure and Access
- Three 3-year mean CSV files for 2013–2015:
  - CBED-deposition-moorland-2013-2015.csv (ox. and reduced nitrogen, non-marine sulfur, non-marine base cations to moorland)
  - CBED-deposition-forest-2013-2015.csv (deposition to forest categories)
  - CBED-deposition-gridaverage-2013-2015.csv (grid-average deposition)
- Each file contains:
  - easting, northing (centre of 5x5 km grid square)
  - deposition components with descriptive names (e.g., nox_m, nhx_m, nms_m, nm_ca_mg_m for moorland; suffixed variants for forest and grid average)
  - units: keq ha^-1 year^-1
- Documentation and data are linked via UKEAP and UK-AIR Defra network information pages.

## Quality Control and Governance
- Methods align with government QA for analytical models; extensive peer review and participation in Defra model inter-comparison exercises.
- Versioning, central storage of code, and clear documentation of method developments.
- Mass-balance checks and consistency comparisons across years to ensure numerical integrity.
- Data and methodologies are published in peer-reviewed literature and managed by senior responsible officers.

## Relevance for Monitoring Frameworks
- Provides spatially explicit, policy-relevant deposition metrics suitable for monitoring environmental health policies and informing future decisions.
- Rolling 3-year means reduce year-to-year noise while preserving long-term trends.
- Clear data governance and openness enable data sharing, reproducibility, and integration with other monitoring indicators.