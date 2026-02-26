# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Describes a dataset from an NH3 enhancement experiment in the Glencorse woodland near Edinburgh, 2021–2022.
- Purpose: study effects of elevated ammonia on forest vegetation, bryophytes, lichens, and soil; analyze lateral and vertical plume movement after release.
- Data produced include high-resolution NH3 concentrations and supporting environmental measurements.

## Data collection and experimental design
- NH3 release system: three 20 m PVC tubes at 0.5, 1.35, and 2.2 m; NH3 fed from a cylinder through a mass flow controller and solenoid valve, injected into a center-mounted fan to dilute and release NH3 through the tubes.
- Release conditions: NH3 released only when wind direction is 275–345 degrees and wind speeds are 0.3–10 m/s (below-canopy).
- Monitoring: Picarro NH3/H2O analyzer located 10 m downwind; sampling at four heights (0.5, 1.0, 1.5, 2.5 m).
- Sampling protocol: 2-minute sampling per height via a valve manifold controlled by LabVIEW; inlet lines heated and purged to minimize response delays; some lag expected due to NH3 adsorption/desorption on surfaces.
- Data capture: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz intervals; data from multiple campaigns in late 2021 and 2022.

## Data structure and contents
- Dataset size: 97,378 measurements across 6 parameters.
- Format: CSV with columns including:
  - Timestamp (minute-precision), instrument and manufacturer identifiers, status of NH3 release (ON/OFF), NH3 flow (through MFC), below-canopy wind speed and direction, NH3 concentration (downwind), and inlet height.
- Metadata: detailed descriptions and units for each column, enabling traceability to equipment and measurement conditions.

## Quality control and data processing
- Visual quality checks performed; obviously erroneous data from instrument issues, datalogger problems, or power cuts removed.
- Gaps from valve switching interpolated linearly.
- Acknowledges potential lag between NH3 release dynamics and measured concentrations, especially when switching between high and low concentrations.

## Data interpretation considerations
- Lag effects due to adsorption/desorption on inlet surfaces and measurement systems; heating can volatilize NH4NO3, contributing to a relatively smooth background.
- Concentration dynamics are influenced by release timing, wind conditions, and plume dispersion within the canopy.

## Accessibility and usage
- Data provided as a CSV with GMT timestamps and comprehensive instrument metadata, facilitating independent reanalysis and integration with other site data.
- Suitable for analyses of plume movement, concentration-response relationships with wind parameters, and deposition assessments.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key reference for methodology and analysis: Deshpande AG et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024.

## Implications for data support and potential data products
- The dataset is well-documented with clear provenance, measurement conditions, and quality controls, enabling self-serve analyses and dashboarding.
- Potential data products:
  - Real-time or retrospective dashboards displaying NH3 concentration alongside wind speed/direction, release status, and inlet height.
  - Plume-tracking visualizations showing vertical/horizontal dispersion under varying wind conditions.
  - Data quality reports highlighting periods affected by lag or valve-switch gaps.
- Recommendations for data support:
  - Link the dataset to the full methodology (Deshpande et al., 2024) for context on release optimization and sampling.
  - Provide data lineage and a mapping guide for the column descriptions to ensure consistent reuse across projects.
  - Consider publishing derived metrics (e.g., plume arrival times at each height, concentration ratios) to facilitate rapid analyses.