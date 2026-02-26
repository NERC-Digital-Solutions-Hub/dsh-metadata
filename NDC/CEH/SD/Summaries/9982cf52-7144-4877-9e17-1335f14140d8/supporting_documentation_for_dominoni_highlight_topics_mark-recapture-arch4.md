# Collection/generation methods: Study sites

- Overview
  - An approximately 35-kilometre urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
  - Monitored annually from 2014 to 2022, with 5–20 study sites per year.
  - Focus on nests of blue tit (Cyanistes caeruleus) and great tit (Parus major); productivity measured via breeding attempts in nestboxes.

- Study sites and monitoring schedule
  - Nestboxes used to monitor blue tit and great tit populations.
  - Monitoring window: 1 April to 20 June each year.
  - Procedures:
    - Weekly checks from 1 April until incubation begins.
    - After incubation starts, checks paused for 14 days to minimize disturbance.
    - Post-hatching checks every 2 days until chicks observed.
    - Adults marked with unique metal rings (or ring numbers noted if previously ringed).
    - Nestlings marked at 13 days old with unique metal rings.
  - Additional data: Opportunistic mist netting outside the breeding season to supplement mark–recapture data and collect data on other passerine bycatch.
  - Morphological measurements collected: wing length, weight, tarsus length.

- Data management and storage
  - At year-end, all data are checked and uploaded to a central long-term Access database.
  - The database links reproductive attempts with individual bird information (mark–recapture data) and the data are deposited with the EIDC (enduring data repository).

- Data structure and key fields (Table 1)
  - Rows represent individual capture events; columns capture event details.
  - Key fields include:
    - ID, year (yr), retrap status (N, R, C, X, U), ring_number, species (five-letter BTO codes), age (BTO age codes), sex (M/F/U), date and time of capture, site (e.g., SCENE, sallochy, cashel, etc.), morphometrics (wing length in mm, weight in g, tarsus length in mm), moult score, fat score, and notes.
    - Ringing and tagging data: initial processor, RFID_fitted and RFID_number, radio_tag_fitted and radio_tag_ID, father_ring, mother_ring, nestbox_number.
    - Colour ring details: colour_left_up, colour_left_down, colour_right_up, colour_right_down.
    - CES visit details: Week number, CES_visit_number; notes_colour_ for color-ring notes.
    - Additional fields: chicks_alive, chicks_ringed, chick_age, and various free-text notes (notes).
  - Data structure specifics emphasize linking reproductive events to individual birds and to nestbox data.

- Coding schemes and quality control
  - Age codes follow BTO conventions (Table 2), including detailed categories such as 0 (unknown age), 1 (pullus), 1J (fledged but weak), 2, 2J, 3 (hatched this year), 3J*, 4, 4I, 5, 5J, 6, with notes on accuracy in certain juvenile categories.
  - Fat scores use the BWG/ESF equivalents with descriptive categories ranging from no visible fat to fully fat reserves, including intermediate descriptions (e.g., trace of fat, light red, yellow-pink, etc.).
  - Data quality control: annual checks and upload to the central database ensure data integrity and linkage between reproductive data and individual mark–recapture records.

- Considerations for reuse and governance
  - Data are organized to support longitudinal analyses of seabird passerines across an urban–rural gradient.
  - Use of standardized BTO codes for species and age, along with standardized fat scoring, enhances interoperability and discoverability for data leaders managing cross-network data assets.
  - Centralized storage and formal deposition with EIDC improve data discoverability, provenance, and potential for integration with wider data communities and data products.