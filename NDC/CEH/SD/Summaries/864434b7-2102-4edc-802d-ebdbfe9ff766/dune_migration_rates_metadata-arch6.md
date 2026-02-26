# Dune_migration_rates.csv

- Overview
  - Data file of dune migration rates, water depths, and velocities measured at cross-sections on the South Saskatchewan River, Canada, collected in 2017 (on 12 June).
  - Six columns: Cross-section number; Measurement location UTM Easting (m); Measurement location UTM Northing (m); Dune migration rate (m per hour); Depth-averaged velocity magnitude (m per second); Water depth (m).

- Data collection and processing
  - Dune migration rates
    - Measured via repeat aerial imagery on a grid pattern with 80% lateral and longitudinal overlap.
    - Several flights at 1-hour intervals (up to five epochs in a day).
    - Orthomosaics created using Pix4D.
    - Ground Sampling Distance typically 0.025–0.03 m.
    - Bedform crests digitised; average migration rates computed from the mean migration distance between image pairs divided by the time between image collection.
  - Water depth and velocity
    - Measured with a Sontek M9 acoustic Doppler current profiler (ADCP) mounted on a small zodiac boat.
    - Position tracked with RTK dGPS; velocities corrected using boat speed and heading.
    - ADCP data collected in pulse coherent mode; averaging 7 pings per second, then averaged to 1 Hz.
    - Instrument has 9 transducers, operating at 0.5–3.0 MHz.
    - Data collected along cross-sections extending across the river, between both banks and perpendicular to downstream flow.

- Context and purpose
  - Designed to provide information on spatial patterns of dune migration rates and related flow characteristics at the same locations.

- Provenance and metadata
  - Discovery metadata: file titled Dune_migration_rates.csv; authors include Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
  - Data from 2017; cross-sections with UTM coordinates; measurements include dune migration, depth-averaged velocity, and water depth.

- Data quality and usage notes
  - Rich methodological documentation supports understanding and reuse.
  - Users should note the single-date snapshot (12 June 2017) and ensure proper alignment between imagery-derived dune rates and ADCP measurements; keep in mind units and UTM coordinates.

- Potential data products and reuse
  - Supports spatial analysis of dune migration alongside flow characteristics.
  - Suitable for dashboards, maps, pivot tables, and other self-serve exploration tools.
  - Can be integrated with additional geomorphology or hydrology datasets for broader analyses.