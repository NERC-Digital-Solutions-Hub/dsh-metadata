# Audible and ultrasound recordings to survey birds and bats on Barro Colorado Island and in the Gamboa forest region, Panama, January 2023

## Overview
- Acoustic recordings collected in Panama in January 2023 to trial song meter devices for recording surrounding audio and ultrasound noise.
- Devices used: Wildlife Acoustics SM4 (audible) and SM4BAT (ultrasound); capable of long deployments and scheduling around sunrise/sunset.
- Data include both audible and ultrasound recordings across multiple sites.

## Spatial and temporal coverage
- Study area: Barro Colorado Island (BCI) and the Gamboa forest region (4 sites total).
- Recording window: 21–26 January 2023, centered around sunrise and sunset hours.
- Audible recordings: during intervals around sunrise/sunset (e.g., 1 hour before sunset to 1 hour after sunset).
- Ultrasound recordings: during daylight hours (e.g., 30 minutes before sunset to 30 minutes after sunrise).
- Deployment details (dates, times, coordinates) are provided in Metadata.csv.

## Data structure and naming conventions
- Audible recordings:
  - Folder naming: yy_mm_dd_Gamboa or yy_mm_dd_BCI (indicating date and site/region).
- Ultrasound recordings:
  - Folder naming: Bat_yy_mm_dd (date-prefixed ultrasound data).
- The date segment in folder names corresponds to the survey start date.
- For a comprehensive overview of file naming, see dataset details on the EIDC catalogue.

## Access and metadata
- Metadata.csv contains per-deployment information including device, survey start/end times, and longitude/latitude.
- Additional dataset details are available on the EIDC catalogue.
- Product information:
  - SM4: https://www.wildlifeacoustics.com/products/song-meter-sm4
  - SM4BAT: https://www.wildlifeacoustics.com/products/songmeter-sm4bat

## GIS considerations
- Enables mapping of sampling sites and comparison of audible vs ultrasound coverage.
- Temporal windows align with daylight periods, suitable for integrating with environmental covariates (e.g., sunrise/sunset timings, habitat data).
- Requires joining audio data with Metadata.csv to extract coordinates and deployment details for spatial analyses.
- Data may require cleaning and transformation due to multi-site deployment and varying data volumes.