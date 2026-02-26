# Lynx_Dataset_Supporting_Document

- Overview
  - A catalogue of motion-activated digital trap camera images (and some videos) of Eurasian Lynx (Lynx lynx) in the Ukrainian Chornobyl Exclusion Zone (CEZ), collected over 2012–2018.
  - Data come from three projects (TREE, NatEnvPr, REDFIRE) with different designs; the studies were not intended to obtain quantitative abundance or density estimates.
  - Images and metadata are organized to support site- and camera-level analyses, with some data used in site-specific analysis (Gashchak et al. 2022; Gashchak et al. submitted).

- Projects and study scope
  - TREE: 2014–2016; funded by NERC, EA, RWM; random camera relocation within sites after 8–9 weeks; no bait.
  - NatEnvPr: 2012–2018; Ukrainian Ministry of Ecology and Natural Resources.
  - REDFIRE: 2016–2017; NERC.
  - Eight CEZ study sites; 394 unique camera-trap locations; most cameras deployed 8–12 months per site (TREE deployments shorter and relocated within site).
  - No bait used across projects.

- Study area and habitat context
  - CEZ area: ~2600 km2 in northern Ukraine, between Prypiat and Uzh rivers.
  - Habitat: about 63% forest (dominant Pinus sylvestris); remaining former agricultural land largely now scrub; marshes and water bodies ~10% of CEZ; low human presence outside central areas.
  - Administrative status: 2016 Chornobyl Radio-ecological Biosphere Reserve established (87.6% of CEZ area); limited industrial activity and tourism restricted to a few areas.

- Digital trap cameras and deployment details
  - Primary camera models: Ltl Acorn 6210 MC; plus Browning, Bushnell, ScoutGuard, Weltar and others.
  - Settings: most recordings were still images, typically three images per triggering event with 0–5 s between images; infrared flash at maximum power; recovery time 3–10 s; some units used video mode (notably from 2018).
  - Placement and orientation: cameras placed ~3–10 m from areas of activity; mounted 0.5–1.1 m above ground on trees or poles; faced away from direct sun to reduce false triggers; vegetation regularly trimmed.
  - Deployment layout: cameras positioned on well-marked paths or at intersections/bridges; TREE deployments randomly relocated within sites.
  - Data capture aids: up to 20 measuring poles placed in front of cameras during initial deployment for scale; poles later removed.

- Data products and structure
  - Image catalogue: Lynx_2012-2018_Image_Catalogue
    - Records images (or videos) by triggering event, including:
      - Project_ID, Study_Site, Setup, Camera_Trap_Location_ID, Location-related IDs, Image_Location_Folder_Name
      - First_Image_Per_Triggering_Event, Last_Image_Per_Triggering_Event
      - Triggering_Event_Number, Date_And_Time_Image_Taken, Year, Month
      - Lynx_ID (if identifiable), Lynx_Gender_Age, Triggering_Event_Duration_Minutes
      - Day_period, Number_Trapping_Days_Per_Month, Events_Per_Trapping_Day
      - Notes; Data_Used_For_Analysis_Y/N (Y only for sites used in Gashchak et al. 2022)
  - Camera details: Lynx_Camera_Details
    - Project_ID, Camera_Trap_Location_ID, Location_ID_Related_To_Project
    - Coordinates (Latitude/Longitude, WGS84; ~7.7 m accuracy)
    - Site, Year, Setup, Date/Time of Setup and Last Operation (Eastern European Winter Time)
    - Comments on settings; Ambient dose rate at site (micro-Sv/h)
    - Camera Make/Model, Camera_ID, Deployment Duration, Totals of still images and videos
    - Height, Distance to nearest trail, Orientation, Tilt, Generic Conditions
  - Additional guidance: Descriptions of trap cameras, locations, and deployment periods are in the accompanying Lynx_Camera_Settings.csv (referenced but not detailed here).

- Individual identification and data quality
  - When possible, individuals were assigned a Lynx_ID based on identifiable features (Camera_Trap_Location_ID + a unique suffix); otherwise, no unique ID.
  - Image catalog entries include duplicates if multiple Lynx appear in the same trigger event; duplicates map to separate rows with updated individual details where available.
  - Quality control performed by UKCEH staff; missing or non-Lynx-triggered records are included to enable population-level estimates of Lynx frequency in some analyses.
  - Limitations in metadata: some records come from irregular or short sampling periods (not used in site-level analyses); time stamps are in Eastern European Winter Time; coordinate precision ~7.7 m.

- Analytical uses and limitations
  - Not designed for robust abundance or density estimation; suitable for presence/absence signals, detection frequency, individual identification (where possible), and occupancy/detection modeling with appropriate caveats.
  - By-site analysis and population density estimation have been pursued in subsequent work (Gashchak et al. 2022; Gashchak et al. 2022 submission).
  - Data offer a structured basis for cross-site comparison, spatial-temporal patterns, and integration with environmental variables, within the bounds of irregular sampling and varying camera setups.

- References and acknowledgements
  - Legal and historical context: Decree of the President of Ukraine (2016) establishing the Chornobyl biosphere reserve; Development 2006 forestry project references.
  - Related works: Gashchak et al. on site analyses and density estimation (2022; submitted); prior bear-related CAMTRAIT work in 2016.
  - Acknowledgements to field collaborators (e.g., Igor Chyzhevsky, Maksim Krachkovsky).

- Practical notes for analysts
  - Ensure alignment of camera metadata with image records when merging datasets.
  - Recognize varying deployment durations and camera models across sites and years when modeling detection probabilities or occupancy.
  - Consider the non-random sampling and absence of standardized effort across the full 2012–2018 window in any inferential analyses.