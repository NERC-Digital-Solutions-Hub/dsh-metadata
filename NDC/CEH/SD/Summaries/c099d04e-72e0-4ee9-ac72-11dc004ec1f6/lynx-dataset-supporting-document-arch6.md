# Lynx_Dataset_Supporting_Document

- Overview
  - A catalogue of motion-activated digital trap camera images (and some videos) of Eurasian Lynx (Lynx lynx) in the Chornobyl Exclusion Zone (CEZ), Ukraine, collected over 2012–2018.
  - Data come from three projects (TREE, NatEnvPr, REDFIRE) with different study designs; cameras aimed to capture medium-large mammals but not designed for quantitative abundance estimates of Lynx.

- Data provenance and projects
  - TREE: 2014–2016; funded by NERC, Environment Agency, RWM; random camera relocations within sites after 8–9 weeks.
  - NatEnvPr: 2012–2018; supported by Ukraine’s Ministry of Ecology and Natural Resources.
  - REDFIRE: 2016–2017; funded by NERC.
  - All projects used camera traps without bait.

- Study area and sites
  - CEZ area: ~2600 km2 in northern Ukraine; varied habitats with increasing forest cover (2012–2018) and numerous lakes, rivers, marshes.
  - Eight study sites within CEZ; 394 unique camera trap locations (some locations reused across projects).
  - Cameras deployed for up to 8–12 months per site (TREE deployments were shorter and relocated within sites).
  - Human activity minimal; 2016–onward Chornobyl Biosphere Reserve established.

- Digital trap cameras and deployment
  - Common models include Ltl Acorn 6210 MC, Browning BTC5/BTC-7FHD-PX, Bushnell models, ScoutGuard, Weltar, among others.
  - Settings: mostly still images, 3 images per trigger, 0–5 s delay between images; maximum infrared power used; recovery time 3–10 s.
  - Some cameras recorded video (from 2016–2018 for some models); alignment to reduce false triggers (facing away from direct sun, vegetation cleared).
  - Placement: ~0.5–1.1 m above ground, near trails or at intersections; cameras attached to trees or vertical poles; efforts to remain inconspicuous where risk of detection by people existed.
  - Field procedures: up to 20 measuring poles placed in front of cameras during initial deployment to calibrate scale; poles removed after photos were captured.

- Data structure and catalogues
  - Lynx_2012-2018_Image_Catalogue: records per triggering event with fields including:
    - Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, Location IDs, Image_Location_Folder_Name
    - First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event, Triggering_Event_Number
    - Date_And_Time_Image_Taken, Year, Month, Lynx_ID, Lynx_Gender_Age
    - Triggering_Event_Duration_Minutes, Day period, Number_Trapping_Days_Per_Month, Events_Per_Trapping_Day
    - Notes, Data_Used_For_Analysis_Y/N
    - Handling of multiple Lynx in a single image (duplicates with separate Lynx data)
  - Lynx_Camera_Details: camera- and site-level metadata including:
    - Project_ID, Camera_Trap_Location_ID, Location IDs, GPS coordinates (Latitude/Longitude, WGS84)
    - Site, Year, Setup, Date/Time of Setup and Last Day of Operation (Eastern European Winter Time)
    - Camera make/model, Camera_ID, Deployment duration, counts of images/videos
    - Height, Distance to nearest trail, Orientation, Tilt, Generic Conditions
    - Ambient dose rate at site (micro-Sv/h) at deployment year
  - Image storage and referencing
    - Images and videos organized in folders named SetupXX_SiteY_ZZZ (matching Image_Location_Folder_Name)
    - Measuring poles images stored alongside Lynx images
    - Quality control by UKCEH staff to ensure all observed Lynx were captured and catalogued; queries resolved as needed

- Image data details
  - Total Lynx-related outputs: 1570 still images and 23 videos of Lynx; plus 32 images of measuring poles.
  - Not all cameras recorded Lynx; some events contain no Lynx imagery.
  - Image catalogues include records for events with Lynx presence and also events without Lynx to aid estimation of average Lynx frequency if needed.
  - Where individual Lynx could be identified by features (spot pattern, gender, size), a unique ID was assigned; otherwise, the animal was not uniquely identified.
  - Image quality varies by camera model, lighting, time of day, and Lynx behavior.

- Data usage and quality notes
  - Some rows are designated Data_Used_For_Analysis_Y/N to indicate inclusion in site-level analyses (e.g., Gashchak et al., 2022).
  - Data quality controlled by field teams; issues with irregular or short-term data may exclude some rows from certain analyses.
  - Metadata enables end users to estimate presence, frequency, and potential individual identification, though not intended for robust population density estimation.

- Spatial and temporal metadata
  - Timestamps provided in local European winter time (GMT+03:00) for camera setup and operation.
  - GPS coordinates for camera locations with approximate accuracy (~7.7 m).
  - Ambient radiation dose rates recorded at camera sites when deployed.

- References and acknowledgments
  - References to Ukrainian presidential decree establishing the Chornobyl radiation and ecological biosphere reserve (2016) and related Ukrainian forestry documentation.
  - Related publications: Gashchak et al. on Lynx population density estimation and earlier bear-related camera-trap work in the CEZ.
  - Acknowledgments to field assistance and collaborators.