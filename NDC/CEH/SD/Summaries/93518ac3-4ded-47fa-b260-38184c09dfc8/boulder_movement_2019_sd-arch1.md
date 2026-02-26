# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Overview
- Dataset of raw GPS and accelerometer readings from 23 sensors embedded in boulders.
- Locations: two debris flow channels and one landslide in the Bhote Koshi catchment, Nepal.
- Collected May–October 2019 (monsoon season).
- Data transmitted in real time when gateway was online; otherwise buffered and sent later.
- Accessed and downloaded as CSV files from a server; detailed methodology described in Dini et al., 2021.

## Data content and units
- CSV contains headers for each recorded parameter; not all columns used in the study (pressure, temperature, altitude excluded).
- Accelerometer readings on X, Y, Z axes are in g units.
- Data organized by device ID (23 total; second column of the dataset).
- Accelerometer data used in the study are in columns 13, 14, and 15.
- The last column provides the parameter name.
- Some devices collected more data than others due to differing programming settings and sensitivity.

## Data collection design and structure
- Sensor deployment uneven across the study area.
- Data flow: devices → LoRaWAN gateway → server → CSV download for analysis.
- Data are divided by device ID; 23 IDs present.
- Temporal data include both server timestamps (arrival time at the server) and GPS timestamps (actual acquisition time; GPS times may be missing when satellite reception was unavailable).
- The paper discusses how to align and interpret these timestamps to distinguish real-time transmissions from delayed uploads.

## Data quality and caveats
- No dedicated quality control performed on the raw data.
- Interpretive guidance provided in the source paper, including considerations of sampling frequency and GPS acquisition performance.
- Variability in data across devices due to programming settings and sensor sensitivity.
- Real-time data reliability depends on gateway connectivity; gaps may occur when gateways are offline or temporarily unavailable.

## Usage, provenance, and references
- Data intended for monitoring mass movements via IoT; suitable for correlating accelerometer signals with GPS positions to infer movement events.
- For detailed data interpretation, sampling characteristics, and methodological context, refer to Dini et al. (2021): Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal, Earth Surface Dynamics, 9(2), 295-315.