# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Aim and study design
- Ammonia (NH3) enhancement experiment to study effects on forest vegetation, bryophytes, lichens, and soil.
- Two campaign studies designed to optimize NH3 release rates and to understand lateral and vertical plume movement within the canopy post-release.
- Location: Glencorse woodland (latitude 55.8539, longitude -3.2151), altitude ~200 m, near Edinburgh.

## Experimental setup
- Enhancement system releases NH3 only when wind conditions meet direction (275–345 degrees) and threshold speeds (0.3–10 m s-1).
- Release hardware: three 20 m long PVC tubes (110 mm OD) placed horizontally at ground-related heights 0.5, 1.35, and 2.2 m; six 4 mm holes per tube for release around the circumference.
- NH3 supplied from a cylinder via a 6.35 mm stainless pipe, mass flow controller (MFC), and solenoid valve; positive pressure drives NH3 into the tube airflow for dilution and release.
- Monitoring: Picarro G2123 NH3/H2O analyser located ~10 m downwind; custom enclosure; sampling at four heights (0.5, 1, 1.5, 2.5 m) using a PTFE sampling system; automatic LabVIEW control; temperature ~40°C ±3°C; purge rates 7 to 12 standard L min-1.
- Data capture: NH3 concentrations recorded at 10 Hz, averaged to 0.016 Hz; sampling occurred over multiple dates in 2021 and 2022.

## Data collection and structure
- Data windows (GMT): 16–23 Sept 2021; 28 Sept–1 Oct 2021; 6–10 Oct 2021; 3–9 Nov 2021; 10 Aug–27 Sept 2022.
- Data volume: 97,378 measurements across 6 parameters.
- Data format: CSV with columns including:
  - Timestamp (date/time, minute resolution)
  - NH3_status (valve type, release status)
  - NH3_flow (through MFC into release manifold)
  - Wind_speed (below-canopy)
  - Wind_direction (below-canopy)
  - NH3_conc (NH3 concentration downwind)
  - Inlet_height (height above ground where NH3 concentration measured)
- Instruments referenced: NH3_status (solenoid valve, Bürkert), NH3_flow (MKS Instruments), Wind_speed (WXT536 and Vaisala), Wind_direction (WXT536 and Vaisala), NH3_conc (G2123 and Picarro), Inlet_height (G2123 and Picarro).

## Quality control and data processing
- Visual checks to remove obvious instrument/logger errors and power-cut artefacts.
- Gaps during valve switching filled by linear interpolation.
- Acknowledged lag due to NH3 adsorption/desorption on inlet surfaces and potential volatilisation from heating.
- Some lag expected when switching heights or concentrations; air sampling designed to minimize delays.

## Data usage and interpretation
- Enables estimation of NH3 plume movement and deposition dynamics in a forest canopy context.
- Data intended to support analyses like estimating NH3 deposition to forest ecosystems in Scotland and Sri Lanka (as per related work by Deshpande et al., 2024).
- The dataset is part of a broader study on controlled NH3 enhancement and environmental responses.

## Funding
- UKRI GCRF South Asian Nitrogen Hub funded the establishment of the facility.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.