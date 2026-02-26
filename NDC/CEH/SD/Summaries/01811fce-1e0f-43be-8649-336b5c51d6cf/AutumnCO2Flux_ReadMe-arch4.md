# ReadMe file for AutumnCO2Flux.csv

## What the dataset is
- CO2 flux measurements from grazing land plots under three treatments (control with no urine, artificial sheep urine, nitrate + glucose) applied to a humic gleysol in Snowdonia National Park, Wales, UK.
- Sheep excluded on 15/05/17 to avoid confounding excretal events.
- Data represent quality-assessed flux values (not raw gas concentrations) from automated monitoring.

## Treatments and experimental design
- Treatments (n = 4 replicates each):
  - Control: no urine application.
  - Artificial sheep urine (ArtUrine): applied in triplicate patches inside the chamber; each patch delivers 1120 kg N ha-1; 200 ml artificial urine over 100 cm2 per patch.
  - Nitrate and glucose (CandN): nitrate + glucose at 106 kg N ha-1 and 213 kg C ha-1; 1 L applied across a 40 × 40 cm square inside the chamber.
- Experimental design: randomized block with four replicates per treatment.
- Treatment application date: 25/10/17.

## Monitoring and instrumentation
- Emissions monitored for 45 days post-treatment using an automated greenhouse gas monitoring system (QUT) with a LI-COR LI-820.
- Measurement cadence: eight flux measurements per chamber per day (1 h chamber closure; 4 gas samples per closure).
- Calibration: standard analyzed after every fourth gas sample.

## Chamber specifications
- Chamber basal area: 0.25 m2.
- Chamber size: 50 cm × 50 cm × 15 cm (L × W × H).

## Data content and structure
- Data period: high-frequency data from the automated system.
- Data type: quality-assessed flux data (not raw gas concentrations).
- Headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B to M: CH4 fluxes (in mg CO2-C m-2 h-1)
  - Column headers include treatment and chamber/plot numbers (Control, ArtUrine, CandN)

## Quality assurance and data processing
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; removal of anomalous data as needed (e.g., gas peak interference).

## Location and time context
- Location: unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK.
- Coordinates and elevation: 53°22'N, 3°95'W; 556 m above sea level.

## Authorship and usage
- Authors must be acknowledged if data are re-used or reproduced.

## Relevance for data leadership and governance
- Demonstrates end-to-end data lifecycle: experimental design, precise treatment application, high-frequency data capture, QA/QA, and clear metadata.
- Highlights the importance of metadata richness (treatment details, patch sizes, N/C rates, chamber specs) for discoverability and reuse.
- Illustrates data governance aspects: documentation of data processing (not raw data), clear licensing/acknowledgment requirements, and data quality considerations.
- Shows challenges alignment with data system goals: data availability, standardization of headers/units, and metadata clarity to support cross-project use and integration.