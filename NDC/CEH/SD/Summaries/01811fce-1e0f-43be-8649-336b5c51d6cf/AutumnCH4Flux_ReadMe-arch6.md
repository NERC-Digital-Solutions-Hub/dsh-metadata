# ReadMe file for AutumnCH4Flux.csv

- This ReadMe describes CH4 flux data collected from soils under three treatments (control, artificial sheep urine, nitrate + glucose) in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.

## Overview of the data
- Emissions: CH4 flux measurements (µg CH4-C m-2 h-1) using an automated greenhouse gas monitoring system.
- Treatments (n = 4 plots each): 
  - Control: no urine application.
  - Artificial sheep urine (ArtUrine): applied in triplicate patches inside each chamber (N application rate 1120 kg N ha-1; 200 ml artifical urine per 100 cm2 patch).
  - C and N: nitrate and glucose treatment (106 kg N ha-1 and 213 kg C ha-1) applied across a 40 × 40 cm square inside the chamber.
- Experimental design: randomized block; measurements from plots over 45 days after treatment.
- Location and environment: humic gleysol soil, unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK; 556 m above sea level; coordinates 53°22'N, 3°95'W.
- Timeframe: treatments applied on 25/10/17; data collected for 45 days post-treatment.
- Data products: quality-assessed flux data (not raw gas concentration data); data have been cleaned for anomalies in raw files and GC chromatograms.

## Data collection and measurement details
- Instrumentation: automated system (Queensland University of Technology) with a SRI 8610 GC for gas analysis.
- Sampling frequency: eight flux measurements per chamber per day (1-hour chamber closure; 4 gas samples per closure).
- Calibration: calibration standard analyzed after every fourth gas sample.
- Chamber specifications: basal area 0.25 m2; chambers sized 50 cm × 50 cm × 15 cm (L × W × H).
- Data processed: flux data that passed quality assurance; not raw gas concentrations.
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; anomalous data removed as needed (e.g., gas peak interference).

## Data structure and contents
- Timestamp: format dd/mm/yy hh:mm.
- Days: number of days pre- or post-treatment relative to application.
- CH4 flux columns: B to M represent CH4 fluxes for each chamber/plot; all units are µg CH4-C m-2 h-1.
- Column headers indicate treatment type and chamber/plot numbers:
  - Control = Control treatment
  - ArtUrine = artificial urine treatment
  - CandN = nitrate and glucose treatment

## Data use and attribution
- Data authors must be acknowledged if data are re-used or reproduced.
- The dataset provides a ready-to-analyze set of CH4 flux measurements suitable for comparing treatment effects and temporal dynamics across plots.

## Practical considerations for analysis
- Suitable for comparing CH4 flux responses among the three treatments over time.
- Can be aggregated by treatment, chamber/plot, or time (Days) to assess patterns.
- Be mindful that the data are quality-assessed flux values, not raw concentration data; ensure alignment with the provided QA notes during any re-processing or re-use.
- The study context (soil type, location, and experimental design) should be considered when extrapolating beyond the study plots.

## Notes on provenance and scope
- Site-specific context: humic gleysol soils in a high-lidelity grazing system; results are tied to the Carneddau mountain environment.
- The data are drawn from a controlled experimental design with explicit patch-level urine applications and a standardized nitrate+glucose treatment, enabling interpretation of fertilization and urination-like inputs on CH4 flux.