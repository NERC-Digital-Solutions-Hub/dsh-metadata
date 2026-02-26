# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Ammonia (NH3) enhancement experiment at Glencorse woodland near Edinburgh to study effects on forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland (coordinates 55.8539 N, -3.2151 W), altitude 200 m.
- Timeframe: 16 September 2021 to 5 January 2023.
- Data capture: NH3 release parameters and below-canopy wind measurements to assess exposure.

## Data collection and experimental setup
- NH3 release conditions:
  - NH3 is released only when wind direction is 275–345 degrees and wind speeds are between 0.3 and 10 m/s.
- Release hardware:
  - Three horizontal PVC tubes (20 m long, 110 mm OD) at 0.5, 1.35, and 2.2 m above ground.
  - Six 4 mm holes per tube (every 20 cm) for NH3 release around the circumference.
  - Central manifold with a fan creating positive pressure.
  - Pure NH3 delivered from a cylinder via a mass flow controller (MFC) and solenoid valve into the manifold.
- Control and measurement:
  - Solenoid valve opens only under correct wind conditions.
  - NH3 flow setpoint and NH3 flow measured via MKS Instruments G series MFC.
  - Below-canopy wind data captured by a WXT536 weather station (Vaisala).
  - NH3 release rate recorded every 20 seconds; 15-minute averages computed.
- Data period structure:
  - All data are in GMT.
  - 15-minute timestamps provided in dd/mm/yyyy hh:mm format.
- Total dataset:
  - 45,538 measurements across 5 parameters.

## Data structure and content
- File format: CSV.
- Key parameters (with associated metadata):
  - Timestamp: 15-minute time points.
  - NH3_status: 0 (OFF) or >0 (ON); instrument: Type 6027 solenoid valve; manufacturer: Bürkert; description: NH3 release status.
  - NH3_flow_set: NH3 flow set point (slpm); instrument: G series MFC; manufacturer: MKS Instruments; description: NH3 flow setpoint for prevailing wind conditions.
  - NH3_flow: NH3 flow through MFC into release manifold (slpm); instrument: G series MFC; manufacturer: MKS Instruments; description: Actual NH3 flow.
  - Wind_speed: below-canopy wind speed (ms^-1); instrument: WXT536; manufacturer: Vaisala; description: Wind speed.
  - Wind_direction: wind direction (degrees); instrument: WXT536; manufacturer: Vaisala; description: Below-canopy wind direction.
- Additional metadata fields are included per parameter (instrument, manufacturer, description).

## Data quality, limitations, and notes
- Quality control:
  - Visual checks performed; obvious instrument/malfunction errors removed.
  - Some gaps occurred due to replacement of faulty gas control components.
- Completeness:
  - The dataset provides continuous NH3 release and wind data within the specified period, subject to the noted gaps.
- References for methods:
  - Full experimental design, methodology, analysis, and findings described in Deshpande et al. (2024).
  - DOI: 10.1016/j.atmosenv.2023.120325.

## Usage, access, and context
- Purpose aligned with creating data products to enable exploration and self-service analysis of NH3 exposure in forest ecosystems.
- Data suitable for analyses of NH3 deposition and exposure under wind-controlled release scenarios, potentially integrable with related atmospheric deposition studies.
- Funding:
  - UKRI GCRF South Asian Nitrogen Hub.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.