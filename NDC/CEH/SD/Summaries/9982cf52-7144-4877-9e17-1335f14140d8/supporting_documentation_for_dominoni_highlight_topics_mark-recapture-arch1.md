# Collection/generation methods: Study sites

- Overview
  - Approximately 35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
  - Monitored annually from 2014 to 2022 across 5–20 sites each year.
  - Target species: blue tit (Cyanistes caeruleus) and great tit (Parus major) nestbox populations.
  - Monitoring period: 1 April to 20 June; productivity assessed via breeding attempts in nestboxes.

- Field methods and sampling design
  - Nestbox monitoring: weekly checks from 1 April until incubation; during incubation checks paused to reduce disturbance; after hatch, checks resumed every other day until chicks observed.
  - Breeding data: date of first egg, clutch size recorded.
  - Mark–recapture: adults marked with unique metal rings; nestlings ringed at 13 days post-hatching.
  - Opportunistic mist netting: conducted outside the breeding season at both study sites; captures provide mark–recapture data and bycatch for other passerines.
  - Morphometrics collected: wing length, weight, tarsus length; additional measurements include moult scores, fat scores, and other notes.

- Data management and quality control
  - End-of-year data uploaded to a central long-term Access database that links reproductive attempts with individual bird information (mark–recapture data).
  - Datasets deposited with the EIDC (central repository).
  - Quality control: annual checks and uploads to the central database.

- Data structure and coding
  - Table 1 (data records): fields include
    - ID, year, retrap status (N, R, C, X, U), ring_number, species code (BTO codes), age code, sex, date, time, site, wing (mm), weight (g), initial processor, moult code, tarsus (mm), fat score, chicks_alive, chicks_ringed, nestbox_number, notes, chick_age, father_ring, mother_ring, RFID_fitted and RFID_number, radio_tag_fitted and radio_tag_ID, colour_rings (left/right, up/down), CES_visit_number, notes on colour rings, old_greater_coverts, muscle score, among others.
  - Table 2: BTO age codes with definitions (including 0, 1, 1J, 2, 2J, 3, 3J*, 4, 4I, 5, 5J, 6); notes that 3J and related codes indicate higher confidence in juvenile identification. Also includes information on fat score mappings and references to BWG/ESF scales and Fat Score descriptions.
  - Coding references and standards: BTO species codes, age codes, fat scores; terminology and descriptions align with Redfern & Clark (Ringers' Manual) and related BTO guides.

- Data accessibility and provenance
  - Data linked across reproductive and mark–recapture datasets within the central database.
  - Datasets deposited with the EIDC; datasets and metadata are prepared to support discoverability and reuse.

- Considerations for analysis and use
  - Longitudinal, site-gradient design enables analysis of spatial and temporal trends in productivity and body condition.
  - Rich individual-level data (ringing, mark–recapture, morphometrics, fat/moult) facilitate modeling survival, recruitment, and growth trajectories.
  - Data include standardized coding for species, age, and morphology, enabling cross-year comparisons, though some fields may be blank or uncertain (e.g., age, sex) requiring careful handling of missing or uncertain data.
  - Data management practices support traceability from raw observations to processed records via the central database and EIDC deposition.