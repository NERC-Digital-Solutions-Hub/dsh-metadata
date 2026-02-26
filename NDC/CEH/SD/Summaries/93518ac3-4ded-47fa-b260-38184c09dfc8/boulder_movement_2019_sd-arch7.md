# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- 23 sensors embedded in boulders across two debris flow channels and one landslide in the Bhote Koshi catchment.
- Data collected May–October 2019 (monsoon season): raw GPS and tri-axial accelerometer readings (x, y, z).
- Devices connected via LoRaWAN; real-time data when gateway online, otherwise buffered and sent when gateway available.
- Data stored on a server and downloaded as CSV for analysis.

## Collection and data generation methods
- Uneven distribution of boulder deployments within the study area.
- Data organized by device ID (23 IDs present in the dataset).
- Accelerometer readings used in the study are in columns corresponding to x, y, z (columns 13–15 in the dataset).
- Other recorded parameters (e.g., pressure, temperature, altitude) were present but not used in this study.
- Timestamps:
  - Server timestamp reflects data arrival time to the server (affected by gateway connectivity).
  - GPS timestamp reflects actual acquisition time (subject to satellite availability; may be missing).
- Full methodological details are described in Dini et al., 2021.

## Data structure and content
- Data divided by device ID; 23 devices in the second column.
- Headers in the CSV indicate the recorded parameters; not all columns are used in the study.
- Accelerometer data used for analysis are in specific columns (x, y, z).
- The dataset contains a mix of data densities due to programming settings and sensor sensitivity across devices.

## Data quality and limitations for GIS use
- No formal quality control on the raw data was performed in this description.
- Real-time transmission depends on gateway availability, causing potential delays or batching in data delivery.
- Uneven data density across devices due to differing settings and sensitivity.
- GPS acquisition times can be missing; server times may not perfectly align with actual sensor events.
- Interpretation of data requires understanding sampling frequency and GPS performance, as detailed in the referenced paper.

## How this data can support GIS work
- Enables map-based visualization of boulder movements and mass movement indicators during the monsoon season.
- Facilitates temporal analysis by device, aiding identification of when accelerations correlate with debris-flow events.
- Can be integrated with spatial layers (channels, landslide extents) to assess spatial patterns and risk in the Bhote Koshi catchment.
- Useful as a pilot dataset for developing GIS-ready data products that combine IoT sensor readings with geospatial features.

## Reference
- Dini, B., Bennett, G. L., Franco, A., Whitworth, M. R., Cook, K. L., Senn, A., & Reynolds, J. M. (2021). Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal. Earth Surface Dynamics, 9(2), 295-315.