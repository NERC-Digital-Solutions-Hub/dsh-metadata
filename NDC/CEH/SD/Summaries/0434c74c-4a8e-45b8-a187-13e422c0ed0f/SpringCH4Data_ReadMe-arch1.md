# ReadMe file for SpringCH4Data.csv

## Overview
- Dataset of CH4 emissions measured under three treatments (Control, artificial urine, real urine) on an orthic podzol within semi-improved upland grassland.
- Location: Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Time: Spring 2016.
- Emissions measured using an automated gas monitoring system; data represent quality-assessed flux values, not raw gas concentrations.
- Authors must be acknowledged if data are reused or reproduced.

## Experimental design
- Plot layout: Randomised block design.
- Treatments: Control (no urine), artificial urine, real urine.
- Chamber dimensions: 50 cm x 50 cm x 15 cm (area 0.25 m² per chamber).
- Chambers deployed on plots within semi-improved upland grassland.

## Measurements and instrumentation
- Automated gas monitoring system (SRI 8610 GC) operated by Queensland University of Technology, Institute for Future Environments.
- Data collected by eight CH4 flux measurements per chamber per day.
  - Each 1-hour chamber closure period yields four gas samples analyzed per closure, totaling eight flux measurements daily per chamber.
- Calibration: Calibration standard analyzed after every fourth gas sample.

## Data content and structure
- Data type: Quality-assessed CH4 flux data (mg CH4-C m^-2 h^-1); not raw gas concentration data.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Columns B to M: CH4 flux values (mg CH4-C m^-2 h^-1)
  - Treatement and plot/chamber identifiers embedded in headers (Control, ArtUrine, Urine).

## Data quality assurance
- QA steps include inspection of raw data files and GC chromatograms for anomalies; data removed if issues detected (e.g., gas peak interference).
- Data represent cleaned, processed flux values following QA procedures.

## Location, timing, and scope
- Site coordinates and elevation provided.
- Spring 2016 data collection period.
- Flux data captured per chamber per day across the three treatments.

## Usage notes and attribution
- Suitable for comparing CH4 flux responses to urine treatments under upland grassland conditions.
- Consider scale and unit limitations: chamber-based measurements (0.25 m²) reflect fluxes at small plot scale.
- Proper attribution required when reusing or reproducing the dataset.