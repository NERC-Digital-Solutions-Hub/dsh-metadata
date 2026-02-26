# ReadMe file for SummerCH4Flux.csv

## Overview of the dataset
- Methane (CH4) flux data collected from an experimental field site in the Carneddau mountains, Snowdonia National Park, Wales, UK (dystric histosol, unimproved grazing land; 556 m a.s.l.; coordinates 53°22'N, 3°95'W).
- Treatments (n = 4 blocks): Control (no urine), Artificial sheep urine, Real sheep urine.
- Replication: Each treatment applied in triplicate discrete patches inside chambers; experimental design is a randomized block.
- Treatment dates: 24/07/17.
- Exclusion of sheep from plots from 15/05/17 to minimize recent excretal interference.
- Monitoring duration: 80 days post-treatment.

## Experimental design and treatments
- Control: No urine application.
- Artificial urine: N application rate 920 kg N ha-1 per patch; 200 ml artificial urine over 100 cm2 per patch; applied in triplicate patches within each chamber.
- Real urine: Real sheep urine from ewes grazing the site; N application rate 930 kg N ha-1 per patch; 200 ml urine over 100 cm2 per patch; applied in triplicate patches.
- Chambers: Basal area 0.25 m2; dimensions 50 cm x 50 cm x 15 cm (L x W x H).

## Data collection and instrumentation
- Instrumentation: Automated greenhouse gas monitoring system (Queensland University of Technology) connected to a SRI 8610 GC (Torrance, USA).
- Measurement cadence: Eight flux measurements per chamber per day (1 h chamber closure; four gas samples per closure; calibration after every fourth sample).
- Data scope: High-frequency data during the post-treatment period; flux data (not raw gas concentration data) after quality assessment.
- Data that accompany this ReadMe: quality-assessed CH4 flux values in µg CH4-C m-2 h-1.
- Data headers: Timestamp (dd/mm/yy hh:mm); Days (time pre- or post-treatment); Columns B–M represent CH4 fluxes with treatment and chamber/plot identifiers (Control, ArtUrine, Urine).

## Data quality and processing
- Quality assurance: Visual inspection of raw data files and GC chromatograms to identify and remove anomalies (e.g., gas peak interference).
- Data processing: Only flux data that passed QA are included; not the raw gas concentration data.
- Documentation of data content is limited to what is described in the ReadMe and header naming conventions.

## Data structure and access notes
- Data format: Flux measurements per chamber per day, with treatment-specific column headers indicating the chamber/plot numbers.
- Units: CH4 flux expressed as µg CH4-C m-2 h-1.
- Time references: Days variable indicates time relative to treatment (pre- and post-treatment days available).
- Authorship: Authors must be acknowledged if data are reused or reproduced.

## Implications for data strategy and use
- Reuse considerations: Acknowledge authors; clarify license or usage rights if distributing beyond the original dataset.
- Metadata gaps to consider for data governance (potential enhancements):
  - Site-level metadata (soil properties, weather conditions, management history).
  - Calibration details (dates, standards, performance metrics) beyond the brief QA note.
  - Data lineage and versioning information (dataset release date, any subsequent updates).
  - Clear license or user rights to facilitate data sharing and integration with other datasets.
- Discoverability and interoperability suggestions:
  - Provide a data dictionary or metadata file detailing variable definitions, treatment mappings, and plot identifiers.
  - Include a DOI or persistent identifier for easy citation and retrieval.
  - Offer a data access note or repository link to facilitate reuse by data teams and modelers.