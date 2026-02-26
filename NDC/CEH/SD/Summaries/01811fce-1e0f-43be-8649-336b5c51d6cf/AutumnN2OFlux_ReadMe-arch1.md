# ReadMe file for AutumnN2OFlux.csv

- Purpose: Describes N2O flux measurements under different treatments applied to a humic gleysol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK. Sheep were excluded from 15/05/17 to avoid confounding from recent excretal events.
- Location and context: 556 m above sea level; coordinates 53°22'N, 3°95'W.

## Treatments and Experimental Design
- Treatments (n = 4 plots per treatment): 
  - Control: no urine application.
  - Artificial sheep urine: urine applied in triplicate patches inside the chamber; each patch delivers 1120 kg N ha-1; 200 mL artificial urine per patch over 100 cm2 soil surface.
  - C and N: nitrate and glucose treatment; 106 kg N ha-1 and 213 kg C ha-1; 1 L applied across a 40 × 40 cm square inside the chamber.
- Application date: 25/10/17.
- Experimental design: randomized block design.
- Monitoring duration: 118 days post-treatment application.

## Data Collection and Instruments
- Primary measurement system: automated greenhouse gas monitoring system (Queensland University of Technology) with an SRI 8610 GC.
- Sampling cadence (high-frequency period): 8 flux measurements per chamber per day; 1 h chamber closure; 4 gas samples per closure; calibration after every fourth sample.
- Chamber specifications: basal area 0.25 m2; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
- Secondary measurements: monthly manual flux measurements from the same chambers after the high-frequency period.
- Manual analysis: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 autosampler; four gas standards spanning measured concentrations (BOC gases, Liverpool) used for calibration.
- Data type: flux data that have passed quality assessment (not raw gas concentrations). Includes QA steps to identify/remove anomalies in raw data and GC chromatograms.

## Data Content and Structure
- Data coverage: emissions data during the high-frequency automation period plus later monthly manual flux measurements.
- Data headers (in AutumnN2OFlux.csv):
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B to M: N2O fluxes (µg N2O-N m-2 h-1)
  - Column headers encode treatment and chamber/plot identifiers (Control, ArtUrine for artificial urine, CandN for nitrate and glucose)
- Data scope: represents quality-assessed flux data (not raw gas concentrations).

## Quality Assurance and Data Handling
- QA procedures: inspection of raw data files and GC chromatograms for anomalies; removal of anomalous data as necessary.
- Documentation: authorship must be acknowledged if data are reused or reproduced.

## Practical Considerations for Analysts
- Use cases: identify correlations between N2O flux and treatments, compare flux dynamics across treatments, develop predictive models of N2O emissions in response to urine and nutrient additions.
- Scale and granularity: high-frequency flux data suitable for short-term dynamics; monthly measurements provide longer-term context.
- Data integration: be prepared to unify high-frequency flux data with monthly measurements; ensure alignment with treatment and chamber identifiers.