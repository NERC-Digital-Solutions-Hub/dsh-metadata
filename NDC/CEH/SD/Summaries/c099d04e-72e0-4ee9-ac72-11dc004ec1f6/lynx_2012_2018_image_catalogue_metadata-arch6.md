# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalogue for Lynx camera-trap images collected during 2012–2018 as part of Ukrainian programs (NatEnvPr, REDFIRE, TREE).
- Includes both Lynx-related records and non-Lynx trapping periods to support estimation of baseline Lynx frequency.
- Structured around project, site, camera location, timing, and event-level details to enable analysis and product creation (e.g., dashboards, reports).

## Key Fields and Meanings
- Project_ID: Project identifier; values include NatEnvPr (Ukrainian environmental program), REDFIRE, TREE.
- Study_Site: Study site numbers 1–8.
- Setup: Setup period (1–11); Lynx were not identified, so setup may be absent for some rows.
- Camera_Trap_Location_ID / Camera_Trap_Location_ID_Related_To_Project: Numeric IDs for trap locations and their relation to projects.
- Image_Location_Folder_Name: Folder name where images are stored.
- First_Image_Per_Triggering_Event / Last_Image_Per_Triggering_Event: Image filenames for first/last images of a triggering event (not applicable when no Lynx are present).
- Triggering_Event_Number: Sequential event number; total of 265 events (166 not used); a new event starts when the motion sensor triggers; multiple Lynx in the same event share the same event number.
- Date_And_Time_Image_Taken: Date/time of the first image for a triggering event; times corrected to GMT+03:00 (Eastern European winter time) due to potential camera missettings.
- Year / Month: Year and month of image capture or trapping activity; used to facilitate time-based analyses.
- Lynx_ID: Not available; if present, would combine Camera_Trap_Location_ID with a unique suffix (e.g., location + sequence).
- Lynx_Gender_Age: If determinable, categories include adult/adult female (adf), adult male (ad), immature (imm); otherwise n/a.
- Triggering_Event_Duration_Minutes: Duration of the triggering event (first to last image/video clip).
- Day period: Classification of the time of day (Night, Twilight, Day) with specific interval mappings to the local area.
- Number_Trapping_Days_Per_Month: Total trapping days in a given month.
- Events_Per_Trapping_Day: Number of events per trapping day (computed fields for records with Lynx).
- Notes: Notes related to Lynx visible in the image.
- Data_Used_For_Analysis_Y_OR_N: Indicates whether the data were used in the by-site analysis in Gashchak et al. 2022 (Y) or not (N) due to irregular/short-term nature (all data from 2012 and early 2013).

## Data Quality, Gaps, and Handling
- Many fields are marked as n/a or not applicable.
- Lynx_ID is not available; site-specific identification of individuals is not possible in this catalogue.
- Time corrections applied to dates/times; ensure consistent time zone handling in analyses.
- Event count notes: 265 events in total with 166 not used; some data not used in published analyses due to irregular or short-term sampling.
- Rows without Lynx presence included to support estimation of average Lynx frequency across sites.

## Potential Data Products and Analyses for Data Support
- Per-site, per-month activity frequency estimates (including non-Lynx periods for baseline comparisons).
- Day/night/twilight activity distributions across study sites.
- Event duration analysis and distribution across years and sites.
- Aggregated dashboards linking trap locations to geographic coordinates for spatial visualizations.
- Self-serve reports and visualizations (e.g., monthly event counts, trapping days, and data usage status) with provenance notes (Gashchak et al. 2022 as applicable).

## Usage Notes and References
- Some data designated for by-site analysis in Gashchak et al. 2022 (Data_Used_For_Analysis_Y_OR_N = Y).
- Practical uses include building dashboards, performing cross-site comparisons, and guiding data cleaning/quality assurance for further analyses.