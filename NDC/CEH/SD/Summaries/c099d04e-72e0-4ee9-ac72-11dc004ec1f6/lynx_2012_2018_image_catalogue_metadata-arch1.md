# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalogue for Lynx images collected 2012–2018.
- Part of multiple projects: NatEnvPr (Ukrainian national program of environmental studies), REDFIRE, TREE.
- Captures camera-trap study-site information, camera-trap locations, timing, and Lynx-specific details to support presence, frequency, and activity analyses.
- Includes entries both with Lynx observations and without (to estimate average Lynx frequency).

## Key Data Fields and What They Represent
- Project_ID: Identifier for the overarching project the images belong to (e.g., NatEnvPr, REDFIRE, TREE).
- Study_Site: Numeric code for the study site (1–8).
- Setup: Setup period related to the project (1–11); Lynx were not identified in some cases, so setup may be absent.
- Camera_Trap_Location_ID: Numeric ID for each camera trap location.
- Camera_Trap_Location_ID_Related_To_Project: Location ID linked to the project.
- Image_Location_Folder_Name: Folder name where the images are stored.
- First_Image_Per_Triggering_Event / Last_Image_Per_Triggering_Ev ent: Filenames of the first/last image for a triggering event (often not applicable if no Lynx is detected).
- Triggering_Event_Number: Sequential number for each triggering event (note: event 166 was not used; 265 events in total).
- Date_And_Time_Image_Taken: Date/time for the first image of a triggering event; dates adjusted to Eastern European winter time (GMT+03:00) if camera times were mis-set.
- Year / Month: Year and month when the Lynx image was taken or when the trap was operating (non-Lynx rows included to estimate Lynx frequency).
- Lynx_ID: Unique Lynx identifier composed of Camera_Trap_Location_ID and a unique suffix; may be unavailable if Lynx could not be identified.
- Lynx_Gender_Age: Coded information on gender/age when determinable (ad, adv, adf, imm; or n/a when not determinable or no Lynx present).
- Triggering_Event_Duration_Minutes: Time span of a triggering event from first to last image/video clip.
- Day_period: Coded time-of-day category for images (Night, Twilight, Day with subcodes); definitions derived from local civil twilight and solar position.
- Number_Trapping_Days_Per_Month: Duration (in days) the trap was operating within a given month.
- Events_Per_Trapping_Day: Calculated as trapping days divided by triggering duration; applicable only when Lynx are present.
- Notes: Qualitative notes related to Lynx visible in the image.
- Data_Used_For_Analysis_Y_Or_N: Indicator if the data were used in the by-site analysis in Gashchak et al. 2022 (Y) or not (N) due to irregular/short-term data or other limitations.

## Data Quality, Scope, and Limitations
- Some fields are not applicable (n/a), particularly where Lynx were not detected or where data collection did not generate certain metadata.
- Time corrections applied to ensure consistency across datasets (Eastern European winter time; GMT+03:00).
- 265 total triggering events documented; event 166 is omitted from counts.
- Rows without Lynx exist to support baseline estimates of Lynx frequency, creating a mix of presence and absence data.
- Data integration considerations:
  - Lynx_ID depends on camera location and a unique suffix; may be missing if Lynx could not be identified.
  - Some datasets are irregular or short-term, affecting inclusion in per-site analyses (as noted for Gashchak et al. 2022).

## Usage and References
- Data included in by-site analysis in Gashchak et al. 2022 for records used (Y) and excluded for irregular/short-term data (N).
- Suitable for analyses of Lynx frequency, activity distribution across day periods, and event-based occupancy when combined with location and timing metadata.
- Useful for researchers needing to standardize multi-source camera-trap metadata, link events to specific Lynx individuals (where possible), and align timing with local time conventions.