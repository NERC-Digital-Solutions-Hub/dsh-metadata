# Supporting documentation for bird ringing data

## Overview
- Dataset collected in Wytham woods, Oxfordshire, UK, during 2020–2021 for long-term monitoring of breeding biology and behaviour in birds.
- birds captured at nests (April–June) if unringed, fitted with BTO metal ring; Great tits and blue tits additionally fitted with a plastic PIT tag; nestlings tagged at 2 weeks old.
- Additional ringing carried out in autumn and winter across the woodland.
- Birds trapped with mistnets; biometrics recorded (mass, wing length, tarsus length, fats score, bill length); immigrants fitted with tags; birds released after processing.
- Data entered into the Edward Grey Institute (EGI) Bird data Management Project (EBMP) and subjected to quality checks.
- Data entry mainly by Keith McMahon and Sam Crofts, with involvement from other field workers.

## Data Collection and Provenance
- Primary data collection period: nest captures in April–June; subsequent autumn/winter ringing.
- Data flow: field collection → EBMP entry → quality checks → storage/curation.
- Tags used: BTO metal rings and RFID PIT tags; PIT-tag state tracked (see data dictionary).
- Location and timing details recorded for each event; data quality checks include verification of nestbox identities and other entry checks.

## Data Structure
- One CSV data file: Ringing_data containing 23 columns.
- Key columns and meanings:
  - Record.type: physical (held) or diurnal (identified without capture)
  - Retrap: new capture or retrapped
  - Bto.ring: BTO Ring number
  - Pit.tag: alphanumeric PIT-tag or empty if none
  - Pit.tag.state: 0 (no PIT-tag), 1 (new PIT-tag), 2 (tag present but not scanned), 3 (tag present and scanned), 4 (tag replaced), 5 (tag removed and not replaced), 6 (faulty tag removed and replaced)
  - Bto.species.code: species code (refer to species_codes.pdf)
  - Age: age code (refer to agecodes.pdf)
  - Sex: NA (unknown), F (Female), M (Male)
  - Sexing method: pl (plumage), bp (brood patch), cp (cloacal protuberance), ib (inferred from previous ringing), ip (inferred from partner)
  - Date.time: date and time of capture
  - Location: capture location (e.g., nestbox code)
  - Wing.length: mm
  - Weight: g
  - Bill.length.method: s (skull), f (feathers), n (nostril)
  - Bill.length: mm
  - Bill.depth.method: d (deepest point), f (feathers)
  - Bill.depth: mm
  - Tarsus.length.method: M (max) or S (min)
  - Tarsus.length: mm
  - Pox: NA (not checked), FALSE (nopox), TRUE (pox present)
  - Leg.condition.description: leg injuries
  - Tick.description: number and location of ticks
  - Comments: additional notes
- Codes and dictionaries:
  - Bto.species.code and Age codes referenced via linked PDFs (species_codes.pdf and agecodes.pdf).
  - Location and date formats consistent with field records.

## Data Quality and Validation
- Data entered into EBMP undergoes quality checks (e.g., identification of erroneous nestbox identities).
- Data collection and entry performed by named personnel (e.g., Keith McMahon, Sam Crofts) with support from field workers.
- Tag-status (PIT) requires careful handling and scanning; PIT-tag state codes document tag presence and scan results, enabling traceability of tagging events.
- Some fields may be NA (e.g., Sex when unknown); standardization relies on multiple methods for sexing and clear documentation of method used.

## Uses and Access
- Suitable for analyses of breeding biology, population dynamics, and tag-based resighting studies.
- Data products could include dashboards, pivot tables, and reports to enable self-service analysis; outputs should reference the data dictionary and code mappings.
- Users should consult the linked code resources (species_codes.pdf, agecodes.pdf) for correct interpretation of categorical fields.
- Data provenance and quality checks described here support reproducibility and data use across local studies or broader collaborations.

## References and Code Mappings
- BTO species codes and age codes are defined in the referenced PDFs:
  - species_codes.pdf
  - agecodes.pdf
- Location and date conventions, along with PIT-tag state codes, are documented within the Ringing_data dataset and the EBMP data management framework.