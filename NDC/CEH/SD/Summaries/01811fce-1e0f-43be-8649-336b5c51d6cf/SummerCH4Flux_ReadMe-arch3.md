# ReadMe file for SummerCH4Flux.csv

## Overview
- CH4 flux measurements from plots subjected to control (no urine), artificial sheep urine, and real sheep urine on a dystric histosol in unimproved grazing land.
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Exclusion: Sheep removed from 15/05/2017 to avoid recent excretal effects.
- Study duration: 80 days post-treatment.
- Data type: High-frequency emissions data from an automated greenhouse gas monitoring system; not raw gas concentrations.

## Experimental Setup and Site
- Field design: Randomised block experimental design with four treatments (as described below) and triplicate patches per treatment within chambers.
- Chamber specifications: 0.25 m2 basal area; dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Monitoring period: 80 days after treatment application.

## Treatments and Experimental Design
- Treatments (n = 4): 
  - Control: no urine application.
  - Artificial sheep urine: applied in triplicate discrete patches inside the chamber (N rate 920 kg N ha-1; 200 mL artificial urine per patch over 100 cm2).
  - Real sheep urine: patches applied in triplicate discrete patches (N rate 930 kg N ha-1; 200 mL real sheep urine per patch over 100 cm2).
- Treatment application date: 24/07/2017.
- Patches: Discrete patches within each chamber; each patch represents an N input as specified above.

## Data Collection and Instrumentation
- Instrumentation: Automated greenhouse gas monitoring system (Queensland University of Technology) with a SRI 8610 GC (Torrance, USA).
- Flux sampling: Eight flux measurements per chamber per day; 1-hour chamber closure with four gas samples analysed per closure.
- Calibration: Calibration standard analysed after every fourth gas sample.
- Data scope: Includes data from the high-frequency automated system period; reflects quality-assessed flux data, not raw gas concentration data.

## Data Structure and Format
- Chamber area and geometry: Chamber basal area 0.25 m2; dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Data period: Emissions data analyzed during the high-frequency period only.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B to M: CH4 fluxes (µg CH4-C m-2 h-1)
  - Treatments encoded in headers: Control, ArtUrine (artificial urine), Urine (real urine)
    - Control = Control treatment
    - ArtUrine = artificial urine treatment
    - Urine = real urine treatment

## Quality Assurance and Data Curation
- QA procedures: Visual inspection of raw data files and GC chromatograms for anomalies; removal of problematic data as necessary (e.g., peak interferences).
- Data quality: Only quality-assessed flux data included; not the raw gas concentration data.
- Data provenance: Data attributed to the specific field site, treatment, and chamber/plot configuration; each entry is linked to timestamp and Days relative to treatment.

## Metadata, Attribution, and Data Access
- Attribution: Authors must be acknowledged if data are reused or reproduced.
- Data provenance: Clear linkage between treatment type, patch, chamber, and date of measurement.
- Accessibility notes: Data are provided with accompanying metadata to support verification and reuse; underlying data management and sharing considerations are in place.