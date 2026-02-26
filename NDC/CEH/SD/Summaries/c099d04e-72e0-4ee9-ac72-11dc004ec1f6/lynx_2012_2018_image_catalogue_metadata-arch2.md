# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalogue for Lynx camera-trap images from 2012–2018, encompassing project, study site, camera positions, image events, and Lynx-specific data when available.
- Times corrected to Eastern European winter time (GMT+03:00); date/time fields reflect first and last images within triggering events; some fields are not applicable when Lynx were not identified.
- Contains 265 triggering events (166 was not used); a new triggering event starts when the camera motion sensor is triggered.
- Data usage flag indicates whether records were used in site-level analysis (Gashchak et al. 2022); some records (2012 and Jan–June 2013) were not used due to irregular/short-term nature but are included to enable frequency estimation.

## Key Fields and Meanings

- Project and Study Context
  - Project_ID: NatEnvPr, REDFIRE, TREE
  - Study_Site: 1–8
  - Setup: 1–11 (n/a if Lynx were not identified)

- Camera and Image Metadata
  - Camera_Trap_Location_ID
  - Camera_Trap_Location_ID_Related_To_Project
  - Image_Location_Folder_Name
  - First_Image_Per_Triggering_Event
  - Last_Image_Per_Triggering_Event

- Triggering and Event Details
  - Triggering_Event_Number: total 265 events; 166 not used
  - Date_And_Time_Image_Taken: date/time for the first image in a triggering event; adjusted and stored in GMT+03:00
  - Year; Month: year and month of image/trap operation (including non-Lynx rows for baseline)

- Lynx Identification and Attributes
  - Lynx_ID: unique ID formed from Camera_Trap_Location_ID and a suffix; may be n/a when Lynx ID is not possible
  - Lynx_Gender_Age: Ad (adult), AdF (adult female), Adf (adult male), imm (immature), or n/a when not determinable

- Event Duration and Temporal Segments
  - Triggering_Event_Duration_Minutes
  - Day period: Night, Twilight, Day with defined intervals (specific to Chornobyl timing)
  - Number_Trapping_Days_Per_Month
  - Events_Per_Trapping_Day: calculated for records containing Lynx

- Notes and Data Usage
  - Notes: notes related to Lynx visible in images
  - Data_Used_For_Analysis_Y_Or_N: Y if used in by-site analysis (Gashchak et al. 2022); N if not used due to irregular/short-term nature; 2012 and early 2013 data included for average Lynx frequency estimates

## Data Quality and Processing Notes
- Dates/times corrected if camera clock was mis-set; all times standardized to GMT+03:00.
- Several fields are n/a when Lynx were not observed or identifiable (e.g., First/Last Image per Triggering Event for non-Lynx records).
- Some records are included to enable estimation of Lynx frequency despite lacking Lynx identifications in certain entries.

## Implications for Environmental Monitoring
- Provides a structured, standardised metadata framework across multiple projects and study sites, enabling temporal and spatial analyses of Lynx activity.
- Clear data usage flags support reproducibility and transparent reporting, indicating which data contributed to site-level analyses (Gashchak et al. 2022) and which did not due to irregular sampling.
- Facilitates potential integration with other datasets by aligning field definitions (dates, events, day periods, and camera locations).

## Conclusion
- The Lynx_2012_2018_Image_Catalogue_Metadata document delivers a comprehensive, time-adjusted, multi-project metadata schema for Lynx camera-trap images, supporting both frequency estimates and activity analyses while clearly delineating data usable for site-specific analyses and highlighting data limitations.