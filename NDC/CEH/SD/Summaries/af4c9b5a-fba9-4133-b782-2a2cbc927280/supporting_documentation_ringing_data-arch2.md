# Supporting documentation for bird ringing data

## Overview
- Long-term population monitoring of breeding biology and behaviour of birds in Wytham woods, Oxfordshire, UK.
- Data collection period: 2020 and 2021; includes spring trapping and ringing, autumn/winter ringing.
- Focus on unringed breeding pairs, nestlings, and immigrants; data entered into a centralized management system (EBMP) with quality checks.

## Data collection methods
- April–June: trap unringed breeding pairs at nests; fit with BTO metal leg rings.
- Great tits and blue tits: also fitted with plastic RFID (PIT) tags; nestlings tagged at 2 weeks.
- Autumn/winter: additional ringing across the woodland.
- Trapping method: mist nets; biometrics recorded (mass, wing length, tarsus length, fats score, bill length).
- Immigrants to the population also tagged; all birds released after processing.
- Data entry and quality control performed in the EBMP; key contributors include Keith McMahon, Sam Crofts, and other field workers.

## Data management and quality assurance
- EBMP workflow includes multiple quality checks (e.g., identifying erroneous nestbox identities).
- Datasets are prepared, validated, and stored for subsequent use.
- Data management emphasizes standardised procedures and reproducibility.

## Data structure and variables
- One CSV file: Ringing_data (23 columns).
- Key fields and codes (examples):
  - Record.type (physical or diurnal)
  - Retrap (new capture or retrapped)
  - Bto.ring (BTO ring number)
  - Pit.tag (alphanumeric PIT tag or blank)
  - Pit.tag.state (0–6 indicating tag status)
  - Bto.species.code (species abbreviations; reference provided)
  - Age (age codes; reference provided)
  - Sex (NA, F, M)
  - Sexing method (pl, bp, cp, ib, ip)
  - Date.time (date and time)
  - Location (capture site identifiers)
  - Wing.length (mm)
  - Weight (g)
  - Bill.length/ Bill.depth (mm) with methods
  - Tarsus.length (mm) with M or S
  - Pox (NA, TRUE, FALSE)
  - Leg.condition.description; Tick.description; Comments
- Metadata references for codes:
  - Species codes (BTO resource)
  - Age codes (BTO resource)

## Outputs and applications
- Supports monitoring of breeding biology and population health over time.
- Enables standardized analysis and categorization of demographic and physical health indicators.
- Provides structured data suitable for integration into broader environmental health assessments.

## Accessibility and data sharing
- Data managed within EBMP with routine quality assurance.
- Datasets prepared for uploading to appropriate portals; underlying data potentially accessible to authorized users.

## Challenges and opportunities
- Increasing dataset value by integrating ringing data with other relevant datasets (e.g., environmental variables, habitat data).
- Enhancing access to underlying data to support broader analyses and transparency.

## Notes and references
- External codes and resources are linked in the data description (species codes and age codes PDFs from BTO).