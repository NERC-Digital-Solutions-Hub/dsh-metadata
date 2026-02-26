# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Overview
- A dataset of dive times (StartTime, EndTime) and maximum dive depths (DiveDepth) for three auk species collected outside the seabird breeding season.
- Species: Atlantic puffin (Fratercula arctica), common guillemot (Uria aalge), razorbill (Alca torda).
- Sampling period by species:
  - Atlantic puffin: 19 July 2008 – 3 December 2008
  - Common guillemot: 20 July 2005 – 28 January 2006
  - Razorbill: 1 July 2008 – 24 January 2009
- Sample sizes: 12 puffins, 13 guillemots, 13 razorbills.
- Data collected by capturing chick-rearing adults, fitting time-depth recorders (TDRs) to Darvic leg-rings, and later recapturing to recover TDRs and remove devices.
- Original aim: collect diving data across the entire nonbreeding period; actual data collection was affected by device failures, reducing the number of contributing individuals over time.

## Methods and Data Collection
- TDR equipment:
  - Puffins and razorbills: G5 TDRs (CEFAS, Lowestoft, UK; 31 × 8 mm)
  - Common guillemots: LT2400 TDRs (Lotek Wireless, St John's, Newfoundland, Canada; 36 × 11 mm)
- Procedure: attachment in under 5 minutes; feather samples collected under UK Home Office Licence to enable sexing using CHD I genes; TDRs removed when birds were recaptured during the following breeding season.
- Recording scheme to extend data collection:
  - Depth readings were programmed at varying intervals to balance resolution with the number of days recorded. Sampling schemes used:
    - 16 s depth readings for 24 h every 30 days (guillemots, n=9 retrieved)
    - 32 s depth readings for 24 h every 15 days (guillemots, n=4)
    - 3 s depth readings for 24 h every 10 days (razorbills, n=7; puffins, n=6)
    - 30 s depth readings for 24 h every day (razorbills, n=6; puffins, n=6)
- Data management: all data compiled to a single CSV file; authors involved in data processing.

## Dataset Contents
- File: IoM_AukDiving.csv
- Columns:
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment ID per individual)
  - StartTime (start of each dive; Y-M-D H:M:S)
  - EndTime (end of each dive; Y-M-D H:M:S)
  - DiveDepth (maximum depth per dive in meters)

## Provenance and Location
- Location: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W)
- Data collectors: Scottish Natural Heritage granted access; Sarah Wanless, Mike Harris, Francis Daunt collected the data; Ruth Dunn processed the data.
- Timeframe context: study conducted outside breeding season; field activities occurred during the breeding season for handling and recapture.

## Data Quality, Limitations, and Gaps
- Device reliability: some TDRs failed completely or progressively during autumn; data coverage declined over time.
- Resulting data gaps: reduced number of contributing individuals as the study progressed; limited nonbreeding-period continuity for some birds.
- Metadata and standardization: dataset documents limited columns and specific sampling schemes; broader metadata context (e.g., environmental conditions) is not included.
- Data sharing and governance notes: data collection occurred under regulatory permissions (Home Office Licence for feather sampling); explicit public data-sharing policy for the dataset is not stated.

## Governance, Access, and Use
- Data are provided as a single CSV dataset with clearly defined fields for analysis and cross-species comparison.
- The record reflects careful documentation of sampling rates and deployment identifiers to support traceability and reproducibility.
- Relevance for monitoring frameworks: provides baseline, cross-species dive behavior metrics during the nonbreeding period that can inform habitat use, foraging effort, and temporal patterns; highlights the importance of robust tagging, metadata completeness, and data governance to ensure data quality and reusability in environmental health monitoring.

## Implications for Monitoring and Policy Decision-Making
- Establishes a reference for nonbreeding-season diving behavior in three auk species, useful for trend analysis and habitat management.
- Demonstrates how varying sampling resolutions affect data volume and temporal coverage, informing design choices in monitoring frameworks.
- Underlines the need for reliable data streams, comprehensive metadata, and governance to enable timely data sharing and transparent decision-making.