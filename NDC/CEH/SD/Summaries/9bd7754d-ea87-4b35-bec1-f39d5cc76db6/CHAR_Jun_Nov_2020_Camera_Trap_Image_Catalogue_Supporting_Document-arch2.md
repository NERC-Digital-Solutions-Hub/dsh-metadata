# CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue_Supporting_Document

- Purpose and context
  - Assess large mammal activity after wildfires in the Ukrainian portion of the Chernobyl Exclusion Zone (June 2020–August 2021) to understand environmental health and policy performance over time.
  - Three study sites (each ~80 km2) within the exclusion zone were used to evaluate mammals along a contamination gradient after a major fire (June–Nov 2020 dataset window labeled as Setup 1).

- Study design and sampling
  - Camera deployment
    - 39 cameras total (13 per site) randomly located across three sites: Site 1 (northeast, most contaminated), Site 2 (western plume trace, large contamination gradient), Site 3 (south, least contaminated).
    - Cameras: Ltl Acorn 6210MC; mounted at ~0.6–0.7 m height, usually tree-mounted, facing predominantly north.
    - Setup in front of each camera included 16 poles laid out in three parallel rows to estimate animal height and distance; poles removed after capture; images of poles included in dataset for calibration.
    - No bait used; area in front cleared (~100 m2) to reduce false triggers; PIR sensor with 940 nm invisible infrared flash; day/night/transition mode is automated but subjective.
  - Image capture and triggering
    - Each camera set to three-image burst per triggering event; 0–1 s between images; 2–4 s recovery between bursts; new triggering event begins after at least 90 s since last observation (some sequences may represent a single extended event).
    - Triggering events recorded with sequential numbering per site/camera; images from events may contain multiple animals or species.
  - Deployment timing and privacy
    - Fieldwork conducted June 2020–August 2021; dataset covers June–November 2020 (Setup 1).
    - Images containing people, vehicles, or CHAR team members were catalogued but not included in the image dataset to protect privacy; disturbances from human activity are flagged in notes.

- Data structure and contents
  - Catalogue and metadata
    - Image catalogue file: CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue
      - Key columns include: Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period, Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Number_Sequential, Young_Animal_In_Image, Notes.
      - Notes clarify multi-species images, service/ disturbance entries, and how triggering events are recorded.
  - Site and camera descriptions
    - Site descriptions file: CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv
      - Includes: camera coordinates (WGS84), habitat descriptions, ambient dose rates at the camera location (June 2020, using ATOMEX dosimeter), descriptions of animal trails within 20 m, burn degree from fire within 200 m, and vegetation lists.
  - Camera details and image summaries
    - Camera details file: CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv
      - Includes: setup, site, camera serial number as shown on images, folder location of images, deployment start/end times (Eastern European Summer Time), number of deployment days, total images captured, and general notes.
  - Image storage and organization
    - Images are organized in three main subfolders by site and setup: Setup1_Site1, Setup1_Site2, Setup1_Site3; within each, subfolders per camera location (e.g., Setup1_Site1_1570), and further subfolders by species name with individual image files (JPEGs).
  - Dataset scope and scale
    - Total images: 61,736 captured during Setup 1 (June–November 2020); dataset focuses on occurrences of mammals, birds, insects, and other groups; some images are unidentifiable due to quality.
  - Species and observations
    - Table 2 enumerates observed taxa (mammals, birds, insects) with the number of image rows per species; includes common mammals such as red deer, Przewalski’s horse, roe deer, wild boar, red fox, Eurasian elk, and others; unidentifiable images are noted.
    - Images containing people or vehicles are catalogued (for disturbance assessment) but excluded from the dataset; where multiple species appear in a single image, separate rows are created for each species.

- Data quality, processing, and governance
  - Data entry and QA
    - Single UKCEH staff member populated the image catalogue; quality assurance performed by a second UKCEH staff member and the Chornobyl Centre.
    - Descriptive parameters for sites were provided by the Chornobyl Centre; cross-checked for accuracy.
  - Timekeeping and localization
    - Times are primarily Eastern European Summer Time; one camera (serial 0851) was incorrectly set to Eastern European Winter Time.
    - Some first-row triggering-event data show total animals; subsequent rows for the same event may be blank (n/a) to avoid duplication.
  - Privacy and ethics
    - Images with people, vehicles, or CHAR field team activity removed from image dataset to protect privacy; still catalogued with notes on disturbance where relevant.

- Accessibility and uses for environmental analysis
  - The standardized catalogue and accompanying site/camera descriptors enable integration with other environmental datasets to evaluate mammal activity, habitat use, and potential impacts of fire-related changes and contamination gradients.
  - Clear documentation of data structure, variable definitions, and QC steps supports reproducibility and policy performance assessments over time.
  - Potential analyses include occupancy or abundance indicators by species, activity patterns by time of day, and correlation with burn degree and ambient radiation gradients.

- Limitations and considerations for analysts
  - Temporal scope limited to Setup 1 (June–November 2020); additional data from 2021–2022 would be needed for longer-term trend analysis.
  - Some cameras were lost (e.g., camera 1556 stolen) or failed (camera 1541 not switched on); gaps exist in spatial coverage.
  - Day/Night/Transition classification is automated and may be subjective; time stamps rely on time zone accuracy with known exception.
  - Disturbance from human activity is acknowledged but not quantified in image data; remains a consideration for interpreting wildlife activity.

- Acknowledgments and funding
  - CHAR (Chernobyl - a radioactive ecosystem on fire) project funded by NERC (Grant NE/V009346/1 and EP/V520846/1).
  - Fieldwork and data collection supported by Chornobyl Centre personnel; data curation conducted by UKCEH.