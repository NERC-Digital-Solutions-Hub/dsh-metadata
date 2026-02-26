# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Overview
- A study of ammonia (NH3) enhancement effects on forest vegetation, bryophytes, lichens, and soil at Queensberry Estate, central Sri Lanka.
- Data collected from 1 Jan 2023 to 31 Dec 2024; 61,751 measurements across 4 parameters.
- Dataset provided as a CSV with detailed temporal measurements and system status.

## Study site & purpose
- Location: Queensberry Estate, tropical sub-montane forest; coordinates 6.9693° N, 80.5911° E; altitude 1645 m.
- Purpose: Assess impacts of elevated ambient NH3 on local ecosystems using controlled NH3 release modulated by wind conditions.
- NH3 release control: Enabled only when wind direction falls within 5-75° or 185-255° and wind speeds are between 0.3 and 10 m/s.
- Release mechanism: Three parallel 20 m PVC tubes at ground clearance levels 0.5, 1.35, and 2.2 m; NH3 distributed through six holes per tube; powered by a central airflow manifold and a mass flow controller with a solenoid valve.

## Data collection & instrumentation
- Wind and meteorological data: Collected by a WXT536 weather station (Vaisala) monitoring below-canopy wind speed and direction.
- NH3 delivery: Controlled by a Bürkert solenoid valve and a G series MFC (MKS Instruments) injecting NH3 into the release manifold.
- Temporal resolution: NH3 release volume logged every 20 seconds; data averaged over 15-minute intervals.
- Time reference: All data in Sri Lanka Standard Time (SLST).
- Related publications: Complete experimental design, methodology, analyses, and findings are described in Deshpande et al. (2024a); extension of the 2022 dataset described in Deshpande et al. (2024b).

## Data structure & variables
- Dataset size: 61,751 measurements.
- File format: CSV.
- Key columns (examples):
  - Timestamp, Unit = -, Instrument = -, Description = 15-minute timestamps in the format dd/mm/yyyy hh:mm
  - NH3_status, Unit = Minutes, Instrument = Type 6027 solenoid valve, Manufacturer = Bürkert, Description = Amount of time NH3 is released
  - NH3_flow, Unit = slpm, Instrument = G series MFC, Manufacturer = MKS Instruments, Description = NH3 flow through the MFC into the release manifold
  - Wind_speed, Unit = ms^-1, Instrument = WXT536, Manufacturer = Vaisala, Description = Below-canopy wind speed
  - Wind_direction, Unit = o, Instrument = WXT536, Manufacturer = Vaisala, Description = Below-canopy wind direction
- Coverage: Data collected within 2023 and 2024; all timestamps in SLST.
- Dataset lineage: Extension of the 2022 dataset from the same study site.

## Quality control & limitations
- Visual QA applied to identify and remove obvious instrument malfunctions, misconfigurations, and power-related errors.
- Some data gaps present due to the time required to replace faulty gas-control components.
- Data cleaning focused on ensuring consistent 15-minute averaging despite intermittent equipment issues.

## Data access, funding, and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- References:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Queensberry, Sri Lanka, 2022, NERC EDS Environmental Information Data Centre.

## Potential GIS applications
- Spatial-temporal visualization of NH3 release events and corresponding wind-driven dispersion patterns.
- Integration with land cover, vegetation, and soil maps to assess deposition hotspots and ecological responses.
- Map-based dashboards showing NH3 flow, release duration, wind direction, and deposition estimates over time.
- Temporal GIS analyses combining this NH3/meteorological data with other environmental datasets for policy or stakeholder communications.