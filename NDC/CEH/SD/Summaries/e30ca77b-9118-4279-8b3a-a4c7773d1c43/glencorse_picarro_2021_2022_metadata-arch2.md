# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- A controlled NH3 enhancement experiment conducted in Glencorse woodland (near Edinburgh) to study how elevated ammonia affects forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland, coordinates 55.8539 N, -3.2151 W, altitude 200 m.
- Timeframe: Data collected across 2021 and 2022 (specific sampling campaigns listed in the study).

## Data collection and experimental setup
- NH3 release system design:
  - Three horizontal PVC tubes (20 m long, 110 mm OD) with holes along their length to emit NH3.
  - Release is controlled by a central fan-driven flow and a 6.35 mm stainless steel manifold connected to a cylinder of anhydrous NH3 via a mass flow controller and solenoid valve.
  - NH3 release enabled only when wind direction falls between 275°–345° and wind speeds meet 0.3–10 m/s.
- Monitoring and sampling:
  - NH3 concentration measured downwind ~10 m from the source using a Picarro NH3/H2O analyser housed in a climate-controlled enclosure.
  - Sampling performed at four heights above ground: 0.5, 1, 1.5, and 2.5 m.
  - At each height, sampling lasted 2 minutes via a valve manifold.
  - Inlet lines and sampling hardware kept warm (~40°C) to minimize adsorption/desorption delays and to stabilize measurements; air lines purged between sampling intervals.
  - Data captured at 10 Hz and aggregated to 1-minute intervals.

## Measurement specifics
- Primary measurements:
  - NH3 concentration (ppb) downwind of the release system (from the analyser; instrument source indicated per row).
  - Wind speed and wind direction below the canopy (instrument types include WXT536 and Vaisala variants).
  - Release system status and flow (NH3_status, NH3_flow) reflecting valve state and MFC-controlled delivery.
  - Inlet height at which NH3 concentration was measured.
- Campaign optimization:
  - Two campaign studies aimed to optimize NH3 release rates and to understand horizontal and vertical NH3 plume movement within the canopy after release.

## Data quality and handling
- Quality control:
  - Visual checks to remove obvious instrument malfunctions, programming issues, and power-cut artifacts.
  - Gaps introduced during valve switching are filled by linear interpolation.
- Data caveats:
  - Possible lag due to NH3 adsorption/desorption on inlet surfaces, especially when switching between high and low concentrations.
  - NH4NO3 volatilization under heating may contribute a smooth, relatively constant background signal.
- Timestamping:
  - Data recorded in Greenwich Mean Time (GMT); timestamps are provided at 1-minute resolution.

## Data structure and content
- Dataset size: 97,378 measurements consisting of 6 parameters.
- Format: CSV file with the following columns (descriptions provided in the dataset notes):
  - Timestamp (1-minute intervals)
  - NH3_status (solenoid valve type/status)
  - NH3_flow (mass flow controller setting)
  - Wind_speed (below-canopy wind speed)
  - Wind_direction (below-canopy wind direction)
  - NH3_conc (NH3 concentration in air at the downwind measurement point; instrument source noted)
  - Inlet_height (height above ground where NH3 concentration was measured)
- Additional context:
  - NH3 concentration data were collected at four heights and linked to corresponding wind and release system data for plume characterization.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.