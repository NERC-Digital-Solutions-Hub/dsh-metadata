# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Overview
- A controlled ammonia (NH3) enhancement experiment conducted in a tropical sub-montane forest at Queensberry Estate, central Sri Lanka, to study NH3 impacts on vegetation, bryophytes, lichens, and soil.
- Data collection period: 1 January 2023 to 31 December 2024.
- Data intended to support understanding of NH3 deposition and environmental responses, and to extend earlier site data from 2022.
- Funding provided by UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## Experimental design and data collection
- Site and setup:
  - Location: Queensberry Estate, coordinates 6.9693° N, 80.5911° E; altitude 1645 m.
  - NH3 release system activated only when wind conditions are favorable, measured below the forest canopy.
  - NH3 released from three horizontal PVC tubes (20 m long, 110 mm diameter) at heights 0.5, 1.35, and 2.2 m.
- Release mechanism:
  - NH3 delivered from a cylinder via a stainless steel manifold, using a mass flow controller (MFC) and solenoid valve.
  - NH3 release occurs through six holes per tube, distributed every 20 cm around the tube circumference.
  - A fan in the manifold creates positive pressure; release occurs only when wind direction falls within specified sectors (5–75° and 185–255° relative to monitoring quadrats) and at threshold wind speeds (0.3–10 m/s).
- Sensing and timing:
  - Wind data captured by a WXT536 weather station (below-canopy wind speed and direction).
  - NH3 release rate recorded by the MFC; NH3 volume released logged every 20 seconds and averaged over 15-minute intervals.
  - Data expressed in Sri Lanka Standard Time (SLST).
- Documentation:
  - Full experimental design, methodology, analysis, and findings described in Deshpande et al. (2024a); dataset extends the 2022 dataset (Deshpande et al., 2024b).

## Quality control and data integrity
- Visual quality control performed; obvious instrument- or power-related errors removed.
- Some gaps occur due to replacement of faulty gas-control components.

## Data content, structure, and coverage
- Size: 61,751 measurements across 4 parameters.
- Data format: CSV file with the following columns (descriptions provided in dataset documentation):
  - Timestamp (date and 15-minute interval)
  - NH3_status (minutes; duration NH3 was released)
  - NH3_flow (slpm; NH3 flow through the MFC into the release manifold)
  - Wind_speed (ms^-1; below-canopy wind speed)
  - Wind_direction (degrees; below-canopy wind direction)
  - Instrument metadata (for each parameter: type, manufacturer, description)
- Scope: 2023 and 2024 data from the Queensberry site, building on the 2022 dataset.

## Data management, availability, and use
- Data stewardship follows standard monitoring-data practices: collection, verification, quality assurance, cleaning, transformation, and standardised outputs.
- Outputs and metadata designed to support deposition and environmental analysis, with datasets typically stored and uploaded to appropriate data portals.
- Related publications provide methodological and analytical context:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from the Queensberry site, Sri Lanka, 2022.
  - These references align with the dataset's aim to enable cross-site deposition assessments and standardised reporting.

## Funding and references
- Funded by UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Key references:
  - Deshpande et al. (2024a) Atmos. Environ. 120325
  - Deshpande et al. (2024b) NERC EDS Environmental Information Data Centre entry