# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

## Purpose and scope
- Study of the effects of high atmospheric NH3 on forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland, near Edinburgh (55.8539°, -3.2151°, altitude 200 m).
- Timeframe: 2023-01-01 to 2024-12-31 (GMT).
- Dataset extends the 2021-22 data from the same site.

## Experimental design and data collection
- Ammonia release is wind-controlled: NH3 is released only when wind direction is 275–345° toward monitoring quadrats at threshold speeds (0.3–10 m s⁻¹).
- Release system: three 20 m long tubes (110 mm OD) at heights 0.5, 1.35, and 2.2 m; six 4 mm holes along each tube.
- Gas delivery: pure NH3 from a cylinder through a mass flow controller (MFC) and solenoid valve into a central manifold; release occurs only with correct wind conditions.
- Monitoring: wind data from a WXT536 weather station; NH3 release volume recorded by the MFC every 20 seconds; 15-minute interval averages used for analyses.
- Data period: 2023-01-01 to 2024-12-31; 68,396 measurements of 5 parameters; stored as CSV with 15-minute timestamps.

## Data structure and key fields
- Timestamp: 15-minute GMT timestamps.
- NH3_status: duration (minutes) NH3 is released; related to solenoid valve (Type 6027, Bürkert).
- NH3_flow_set: NH3 flow set point (slpm) for the prevalent wind conditions.
- NH3_flow: NH3 flow through the MFC into the release manifold (slpm).
- Wind_speed: below-canopy wind speed (ms⁻¹) from WXT536 (Vaisala).
- Wind_direction: below-canopy wind direction (degrees).

## Quality control and limitations
- Data visually checked; obvious instrument malfunctions, datalogger issues, and power-cut artifacts removed.
- Some gaps present due to replacement of faulty gas control components.

## Location context and data lineage
- Site: Glencorse woodland near Edinburgh; altitude 200 m.
- This dataset is an extension of the 2021-22 site dataset.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Related publications:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Glencorse, UK, 2021-2022.