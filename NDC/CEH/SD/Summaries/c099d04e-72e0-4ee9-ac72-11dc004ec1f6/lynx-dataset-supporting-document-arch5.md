# Lynx_Dataset_Supporting_Document

- Overview
  - A catalogue of motion-activated digital trap camera images (and videos) of Eurasian Lynx (Lynx lynx) from the Ukrainian Chornobyl Exclusion Zone (CEZ), collected over 2012–2018.
  - Data include images/videos of Lynx and measuring poles; not designed to provide quantitative abundance or density estimates.
  - Collected from three projects: TREE (2014–2016), NatEnvPr (2012–2018), and REDFIRE (2016–2017).

- Data provenance and study design
  - TREE, NatEnvPr and REDFIRE contributed differing study designs and approaches.
  - No bait used; aims were to capture images of medium-large mammals, with Lynx capture incidental to broader objectives.
  - Some data (from 2012–2018 and January–June 2013) were irregular or short-term, limiting suitability for site-level density analyses.

- Study area
  - CEZ: ~2600 km2 in northern Ukraine; varied habitats including forests (majority by 2012–2018), wetlands, lakes, and abandoned settlements.
  - 8 study sites with cameras at 394 unique locations; most sites had cameras deployed up to 8–12 months; TREE deployments were 8–9 weeks with relocations within the same site.
  - Environmental context includes floodplains, reed beds, and minimal current human activity outside restricted zones.

- Digital trap cameras and deployment
  - Primary camera models: Ltl Acorn 6210 MC; others include Browning, Bushnell, ScoutGuard, Weltar, etc.
  - Settings: mostly still images, typically 3 images per trigger with 0–5 s delay; infrared at maximum power; recovery times of 3–10 s; some cameras recorded video (from 2016–2018 for certain models/projects).
  - Strategies to reduce false triggering: facing cameras away from direct sunlight, vegetation management, and 0.5–1.1 m mounting heights.
  - Deployment details: cameras ~3–10 m from areas of Lynx activity; mounted on trees or vertical poles; orientation and tilt adjusted per terrain; random placement for TREE; poles placed as assessing targets prior to activation.

- Data collection and processing
  - Image cataloguing approach: images organized by triggering events; each event records first and last image of the trigger sequence.
  - Individual identification: unique Lynx IDs assigned when features permit; otherwise lynx without identifiable features are not assigned IDs.
  - Quality control: UKCEH staff downloaded images, validated Lynx observations, and resolved queries related to image catalogues and site descriptions.
  - Pole measurements: measuring poles included in some camera setups to aid size estimation (~±5 cm for shoulder and hind-quarter height).

- Image catalogue structure and metadata
  - Lynx_2012-2018_Image_Catalogue
    - Records per triggering event with fields such as Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, Image_Location_Folder_Name, First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event, Triggering_Event_Number, Date_And_Time_Image_Taken, Year, Month, Lynx_ID, Lynx_Gender_Age, Triggering_Event_Duration_Minutes, Day period, Number_Trapping_Days_Per_Month, Events_Per_Trapping_Day, Notes, Data_Used_For_Analysis_Y/N.
    - Some rows indicate data used in site-level analyses (Gashchak et al. 2022) or not used due to irregularities.
  - Image location folders and naming conventions align with the Image Catalogue entries (e.g., Setup01_Site1_1396).

  - Lynx_Camera_Details
    - Camera_location metadata: latitude/longitude (WGS84), Site, Year, Setup, setup timestamps, comments on time settings, ambient radiation dose rate, camera make/model, Camera_ID, deployment duration, totals for images/videos, camera height and distance to main activity area, orientation and tilt, and generic site conditions.

- Data structure and accessibility
  - Datasets are organized into two main CSV catalogues plus image/video files stored in folders named to reflect camera site and setup.
  - Cross-referenced by Camera_Trap_Location_ID and related project identifiers to enable data integration across projects.
  - The document provides comprehensive descriptive metadata to support discovery, interpretation, and reuse.

- Data governance and usage considerations
  - Data include detailed provenance, site context, and camera specifications to support reproducibility and appropriate use.
  - While suitable for presence-focused analyses and relative activity assessments, the data are not a robust abundance/density dataset due to study designs, irregular deployments, and variability across camera models and settings.
  - Potential usage includes estimating Lynx frequency at camera sites, presence-absence indicators, and contextualizing Lynx activity within CEZ habitats, with caution about dataset limitations.
  - References to related analyses (e.g., Gashchak et al. 2022) illustrate how portions of the data have informed site-level interpretations.

- References and acknowledgements
  - Decree of the President of Ukraine (2016) establishing Chornobyl radiation and ecological biosphere reserve.
  - Related publications (Gashchak et al. 2022; earlier works on wildlife in CEZ) and field work acknowledgements.
  - Acknowledgements to individuals who assisted during fieldwork.