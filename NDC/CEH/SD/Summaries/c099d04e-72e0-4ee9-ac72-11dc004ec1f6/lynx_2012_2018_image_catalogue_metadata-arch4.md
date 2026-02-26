# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata for Lynx image catalogue spanning 2012–2018, associated with Ukrainian environmental programs/projects (NatEnvPr), REDFIRE, and TREE.
- Includes records with and without Lynx to enable estimation of Lynx frequency and activity.

## Dataset structure and key fields
- Project_ID: Projects include NatEnvPr (Ukrainian national program of environmental studies), REDFIRE, TREE.
- Study_Site: Values 1–8.
- Setup: Setup period 1–11; note that Lynx were not ID'd, so setup is not given.
- Camera_Trap_Location_ID and Camera_Trap_Location_ID_Related_To_Project: location identifiers for cameras and their relation to projects.
- Image_Location_Folder_Name: folder name where images are stored.
- Triggering_Event_Number: events are sequential; 166 was not used, totaling 265 events. An event is triggered by camera motion; multiple Lynx in the same event share the same triggering event.
- Date_And_Time_Image_Taken: date/time for the first image of a triggering event; times adjusted to Eastern European winter time (GMT+03:00); may differ from the timestamp shown on images.
- Year and Month: year (YYYY) and month (MM) of the Lynx image or of camera operation; rows without Lynx are included to estimate average Lynx frequency.
- Lynx_ID: unique Lynx identifier intended to be composed of Camera_Trap_Location_ID and a suffix; in this dataset the Lynx ID could not be established (n/a).
- Lynx_Gender_Age: coded categories (e.g., Ad = adult, adf = adult female, adm = adult male, imm = immature); n/a when not determinable.
- Triggering_Event_Duration_Minutes: duration between first and last image/video in a triggering event.
- Day_period: coded time-of-day categories (Night, Twilight, Day) with explicit definitions for the local location (Chornobyl), including how twilight intervals are determined.
- Number_Trapping_Days_Per_Month: total number of days the trap camera operated in a given month.
- Events_Per_Trapping_Day: number of events per trapping day; calculated for records containing Lynx as Number_Trapping_Days_Per_Month divided by Triggering_Event_Duration_Minutes.
- Notes: notes related to Lynx visible in images.
- Data_Used_For_Analysis_Y_Or_N: indicates whether the data were used in the by-site analysis in Gashchak et al. 2022 (Y) or not (N) due to irregular and short-term nature of some data (e.g., all data from 2012 and January–June 2013).