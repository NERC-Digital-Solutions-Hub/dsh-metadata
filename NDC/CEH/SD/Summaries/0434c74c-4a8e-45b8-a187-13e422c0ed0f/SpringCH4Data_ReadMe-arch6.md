# ReadMe file for SpringCH4Data.csv

## Overview
- CH4 emissions measured from plots subjected to three treatments: Control, artificial urine (ArtUrine), and real urine (Urine).
- Experimental setup: orthic podzol within a semi-improved upland grassland, Henfaes Research Station, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Study design: randomised block.

## Data collection and design
- Monitoring system: automated greenhouse gas monitoring system with a SRI 8610 GC.
- Measurements: eight flux measurements per chamber per day (1-hour chamber closure; 4 gas samples analysed per closure).
- Calibration: a calibration standard analysed after every fourth gas sample.
- Chamber specifics: each chamber has a basal area of 0.25 m2; dimensions 50 cm x 50 cm x 15 cm (l x w x h).
- Data type: flux data that have passed quality assessment (not raw gas concentration data).

## Data content and structure
- Time component: Timestamp format is dd/mm/yy hh:mm.
- Flux data: Columns B to M contain CH4 fluxes in mg CH4-C m-2 h-1.
- Metadata in headers: column headers indicate treatment (Control, ArtUrine, Urine) and chamber/plot numbers.
- Output focus: data are ready-to-use flux values with documentation on treatments and plots.

## Quality assurance and data cleaning
- QA procedures: inspect raw data files and GC chromatograms for anomalies.
- Problem handling: anomalous data (e.g., gas peak interference) removed as needed.

## Location, timing, and context
- Site: Henfaes Research Station, Abergwyngregyn, North Wales.
- Elevation: 270 m a.s.l.
- Coordinates: 53°13'N, 4°0'W.
- Timeframe: spring 2016.
- Data scope: represents quality-assessed flux measurements rather than raw concentrations.

## Usage notes and attribution
- Data should be cited with an acknowledgment of the authors if re-used or reproduced.
- Headers and column labeling provide clear mapping to treatment type and chamber/plot identifiers to facilitate analysis and self-serve exploration.