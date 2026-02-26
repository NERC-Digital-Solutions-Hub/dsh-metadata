# Supporting documentation for the experiment manipulating local population density

## Overview
- Location: Wytham Woods, Oxfordshire, UK (51°46′N, 1°20′W)
- Species: great tit (Parus major), blue tit (Cyanistes caeruleus), marsh tit (Poecile palustris), nuthatch (Sitta europaea)
- Timeframe: January–March 2021
- Objective: manipulate local population density using selective feeders and RFID tagging to study visitation dynamics

## Experimental design
- Setup: eight sites, each with two feeders ~100 m apart; sunflower seeds provided
- Treatments:
  - Six experimental sites: one feeder assigned to low-density, the other to high-density
  - Two control sites: both feeders around control conditions
- Pre-experiment phase: ~2 weeks with unrestricted access to both feeders
- Density assignment: based on pre-experiment visitation frequencies
  - In three sites, high-density feeder was the majority-visited feeder during pre-experiment
  - In three sites, low-density feeder was the majority-visited feeder during pre-experiment
  - At all sites, 20% of birds with ≥100 visits during pre-experiment were randomly assigned to the low-density treatment and excluded from the high-density feeder
- Duration of manipulation: six weeks
- Data collection cadence: feeder visits checked/refilled every 2–3 days
- Data collection team: Keith McMahon, Sam Croft, Kristina Beck

## Data collected and file structure
- Dataset: one CSV file with records of individual visits
- Key fields per record:
  - Date (date of visit)
  - Time (time of visit)
  - Logger (feeder identifier)
  - Bto.ring (individual identity from BTO ring)
  - Site (experimental site identifier)
  - period (pre/during experiment)
  - treatment (logger-level assignment: low/high/c1/c2 for controls)
  - id.treatment (individual-level treatment: low/high/control)
  - Bto.species.code (species code)
- Species codes:
  - greti = great tit
  - bluti = blue tit
  - marti = marsh tit
  - nutha = nuthatch

## Data structure and metadata
- Location metadata: site identifiers (e.g., 1B, 1H, 2C, etc.)
- Temporal metadata: pre-experimental vs during-experiment periods
- Experimental manipulation metadata: per-logger treatment and per-individual treatment
- Data capture mechanism: RFID-enabled PIT tagging with records logged on SD cards

## Data quality and cleaning considerations
- Ensure consistency between:
  - Logger-level treatment (treatment) and individual-level treatment (id.treatment)
  - Date/time formats across records
- Handle potential missing data from RFID detection gaps or feeder sensor issues
- Validate species codes against the BTO codes and maintain a mapping table
- Distinguish pre- vs during-experiment periods in analyses to correctly attribute effects

## Potential data products and analyses for data support
- Self-serve dashboards/pivot tables to compare visit counts by:
  - Density treatment (low vs high) and period (pre vs during)
  - Per-site and per-feeder-level analyses
  - Per-species response patterns
- Reports and charts:
  - Visit frequency over time by site and treatment
  - Proportion of visits by species under different densities
- Data quality checks and provenance documentation to accompany dashboards
- Reproducible analysis pipelines (e.g., scripts to read CSV, clean, merge with site/treatment mappings, and generate summaries)

## Data provenance and access
- Fieldwork conducted by named researchers; data recorded via RFID/PIT tagging
- Data stored in a single CSV with explicit column names as described
- Location and date range clearly documented to support replicability and contextual interpretation