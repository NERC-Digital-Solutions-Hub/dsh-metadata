# Lynx_Dataset_Supporting_Document

## Overview
- A dataset comprising motion-activated digital trap camera images (and videos) of Eurasian Lynx (Lynx lynx) in the Ukrainian Chornobyl Exclusion Zone (CEZ), collected over 2012–2018.
- Data come from three projects (TREE, NatEnvPr, REDFIRE) with differing study designs; cameras aimed to capture medium-large mammals but not designed for quantitative lynx abundance/density estimates.
- Includes 1570 still images, 23 videos of Lynx, plus 32 measuring-pole images; images are catalogued with associated metadata and camera deployment details.
- Serves as a resource for monitoring framework authors to assess data availability, metadata quality, provenance, and potential for informing policy and future monitoring decisions.

## Study Area and Sites
- CEZ covers ~2600 km2 in northern Ukraine with varied habitats (extensive forests, wetlands, small lakes, rivers) and largely limited human activity; a Chornobyl Biosphere Reserve was established in 2016.
- Eight study sites within the CEZ; cameras deployed at 394 unique locations (some locations used by multiple projects).
- Deployments: most cameras at a site for 8–12 months; TREE project deployments were 8–9 weeks per location with relocation within the same site.
- No bait used; site descriptions draw on Development (2006) and field observations.

## Data Collection Methods and Equipment
- Digital trap cameras: primarily Ltl Acorn 6210 MC; other models included Browning, Bushnell, ScoutGuard, Weltar, and CCBetter.
- Camera configuration: most settings recorded three images per triggering event with 0–5 second delay; infrared flash at maximum power; recovery times 3–10 seconds; temperature-dependent sensor sensitivity with seasonal adjustments; some videos were recorded (notably later in the study).
- Placement strategies: cameras facing away from direct sunlight to reduce false triggers; vegetation regularly cleared; typical height 0.5–1.1 m; positioned near animal activity areas (paths, bridges, intersections).
- Field procedures: up to 20 measuring poles (1 m tall, evenly spaced) placed in front of cameras during deployment to aid calibration; poles later removed; in some locations poles were not photographed.
- Deployment details: cameras mounted on trees or vertical posts; orientation and tilt recorded; some deployments random (TREE) vs. more systematic placements.

## Datasets and Metadata Structure
- Lynx_2012-2018_Image_Catalogue: per-triggering-event records with fields including Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, Location_Name, Image_Location_Folder_Name, First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event, Triggering_Event_Number, Date_And_Time_Image_Taken, Year/Month, Lynx_ID, Lynx_Gender_Age, Triggering_Event_Duration, Day_Period, Data_Used_For_Analysis_Y/N, and Notes.
- Lynx_Camera_Details: per-camera deployment metadata including Project_ID, Camera_Trap_Location_ID, coordinates (lat/long, WGS84), Site, Year, Setup, Deployment times, ambient dose rate (micro-Sv/h), Make/Model, Camera_ID, Deployment Duration, counts of images/videos, height, distance to nearest trail, Orientation, Tilt, and Generic_Conditions.
- Unique Lynx IDs are assigned when identifiable features exist (Camera_Trap_Location_ID + sequence number); otherwise, Lynx entries may be non-identifiable.
- Output folders and file naming conventions standardize access to images and poles; quality control ensured all observed Lynx images were provided and queries resolved.

## Data Quality, Gaps, and Limitations
- Not designed for quantitative density/abundance estimates; primarily presence/trigger data and qualitative features.
- Variability across camera models and settings, including recovery times and sensor sensitivity, impacts detectability.
- Some cameras did not record Lynx; not all triggers contained Lynx data; data flagged in the catalogue (Data_Used_For_Analysis_Y/N) for site-specific analyses.
- Potential for missed detections due to camera recovery times and environmental conditions; field methods included measures to reduce false activations, but some false positives/negatives may remain.
- Metadata completeness is mixed; some records may lack certain fields or precise timing details depending on project and deployment period.
- Data integrity relies on multiple teams and field coordinators; quality control steps are documented, but cross-project standardization is limited by differing original designs.

## Governance, Access, and Use in Monitoring Frameworks
- Data provenance and cross-project integration are explicit, with standardized fields to facilitate meta-analyses and comparability.
- Clear documentation of deployment times, camera settings, and site conditions supports evaluation of data quality and suitability for monitoring indicators.
- The dataset includes explicit flags for data used in analyses, aiding transparency in policy-relevant monitoring assessments.
- Public sharing considerations are noted as a governance concern in monitoring practice contexts; while the dataset provides rich metadata, policies regarding data sharing, licensing, and long-term accessibility should be considered in monitoring frameworks.
- The dataset is connected to published analyses (e.g., Gashchak et al. 2022) and to broader reports on Chornobyl site ecology, providing pathways for policy-relevant interpretation.

## Implications for Monitoring Frameworks and Policy
- Provides a rich source of presence/trigger data and site-specific camera metadata that can inform:
  - Detection probability assessments and occupancy modelling in wildlife monitoring.
  - Evaluation of methodological gaps in camera-trap monitoring within restricted or unique landscapes (e.g., CEZ).
  - Data governance best practices: metadata completeness, provenance, versioning, and open data considerations.
- Highlights the importance of standardized metadata schemas to enable cross-project comparability and systematic policy evaluation.
- Demonstrates challenges in data sharing and timeliness, emphasizing need for clear governance, data inventories, and open-data practices in monitoring frameworks.

## Acknowledgements and References
- Acknowledges field assistance (e.g., Igor Chyzhevsky, Maksim Krachkovsky).
- References include:
  - Decree of the President of Ukraine (2016) establishing the Chornobyl radiation and ecological biosphere reserve.
  - Development 2006 forestry project in the Chornobyl area.
  - Gashchak et al. works on lynx density estimation and other CEZ fauna studies.
- Data provenance and project sources (TREE, NatEnvPr, REDFIRE) are documented for traceability.