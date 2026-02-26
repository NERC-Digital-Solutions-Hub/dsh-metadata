# CHAR_Jun_Nov_2020_Camera_Trap_Image Catalogue Supporting Document

## Overview and Aim
- Describes the CHAR project study of large mammal activity following the 2020 fires in the Ukrainian portion of the Chernobyl exclusion zone.
- Field deployment: June 2020 to August 2021 across three sites (each ~80 km²) with 13 camera traps per site.
- Dataset scope: Setup 1 images from June–November 2020, totaling 61,736 camera-trap images; three site folders with per-camera subfolders and per-species image groupings.
- Purpose for data stewards: document data governance, provenance, metadata standards, and quality control to ensure discoverability, reusability, and compliant sharing.

## Data Collection and Methods
- Equipment: 39 cameras (13 per site) of model Ltl Acorn 6210MC; PIR motion sensors and 940 nm infrared flash; daytime and nighttime imaging.
- Deployment details: Cameras mounted at 0.6–0.7 m height, usually facing north; area clearance in front of each camera to ~100 m²; no bait used.
- Triggering and imaging: Three-image burst per triggering event with 0–1 s between shots; ~2–4 s recovery between bursts; new triggering event begins after 90 seconds since last observation (may blend into same sequence).
- Data management: Images and metadata downloaded November 2020; catalogue populated with species, counts, triggering events, and notes.
- Privacy and ethics: Images containing people or CHAR team members are catalogued but not included in the dataset to protect privacy; 76 images featuring people excluded from the dataset.
- Data gaps: Camera 1556 stolen; camera 1541 not turned on; some images missing due to these issues.

## Dataset Structure and Content
- Core data files:
  - CHAR_Jun_Nov_2020_Camera_Trap_Image_Catalogue.csv: image-by-image catalogue with fields describing site, camera, setup, location folder, image filename, date/time (Eastern European Summer Time, with one DST note), day period, species name, counts, triggering event data, and notes.
  - CHAR_Jun_Nov_2020_Camera_Trap_Site_Descriptions.csv: site-level metadata including GPS coordinates (WGS84), habitat description, ambient dose rate (µSv/h), animal-trail descriptions, burn degree within 200 m of camera, and vegetation notes.
  - CHAR_Jun_Nov_2020_Camera_Trap_Details_And_Image_Summary.csv: deployment details per camera (start/end times, number of days deployed, total images), camera serial numbers as displayed on images, folder locations, and general notes.
- Data organization and access:
  - Images stored in three top-level folders by site: Setup1_Site1, Setup1_Site2, Setup1_Site3.
  - Within each site, images are organized into per-camera folders (e.g., Setup1_Site1_1570) and further into per-species subfolders containing individual image files (.jpg).
  - Image catalogue rows may include multiple rows per image if more than one species is present; images containing people or CHAR staff are catalogued but not provided in the dataset.
- Columns and data semantics (examples):
  - Site, Camera_Location_Identifier, Setup_Number, Image_Location_Folder_Name, Image_Filename, Date, Time, Day_Period.
  - Species_Common_Name, Number_Animals_In_Image, Total_Number_Animals_Per_Triggering_Event, Triggering_Event_Number_Sequential.
  - Young_Animal_In_Image, Notes.
- Species coverage:
  - Table 2 lists mammals, birds, and other taxa observed; includes both identified species (e.g., red deer, Przewalski’s horse, roe deer, red fox) and unidentifiable entries.
  - Note: Some records are “unidentifiable” due to image quality; insects and other invertebrates present in some images (with appropriate taxonomic tagging).

## Data Quality, Provenance, and Curation
- Provenance: Data collected by Chornobyl Center; QC performed by UK CEH staff and Chornobyl Centre personnel; dataset amended as needed to resolve queries.
- Time and DST notes: Camera times are in local time (Eastern European Summer Time); one camera (0851) was erroneously set to Eastern European Winter Time.
- Data integrity: Unique identifiers for sites, cameras, and image folders enable traceability; triggering event sequencing is documented; notes capture ambiguities and contextual details.
- Limitations and caveats:
  - Some images may capture the same triggering event across multiple frames; the first data row for an event shows the total number of animals observed.
  - Some events contain multiple species; multiple rows are created to reflect each species per image.
  - Privacy-sensitive images (people or services) are excluded from the dataset even though catalogued; disturbance annotations may reflect human activity near cameras.

## Privacy, Access, and Limitations
- Privacy protections implemented: images with people not included in the dataset; non-sensitive disturbance notes provide context without exposing individuals.
- Access notes: dataset files describe image contents and metadata; actual image files are provided under restricted conditions (per the described folders and catalogue references).
- Temporal and spatial limitations: Setup 1 covers June–November 2020; ambient dose rate and habitat descriptions are provided for context but not exhaustive for all sites or time periods.

## Guidelines for Use and Data Stewardship
- Metadata interpretation:
  - Use Setup_Number, Site, and Camera_Location_Identifier to locate images and related metadata.
  - Reference Image_Location_Folder_Name and Image_Filename to map to actual image files.
  - Treat Date and Time with awareness of DST notes and local time consistent with the dataset’s conventions.
  - Use Triggering_Event_Number_Sequential to aggregate animals per event; note that total counts appear on the first row of each event.
- Quality and governance:
  - Respect privacy constraints; do not attempt to retrieve or distribute excluded images.
  - Acknowledge field partners and funding (NERC grants NE/V009346/1 and EP/V520846/1) when using or publishing analyses.
  - Consider environmental context notes (ambient dose rate, burn degree, trails, vegetation) when interpreting habitat-related findings.
- Limitations to communicate:
  - Some cameras were not functional (e.g., 1556 stolen; 1541 not turned on); a subset of expected data is missing.
  - Time offset or DST anomalies may affect time-series analyses; adjust as needed.

## Acknowledgments and Funding
- CHAR (Chernobyl - a radioactive ecosystem on fire) project funded by the NERC (Grant Ref: NE/V009346/1 and EP/V520846/1).
- Acknowledgements to field collaborators and Chornobyl Center staff for assistance during fieldwork.