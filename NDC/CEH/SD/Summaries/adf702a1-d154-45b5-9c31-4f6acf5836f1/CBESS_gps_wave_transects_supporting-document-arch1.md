# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- Dataset provides global positioning system (GPS) locations for instruments and features tied to wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Measurements include surface elevation relative to an rSET instrument and depths of sediment deposited above feldspar marker horizons near the rSET benchmark.
- Data are organized with detailed metadata and are intended for inter-comparability with other CBESS sites.

## Study sites and habitats
- Essex sites representing clay soils within saltmarsh and adjacent mudflat areas:
  - Abbotts Hall (AH)
  - Fingringhoe Wick (FW)
  - Tillingham Marshes (TM)
- Morecambe Bay sites representing sandy soils:
  - Cartmel Sands (CS)
  - Warton Sands (WS)
  - West Plain (WP)
- Habitat types included: Saltmarsh (SM) and Mudflat (MF); differing inundation frequency, creek structure, and vegetation between Essex and Morecambe Bay.

## Monitoring design and timeline
- Monitoring stations installed in autumn 2012.
- Rod Surface Elevation Table (SET) used for standardized, inter-comparable measurements.
- Measurements taken approximately every 3–6 months, totaling two observations over a one-year monitoring period.
- GPS coordinates for SET benchmarks and marker horizons accompany the dataset.

## Measurements and data collection
- Height measurements at nine pins (Pin 1–Pin 9) around each SET benchmark.
- Marker horizons: 50 cm × 50 cm potash feldspar horizons installed just beyond arm reach in each quadrant; sediment depth above horizons measured via cores (Core 1–Core 3).
- Recording notes include potentially significant factors affecting results; NA indicates non-recorded or non-detectable readings.
- Data handling details:
  - If a horizon is not horizontal, mean depth taken from three sides of the core.
  - Cores with less than 1 mm of sediment above the horizon recorded as 0 mm.
  - NA values indicate measurements were not performed.

## Instrumentation and localization
- SET methodology follows Rod Surface Elevation Table principles for high-precision wetland elevation measurements.
- SET installations involved driving benchmark rods 6–12 meters into the substrate; receivers mounted and top of rod cemented into protective casings.
- GNSS coordinates (Leica GS08) provided with accuracy better than 50 mm in all directions.
- Reference framework and procedures align with Cahoon et al. 2002 for high-precision wetland sediment elevation measurements.
- Real-time Leica RTK corrections used for calibration where applicable.

## Data structure and formats
- Dataset titled: CBESS_gps_wave_transects (GPS locations for wave transects and SET markers).
- Observations and metadata stored in Excel spreadsheets.
- Dataset fields include:
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat (1–22)
  - Scale (A: 1 m, B: 1–10 m, C: 10–100 m, D: 100–upper limit)
  - Record (data entry sequence for analysis)
  - Date (DD.MM.YYYY) and Time (HH:MM:SS)
  - SET Number (increases landward)
  - Pin readings (Pin 1–Pin 9)
  - Marker horizon depths (Core 1–Core 3)
  - Notes/comments on readings
- All GPS coordinates for SET benchmarks and marker horizons are included within the associated dataset CBESS_gps_wave_transects.

## Provenance, references, and quality
- Data collection and naming reference Cahoon, D. R. et al. (2002) for high-precision measurements of wetland sediment elevation using SET.
- Calibration procedures include real-time Leica RTK corrections.
- Data quality notes:
  - Coordinates provided with OSGB1936 reference frame; accuracy better than 50 mm.
  - Data entries and field descriptions are designed to support subsequent analyses, including potential cross-site comparisons within the CBESS network.

## Notes and data usability
- NA values indicate non-recorded measurements or undetected horizons.
- The dataset is designed to support analyses of sedimentation dynamics, elevation change, and cross-habitat comparisons between clay and sandy soil contexts, across saltmarsh and mudflat environments.
- Access to the CBESS_gps_wave_transects dataset is implied as part of the broader CBESS data portal or accompanying documentation.