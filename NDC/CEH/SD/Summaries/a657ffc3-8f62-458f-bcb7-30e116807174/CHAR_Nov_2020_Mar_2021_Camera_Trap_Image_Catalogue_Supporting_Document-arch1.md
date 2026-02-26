# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue _Supporting_Document

- Purpose and scope
  - CHAR project studying large mammal activity in the Ukrainian part of the Chornobyl Exclusion Zone after extensive wildfires (April 2020).
  - Study design: three sites (each ~80 km²) within the Ukrainian exclusion zone, surveyed from June 2020 – August 2021 to assess post-fire mammal activity.
  - Setup II data cover November 2020 – March 2021 (setup 2): 3 sites, 13 camera traps per site, total of 11633 images catalogued (images taken Nov 2020–Mar 2021; privacy-protected: 692 images of people/vehicles removed from the image set).

- Field methods and camera deployment
  - Equipment: Ltl Acorn 6210MC camera traps; PIR sensor with 940 nm invisible IR flash; daylight/night/transition modes.
  - Mounting: cameras at ~0.6–0.7 m height, usually on trees; north-facing to reduce sun glare; patch cleared in front (~100 m²) when needed.
  - Triggering: three-image burst per trigger; 0–1 s between images; 2–4 s recovery between bursts; new triggering event typically begins after 90 seconds since last observation.
  - Setup details: 13 cameras per site; poles placed for calibration and to capture animal height/distance; no bait used.
  - Data collection: Chornobyl Center deployed/maintained cameras and downloaded images; metadata and site descriptions collected; data quality checked by UKCEH.

- Data structure and content
  - Image catalogue and metadata
    - Fields include: Site, Camera_Location_Identifier, Setup_Number (2), Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period (day/night/transition), Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Sequential, Notes.
    - Images organized in folders by site and camera (e.g., Setup2_Site1_1570) with subfolders per species; images provided as .jpg files; images containing people, vehicles, or CHAR staff servicing cameras are excluded from the dataset.
    - Triggering event numbers are sequential within a given site/camera; a first row for an event shows the total animals; subsequent rows for the same event are marked n/a.
    - For images with “Nothing” in the first frame, notes indicate the likely trigger (e.g., "Camera triggered by Red deer"); unidentifiable species are labeled accordingly.
  - Species table (Table 1)
    - List of mammals and birds observed with two counts: total images attributed to the species (including frames where the species wasn’t visible) and images where the species was visible.
    - Examples: Red deer 4491/4052; Przewalski’s horse 771/694; Wolf 546/375; Roe deer 792/654; Elk 1617/1387; Red fox 201/122; Unidentifiable mammals 213/94; Bird examples include Tawny owl, Great tit, Bullfinch, Spotted nutcracker; Disturbance entries include People 93/87 and Vehicles 9/9; Service entries 590/545 (images catalogued but not provided).
  - Site descriptions file
    - Setup2 site-level data (Site, Camera_Location_Identifier, coordinates, description, ambient dose rate, deployment dates, days in operation, etc.).
    - Ambient dose rates measured at camera locations (µSv h⁻¹) using a radiometer; several habitat notes and vegetation descriptions; distance trails observed within ~20 m; fire-burn degree near camera locations (categories None/Low/Medium/High/Very high/Total destruction); vegetation species listed (e.g., alder, aspen, birch, pine species, oak, willow, grasses, nettle, etc.).
    - All descriptive parameters were recorded by the same individual.
  - Camera details file
    - Setup 2 specifics: Start/End deployment times, number of days in operation, number of images taken, camera serial numbers as displayed on images, and folder identifiers.
    - Noted incidences: camera location 1575 and camera serial 2081 were stolen during setup 2.
  - Data provenance and references
    - For setup 1 data, see Barnett et al., 2022 (Wildlife camera-trap photographs from the Chornobyl Exclusion Zone, setup 1 and 2 context in that publication).

- Notable findings and dataset characteristics
  - Species richness and abundance
    - The dataset provides counts of images where species were seen and counts including frames where the species was not visible.
    - Highest image counts observed for Red deer and Przewalski’s horse among mammals; significant counts for Elk and Roe deer; notable presence of wolves and foxes; several unidentifiable mammal/bird images.
  - Human disturbance and privacy
    - Images containing people or vehicles are catalogued but the actual images are excluded to protect privacy; disturbance metadata is still recorded (e.g., number of people/vehicles per triggering event).
  - Post-fire and environmental context
    - Fire burn degree around camera sites recorded, with no sites categorized as Very high or Total destruction in setup 2; ambient dose rates captured at each camera location provide environmental radiation context.
    - Habitat descriptions and vegetation lists accompany site data to support habitat-association analyses.

- Data quality, limitations, and considerations for analysts
  - Data completeness and access
    - Some data gaps due to theft of cameras (sites/sites identifiers affected); 692 images of people/CHAR staff excluded from the image set.
    - Setup 1 data referenced but not included here; detailed context available in Barnett et al. 2022 for setup 1.
  - Detection and sampling constraints
    - Triggering rules may miss fast-moving animals due to short burst window and ~90-second gap between events.
    - Images include detection bias from camera placement, habitat obscurity, and the presence of disturbance in the vicinity.
  - Temporal scope
    - Data cover November 2020–March 2021 for setup 2; broader temporal context may be obtained from Barnett et al. (setup 1) and the project’s ongoing data.
  - Data usage implications
    - Suitable for occupancy models, abundance estimates from image counts, activity patterns (day/night/transition), and analyses of environmental correlations (burn degree, ambient dose rate, habitat features).
    - Caution required when combining with other datasets due to different scales, missing data, and the privacy-excluded images.

- How to access and utilise the data
  - Data are organized into multiple files and folders within the project materials:
    - CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue: image-level catalogue (11633 images, minus privacy-excluded frames).
    - CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions: site-level habitat and environment data.
    - CHAR_Nov_2020_Mar_2021_Camera_Trap_Details: camera deployment metadata.
  - Key analytical opportunities
    - Occupancy/detection probability modeling by species with site- and camera-level covariates (burn degree, ambient dose rate, habitat type).
    - Species-specific activity and presence patterns across day/night/transition periods.
    - Associations between wildlife presence and fire impact gradients near camera locations.
    - Cross-site comparisons among high, mid, and low contamination zones to assess ecological responses post-fire.
  - Related resources
    - Barnett et al. (2022) for setup 1 context and methodology.
    - Data provenance and acknowledgment of funding and contributors (NERC, CERAD).

- References and acknowledgements
  - Barnett, C.L.; Gashchak, S.; Wood, M.D.; Beresford, N.A. (2022). Wildlife camera trap photographs from the Chornobyl Exclusion Zone, Ukraine (June 2020 - November 2020) following extensive wildfires. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/9bd7754d-ea874b35-bec1-f39d5cc76db6
  - Acknowledgements: thanks to field assistants; funding from NERC (NE/V009346/1 and EP/V520846/1) and CERAD for supporting data preparation.