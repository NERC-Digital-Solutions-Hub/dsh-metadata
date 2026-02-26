# Dune_migration_rates.csv

- Overview
  - This file contains dune migration rates, water depths and velocities measured at cross-sections on the South Saskatchewan River, Canada in 2017.

- Data content and structure
  - Six columns:
    - Cross-section number
    - Measurement location UTM Easting (m)
    - Measurement location UTM Northing (m)
    - Dune migration rate (m per hour)
    - Depth-averaged velocity magnitude (m per second)
    - Water depth (m)

- Collection time and purpose
  - Data were collected on 12 June 2017 to provide information on spatial patterns of dune migration rates and associated flow characteristics at the same locations.

- Methods and processing
  - Dune migration rates
    - Measured using repeat aerial imagery with flight lines on a grid pattern, 80% lateral and longitudinal overlap.
    - Orthomosaics constructed from images using the SfM program Pix4D.
    - Multiple flights conducted at 1-hour intervals (max five epochs in a day) to track bedforms.
    - Image Ground Sampling Distance (GSD) typically 0.025–0.03 m.
    - Bedform crests digitised in individual images; average dune migration rates calculated from the mean migration distance between image pairs divided by time between image collection.
  - Water depth and velocity
    - Collected with a Sontek M9 acoustic Doppler current profiler (aDcp) mounted on a small zodiac boat.
    - Position recorded with RTK dGPS; velocities corrected for boat speed and heading.
    - aDcp data in pulse coherent mode; averaged to 1 Hz to improve signal-to-noise.
    - Instrument specs: 9 transducers, 0.5–3.0 MHz.
    - Data collected along cross-sections across the river, extending between banks and oriented approximately perpendicular to downstream flow.

- Provenance and authors
  - Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.

- Metadata and standards
  - Discovery metadata and contextual metadata are provided for the file Dune_migration_rates.csv.
  - Data encoded as a CSV with clearly defined column headers and units.

- Quality, limitations, and considerations
  - Data rely on multiple data collection methods (aerial imagery, remote sensing, in-situ ADCP measurements) and precise geolocation (RTK dGPS); ensure consistency in coordinate reference frame and units when integrating with other datasets.
  - Temporal snapshot from a single day; interpretations should consider potential temporal variability beyond the 12 June 2017 measurements.

- Data governance and sharing considerations for Data Stewards
  - Ensure metadata completeness (both discovery and contextual) are captured in the data portal/catalog.
  - Maintain clear provenance: authorship and collection date; preserve method details (Pix4D workflow, ADCP setup) for reproducibility.
  - Confirm data format (CSV) and unit conventions are standardized; document coordinate reference system (UTM) and zone used.
  - Identify any sharing limitations, embargoes, or proprietary considerations and reflect them in data policies.
  - Plan for updates or new releases if additional observations are collected; document versioning and changelog.
  - Upload to and catalogue in relevant data portals, with accompanying methodological notes to support reuse by data users.