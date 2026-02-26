# Collection/generation methods: Study sites

- Scope and geography
  - Approximately 35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
  - Monitored annually from 2014 to 2022.
  - 5 to 20 study sites per year.

- Target populations and monitoring period
  - Blue tit (Cyanistes caeruleus) and great tit (Parus major) nestbox populations.
  - Monitoring window: 1 April to 20 June each year.
  - Productivity measured by recording breeding attempts in nestboxes.
  - Nestbox monitoring schedule:
    - From 1 April: weekly checks until incubation begins.
    - During incubation: checks paused to minimise disturbance.
    - After hatching: checks every 2 days to 10 days post-hatching; efforts to catch breeding adults on the nest 2–13 days after hatching.

- Data collection methods and measurements
  - Mark-recapture: adults caught on the nest, marked with unique metal rings or ring numbers noted from previous rings.
  - Nestling marking: 13 days after hatching, nestlings marked with unique metal rings.
  - Opportunistic mist netting outside the breeding season to supplement mark-recapture data and collect bycatch data for other passerine species.
  - Morphological measurements collected:
    - Wing length (maximum chord, millimetres)
    - Weight (grams)
    - Tarsus length (millimetres)
    - Fat score (various BWG/ESF-equivalent scales)
    - Muscle score, etc. (as per BTO guidelines)
  - RFID and radio tagging:
    - RFID fitted during ringing; RFID tag details recorded.
    - Radio tag fitting recorded when applicable.
  - Additional data fields captured include nestbox number, notes, parent rings, colour rings, CES visit numbers, and various colour-ring details.

- Data management and storage
  - All yearly data checked and uploaded to a central long-term Access database.
  - This database enables linking between reproductive attempts and individual bird information (mark-recapture data).
  - Datasets deposited with the EIDC (European Invertebrate or Integrated Data Centre, depending on context).

- Quality control
  - Annual data quality checks and uploads to the central database to ensure linkage and consistency.

- Data structure and key fields (Table 1)
  - Rows represent individual capture events; columns store event details.
  - Important fields include:
    - ID, year (yr), retrap status (N, R, C, X, U)
    - ring_number, species code (five-letter BTO codes), age code, sex
    - date, time, site (with predefined options or grid reference)
    - morphometrics: wing, weight, tarsus, fat, muscle scores
    - processing initials (initial), moult, nestbox_number
    - chicks_alive, chicks_ringed, chick_age (if age code = 1)
    - parental and offspring ring information (father_ring, mother_ring)
    - RFID_fitted, RFID_number, radio_tag_fitted, radio_tag_ID
    - colour ring details (colour_left_up/down, colour_right_up/down)
    - additional notes and CES visit numbers

- Data standards and codes (Table 2)
  - BTO age codes (definitions provided, including special 3J/5J variants for passerines)
  - Fat score codes and BWG/ESF equivalents (descriptions linking fat reserve to scale values)
  - Ringer’s Manual and related references cited for measurement and coding conventions

- Spatial and GIS relevance
  - Locations captured as site names or grid references, enabling spatial analysis across the gradient.
  - Data structure supports linking spatial locations with individual-level life-history data (productivity, survival, movement) for map-based visualisations and spatial trend analyses.