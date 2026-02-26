# Lynx_Dataset_Supporting_Document

## Aim and overall purpose
- Provides a catalogue of motion-activated digital trap camera images and videos of Eurasian Lynx (Lynx lynx) from the Ukrainian Chornobyl Exclusion Zone (CEZ) over 2012–2018.
- Data are intended to support environmental monitoring and, where possible, facilitate secondary analyses such as estimating Lynx presence and informing environmental health assessments; not designed for quantitative abundance or density estimates.
- Datasets are curated from multiple projects and are prepared for quality assurance, standardised presentation, and storage in appropriate data portals to enable broader access and reuse.

## Study area, sites, and design
- Location: Chornobyl Exclusion Zone (CEZ), northern Ukraine, ~2600 km2 with a mix of forest, open habitats, marshes, rivers, and limited human activity.
- Climate and habitat context: extensive forestation over time; many water bodies and reed-dominated wetlands; limited ongoing agricultural activity and restricted industrial activity.
- Projects contributing data: TREE (2014–2016), NatEnvPr (2012–2018), REDFIRE (2016–2017).
- Study design: camera placement focused on medium-large mammals; not intended to quantify Lynx abundance or density.
- Sites and cameras: eight study sites, 394 unique camera-trap locations. Cameras often deployed for 8–12 months at a site; TREE cameras were moved to new random locations within the same site after 8–9 weeks. No bait used.

## Digital trap cameras and deployment
- Camera models: primarily Ltl Acorn 6210 MC, with several other models (Browning, Bushnell, CCBetter, Covert, ScoutGuard, Weltar, etc.).
- Recording and settings:
  - Mostly still images; three images per triggering event with short intervals; some videos were recorded (especially from 2016–2018 in certain cameras).
  - Infrared flash used at maximum power; recovery time after triggering varied 3–10 seconds.
  - Sensor sensitivity adjusted seasonally (low/normal in cold; high/normal in warm; some automatic adjustments).
  - Orientation choices to minimize false activations (facing away from direct sun; vegetation regularly cleared).
- Deployment specifics:
  - Cameras placed 0.5–1.1 m above ground, near animal activity areas (3–10 m from focus area).
  - Placement on trees or poles; often on marked forest tracks or bridges; some efforts to reduce visibility where there was risk of detection.
  - Initial setup sometimes included measuring poles (1 m high, marked every 20 cm) to calibrate scale; poles later removed.
  - Some sites used random deployment (TREE) versus more fixed, path-oriented deployments.

## Data products and organization
- Images and videos: 1570 still images of Lynx, 23 Lynx videos, plus 32 images of measuring poles.
- Image catalogue structure:
  - Lynx_2012-2018_Image_Catalogue: records per triggering event with details such as Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, Image_Location_Folder_Name, Triggering_Event_Number, Date_And_Time_Image_Taken, Year/Month, Lynx_ID (when identifiable), Lynx_Gender_Age, Triggering_Event_Duration_Minutes, Day period, Events_Per_Trapping_Day, Notes, Data_Used_For_Analysis_Y/N.
  - Triggering events are created per camera activation; duplicate rows can occur if multiple Lynx are present in one image (with per-Lynx details repeated as needed).
  - Some rows include non-Lynx events to support estimating average Lynx frequency and for site-level context.
- Image location and access:
  - Images stored in folders named per deployment (e.g., Setup01_Site1_1396) aligning with the Image_Location_Folder_Name field.
  - Pole measurement images accompany Lynx images when present.
- Image and camera metadata:
  - Lynx_Camera_Details: camera-trap location coordinates (GPS/WGS84; ~7.7 m accuracy), site, deployment year, setup, setup timestamps (Eastern European Winter Time), camera characteristics (Make/Model, Camera_ID), deployment duration, total images and videos, camera height, distance to nearest trail, camera orientation and tilt, and generic site conditions.
  - Additional fields capture data quality and context (Comments_Relating_To_Date_And_Time_Settings, Ambient_Dose_Rate_At_Site_Micro_Sievert_Per_Hour, etc.).

## Data fields and data quality
- Metadata coverage:
  - Detailed per-event and per-camera fields enabling linkage between images, camera settings, and site context.
  - Identifiers to relate Lynx detections to individual animals when possible (Lynx_ID) and to capture demographics when identifiable (Lynx_Gender_Age).
- Quality considerations:
  - Image quality varies by camera model, lighting, and lynx behavior.
  - Some events may be missed due to camera recovery times or sensor temperature sensitivity.
  - Data primarily suitable for presence/absence or frequency-based analyses, with caveats for non-systematic sampling and non-quantitative abundance estimates.

## Usage, access, and references
- Data were collected under multiple Ukrainian and international research programs; citations reflect project context and related analyses (e.g., population density estimation work by Gashchak et al., 2022).
- Data are curated with QA processes and stored for accessibility in designated data portals; not all camera deployments produced Lynx imagery, and some entries are non-Lynx to support frequency estimation.
- Acknowledgements note field assistance and contributions to data collection.

## Limitations and considerations for analysts
- Not designed to provide quantitative abundance or density estimates across the CEZ; suitable for presence, occurrence, and partial frequency analyses with careful interpretation.
- Temporal and spatial sampling is uneven due to differing project designs and camera deployment durations.
- Metadata completeness varies by project and camera; some fields (e.g., data usage flag for certain rows) indicate selective inclusion in site-level analyses.

## References and related documents
- Decree of the President of Ukraine 2016 establishing Chornobyl radiation and ecological biosphere reserve.
- Development 2006 forestry and site context reports.
- Gashchak et al. (various works) on camera-trap methods and Lynx population estimation in the CEZ.
- Acknowledgements to field collaborators.