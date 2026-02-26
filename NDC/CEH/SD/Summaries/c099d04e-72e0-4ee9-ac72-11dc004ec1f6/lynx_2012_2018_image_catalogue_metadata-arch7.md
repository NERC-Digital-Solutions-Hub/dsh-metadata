# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalog for Lynx camera-trap images collected during 2012–2018.
- Associated with projects: NatEnvPr (Ukrainian national environmental studies program), REDFIRE, and TREE.
- Includes both Lynx records and non-Lynx records to enable estimation of activity and frequency.
- Date/time values are standardized to Eastern European winter time (GMT+03:00) when necessary.
- Provides a mix of event-level and image-level information to support GIS-based visualization and analysis.

## Data structure and key fields
- Project_ID: Identifier of the project under which images were collected.
- Years and Months: Year (YYYY) and Month (MM) of image capture or of camera operation; includes periods without Lynx to aid frequency estimates.
- Study_Site: Study site index (1–8).
- Setup: Setup period indicator (1–11); note that Lynx were not ID’d, so setup may be n/a.
- Camera_Trap_Location_ID: Numerical ID for the camera location.
- Camera_Trap_Location_ID_Related_To_Project: Link between trap location and project.
- Image_Location_Folder_Name: Folder path/name containing the images.
- First_Image_Per_Triggering_Event / Last_Image_Per_Triggering_Event: Filenames of first/last image in a triggering event (not applicable for Lynx-only catalogs).
- Triggering_Event_Number: Sequential event number; 265 events present (166 is unused).
- Date_And_Time_Image_Taken: Timestamp for the first image of a triggering event; adjusted to GMT+03:00 if needed.
- Lynx_ID: Unique Lynx identifier (constructed from Camera_Trap_Location_ID and a suffix); may be n/a when no Lynx are present.
- Lynx_Gender_Age: Coded gender/age of Lynx (e.g., Ad, AdF, AdF, imm); n/a if undeterminable or no Lynx.
- Triggering_Event_Duration_Minutes: Duration of the triggering event.
- Day_period: Time-of-day category (Night, Twilight, Day) with coded intervals.
- Number_Trapping_Days_Per_Month: Total trapping days in the month.
- Events_Per_Trapping_Day: Events per trapping day (calculated when Lynx records exist).
- Notes: Additional notes related to Lynx observed.
- Data_Used_For_Analysis_Y_Or_N: Indicates whether the data were used in site-level analysis (Y) or not (N), with rationale (e.g., used in Gashchak et al. 2022 or excluded due to irregular/short-term data).

## Temporal and spatial context
- Spatial: Camera trap locations and study sites facilitate map-based visualization of Lynx activity across sites.
- Temporal: Covers 2012–2018 with both Lynx detections and non-detection periods; time values corrected to GMT+03:00 when needed.
- Event structure: A new triggering event begins when the camera motion sensor is triggered; multiple Lynx within the same event share the same event number.

## Data quality, limitations, and caveats
- Some fields are not applicable (n/a), especially where Lynx could not be identified or where setup information was not recorded.
- Lynx_ID is not available for records without Lynx sightings; non-Lynx rows aid estimation of average Lynx frequency.
- A number of records pertain to periods with no Lynx detections, included to support frequency analyses but not to identify individuals.
- Data used for site-level analysis is limited to records relevant to that analysis (per Gashchak et al. 2022); other data are excluded due to irregular or short-term sampling.
- Event 166 is noted as not used, resulting in 265 applicable events.
- Time and date consistency may reflect corrections; users should be aware of potential discrepancies between camera timestamps and catalogue timestamps.

## GIS usage and recommended workflows
- Use Camera_Trap_Location_ID and Study_Site to join with spatial layers (camera locations, study-area polygons).
- Use Date_And_Time_Image_Taken (and Year/Month) to create time-enabled maps and time-series visualizations of activity.
- Leverage Day_period and Triggering_Event_Duration_Minutes for temporal stratification (e.g., day vs. night activity patterns).
- Filter by Data_Used_For_Analysis_Y_Or_N to reproduce analyses (e.g., Gashchak et al. 2022) or to work with exploratory datasets (including non-Lynx periods).
- Link Image_Location_Folder_Name with raster/vector assets or image galleries for map-based dashboards.
- If analyzing individual animals, construct Lynx_IDs from Camera_Trap_Location_ID and suffix; otherwise rely on presence/absence and event-level summaries.
- Use Notes and Lynx_Gender_Age to enrich attribute tables where relevant for interpretation and reporting.

## Provenance and scope
- Data originate from multiple environmental and biodiversity projects in Ukraine (NatEnvPr, REDFIRE, TREE).
- Catalog captures both presence data (Lynx detections) and non-detections to support frequency and distribution analyses.
- Metadata designed to support GIS-based exploration and visualization of Lynx activity at different spatial and temporal scales, with explicit notes on data suitability for site-level analyses.