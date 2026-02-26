# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Overview
- Dataset of dive times (start and end) and maximum dive depths for three auk species: Atlantic puffin, common guillemot, and razorbill.
- Location: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W).
- Time period outside seabird breeding season:
  - Atlantic puffin: 19 July 2008 – 3 December 2008
  - Common guillemot: 20 July 2005 – 28 January 2006
  - Razorbill: 1 July 2008 – 24 January 2009
- Sample sizes: 12 puffins, 13 guillemots, 13 razorbills.

## Data scope and variables
- Data captured as one CSV file: IoM_AukDiving.csv
- Seven columns:
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment identifier for each individual)
  - StartTime (dive start; Y-M-D H:M:S)
  - EndTime (dive end; Y-M-D H:M:S)
  - DiveDepth (maximum depth of the dive, in meters)

## Data collection and provenance
- Collected by capturing chick-rearing adults at the breeding site and fitting time-depth recorders (TDRs) to Darvic leg-rings.
- Equipment:
  - Atlantic puffin and razorbill: G5 TDRs (CEFAS, Lowestoft, UK; 31 × 8 mm)
  - Common guillemot: LT2400 TDRs (Lotek Wireless, St John's, Newfoundland, Canada; 36 × 11 mm)
- Attachment time: <5 minutes.
- Sexing: feathers collected (UK Home Office Licence) and sex determined via CHD I genes.
- Recapture: TDRs removed during the subsequent breeding-season visit.
- Data processing: Ruth Dunn; access granted by Scottish Natural Heritage; data collected by Sarah Wanless, Mike Harris, and Francis Daunt.

## Data quality, coverage, and limitations
- Original aim was to record diving data over the entire nonbreeding period, but many TDRs failed over autumn, reducing the number of contributing individuals over time.
- Sampling schedules to extend recording periods (balance between resolution and duration):
  - Guillemots: 16 s every 30 d (n = 9 retrieved birds)
  - Guillemots: 32 s every 15 d (n = 4)
  - Razorbills: 3 s every 10 d (n = 7; puffins n = 6)
  - Razorbills: 30 s daily (n = 6; puffins n = 6)
- Variation in sampling rates by species; incomplete data for some individuals and time windows.
- Data reflect nonbreeding-season activity and may include gaps due to device memory limits and partial deployments.

## Data structure and metadata considerations for governance
- Single, well-structured CSV with explicit identifiers (DepID) for longitudinal tracking per individual.
- Key metadata embedded in columns: species, sex, sampling rate, deployment ID, and precise start/end times for each dive.
- Time data in a consistent format (Y-M-D H:M:S) enabling temporal analyses and alignment with other datasets.
- Clear provenance: explicit mention of collection team, site access, device types, and processing steps.

## Utility for data strategy and reuse
- Demonstrates end-to-end data lifecycle: collection, device provisioning, animal handling ethics, data capture, processing, and archiving.
- Highlights challenges relevant to data systems:
  - Data gaps due to device failures and memory constraints
  - Consistency of metadata across instruments and sampling regimes
  - Need for clear provenance and documentation to support reuse within broader seabird behavior and ecology studies
- Useful for benchmarking data collection approaches, metadata standards, and long-term data stewardship in cross-species telemetry datasets.

## Implications for data leadership and action
- Ensure comprehensive metadata standards (device type, sampling rate, deployment details) to improve discoverability and interoperability.
- Plan for data quality monitoring and contingency strategies for device failures to reduce longitudinal data loss.
- Promote co-ownership and cross-team collaboration to align data products with user needs (e.g., researchers studying foraging behavior, energy expenditure).
- Integrate with broader data communities to support consistent data formats, lineage, and updates.