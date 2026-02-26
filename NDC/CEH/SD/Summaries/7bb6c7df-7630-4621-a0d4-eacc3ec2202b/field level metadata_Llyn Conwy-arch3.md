# Temperature at Depth Measurements (1m–19m) Using Labfacility PRTs and Campbell Scientific CR10X Data Logger

## Overview
- Temperature measurements at depths 1m, 3m, 5m, 7m, 9m, 11m, 13m, 15m, 17m, and 19m.
- Instrumentation: 10 Labfacility platinum resistance thermometers (PRTs) in a stainless steel sheath.
- Data logger: Campbell Scientific CR10X.
- Date range: 03/11/2006 00:00 to 15/12/2008 14:00.
- Location: Grid ref SH 77961 46465; Latitude 53.001555; Longitude -3.8200267; Elevation 460 m.

## Instrumentation and measurement details
- Temperature range for thermometers: -5 to +40 °C.
- Depth-specific temperature readings are stored under field headings (1m, 3m, 5m, ..., 19m) with GMT timestamps.
- Temperature string explicitly notes 10 x Labfacility PRTs.

## Data structure and metadata
- Core fields include: date range, location, grid reference, latitude, longitude, elevation, and the temperature string (sensor details).
- Each depth provides a corresponding temperature measurement in degrees Celsius, with time recorded in GMT.
- Data provenance includes sensor type, number of sensors, and data logger used.

## Data quality and governance considerations for monitoring frameworks
- Metadata sufficiency: field descriptions are present, but fuller metadata (sensor serials, calibration history, maintenance, and metadata completeness) would aid verifiability.
- Data handling: transformation/standardization may be required to align with broader datasets.
- Access and sharing: explicit openness of underlying data is a consideration; sharing raw sensor data and calibration notes supports transparency.
- Data governance: calibration records, sensor replacement history, and logging of any data gaps or instrument downtime are important for reliability.

## Limitations and scope
- Single-site measurement with precise geographical coordinates provided.
- Depths are fixed at 1–19 meters in 2-meter increments.
- Time frame limited to 2006–2008.

## Relevance for environmental monitoring and policy
- Provides a depth-resolved soil/ground temperature profile over time, useful for:
  - Assessing soil temperature dynamics and thermal regimes.
  - Informing climate- or hydrology-related environmental models.
  - Supporting risk assessments and policy decisions involving subsurface temperature impacts.