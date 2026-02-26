# Supporting documentation for bird ringing data

## Overview
- Location and timeframe: Wytham woods, Oxfordshire, UK; 2020 and 2021 as part of a long-term population monitoring project on breeding biology and behaviour of birds.
- Field procedures: 
  - April–June: trap unringed breeding pairs at the nest and fit with a BTO metal leg ring.
  - Great tits and blue tits additionally fitted with a plastic leg ring containing an RFID tag (PIT tag).
  - All nestlings tagged at 2 weeks old.
  - Additional ringing in autumn and winter across the woodland.
  - Trapping via mistnets; biometrics recorded (mass, wing length, tarsus length, fats score, bill length).
  - Immigrants to the population also tagged.
  - Birds released after processing.

## Data management and quality assurance
- Data entry and storage: entered into the Edward Grey Institute (EGI) Bird data Management Project (EBMP).
- Quality checks: include identifying erroneous nestbox identities and other consistency checks.
- Personnel: mainly collected/entered by Keith McMahon and Sam Crofts, with some additional field workers.

## Data structure and contents
- The dataset consists of a single CSV file named Ringing_data containing 23 columns.
- Key data types and fields:
  - Record.type: physical (bird held) or diurnal (identified without capture).
  - Retrap: indicates new capture or retrap.
  - Bto.ring: BTO ring number.
  - Pit.tag: alphanumeric PIT tag or blank if none.
  - Pit.tag.state: coded status for PIT tag (0 none, 1 new, 2 tag present but not scanned, 3 scanned, 4 tag replaced, 5 removed and not replaced, 6 faulty tag removed and replaced).
  - Bto.species.code: species code (reference to BTO codes PDF).
  - Age: age code (reference to age codes PDF).
  - Sex: NA (unknown), F (Female), M (Male).
  - Sexing method: how sex was determined (pl, bp, cp, ib, ip).
  - Date.time: date and time of capture.
  - Location: capture location (e.g., 20201B100 for nestbox B100 in 2020; other locations within the woods described similarly).
  - Wing.length: in mm.
  - Weight: in g.
  - Bill.length.method: s (skull), f (feathers), n (nostril).
  - Bill.length: in mm.
  - Bill.depth.method: d (deepest point), f (feathers).
  - Bill.depth: in mm.
  - Tarsus.length.method: M (max) or S (min).
  - Tarsus.length: in mm.
  - Pox: NA (not checked), FALSE (pox present).
  - Leg.condition.description: any leg injuries.
  - Tick.description: number and location of ticks.
  - Comments: any additional notes.
- Coding references:
  - Bto.species.code and Age codes link to external PDFs (species_codes.pdf and agecodes.pdf respectively) for definitions.
  - Location encoding and other metadata described within the dataset.

## Usage and context
- Purpose: support analysis of breeding biology and behaviour through tagging, biometric measurements, and nest monitoring.
- Data integration: designed for cross-referencing tagging status, biometric data, and nest locations over time within the Wytham woods population.

## Accessibility and provenance
- Data provenance: collected in field by named researchers and entered into EBMP with QA steps.
- Dataset scope: focused on ringing data from 2020–2021 within the Wytham woods project, with emphasis on unringed and immigrant birds, tagging status, and biometric measurements.