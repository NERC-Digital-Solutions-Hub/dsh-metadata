# Supporting documentation for the experiment manipulating local population density

- Location and timeframe
  - Wytham woods, Oxfordshire, UK (51°46′N, 1°20′W)
  - January–March 2021
  - Species studied: great tits (Parus major), blue tits (Cyanistes caeruleus), marsh tits (Poecile palustris), nuthatches (Sitta europaea)

- Experimental design and purpose
  - Objective: manipulate local population density using selective feeders that restrict access by PIT-tagged birds
  - Setup: eight sites, each with two feeders ~100 m apart; six experimental sites and two controls
  - Experimental sites: 1B, 1H, 2C, 6A, 7C, 7H
  - Control sites: 4G, 6G
  - Pre-experiment phase: ~2 weeks with open access to all PIT-tagged birds
  - Density manipulation: after pre-phase, feeders were assigned to high-density or low-density treatments; assignment based on pre-experiment visitation counts
  - Randomization: within sites, 20% of birds with at least 100 visits were assigned to low-density (and excluded from high-density), ensuring the low-density group could only access designated feeders

- Data collection and logging
  - Methods: birds captured and tagged with metal BTO rings and PIT tags; visits recorded via RFID-enabled feeders
  - Data collection cadence: feeders checked and data retrieved every 2–3 days
  - Data logging hardware: SD cards storing time, date, and logger identifier for each individual visit
  - Personnel: Keith McMahon, Sam Croft, Kristina Beck

- Dataset structure
  - File type: single CSV
  - Key columns:
    - Bto.ring: individual visit identifier
    - Site: experimental site identifier
    - period: pre-experimental or during experiment
    - treatment: logger-specific treatment (low/high/c1/c2 for control sites)
    - id.treatment: individual’s assigned treatment (low/high/control)
    - Bto.species.code: species code (greti, bluti, marti, nutha)
  - Species codes
    - greti = great tit
    - bluti = blue tit
    - marti = marsh tit
    - nutha = nuthatch

- Data provenance and context
  - Data origin: direct from RFID logger visits at feeders
  - Location metadata: site identifiers, spatial arrangement, and feeder setup
  - Temporal metadata: date and time of each visit, pre/during experiment period

- Data governance and stewardship considerations
  - Metadata needs: ensure a clear data dictionary or codebook for all fields and site codes
  - Data quality: verify consistency of time formats and logger IDs; account for potential missing/unreadable tag visits
  - Interoperability: maintain standardized codes and, if possible, provide mapping for species and site identifiers
  - Change management: document any changes to treatments, site setups, or logging equipment; version control for dataset
  - Accessibility and reuse: provide documentation on experiment design, treatment assignment methodology, and dataset provenance to enable reuse by others

- Potential challenges for data management
  - Complex assignment logic across sites and treatments; ensure reproducibility of treatment mapping
  - Large historical activity per individual (minimum 100 visits for certain selections) requires careful handling of repeated measures
  - Possible data gaps due to equipment issues or tag read failures; plan for imputation or flagging of incomplete records

- Suggested metadata enhancements for future reuse
  - Time zone and date-time formatting standardization
  - Detailed field-level definitions and allowable values
  - Linkage between Bto.ring and individual metadata (e.g., species, age, sex if available)
  - Embargo notes or data access restrictions (if any) and contact for data access