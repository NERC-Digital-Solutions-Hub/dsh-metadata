# Audible and ultrasound recordings to survey birds and bats on Barro Colorado Island and in the Gamboa forest region, Panama, January 2023

## Overview
- Dataset of acoustic sounds collected in Panama in January 2023 to trial the recording capabilities of song meter devices for audible and ultrasound frequencies.
- Aimed at evaluating methods for surveying birds and bats and for potential integration into environmental monitoring datasets.

## Data Collection Details
- Instrumentation: two acoustic devices
  - Wildlife Acoustics SM4 (audible recordings)
  - Wildlife Acoustics SM4Bat (ultrasound recordings)
- Deployment characteristics:
  - Devices can be deployed for extended periods and programmed to sample around sunrise/sunset times.
  - Sample windows are configurable (e.g., around sunrise/sunset).
- Sampling period and locations:
  - Dates: 21–26 January 2023
  - Sites: four sites across Barro Colorado Island (BCI) and the Gamboa Forest region
- Recording schedules:
  - Audible: during defined intervals around sunrise/sunset (e.g., 1 hour before sunset to 1 hour after sunset).
  - Ultrasound: throughout daylight hours (e.g., 30 minutes before sunset to 30 minutes after sunrise).
- Supplemental data: Metadata.csv contains deployment-specific details (device, start/end times, longitude/latitude).

## Data Organization and File Naming
- Audible recordings:
  - Stored in folders named yy_mm_dd_Gamboa or yy_mm_dd_BCI, indicating region and survey start date.
- Ultrasound recordings:
  - Stored in folders named Bat_yy_mm_dd, with the same date convention indicating survey start date.
- File naming conventions:
  - The yy_mm_dd segment corresponds to the survey start date.
- Further details:
  - A more comprehensive overview of file naming and structure is available in the dataset details on the EIDC catalogue.

## Metadata and Access
- Device/product information:
  - SM4: audible capability (link to product page)
  - SM4Bat: ultrasound capability (link to product page)
- Metadata availability:
  - Metadata.csv provides deployment-level information (device, times, coordinates).
- Data access and deeper documentation:
  - Dataset details and naming conventions are available on the EIDC catalogue.

## Relevance for Environmental Monitoring
- Supports standardized, time-stamped acoustic monitoring across multiple sites, enabling assessment of environmental health indicators and biodiversity presence over time.
- Facilitates QA, verification, and cleaning/transforming of data for integration into standardized environmental datasets and portals.
- Aligns with goals to increase dataset value by enabling combination with other environmental datasets and by ensuring underlying data are accessible to others.

## Notes for Reuse and Quality Assurance
- This dataset represents a targeted, trial deployment (4 sites in Panama, January 2023) and may serve as a testbed for methods in acoustic biodiversity monitoring.
- Adheres to standardised folder naming and metadata practices to support interoperability and reuse in monitoring programs.