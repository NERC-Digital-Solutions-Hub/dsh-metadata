# Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal

## Collection and sensors
- 23 IoT sensors embedded in boulders across two debris-flow channels and one landslide in the Bhote Koshi catchment, Nepal.
- Data collected May–October 2019 (monsoon season) and transmitted via LoRaWAN; real-time when gateway online, otherwise buffered and sent later.
- Data uploaded to a server and downloadable as CSV for analysis.

## Data contents, units and structure
- CSV contains headers; accelerometer readings on x, y, z (used in the study) are in columns 13–15.
- Accelerometer values are in g.
- Data organized by device ID (23 IDs); data availability varies by device due to programming settings.
- Some columns (pressure, temperature, altitude) were not used.
- Timestamps include server arrival time vs GPS acquisition time; GPS times may be missing when satellites were not available.

## Data quality, limitations and interpretation
- No dedicated quality control on the raw data; interpretation discussed in relation to sampling frequency and GPS performance/acquisition time.
- Uneven spatial distribution of devices and patchy data due to gateway connectivity and differing device settings.

## Use and potential data products
- Data can be cleaned, transformed, and combined into self-serve dashboards or reports to analyze boulder movements and mass-flow events.
- The study provides guidance on interpreting timing and transmission (real-time vs queued), aiding data consumers in deriving insights.

## Access and further information
- For full methodology and discussion, refer to Dini et al., 2021: Development of smart boulders to monitor mass movements via the Internet of Things: a pilot study in Nepal.
- DOI: 10.5194/esurf-9-295-2021