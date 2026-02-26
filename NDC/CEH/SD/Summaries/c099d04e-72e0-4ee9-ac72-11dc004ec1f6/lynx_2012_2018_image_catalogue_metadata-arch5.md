# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalogue for Lynx camera-trap images collected during 2012–2018.
- Part of studies including NatEnvPr (Ukrainian national program of environmental studies), REDFIRE, and TREE.
- Captures data across multiple study sites (1–8) and camera-trap locations, with setup periods defined (1–11) where applicable.
- Includes records both with and without Lynx to enable estimation of Lynx frequency and activity.
- Some sites/records were used in downstream analyses (e.g., by-site analysis in Gashchak et al. 2022) and others not, due to irregular or short-term data collection.

## Data Schema / Key Fields
- Project_ID: Identifier for the project the images come from (e.g., NatEnvPr, REDFIRE, TREE).
- Study_Site: Numerical study site (1–8).
- Setup: Setup period related to the project (1–11). Note: not applicable when Lynx not identified.
- Camera_Trap_Location_ID: Numeric ID for each camera trap location.
- Camera_Trap_Location_ID_Related_To_Project: Numeric ID linking camera location to project.
- Image_Location_Folder_Name: Folder name where the images are stored.
- First_Image_Per_Triggering_Event / Last_Image_Per_Triggering_Event: Filenames of first/last image in a triggering event; not applicable when no Lynx.
- Triggering_Event_Number: Sequential event number; some numbers may be unused (e.g., 166).
- Date_And_Time_Image_Taken: Timestamp for the first image of a triggering event; corrected to Eastern European winter time (GMT+03:00) if camera times were mis-set.
- Year / Month: Year and month when Lynx images were taken or when the trap was operating (records without Lynx are included for frequency estimation).
- Lynx_ID: Unique ID for each Lynx (constructed from Camera_Trap_Location_ID and a unique suffix). Not available when Lynx could not be identified.
- Lynx_Gender_Age: Categorical coding for gender/age (adult/adult female/adult male/immature or not applicable).
- Triggering_Event_Duration_Minutes: Duration between first and last image/video clip of a triggering event.
- Day_period: Time of day classification (Night, Twilight, Day) using location-specific definitions.
- Number_Trapping_Days_Per_Month: Total days the trap was operating per month.
- Events_Per_Trapping_Day: Number of events per trapping day (calculated for Lynx-containing records).
- Notes: Any notes related to Lynx visible in the image or other context.
- Data_Used_For_Analysis_YorN: Indicates if the data were used in the by-site analysis (Y) (as per Gashchak et al. 2022) or not (N) due to irregular/short-term nature of data.

## Data Quality & Curation
- Time alignment: All date/time values adjusted to GMT+03:00 (Eastern European winter time) to correct mis-set camera clocks.
- Data completeness: Many fields are “n/a” when not applicable (e.g., Lynx_ID not possible, or no Lynx identification).
- Data granularity: Includes records both with Lynx and without to enable frequency estimation.
- Event integrity: Some triggering events are skipped or unused (e.g., Triggering_Event_Number 166 not used; total events noted as 265).
- Documentation: Catalog entries include clear definitions and unit conventions, with explicit explanations for each field.

## Provenance & Time Normalization
- Date and time normalization is applied to ensure consistency across datasets and to support cross-site analyses.
- Notes clarify potential discrepancies between image timestamps and real-world time when cameras were mis-set, and the corrective approach taken.

## Data Access, Sharing & Usage
- The metadata is organized to support dataset publication, discovery, and reuse via relevant portals or catalogues.
- Some data are explicitly flagged for inclusion in specific analyses (e.g., by-site analysis in Gashchak et al. 2022) and others are retained for frequency estimation.
- Clear indicators of where data are incomplete or not applicable, guiding responsible reuse and interpretation.

## Constraints & Limitations
- Incomplete user data: Several fields are n/a when Lynx was not identified or when data collection did not apply to a given record.
- Temporal gaps: Some study periods or sites have irregular or short-term data, limiting their suitability for certain analyses.
- Heterogeneous data collection: Variations in site setup, camera configurations, and event recording require careful harmonization for cross-site comparisons.

## Governance Implications for Data Stewards
- Ensure ongoing metadata completeness and consistency as new data are added (e.g., updates to Lynx_ID, gender/age determinations, or event counts).
- Maintain standardized time normalization across all records and document any subsequent corrections.
- Preserve original data lineage (image filenames, location IDs, and event numbers) to support reproducibility.
- Clearly indicate data usage status (Data_Used_For_Analysis_YorN) to guide researchers on which records fed into published analyses.
- Provide guidance on interpreting records with n/a fields and those lacking Lynx identification to prevent misinterpretation.
- Facilitate discoverability by organizing and linking location IDs, project IDs, and study sites within catalogue portals for ease of reuse by data creators and data users.