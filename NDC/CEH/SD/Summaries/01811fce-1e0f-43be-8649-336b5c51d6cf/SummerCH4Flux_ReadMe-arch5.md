# ReadMe file for SummerCH4Flux.csv

## Overview
- Document describes the SummerCH4Flux.csv data file and usage expectations.
- Authors should be acknowledged if the data are reused or reproduced.
- Data focus on CH4 fluxes following urine and artificial urine applications to soil in a field experiment.

## Experimental site and treatments
- Location: dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Site specifics: 556 m above sea level; coordinates 53°22'N, 3°95'W.
- Exclusion period: sheep excluded from plots from 15/05/2017 to avoid recent excretal effects.
- Treatments (n = 4 replicates each):
  - Control: no urine application.
  - Artificial sheep urine: applied as patches; each patch receives 200 ml over 100 cm² (N rate 920 kg N ha⁻¹).
  - Real sheep urine: collected from ewes grazing the site; patches receive 200 ml over 100 cm² (N rate 930 kg N ha⁻¹).
- Treatment application date: 24/07/2017.
- Experimental design: randomised block.

## Data collection and monitoring
- Monitoring period: 80 days post-treatment.
- Measurement system: automated greenhouse gas monitoring system (Queensland University of Technology) coupled with a SRI 8610 GC (Torrance, USA).
- Measurements per chamber per day: eight flux measurements (1 h chamber closure; four GC gas samples per closure; calibration after every fourth sample).
- Chamber dimensions and area: 50 cm x 50 cm x 15 cm; basal area 0.25 m².
- Patches: artificial and real urine applied in triplicate discrete patches per chamber.

## Data content and structure
- Data type: high-frequency flux data from the automated system (not raw gas concentration data).
- Time and format: Timestamp (dd/mm/yy hh:mm); Days relative to treatment (pre- or post-treatment).
- Columns: B to M contain CH4 fluxes (µg CH4-C m⁻2 h⁻¹).
- Treatment/plot identifiers: Column headers encode treatment (Control, ArtUrine, Urine) and chamber/plot numbers.
- Coverage: emissions data from the high-frequency period captured by the automated system.

## Quality assurance and data processing
- QA steps: inspection of raw data files and GC chromatograms for anomalies; data with issues removed (e.g., gas peak interferences).
- Data provided: quality-assessed flux data (not the raw gas concentration data).

## Data usage, attribution, and metadata
- Attribution: explicit requirement to acknowledge authors when re-using or reproducing the data.
- Metadata detail provided includes site location, treatment descriptions, patch sizes, application rates, measurement methodology, chamber dimensions, data sampling regime, and data column definitions.
- Data usability notes: suitable for comparison across treatment types (Control, artificial urine, real urine) and for analyses of CH4 flux dynamics over the 80-day post-treatment period.

## Access considerations
- Data are structured to enable discoverability via a clearly defined header scheme (treatment and chamber/plot identifiers) and documented data quality processing.
- Users should reference the original authors for proper attribution and adhere to the stated data-use acknowledgment requirement.