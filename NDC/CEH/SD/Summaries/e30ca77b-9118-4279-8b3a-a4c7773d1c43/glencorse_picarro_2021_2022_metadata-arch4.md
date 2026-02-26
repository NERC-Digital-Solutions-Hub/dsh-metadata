# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Describes an ammonia (NH3) enhancement experiment conducted in the Glencorse woodland near Edinburgh (UKCEH), established in 2021 to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
- NH3 release is wind-controlled to target specific downwind monitoring quadrats; data aim to support understanding NH3 plume movement and forest deposition.

## Data collection and experimental setup
- Location: Glencorse woodland (approximate coordinates 55.8539°N, -3.2151°W; altitude ~200 m).
- Release system: three parallel 20 m PVC release tubes at ground proximity (0.5, 1.35, 2.2 m) with NH3 injected via a stainless steel line, mass flow controller, and solenoid valve; NH3 release activated only under specific wind directions (275–345°) and threshold wind speeds (0.3–10 m s^-1).
- Monitoring: NH3 downwind measurements taken 10 m from release point using a Picarro NH3/H2O analyzer, housed in a controlled enclosure.
- Experimental aims: two campaigns to optimize release rates and characterize lateral/vertical NH3 plume behavior within the canopy.

## Measurements and sampling details
- Sampling location and height: four heights above ground (0.5, 1.0, 1.5, 2.5 m) at 10 m downwind; additional monitoring near the source.
- Instrumentation: Picarro NH3/H2O analyzer; supplementary measurements from a separate system for wind speed and direction (below-canopy).
- Sampling protocol: 2-minute samples at each height, automated via LabVIEW; four 5.5 m PTFE sampling lines; sample lines heated to ~40°C to minimize adsorption/desorption delays; purge flow 7 slpm between samples and 12 slpm during sampling.
- Data cadence: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz intervals.
- Data coverage periods: 16–23 Sept 2021; 28 Sept–1 Oct 2021; 6–10 Oct 2021; 3–9 Nov 2021; 10 Aug–27 Sept 2022.

## Data quality, processing, and limitations
- Quality control: visual checks; removal of obvious instrument malfunctions, programming issues, and power failures.
- Data gaps: valve-switching gaps filled by linear interpolation.
- Potential lag/ artefacts: some lag expected due to switching between high/low NH3 concentrations and adsorption/desorption on inlet surfaces; heating can volatilize ammonium nitrate aerosol, though background NH4NO3 is expected to be smooth.
- Metadata notes: dataset includes instrument and hardware identifiers, enabling traceability and reproducibility.

## Data structure and content
- Size: 97,378 measurements across 6 parameters.
- Format: CSV with the following fields:
  - Timestamp (one-minute resolution, GMT)
  - NH3_status (valve/valve state details)
  - NH3_flow (flow through the release manifold)
  - Wind_speed (below-canopy wind speed)
  - Wind_direction (below-canopy wind direction)
  - NH3_conc (NH3 concentration downwind)
  - Inlet_height (height of NH3 concentration measurement)
- Each parameter includes instrument/source metadata (e.g., NH3_status from Type 6027 valve, NH3_flow from MFC, Wind_speed from WXT536, etc.).

## Temporal coverage and provenance
- Data window spans multiple campaigns in 2021 and a period in 2022 (as listed above).
- Funding: UKRI GCRF South Asian Nitrogen Hub supported establishing the facility.
- Key reference: Deshpande AG et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024. DOI: 10.1016/j.atmosenv.2023.120325.

## Implications for data management and use
- Rich, multi-parameter dataset suitable for analysis of NH3 dispersion, canopy interactions, and deposition estimates.
- Usability aided by clear naming of columns, source instruments, and fixed sampling protocol; potential for integration with other environmental datasets.
- Highlights the importance of documenting sampling geometry, instrument calibrations, and data cleaning steps to ensure reproducibility and discoverability within broader data ecosystems.