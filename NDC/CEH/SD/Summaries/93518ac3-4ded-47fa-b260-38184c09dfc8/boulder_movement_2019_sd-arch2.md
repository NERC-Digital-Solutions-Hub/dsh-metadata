# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- A pilot study deploying IoT-enabled smart boulders to monitor mass movements in Nepal.
- Field sites include two debris flow channels and one landslide in the Bhote Koshi catchment.
- Data collection focused on raw GPS and 3-axis accelerometer readings from 23 embedded sensors during the May–October 2019 monsoon season.

## Collection method
- Devices embedded in 23 boulders transmit data via a long-range LoRaWAN network.
- Real-time data when the gateway is online; otherwise data are buffered and sent when connectivity is restored.
- Data are sent to a server and downloadable as CSV files for analysis.
- Detailed methodology and interpretation are described in Dini et al., 2021.

## Data content and structure
- CSV contains multiple parameters; the study uses accelerometer data (x, y, z) and GPS readings; some columns (e.g., pressure, temperature, altitude) are not used.
- Accelerometer values are in g units; accelerometer columns used in the study are typically columns 13–15.
- Data are organized by device ID (23 IDs); uneven data capture across devices due to differences in programming and sensitivity.

## Quality control and interpretation
- No specific quality control applied to raw data in this dataset.
- The accompanying literature discusses how to interpret data, particularly regarding accelerometer sampling frequency and GPS performance/acquisition time.
- Differences between server timestamps (arrival at server) and GPS timestamps (actual acquisition) are noted and can be analyzed jointly to assess real-time data delivery.

## Data access and storage
- Data are stored on a central server and can be accessed/downloaded as CSV files.
- Data are divided by device ID, enabling traceability and independent quality checks.
- The work points to broader data sharing and portal upload for improved accessibility.

## Relevance to environmental monitoring
- Demonstrates a standardized data collection approach for monitoring mass movements, enabling consistent environmental health and policy performance assessments over time.
- Highlights the potential to combine this dataset with other environmental data to increase value beyond single-use applications.
- Emphasizes the importance of enabling access to underlying data for broader scrutiny and reuse.

## Reference
- Dini, B., Bennett, G. L., Franco, A., Whitworth, M. R., Cook, K. L., Senn, A., & Reynolds, J. M. (2021). Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal. Earth Surface Dynamics, 9(2), 295-315.