# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue _Supporting_Document

- Acknowledges the CHAR project’s aim to assess large mammal activity in the Ukrainian Chornobyl Exclusion Zone after wildfires (Nov 2020–Mar 2021 setup 2), using motion-activated camera traps across three 80 km2 sites.
- Cameras operated June 2020–Aug 2021 in the broader study; this document covers setup 2 (Nov 2020–Mar 2021) data and metadata.
- Data were collected to enable wildlife presence, abundance indicators, and ecological responses to post-fire environments, with the goal of enabling data use across topics and by non-specialists.

## Data content and overall structure

- Three camera trap sites (Setup 2) within the Ukrainian Exclusion Zone; each site contains multiple camera locations (unique identifiers).
- Primary data product: CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue containing 11,633 individually catalogued images from Nov 2020–Mar 2021.
- Complementary metadata files:
  - CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions
  - CHAR_Nov_2020_Mar_2021_Camera_Trap_Details
- Images physically organized in dataset folders by site and camera (e.g., Setup2_Site1_1570) with subfolders per species (e.g., Red deer, Eurasian elk, etc.) and accompanying image files (.jpg).
- Privacy note: 692 images containing people, vehicles, or CHAR staff were catalogued but excluded from image files to protect privacy.

## Data fields and interpretation (Camera Trap Image Catalogue)

- Core fields for each image record:
  - Site, Camera_Location_Identifier, Setup_Number
  - Image_Location_Folder_Name, Image_Filename
  - Date, Time, Day_Period
  - Species_Common_Name, Number_Animals_In_Image
  - Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Sequential
  - Notes (including suppositions about triggering species when first image is empty)
- Triggering events:
  - A triggering event is a sequence initiated by a camera sensor; typically a new event starts after ~90 seconds since last observation.
  - The first row for an event contains the total number of animals; subsequent rows for the same event are marked n/a.
- Special cases:
  - For images with nothing, “Camera triggered by [species]” may be noted; if species is unidentifiable, a question mark may be appended (e.g., Red deer?).
  - Images marked as “Service” relate to deployment/maintenance and are not included in the image files; their numbers are recorded as n/r (not recorded) or None.
  - For images with people or vehicles, counts of people/vehicles are recorded; these are flagged as disturbance-related data.
- Coverage by species:
  - Table 1 provides counts of images (total vs. visible) per mammal and bird species, including an “Unidentifiable” category.
  - Notable entries include Red deer (Cervus elaphus) 4491/4052 and Przewalski’s horse (Equus ferus przewalskii) 771/694, among others.
  - People: 93/87 images; Vehicles: 9/9 images; Service: 590/545 images (note: the latter are included in counts but not in image files).

## Site descriptions and environmental metadata

- CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions contains per-site metadata for Setup 2:
  - Site, Camera_Location_Identifier, and geographic coordinates (GPS-derived WGS84 decimal degrees)
  - Camera location description (habitat context)
  - Ambient dose rate at camera location (µSv/h)
  - Description of animal trails within ~20 m of the camera
  - Degree of burn/impact from fire within 200 m of the camera location (None to Total destruction scale)
  - Vegetation and habitat notes (e.g., alder, birch, pine, oak, grasses, nettle, etc.)
  - All descriptive parameters were recorded by the same data collector

## Camera deployment details

- CHAR_Nov_2020_Mar_2021_Camera_Trap_Details includes per-setup information:
  - Setup 2 (Nov 2020–Mar 2021): Start/End deployment times (Eastern European Summer Time, with one noted exception for camera 1575)
  - Camera_serial_number as displayed on images; notes about theft (e.g., location 1575 stolen)
  - Folder names where images are located (e.g., Setup2_Site1_1570)
  - Number of days in operation; total images taken
  - Notes about deployment context

## Data processing, quality control, and caveats

- Data were quality checked by UKCEH staff; queries resolved as needed.
- Time data and time zones may include a known exception (camera 1575) where times were set incorrectly to Easter European Summer Time.
- The dataset built on prior Setup 1 data (Barnett et al., 2022) for continuity.
- The dataset provides a robust basis for cross-site comparisons, occupancy or abundance modeling, and integration with environmental covariates (habitat descriptions, burn severity, ambient dose rate).

## How this data can be used (Data Support perspective)

- Enable self-serve exploration of species presence and relative abundance indicators across sites and cameras.
- Combine image-derived data with site-level environmental metadata (habitat type, burn degree, vegetation, dose rates) for ecological analyses.
- Build dashboards or reports to summarize site-level activity (e.g., most frequently photographed species, event-level counts, disturbance from humans or vehicles).
- Facilitate data sharing with stakeholders while preserving privacy for images containing people or staff.

## References and acknowledgements

- Barnett, C.L.; Gashchak, S.; Wood, M.D.; Beresford, N.A. (2022). Wildlife camera trap photographs from the Chornobyl Exclusion Zone, Ukraine (June 2020 - November 2020) following extensive wildfires. NERC EDS Environmental Information Data Centre. DOI link provided in the supporting document.
- Funding: NERC (NE/V009346/1; EP/V520846/1) with additional support from CERAD (Norway) for data preparation. Acknowledges field assistance and local collaborators.