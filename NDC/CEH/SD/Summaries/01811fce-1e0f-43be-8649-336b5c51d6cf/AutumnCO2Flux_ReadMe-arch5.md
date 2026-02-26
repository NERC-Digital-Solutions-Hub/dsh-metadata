# ReadMe file for AutumnCO2Flux.csv

## Purpose and authorship
- Authors must be acknowledged if data are reused or reproduced.
- Dataset provides CO2 flux measurements (with notes that the file includes CH4 flux columns expressed as mg CO2-C m-2 h-1) from a controlled experiment with multiple treatments.

## Study context and location
- Location: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level; 53°22'N, 3°95'W).
- Site characteristics: humic gleysol; sheep excluded from 15/05/2017 to minimize confounding excreta events.

## Treatments and experimental design
- Treatments (n = 4): 
  - Control: no urine applied.
  - Artificial sheep urine: applied in triplicate patches inside the chamber (N application rate 1120 kg N ha-1; 200 ml artifical urine per 100 cm2 patch).
  - C and N: nitrate and glucose treatment (106 kg N ha-1; 213 kg C ha-1; 1 L solution over a 40 × 40 cm square).
- Treatment application date: 25/10/2017.
- Experimental design: randomized block with four plots; 45 days of emissions monitoring post-treatment.

## Data collection and instrumentation
- Monitoring system: automated greenhouse gas system (Queensland University of Technology) using a LI-COR LI-820.
- Sampling regime: eight flux measurements per chamber per day; 1 hour chamber closure; four gas samples analyzed per closure; calibration standard after every fourth gas sample.

## Chambers and sampling details
- Chamber dimensions: base area 0.25 m2; chamber size 50 cm × 50 cm × 15 cm (L × W × H).

## Data content and processing
- Data period: high-frequency emissions data from the automated system.
- Data type: quality-assessed flux data, not raw gas concentration data.
- Quality assurance (QA): inspection of raw data files and GC chromatograms for anomalies; removal of problematic data (e.g., gas peak interference).

## Data structure and units
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B to M: CH4 fluxes (all in mg CO2-C m-2 h-1)
  - Column headers encode treatment and chamber/plot numbers (Control, ArtUrine, CandN)

## Data limitations and governance considerations
- Data are subject to QA-driven exclusion of anomalies; the dataset represents processed flux data rather than raw concentrations.
- Metadata clarity around treatments, units, and column naming aids discoverability and reuse but users should verify any ambiguities (e.g., CH4 flux units expressed as mg CO2-C m-2 h-1).

## Reuse and attribution
- Proper authorship acknowledgment is required for any reuse or reproduction of the data.