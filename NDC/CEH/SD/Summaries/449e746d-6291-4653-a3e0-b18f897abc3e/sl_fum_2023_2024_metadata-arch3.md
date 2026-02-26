# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Purpose and scope
- Investigates the effects of high atmospheric ammonia on forest vegetation, bryophytes, lichens, and soil in a tropical sub-montane forest.
- Location: Queensberry Estate, central Sri Lanka (specific coordinates and altitude provided).
- Study uses a wind-controlled ammonia enhancement system to deliver NH3 to selected monitoring quadrats.
- Data span: 1 January 2023 to 31 December 2024.

## Experimental setup and data collection
- NH3 enhancement system releases ammonia only when wind conditions meet specified directions (5–75° and 185–255°) and threshold speeds (0.3–10 m/s).
- Release hardware: three 20 m long tubes (110 mm OD), arranged parallel at 0.5, 1.35, and 2.2 m above ground; six 4 mm holes per tube for release.
- Gas delivery: pure anhydrous NH3 from a cylinder via a mass flow controller and solenoid valve; release occurs only when wind conditions are satisfied.
- Measurement and monitoring: below-canopy wind data from a WXT536 weather station; NH3 volume released logged by the MFC; wind data recorded concurrently.
- Temporal resolution: NH3 release and flow logged every 20 seconds; aggregated to 15-minute intervals for analysis.
- Time standard: Sri Lanka Standard Time (SLST).

## Data structure and contents
- Dataset size: 61,751 measurements.
- Data format: CSV file with the following columns (descriptions provided in the dataset):
  - Timestamp (SLST), Description fields for 15-minute timestamps.
  - NH3_status: duration of NH3 release (minutes); instrument details (solenoid valve, Bürkert).
  - NH3_flow: NH3 flow through the MFC into the release manifold (slpm); instrument details (G series MFC, MKS Instruments).
  - Wind_speed: below-canopy wind speed (ms^-1); instrument details (WXT536, Vaisala).
  - Wind_direction: below-canopy wind direction (degrees); instrument details (WXT536, Vaisala).
- Data includes metadata for each variable (units, instrument, manufacturer, description).

## Quality control and data integrity
- Data visually checked; obvious instrument malfunctions, datalogger issues, and power cuts removed.
- Some data gaps occurred due to time needed to replace faulty gas control components.
- Data cleaned to remove erroneous records, with gaps acknowledged.

## Data governance and accessibility notes
- Data are provided with explicit metadata for interpretation (units, instruments, and descriptions).
- Complements the wider study on ammonia deposition and related meteorological data from the Queensberry site.
- Complete details of experimental design, methodology, analysis, and findings are available in the referenced publications.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## References
- Deshpande, A. G. et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ., 2024a.
- Deshpande, A. G. et al. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Queensberry, Sri Lanka, 2022, NERC EDS Environmental Information Data Centre, 2024b.