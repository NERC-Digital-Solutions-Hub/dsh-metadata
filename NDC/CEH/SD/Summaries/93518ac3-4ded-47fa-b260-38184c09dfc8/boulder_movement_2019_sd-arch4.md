# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- 23 sensors embedded in boulders across two debris-flow channels and one landslide in the Bhote Koshi catchment.
- Data collected May–October 2019 (monsoon season) via LoRaWAN, transmitted in real time when the gateway was online; otherwise stored and uploaded when connectivity resumed.
- Data received by a gateway and stored on a server, then downloadable as CSV for analysis.
- Detailed methodology and data context are described in Dini et al., 2021.

## Data content and structure
- Data is organized by device ID (23 IDs present in the dataset’s second column).
- Accelerometer readings (x, y, z) are in g units; used columns are 13, 14, 15 for accelerometer data in the study.
- Not all data columns are used in the study; e.g., pressure, temperature, and altitude data were not utilized.
- Uneven distribution of boulders within the study area; some devices captured more data due to differing programming settings and sensitivity.

## Timestamps and transmission
- The dataset includes both server timestamps (time data arrived at the server) and GPS timestamps (actual time of acquisition, which may be unavailable if satellite data was not received).
- Analyzing the difference between timestamps helps distinguish real-time transmission from delayed uploads.

## Quality control and interpretation
- No dedicated quality control was performed on the raw data within this dataset.
- The accompanying paper discusses interpretation considerations, particularly regarding accelerometer sampling frequency and GPS performance/acquisition timing.

## Data accessibility and documentation
- Data provided as CSV with self-explanatory headers.
- For comprehensive methodology, data collection details, and device-specific configurations, refer to Dini et al., 2021.