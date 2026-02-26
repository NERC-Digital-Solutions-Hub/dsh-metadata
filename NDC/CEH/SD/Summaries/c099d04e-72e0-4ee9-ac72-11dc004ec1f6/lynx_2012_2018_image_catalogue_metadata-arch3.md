# Lynx_2012_2018_Image_Catalogue_Metadata

## Overview
- Metadata catalogue for Lynx camera-trap images collected 2012–2018 as part of Ukrainian national environmental studies and international projects (NatEnvPr, REDFIRE, TREE).
- Designed to capture image- and event-level data to assess Lynx activity, frequency, and timing, and to support evaluation of environmental monitoring decisions and policy implications.
- Includes both Lynx-containing and non-Lynx records to enable frequency estimation; some fields are not applicable when Lynx could not be identified.

## Key metadata elements

- Project and study context
  - Project_ID; Explanation includes project identifiers (NatEnvPr, REDFIRE, TREE).
  - Study_Site; Setup period (1–11); Note: Lynx IDs may be unavailable, so some fields are not applicable.
- Location and image data
  - Camera_Trap_Location_ID; Camera_Trap_Location_ID_Related_To_Project; Image_Location_Folder_Name.
- Lynx observations and identifiers
  - Lynx_ID: Unique ID formed from Camera_Trap_Location_ID and a suffix; often not possible to assign.
  - Lynx_Gender_Age: Adult/immature determinations when possible (e.g., Ad, AdF, AdM, imm); may be not applicable.
  - Notes related to Lynx in images.
- Time, date, and temporal context
  - Date_And_Time_Image_Taken; Year; Month.
  - Date/time corrected to Eastern European winter time (GMT+03:00) if camera clock was mis-set.
  - Day period classification: Night, Twilight, Day, with explicit interval definitions for the study area.
- Events and triggering
  - Triggering_Event_Number: Sequential event number; new event starts when motion sensor is triggered; multiple Lynx in same event share the same triggering event.
  - First_Image_Per_Triggering_Event and Last_Image_Per_Triggering_Event: Filenames of first/last images in an event (not applicable when Lynx not present).
  - Triggering_Event_Duration_Minutes: Time span of a triggering event.
  - Day period, Number_Trapping_D days per Month, Events_Per_Trapping_Day: Metrics to characterize activity and sampling effort.
- Data used for analysis
  - Data_Used_For_Analysis_Y_Or_N: Indicator of whether the data were used in site-level analyses (e.g., Gashchak et al. 2022); values indicate usage or not applicable.
  - Notes: Additional interpretation or caveats about records.
- Data completeness and notes
  - Some rows include n/a or not applicable fields (e.g., Lynx_ID when identification is not possible).
  - Notes section captures context or data quality remarks.
- Data usage and publication context
  - Indicates that only part of the data were used for the by-site analysis in Gashchak et al. 2022 due to irregular/short-term studies in 2012–early 2013.

## Data quality, transformations, and governance

- Data quality considerations
  - Frequent absence of Lynx IDs and limited gender/age determinations; metadata gaps require careful interpretation.
  - Correcting timestamps to a consistent time zone introduces a processing step prior to analysis.
  - Some records are irregular or short-term, limiting their suitability for certain analyses.
- Metadata completeness and transformation
  - Some fields are not directly applicable for all records and require interpretation (e.g., several n/a fields).
  - Time-of-day categorization relies on local sunrise/sunset calculations for the study area.
- Data governance and sharing
  - Dataset supports transparency about data sources, processing, and analysis, but certain entries may pose accessibility or applicability challenges due to missing identifiers or non-uniform data.
  - Clear documentation of which data contributed to published analyses (e.g., Gashchak et al. 2022) aids reproducibility and monitoring accountability.

## Data usage and publication references

- Used in by-site analysis in Gashchak et al. 2022 for a subset of the data.
- Other records were not used for that analysis due to irregularity and short-term nature of the studies (2012 and January–June 2013), highlighting the importance of data standardization and consistent sampling for policy-relevant monitoring.

## Implications for Monitoring Frameworks

- Standardized metadata supports robust monitoring by enabling cross-site comparability of camera-trap data, event-based activity metrics, and temporal activity patterns.
- Explicit handling of data gaps, time-zone corrections, and non-identifiable Lynx records informs data quality controls and governance requirements.
- The catalogue demonstrates how to document sampling effort, event definitions, and data usage flags to inform policy evaluation and future decision-making.
- Highlights common barriers for monitoring frameworks: data gaps, data access, organizational silos, data-sharing constraints, metadata adequacy, data transformation needs, clear communication of findings, and establishing data governance.