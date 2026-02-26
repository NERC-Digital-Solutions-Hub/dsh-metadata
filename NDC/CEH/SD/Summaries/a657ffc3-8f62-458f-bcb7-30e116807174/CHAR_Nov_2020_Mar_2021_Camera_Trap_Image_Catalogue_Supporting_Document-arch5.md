# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue _Supporting_Document

## Overview
- Describes a wildlife camera-trap study conducted in the Ukrainian part of the Chornobyl Exclusion Zone following extensive wildfires (Nov 2020–Mar 2021; setup 2 period: Nov 2020–Mar 2021; three sites, 80 km² each).
- 13 cameras per site (total 39), using Ltl Acorn 6210MC with PIR and 940 nm infrared flash; images include day, night, and transition periods.
- Data collected and curated by the Chornobyl Center for Nuclear Safety and UKCEH; dataset includes a catalogue of 11,633 images (setup 2), with privacy-protected images excluded from the dataset (692 images omitted).
- Related data (setup 1) described in Barnett et al., 2022; data are archived and described for reuse.

## Data Scope and Context
- Study aims to assess large mammal activity after wildfires within the Ukrainian exclusion zone.
- Three sites: Site 1 (most contaminated, northeast), Site 2 (western plume with contamination gradient), Site 3 (south, least contaminated).
- Camera locations have unique numerical identifiers; each camera has a visible serial number on images.
- Decay-corrected Cs-137 deposition data provided; ambient dose rates measured at camera locations (June 2020; with one noted exception).

## Data Structure and Content
- Folder structure: images organized by site and camera, e.g. Setup2_Site1, Setup2_Site1_1570, with sub-folders for each species observed.
- Image catalogue file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue (Excel). Columns cover site, camera location, setup number, image location/folder name, image filename, date/time, day period, species name, number of animals in image, total per triggering event, triggering event sequential, and notes.
  - Handling rules: first image of triggering event may show nothing or a species; subsequent rows may reference the observed species; ‘Service’ images marked as not included in dataset; images containing people/vehicles excluded for privacy but catalogued with notes.
  - Triggering events: sequential numbers per site/camera; typical event separation is 90 seconds, though sequences may span longer.
  - Species data: Table 1 lists counts per species for mammals, birds, and unidentifiable categories; includes total vs visible images.
- Site descriptions file: CHAR_Nov_2020_March_2021_Camera_Trap_Site_Descriptions (Setup 2). Contains camera deployment coordinates (WGS84), habitat descriptions, ambient dose rates, burn degree within 200 m, vegetation, and other descriptive parameters recorded by the same data recorder.
- Details file: CHAR_Nov_2020_March_2021_Camera_Trap_Details. Includes camera location identifiers, serial numbers as shown on images, folder names, deployment start/end times, days in operation, number of images taken, and notes. Some cameras were stolen during setup (e.g., camera 1575; 2081), affecting data continuity.
- Context and references: Setup 1 data described in Barnett et al. 2022; dataset linked to NERC EDS (Environmental Information Data Centre).

## Metadata, Provenance, and QA
- Data collection conducted by Chornobyl Center staff; images and descriptive data transferred to UKCEH and quality-checked by UKCEH staff; queries resolved as needed.
- Metadata standards include: coordinates (WGS84, decimal degrees), time zone (Eastern European Summer Time), and clear field descriptions for provenance, camera specifics, and habitat context.
- Decay-corrected Cs-137 deposition data included to contextualize sites.
- Documentation notes: consistent, single recorder for site and habitat metadata; explicit notes on handling of unidentified images, partial identifications, and gender/age cues when available.

## Access, Privacy, and Sharing
- Images containing people or vehicles are catalogued but not included in the dataset to protect privacy.
- Approximately 6.9% of images (692) are excluded from the image set but are catalogued to preserve event integrity.
- Data are prepared for external reuse via the NERC EDS; related publications (Barnett et al. 2022) provide additional contextual material.

## Data Formats and Interoperability
- Primary dataset files are Excel workbooks with structured columns; image files are JPEGs stored within a hierarchical folder structure.
- Clear naming conventions for folders and image files to support programmatic access and linking between catalogue rows and image files.
- Some time/date fields note exceptions (e.g., camera 1575 time zone handling noted as Eastern European Summer Time in error).

## Limitations and Challenges
- Setup 2 dataset is complete for the period; Setup 1 data are documented elsewhere (Barnett et al., 2022).
- Some field data affected by field conditions (e.g., theft of cameras, missing location 1575 data, and missing serials for some images).
- Data interoperability could be enhanced by future migration to more standardized metadata schemas beyond Excel, and by providing machine-readable linkage files for image assets.

## Related Materials and Funding
- Related publication: Barnett, Gashchak, Wood, Beresford (2022) on Wildlife camera-trap photographs from Chornobyl Exclusion Zone (June 2020–Nov 2020).
- Funding: NERC grants NE/V009346/1 and EP/V520846/1; CERAD (Norway) supported data preparation.