# Supporting documentation for the experiment manipulating local population density

## Overview
- Location: Wytham woods, Oxfordshire, UK (56.0°N? Note: original provides coordinates 51°46′N, 1°20′W)
- Species involved: great tits (Parus major), blue tits (Cyanistes caeruleus), marsh tits (Poecile palustris), nuthatches (Sitta europaea)
- Timeframe: January–March 2021
- Objective: manipulate local population density using selective feeders with RFID-enabled access, and record bird visits to study density effects
- Data product: a single CSV file detailing visits and experimental assignments

## Data collection and provenance
- Capture methods: mist-nets in winter and nestboxes in spring; birds tagged with unique metal BTO rings and a plastic PIT tag
- Access control: feeders with one access hole, a flap, and an RFID antenna; flap programmed to open only for specified PIT-tagged individuals
- Logging: visits recorded when a tagged bird landed on the perch; date/time and logger ( feeder ) stored on an SD card
- Data collection cadence: feeders visited every 2–3 days for refilling, maintenance, and data collection
- Study personnel: Keith McMahon, Sam Croft, Kristina Beck
- Experimental phases: a ~2-week pre-experimental phase (all birds with PIT tag access) followed by a six-week experimental manipulation

## Experimental design and treatments
- Sites: eight sites total, each with two feeders ~100 m apart
- Site classification: six experimental sites (1B, 1H, 2C, 6A, 7C, 7H) and two control sites (4G, 6G)
- Density manipulation: one feeder per site assigned to low-density and the other to high-density
- Pre-experiment basis for assignment: inferred visits during the pre-experimental phase to determine which feeder had more visits
- Treatment mapping:
  - At three experimental sites: high-density and low-density assignments aligned with the majority-visit feeder (high-density for the majority feeder)
  - At the other three experimental sites: assignments reversed (low-density for the majority feeder)
- Individual-level randomization: among birds recorded at least 100 times during pre-experimental period, 20% randomly assigned to low-density; these birds were restricted from accessing the high-density feeder, while all birds could access the low-density feeder
- Timeline: six weeks of manipulation
- Data-collected fields related to treatments:
  - Logger-level treatment (column: treatment) with values low/high/c1/c2 (c1/c2 for control sites)
  - Individual-level treatment (column: id.treatment) with values low/high/control
- Data collected per visit: date, time, and the specific feeder (logger) involved

## Dataset structure and metadata
- Format: one CSV file
- Key columns:
  - date, time
  - Bto.ring (individual identifier)
  - Site (experimental site)
  - period (pre/during experiment)
  - treatment (logger-level: low/high/c1/c2)
  - id.treatment (individual-level: low/high/control)
  - Bto.species.code (greti=great tit, bluti=blue tit, marti=marsh tit, nutha=nuthatch)
- Species codes in dataset:
  - greti = great tit
  - bluti = blue tit
  - marti = marsh tit
  - nutha = nuthatch
- Location metadata: explicit site identifiers, study location
- Data provenance: collected by named researchers; feeders and RFID setup described in methodology
- Data scope: pre-experimental and during-experiment periods included for comparative analyses

## Data quality, governance and reuse considerations
- Data provenance is explicit (tagging method, RFID-based access, and visiting schedule)
- Potential quality considerations include RFID detectability, feeder functionality, and adherence to access restrictions
- Metadata supports reproducibility of the experimental design (site IDs, treatment mapping, period labeling, individual IDs, species codes)
- Suitable for analyses of density manipulation effects on visit rates and inter-individual visitation patterns
- Clear documentation of treatment assignment logic and randomization enhances transparency and reuse

## Use cases and implications for data leadership
- Demonstrates end-to-end data lifecycle in an ecological experiment: design, data capture, annotation, and packaging in a single dataset
- Highlights the importance of comprehensive metadata to enable interpretation of experimental treatments, site-level differences, and individual-level responses
- Underlines needs for governance around experimental datasets: consistent coding for treatments, versioning of data, and clear provenance for future reuse or replication
- Provides a concrete example of combining system-level experimental design with granular event-level data (per-visit records) for deeper analysis and cross-site comparability