# Audible and ultrasound recordings to survey birds and bats on Barro Colorado Island and in the Gamboa forest region, Panama, January 2023

## Overview
- A dataset of acoustic sounds collected in Panama in January 2023 to trial the ability of song meter devices to record surrounding audio and ultrasound noise.
- Instruments used: Wildlife Acoustics SM4 (audible) and SM4BAT (ultrasound).
- Devices are suitable for multi-month deployments and configurable to sample around sunrise and sunset.

## Data collection and devices
- Two devices:
  - SM4 for audible frequency recordings.
  - SM4BAT for ultrasound frequency recordings.
- Device deployment can be long-term; sampling can be scheduled via configuration settings.
- Reference to product pages for context:
  - SM4: https://www.wildlifeacoustics.com/products/song-meter-sm4
  - SM4BAT: https://www.wildlifeacoustics.com/products/songmeter-sm4bat
- Sampling strategy:
  - Audible recordings aligned with sunrise/sunset windows (e.g., 1 hour before/after sunset).
  - Ultrasound recordings collected between sunrise and sunset (e.g., 30 minutes before sunset to 30 minutes after sunrise).

## Locations and timing
- Study sites: Barro Colorado Island (BCI) and the Gamboa Forest region.
- Survey period: 21–26 January 2023.
- For each deployment, details such as start/end times and precise coordinates are captured in metadata.

## Data organization and metadata
- File organization:
  - Audible frequency recordings are organized into folders named yy_mm_dd_Gamboa or yy_mm_dd_BCI, with the region indicated in the folder name.
  - Ultrasound frequency recordings are organized into folders named Bat_yy_mm_dd, with the date segment corresponding to the survey start date.
- Date encoding:
  - In both audible and ultrasound structures, the yy_mm_dd portion represents the survey start date.
- Metadata:
  - A Metadata.csv file provides deployment-specific details, including survey start date/time and geographic coordinates (longitude and latitude).
- Naming conventions:
  - A comprehensive overview of file naming structure is available in the dataset details on the EIDC catalogue.