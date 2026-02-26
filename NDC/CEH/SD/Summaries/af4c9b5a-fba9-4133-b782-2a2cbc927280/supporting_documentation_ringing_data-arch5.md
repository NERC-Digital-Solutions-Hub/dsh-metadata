# Supporting documentation for bird ringing data

## Context and Purpose
- Dataset collected in Wytham woods, Oxfordshire, UK during 2020–2021 as part of long-term monitoring of breeding biology and behaviour of birds.
- Birds were ringed (BTO metal rings); great tits and blue tits also fitted with plastic PIT tags; nestlings tagged at 2 weeks; additional ringing in autumn/winter.
- Trapping via mistnets; biometric data recorded; immigrants tagged; birds released after processing.
- Data entered into the internal Edward Grey Institute (EGI) Bird data Management Project (EBMP) and subjected to quality checks.

## Data Collection, Processing and Provenance
- Data primarily collected and entered into EBMP by Keith McMahon and Sam Crofts, with involvement from additional field workers.
- Quality checks conducted within EBMP (e.g., identifying erroneous nestbox identities).
- Aim to support reliable discovery and reuse by others; data management aligned with good data governance practices.

## Data Structure and Metadata
- Single CSV file: Ringing_data.
- Contains 23 columns with fields such as:
  - Record.type (physical vs. diurnal)
  - Retrap (new capture or retrapped)
  - Bto.ring (BTO ring number)
  - Pit.tag and Pit.tag.state (PIT tag presence/state; codes 0–6)
  - Bto.species.code (species abbreviations; see referenced code list)
  - Age and Sex (including Sexing method)
  - Date.time and Location
  - Morphometrics: Wing.length, Weight, Bill.length, Bill.depth, Tarsus.length
  - Pox, Leg.condition.description, Tick.description
  - Comments
- Metadata references external resources for species codes and age codes (codes and PDFs linked in the dataset documentation).

## Quality Assurance and Governance
- Data undergo quality checks during EBMP entry to ensure accuracy and consistency (e.g., nestbox identities).
- Governance considerations include standardization of formats and metadata, traceability of data entry, and documentation of work performed.
- Data ownership and stewardship are aligned with internal project practices; updating and ongoing quality checks implied.

## Access, Sharing and Stewardship Considerations
- Dataset is organized to support discovery and reuse; provenance includes who collected and entered the data.
- Potential sharing considerations include ensuring adherence to data standards, updating processes, and documenting any limitations or embargoes (not explicitly stated in the document, but advised as part of data stewardship).

## Practical Considerations and Limitations
- Data are structured as a single CSV with a fixed schema; compatibility across systems may require mapping of PIT-tag state codes and external code references.
- Handling of missing or unknown values (e.g., Sex=NA) is part of the data’s metadata and quality processes.
- The dataset represents a specific time frame (2020–2021) and location (Wytham Woods) but is part of a larger long-term monitoring effort, implying ongoing updates and potential schema evolution.