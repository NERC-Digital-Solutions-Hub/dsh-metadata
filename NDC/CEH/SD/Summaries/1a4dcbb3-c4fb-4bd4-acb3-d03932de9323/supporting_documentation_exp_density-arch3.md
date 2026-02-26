# Supporting documentation for the experiment manipulating local population density

## Overview
- Location: Wytham woods, Oxfordshire, UK (51°46′N, 1°20′W)
- Subjects: great tits (Parus major), blue tits (Cyanistes caeruleus), marsh tits (Poecile palustris), and nuthatches (Sitta europaea)
- Timeframe: January–March 2021
- Objective: manipulate local population density around selective feeders and record bird visits to assess effects

## Experimental design and setup
- Sites and feeders: eight sites with two selective feeders each, ~100 m apart, providing sunflower seeds
- Experimental vs. control: six experimental sites (1B, 1H, 2C, 6A, 7C, 7H) with high- and low-density treatments, plus two control sites (4G, 6G)
- Baseline data: ~2 weeks of pre-experimental data where both feeders allowed all PIT-tagged birds access
- Density manipulation: after baseline, the feeder with the majority of pre-experiment visits was assigned to either high-density or low-density treatment (two schemes used across sites)
- Individual assignment: within experimental sites, at least 20% of birds recorded ≥100 times during the pre-experimental period were randomly assigned to the low-density treatment and excluded from accessing the high-density feeder
- Duration: six weeks of experimental manipulation
- Visit monitoring cadence: feeders checked and refilled every 2–3 days
- Personnel: data collection by Keith McMahon, Sam Croft, and Kristina Beck

## Technology and data capture
- Tracking method: PIT tags on birds; RFID antennas in perch feeders
- Access control: feeder flap programmed to open only for specified PIT-tag individuals
- Data storage: visits logged on an SD card at the feeder perches

## Dataset and its structure
- Data file: one CSV containing
  - Date and time of each individual visit
  - Logger (feeder) identifier
  - Individual identity (Bto.ring)
  - Site
  - Period (pre/during experiment)
  - Treatment assigned to each logger (low/high/c1/c2 for controls)
  - Individual’s treatment (id.treatment: low/high/control)
  - Species code (Bto.species.code; greti=great tit, bluti=blue tit, marti=marsh tit, nutha=nuthatch)

## Temporal scope and data management
- Periods captured: pre-experiment phase and during-experiment phase
- Data provenance: explicit recording of site, treatment, individual, and species, enabling traceability and reproducibility
- Data collection cadence and maintenance: regular checks to ensure feeder performance and data integrity; data collectors named in documentation

## Data governance and sharing considerations
- Dataset is structured with clear metadata fields to support transparency and analysis
- Data sharing considerations are implied by the need for clear metadata and provenance; however, explicit sharing policies are not detailed in the document

## Relevance for monitoring frameworks and policy evaluation
- Demonstrates a robust, field-based monitoring design:
  - Baseline data collection prior to manipulation
  - Randomized or semi-randomized assignment of treatments
  - Clear, standardized data collection methods and metadata
  - Short-, medium-, and long-term monitoring through repeated measures
- Highlights practical data governance needs relevant to monitoring frameworks:
  - Availability of metadata and provenance to verify data quality and usability
  - Challenges around data access, standardization, and transformation for integration into dashboards or reports
- Provides a concrete example of collecting, managing, and sharing environmental health-related visitation data to evaluate responses to population-density manipulations.