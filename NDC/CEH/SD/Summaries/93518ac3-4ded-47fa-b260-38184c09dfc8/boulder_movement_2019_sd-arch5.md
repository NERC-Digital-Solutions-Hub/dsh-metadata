# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- Data collected are raw GPS and three-axis accelerometer readings from 23 sensors embedded in boulders in two debris-flow channels and one landslide in the Bhote Koshi catchment, Nepal.
- Collection period spans May–October 2019 (monsoon season).
- Data transmitted via LoRaWAN gateway; real-time transmission when the gateway is online, otherwise buffered and sent when connectivity is available.
- Data are stored on a server and available for download as CSV files for analysis.

## Data content and structure
- Data are organized by device ID (23 distinct IDs present).
- Accelerometer readings used in the study are in columns 13–15 (X, Y, Z axes); units are g.
- Some columns (e.g., pressure, temperature, altitude) were collected but not used in this study.
- The last column contains parameter headers; headers are self-explanatory.
- Time stamps include both:
  - Server timestamp (arrival time at the server; gateway-dependent)
  - GPS timestamp (actual acquisition time; may be missing when satellites are unavailable)
- Data distribution across devices varies due to different programming settings and sensitivities.

## Quality and limitations
- No explicit quality control was performed on the raw data.
- Guidance on interpreting the data, including accelerometer sampling frequency and GPS performance, is discussed in the referenced paper (Dini et al., 2021).
- Variability across devices (data quantity, sensitivity) and potential gaps due to gateway connectivity affect data consistency.
- The dataset is tied to a specific deployment and context (smart boulders in Nepal) and may require normalization for cross-device comparability.

## Data governance and reuse considerations
- Rich metadata and documentation are provided in the accompanying paper; refer to Dini et al. (2021) for comprehensive methodology and interpretation guidance.
- Data format is CSV, with explicit device-based organization; ensure metadata captures device settings, deployment times, and sensor nomenclature for reuse.
- Be mindful of context-specific aspects (e.g., device programming, data transmission gaps, and real-time versus retrospective data) when integrating with other datasets or interoperating across systems.

## Reference
- Dini, B., Bennett, G. L., Franco, A., Whitworth, M. R., Cook, K. L., Senn, A., & Reynolds, J. M. (2021). Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal. Earth Surface Dynamics, 9(2), 295-315.