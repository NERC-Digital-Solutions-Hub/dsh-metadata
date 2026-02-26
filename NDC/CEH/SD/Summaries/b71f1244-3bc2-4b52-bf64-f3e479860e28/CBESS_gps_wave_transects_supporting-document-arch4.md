# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

## Overview
- Dataset provides GPS locations for sensors and features used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Includes basic description of measurements: surface elevation relative to a rod SET instrument and depths of sediment deposited above feldspar marker horizons adjacent to the SET benchmark.
- Staff responsible: Tom Spencer, Ben Evans.

## Location and Site Information
- Observational sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitat types: Saltmarsh and Mudflat.
- Site descriptions emphasize contrasting sediment types (clay in Essex vs sandy in Morecambe Bay) and differing inundation frequency, creek structure, and vegetation.
- GPS coordinates and benchmark locations are provided with accuracy better than 50 mm in OSGB1936 coordinates.
- Associated dataset containing GPS locations of benchmarks and marker horizons: CBESS_gps_wave_transects.

## Methods and Instrumentation
- Instruments used: Rod Surface Elevation Table (SET) with receivers mounted to driven benchmark rods.
- Installation began autumn 2012; SET methodology follows USGS standards to enable intercomparison across global networks.
- Benchmark rods driven deep into substrate; instrument arms and top of rods sealed in plastic ducts for stability.
- Marker horizons: 50 cm × 50 cm feldspar horizons installed just beyond instrument reach to measure sediment deposition above horizons.
- Measurement cadence: approximately every 3–6 months during a 1-year monitoring period; observations repeated at nine pins per SET quadrant.

## Data Collected and Structure
- Variables/Parameters:
  - Heights at Pins 1–9; horizon depths for Cores 1–3; SET-related readings.
- Data recording and notes:
  - Notes on significant factors affecting results captured in spreadsheets.
  - Horizon data may be transcribed as 0 mm if less than 1 mm of sediment is present; 'NA' indicates horizon not detectable in multiple cores.
- Data format and field structure:
  - Data stored in Excel spreadsheets.
  - Dataset fields include: Season, Location, Site, Habitat, Quadrat, Scale, Record, Date, Time, SET Number, Pin readings, Marker horizon depths, and Notes.
- GPS and site coordinates:
  - Detailed SET benchmark coordinates (E/N) and elevations provided for all sites.
  - Associated GPS dataset: CBESS_gps_wave_transects.

## Data Quality, Calibration, and Access
- Location accuracy: better than 50 mm in all directions (OSGB1936).
- Calibration: Leica RTK corrections in real-time where applicable.
- Data quality notes: NA values indicate non-performed measurements; some fields may be missing or not applicable.
- Data products: primary data in Excel spreadsheets; field descriptions and metadata provided within dataset structure.
- Access considerations: data may be used for inter-site comparisons and integration with broader CBESS and global SET datasets.

## References and Documentation
- Foundational methodology: Cahoon et al. (2002) on High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table.
- Data notes indicate the CAD/field procedures and calibration context to support data reuse and interoperability.