# Lynx_Dataset_Supporting_Document

## Overview
- A catalogue of motion-activated digital trap camera images of Eurasian Lynx (Lynx lynx) from the Ukrainian Chornobyl Exclusion Zone (CEZ), collected over 2012–2018.
- Data come from three projects: TREE (2014–2016), NatEnvPr (2012–2018), and REDFIRE (2016–2017).
- The studies were designed with the aim of capturing images of medium-large mammals, not to obtain quantitative abundance or density estimates for Lynx.

## Study area and study sites
- CEZ: ~2600 km2 in northern Ukraine; diverse habitats including extensive forest and wetlands; limited human presence and activity; 2016 decree established the Chornobyl radiation and ecological biosphere reserve.
- Habitat context: stable to expanding forest cover during study period; numerous lakes, rivers, marshes, reed beds, and abandoned settlements.
- Sites and locations: eight study sites within the CEZ; cameras deployed at 394 unique locations (some locations used across projects); most cameras used for 8–12 months per site; TREE deployments were 8–9 weeks per location with random relocation within the same site.
- No bait used in any study.

## Digital trap cameras
- Camera models: majority used Ltl Acorn 6210 MC; other models included Browning BTC5/BTC-7FHD-PX, Bushnell models, ScoutGuard, Weltar, and others.
- Settings and operation: mostly still images with three images per trigger; 0–5 second delay between images; infrared flash at maximum power; recovery time 3–10 seconds; some units recorded video (notably from 2018 and during TREE deployments).
- Calibration and placement: cameras oriented to minimize false triggers (facing away from direct sun); vegetation regularly cleared; cameras typically placed 0.5–1.1 m above ground; 3–10 m from expected animal activity areas; positioned on trails, intersections, bridges, or random locations (TREE).
- Field procedures: up to 20 measuring poles placed in front of cameras at deployment (1 m high, marked every 20 cm) to aid scale; poles sometimes photographed; poles later removed.
- Data capture context: no bait; most deployments aimed at maximizing detection while minimizing disturbance.

## Data products and structure
- Images and poles: 1570 Lynx still images and 23 video clips of Lynx; 32 still images of measuring poles included.
- Image catalogue: Lynx_2012-2018_Image_Catalogue, with per-triggering-event records including:
  - Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, related IDs, Image_Location_Folder_Name
  - First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event
  - Triggering_Event_Number, Date_And_Time_Image_Taken, Year, Month
  - Lynx_ID (if identifiable), Lynx_Gender_Age (if determinable)
  - Triggering_Event_Duration_Minutes, Day period, Number_Trapping_Days_Per_Month, Events_Per_Trapping_Day
  - Notes, Data_Used_For_Analysis_Y/N
- Image metadata and file organization: images stored in folders named like Setup01_Site1_1396; image catalogue includes mapping and notes about missing images or non-Lynx records; quality control by UKCEH staff.
- Camera details: Lynx_Camera_Details with:
  - Project_ID, Camera_Trap_Location_ID, related IDs, latitude/longitude (WGS84; ~7.7 m accuracy)
  - Site, Year, Setup
  - Date/Time of camera setup and last operation (Eastern European Winter Time, GMT+03:00)
  - Comments on time settings, ambient dose rate at site (µSv/h), Make/Model, Camera_ID
  - Deployment duration (days), totals of still images and videos, camera height, distance to nearest trail, orientation, tilt
  - Generic_Conditions (brief site description)
- Data scope note: eight study sites; 394 camera locations; not all cameras recorded Lynx; some sites had limited or irregular data (e.g., TREE deployments).

## Data quality, limitations, and provenance
- Image quality varies by camera model, time of day, and Lynx behavior; some events contain duplicates when multiple Lynx appear.
- Some Lynx cannot be uniquely identified; when identifiable, a unique Lynx_ID is assigned; otherwise not.
- Not all cameras captured Lynx; some triggering events did not contain Lynx data; recovery time may miss detections.
- Temporal context provided in local time (Eastern European Winter Time); calibration data (poles) used for scale.
- Provenance and acknowledgement: data collected under Ukrainian regulatory context; references include Decree establishing the biosphere reserve (2016) and related Gashchak et al. works; QA by UKCEH; field team acknowledgments.

## References and acknowledgements
- Decree of the President of Ukraine (2016) establishing the Chornobyl biosphere reserve.
- Development 2006 (lignocultural context and forestry references).
- Gashchak et al. publications (ongoing work on Lynx and other wildlife in CEZ; 2022 by-site analysis cited).
- Acknowledgements to field staff and collaborators.

## Implications for data management and use
- Cross-project integration enables presence/occurrence analysis and site-level comparisons, though not designed for abundance estimates.
- Rich metadata and structured catalogs support discoverability, reuse, and potential cross-disciplinary analyses.
- Clear documentation of camera models, deployment logistics, and site context aids replication and quality assessment.
- Data governance considerations: multi-source data with varying protocols; standardized metadata and clear data-use notes enhance usability for data-led decisions.