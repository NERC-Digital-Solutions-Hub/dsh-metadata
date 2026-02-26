# CHAR_November_2020_March_2021_Camera_Trap_Image_Catalogue _Supporting_Document

## Overview
- Describes the CHAR project study of wildlife activity in the Ukrainian part of the Chornobyl Exclusion Zone after extensive wildfires (Nov 2020–Mar 2021; setup 2 period).
- Aims to assess large mammal activity and biodiversity responses in a radioactive environmental context and post-fire landscape.
- Study design: three sites (each ~80 km²) within the exclusion zone; 13 motion-triggered camera traps per site; random deployment locations; no bait used.
- Data products include a comprehensive image catalogue, site descriptions, and camera deployment details, with quality control and metadata management.

## Study Design and Deployment
- Three 80 km² sites within the Ukrainian exclusion zone used for setup 2 (Nov 2020–Mar 2021).
- 13 cameras randomly located at each site; cameras are Ltl Acorn 6210MC.
- Camera locations and images linked by unique identifiers (site, camera location, and camera serial numbers).
- Deployment environment: ground-mounted, ~0.6–0.7 m height; most cameras oriented north; surrounding vegetation cleared in front of cameras (~100 m²) to reduce false triggers.
- Trigger mechanism: passive infrared (PIR) with 3-image burst per trigger; 0–1 second between images; ~2–4 seconds recovery between bursts; new triggering event typically starts after ~90 seconds without activity.
- Some cameras were stolen during setup 2 (e.g., camera location 1575 and camera serial 2081); this affected data at those locations.

## Data Collected and Structure
- Images collected: 11,633 trap-cam images during setup 2 (Nov 2020–Mar 2021); all images catalogued except those with people, vehicles, or CHAR staff during setup (692 images withheld to protect privacy).
- Image catalogue file: CHAR_Nov_2020_Mar_2021_Camera_Trap_Image_Catalogue (MS Excel) with rows for individual images and fields describing each event.
- Triggering events: sequential numbers per site/camera; first row of an event contains totals for that event; subsequent rows marked as not applicable (n/a) where appropriate.
- Data fields per image include: site, camera location identifier, setup number, image folder name, image filename, date/time, day period (day/night/transition), species common name, number of animals in image, total animals per triggering event, triggering event sequential number, and notes (including species inference when first image shows “Nothing” later images may reveal the species).

## Species and Image Content
- Table of species captured (Table 1) includes mammals and birds; counts are presented as xxx/yyy, where xxx is total images attributed to a species (including images where the triggering species is not visible) and yyy is images where the species is visible.
- Notable results (examples from the dataset):
  - Red deer (Cervus elaphus) - 4491/4052
  - Przewalski’s horse (Equus ferus przewalskii) - 771/694
  - Eurasian elk (Alces alces) - 1617/1387
  - Red fox (Vulpes vulpes) - 201/122
  - Red deer, roe deer, wild boar, grey wolf, brown hare, European badger, Eurasian lynx, etc., with varying counts.
- A number of images are unidentifiable due to quality; images of people and vehicles are tracked as disturbances but excluded from the image dataset.
- A separate category for “Service” images records non-animal content (e.g., camera maintenance) and is largely excluded from the dataset.

## Site Descriptions and Environmental Context
- File CHAR_Nov_2020_Mar_2021_Camera_Trap_Site_Descriptions provides site-level metadata:
  - Setup 2 context; site, camera location identifiers; GPS coordinates (WGS84) for camera locations.
  - Habitat and description of the site (e.g., meadow, woodland, vegetation present).
  - Ambient dose rate at the camera location (µSv/h) measured in June 2020 (except one site measured in May 2021).
  - Description of animal trails within ~20 m of each camera and degree of burn in proximity to the camera (None to Total destruction scale); vegetation and plant species observed near cameras.
  - Vegetative species list observed at sites.

## Camera Details and Deployment Metadata
- File CHAR_Nov_2020_Mar_2021_Camera_Trap_Details includes:
  - Setup 2 context; site and camera location identifiers; camera serial numbers as displayed on images (with noted thefts at specific locations).
  - Folder name where images are located (e.g., Setup2_Site1_1570).
  - Start and end date/time of camera deployment (noting time zone conventions; some exceptions noted for specific cameras).
  - Number of days in operation and total images captured per camera; notes on deployment specifics.

## Data Quality, Metadata, and Governance
- Data quality checks performed by UKCEH staff; queries resolved and corrections made as needed.
- All descriptive parameters recorded by a single designated person to maintain consistency.
- Metadata and accompanying descriptions aim to support data reuse, with explicit guidance on field meanings and data relationships.
- Privacy considerations: images containing people or vehicles are catalogued but not included in the dataset to protect privacy; disturbance due to human activity is flagged in data records.

## Privacy, Access and Use Considerations
- Images containing people or vehicles are excluded from the public dataset, though triggering events and metadata remain catalogued.
- Underlying data and metadata are documented to support reuse in monitoring frameworks, with explicit notes on data provenance and handling of sensitive content.
- Data sharing and governance practices are emphasized, including consistent metadata standards and clear data provenance.

## Limitations and Notable Issues
- Some sites and cameras were affected by theft, creating gaps in deployment data (e.g., camera location 1575 and camera serial 2081).
- Night/day period classifications are subjective due to automatic camera settings; exact sunrise/sunset times were suggested as a potential augmentation if required.
- Images of people and vehicles are excluded from the dataset, which may slightly bias observed activity patterns in certain contexts.
- Structural notes: setup 1 data are described in Barnett et al., 2022; setup 2 data are described in the current documentation.

## References and Acknowledgements
- Barnett, C.L.; Gashchak, S.; Wood, M.D.; Beresford, N.A. (2022). Wildlife camera trap photographs from the Chornobyl Exclusion Zone, Ukraine (June 2020 - November 2020) following extensive wildfires. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/9bd7754d-ea874b35-bec1-f39d5cc76db6
- Funding: NERC grants NE/V009346/1 and EP/V520846/1; additional funding from CERAD (Norway) for data preparation. Acknowledgements to field contributors and staff.