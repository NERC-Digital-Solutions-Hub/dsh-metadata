# ReadMe file for SpringCO2Data.csv

## Overview
- CO2 emissions measurements from three treatments: Control, artificial urine (ArtUrine), and real urine (Urine) applied to an orthic podzol in a semi-improved upland grassland.
- Study location: Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W); spring 2016.
- Experimental design: randomized block experimental design with plots.

## Experimental Setup
- Site characteristics: semi-improved upland grassland on orthic podzol soil.
- Plot and chamber details: chamber basal area 0.25 m²; chamber dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Treatments administered via urine (artificial and real) and a control (no urine).

## Data Collection and Measurement
- Instrumentation: automated greenhouse gas monitoring system (LI-COR LI-820) managed at Queensland University of Technology.
- Sampling regime: eight CO2 flux measurements per chamber per day.
  - Each measurement involves a 1-hour chamber closure with four gas samples analyzed per closure.
  - Calibration standard analyzed after every fourth gas sample.
- Data type: quality-assessed CO2 flux data (mg CO2-C m-2 h-1); not raw gas concentration data.

## Data Structure and Headers
- Timestamp format: dd/mm/yy hh:mm.
- Data columns: Columns B to M contain CO2 flux values (mg CO2-C m-2 h-1).
- Column headers encode treatment and chamber/plot identifiers:
  - Treatments include Control, ArtUrine (artificial urine), and Urine (real urine).

## Data Quality Assurance
- Quality assurance steps include inspection of raw data files and chromatograms for anomalies.
- Anomalies or interference in gas peaks may lead to data removal.

## Metadata and Provenance
- Authors must be acknowledged if the data are reused or reproduced.
- The dataset represents processed, quality-assessed flux data along with detailed experimental and instrumentation metadata.
- Geographic and temporal context provided to enable correct interpretation and replication.

## Potential Analyses and Uses
- Compare CO2 flux across Control, ArtUrine, and Urine treatments.
- Analyze diurnal or daily patterns and treatment effects on soil CO2 efflux.
- Integrate with environmental variables if available for modeling treatment-driven emissions.

## Limitations and Considerations
- Data pertain to spring 2016 at a single upland site, which may limit generalizability.
- Flux data are not raw gas concentrations; interpretation should consider QA steps and calibration protocol.
- Spatial scale is per chamber (0.25 m²); extrapolation to larger areas requires careful scaling.