# CHAR_Jun_Nov_2020_Camera_Trap_Image_Cat alogue_Supporting_Document

## Overview
- Describes a camera-trap image catalogue from the Chernobyl exclusion zone following severe wildfires in Ukraine (June–November 2020).
- Aim: support analysis of large mammal activity post-fire with a structured dataset and metadata.

## Data collection and scope
- Study area: Ukrainian portion of the Chernobyl exclusion zone (three sites, each ~80 km2; total around 2600 km2 burnt area in 2020).
- Deployment: motion-activated digital camera traps at three sites (Setup 1) from June 2020 to August 2021; 13 cameras per site (total dataset includes 39 cameras, with 2 cameras excluded due to theft or non-activation).
- Camera specifications: Ltl Acorn 6210MC; infrared (940 nm) flash; PIR sensor; approximate height 0.6–0.7 m; most were oriented north to reduce sun-driven false triggers.
- Setup details: 100 m2 of foreground cleared where necessary; no bait used; poles and measurement poles photographed at deployment to estimate height/distance.
- Triggering and imaging: three-image bursts per triggering event; initial inter-event gap of 90 seconds; 2–4 second recovery between bursts; day/night/transition automatically selected by camera; some time-zone inconsistencies noted for one camera.
- Privacy: images containing people or CHAR staff are catalogued but not included in the image dataset to protect privacy; disturbances from humans are flagged.

## Dataset contents and structure
- Images: 61,736 camera-trap images (Setup 1, June–November 2020) across three sites.
- Catalogue and metadata files:
  - CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue: per-image metadata including species identified, number of animals, triggering event counts, and notes.
  - CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv: camera location coordinates (WGS84), habitat description, ambient dose rate at camera location (µSv/h, June 2020), deployment dates, and other contextual details.
  - CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv: deployment metadata including serial numbers as displayed on images, folder paths, start/end times, duration of deployment, total images, and notes.
- Folder structure: images stored in three main folders—Setup1_Site1, Setup1_Site2, Setup1_Site3; each folder contains sub-folders per camera location (e.g., Setup1_Site1_1570) and per species (e.g., images of each observed species).
- Tables of species: Table 2 lists mammal, bird, and other taxa with the number of image rows per species. Some images are unidentifiable; images containing people/vehicles are catalogued but not included in the dataset.
- Data quality notes: some cameras had issues (e.g., camera 1556 stolen; 1541 not switched on); a camera’s time setting was incorrect (EEST vs. EEST) for camera 0851.
- Summary counts: total species tallies include red deer, Przewalski’s horse, roe deer, red fox, wild boar, and numerous birds and smaller taxa; many images are of unidentifiable species or unidentifiable birds/mammals.

## Metadata, quality control, and conventions
- Data collected and curated by UK Centre for Ecology & Hydrology (UKCEH) with Chornobyl Center field staff; cross-checked by multiple team members.
- Metadata fields include: camera location latitude/longitude (WGS84), habitat description, ambient dose rate at deployment, burn degree within 200 m, and vegetation descriptions.
- Image-level decisions: separate rows for multiple species in a single image; notes indicate when a triggering event includes several species; “service” events (deployment/maintenance) are marked, with some entries noted as “people” when visits occurred mid-deployment.
- Data handling: images containing people and CHAR personnel are catalogued but not shared in the dataset to protect privacy; images of disturbances due to human activity are flagged for potential behavioural interpretation considerations.

## Accessibility and usage notes for Data Leaders
- File formats: JPEG images and MS Excel metadata files; dataset includes both image data and rich descriptive metadata to support reproducible analysis.
- Discoverability: images are organized by site and camera location with explicit coordinates and descriptive context (habitat, burn degree, ambient dose rate).
- Reusability: enables investigations of species presence and relative activity post-fire, correlation with burn degree and ambient radiation, and temporal patterns across sites.
- Standards and interoperability: provides structured columns and definitions (as detailed in Tables 1–4) to facilitate downstream data integration and cross-site comparisons.

## Practical considerations and caveats
- Data limitations:
  - Some cameras were lost or non-operational; not all expected data may be present for every site/camera.
  - Time inconsistencies for one camera; potential timestamp misalignment.
  - A portion of images are unidentifiable; some identifications rely on manual cataloguing.
  - Exclusion of privacy-sensitive images (people, CHAR staff) reduces dataset completeness for those frames.
- Methodological notes:
  - Triggering events defined by PIR activation with a 90-second minimum separation; not all rapid movements may be captured within a single event.
  - Counting approach records total animals per triggering event, with per-image animal counts where possible; does not guarantee unique individual counts.
  - Post-fire context combines camera data with habitat and burn-degree metadata to enable multifactor analyses.

## Acknowledgements and funding
- CHAR project (Chernobyl - a radioactive ecosystem on fire) funded by NERC (Grant NE/V009346/1 and EP/V520846/1); fieldwork assistance acknowledged; data curated by UKCEH and Chornobyl Center staff.