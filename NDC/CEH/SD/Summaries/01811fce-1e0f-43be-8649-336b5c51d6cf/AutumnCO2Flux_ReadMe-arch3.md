# ReadMe file for AutumnCO2Flux.csv

- Purpose: Document the CO2/CH4 flux measurements and the experimental treatments applied to a humic gleysol in Snowdonia National Park to support environmental health monitoring, analysis, and policy-relevant decisions.
- Data scope: Flux measurements collected 45 days after treatment applications across four plots per treatment in a randomized block design.
- Acknowledgment requirement: Authors must be acknowledged if data are reused or reproduced.

## Location and experimental context

- Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Site characteristics: unimproved grazing land; plots excluded from sheep from 15/05/17 to avoid confounding excretal events.
- Treatments (n = 4 patches per treatment): 
  - Control: no urine application.
  - Artificial sheep urine: applied in triplicate discrete patches within the chamber (1120 kg N ha-1; 200 ml artificial urine over 100 cm2 per patch).
  - C and N (nitrate and glucose): applied at 106 kg N ha-1 and 213 kg C ha-1 (1 L of nitrate+glucose solution across a 40 × 40 cm area).
- Treatment date: 25/10/17.
- Experimental design: randomized block design.

## Measurements and instrumentation

- Monitoring system: automated greenhouse gas monitoring system (Queensland University of Technology) connected to a LI-COR LI-820 gas analyzer.
- Sampling cadence: eight flux measurements per chamber per day; 1-hour chamber closure per measurement; four gas samples analyzed per closure.
- Calibration: calibration standard analyzed after every fourth gas sample.
- Chamber specifications: basal area 0.25 m2; chamber dimensions 50 cm × 50 cm × 15 cm (l × w × h).

## Data content and structure

- Data type: quality-assessed flux data (not raw gas concentration data) representing emissions during the monitoring period.
- Data period: emissions monitored for 45 days following treatment.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B–M: CH4 fluxes (units: mg CO2-C m-2 h-1)
  - Treatment/Plot codes: Control = Control, ArtUrine = artificial urine treatment, CandN = nitrate and glucose treatment
- Data coverage: emissions data from the automated system (high-frequency data) across treatments and chambers/plots.

## Data quality, cleaning, and provenance

- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; removal of anomalies as needed (e.g., gas peak interference).
- Data presented: flux data that passed QA; not raw concentration data.
- Metadata and traceability: detailed treatment, plot, and timing information included to support reproducibility and auditability.

## Usage, attribution, and limitations

- Attribution: authors must be acknowledged if data are reused or reproduced.
- Key limitations and considerations:
  - Data represent flux measurements from a specific site and timeframe; extrapolation beyond this context should be done cautiously.
  - CH4 fluxes are reported with CO2-C-based units, which may require careful interpretation in cross-dataset analyses.