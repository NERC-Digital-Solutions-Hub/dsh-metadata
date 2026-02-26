# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- IoT-enabled monitoring of mass movements using 23 sensors embedded in boulders across two debris-flow channels and one landslide in the Bhote Koshi catchment, Nepal.
- Data collection period: May–October 2019 (monsoon season).
- Transmission: via LoRaWAN; real-time data when gateway online, otherwise buffered and sent when connectivity is restored.
- Data storage and access: data sent to a server and downloaded as CSV for analysis (details provided in the referenced paper).

## Data collection and variables
- Raw data comprise GPS and accelerometer (x, y, z) readings from 23 devices; uneven sensor distribution within the study area.
- Accelerometer readings are recorded in g units; not all recorded columns were used in the study (e.g., pressure, temperature, altitude not utilized).
- Data are organized by device ID; accelerometer data used in the study correspond to specific columns (e.g., columns 13–15).
- Timestamp distinctions:
  - Server timestamp: arrival time of data at the server (affected by gateway connectivity).
  - GPS timestamp: actual acquisition time (may be missing due to satellite availability).

## Data structure and access
- Data structured by device ID (23 IDs).
- Variability in data volume across devices due to programming settings and sensor sensitivity.
- CSV format used for analysis; full methodological details and interpretation guidance provided in Dini et al., 2021.

## Quality and governance considerations
- No explicit quality control applied to raw data in this dataset.
- Interpretations rely on understanding sampling frequency and GPS performance, discussed in the cited paper.
- Metadata gaps and uneven metadata can hinder data reuse; some data require transformation to be usable.
- Public sharing considerations: underlying datasets are shared as CSV, but sharing can pose governance and transparency barriers; data management practices are emphasized in the source paper.

## Relevance for monitoring frameworks
- Demonstrates an end-to-end IoT monitoring workflow for environmental mass-movement events, including data collection, real-time transmission constraints, and CSV-ready outputs.
- Highlights practical governance and metadata challenges relevant to monitoring frameworks: data availability, standardization, documentation, update frequency, and openness.
- Illustrates the trade-offs between real-time data needs and connectivity-dependent data delivery, informing data governance and dissemination strategies.

## Reference
- Dini, B., Bennett, G. L., Franco, A., Whitworth, M. R., Cook, K. L., Senn, A., & Reynolds, J. M. (2021). Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal. Earth Surface Dynamics, 9(2), 295-315.