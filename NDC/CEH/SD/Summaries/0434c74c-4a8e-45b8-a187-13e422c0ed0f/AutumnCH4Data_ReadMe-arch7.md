# Authors must be acknowledged if data is re-used or reproduced. The data corresponds to CH4 emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) in autumn, 2016

## Overview
- Study focus: CH4 emissions from three treatments—Control (no urine), artificial urine, and real urine—applied to an orthic podzol in semi-improved upland grassland.
- Location and design: Henfaes Research Station, North Wales; randomised block experimental design on field plots.
- Data collection system: Automated greenhouse gas monitoring system (GHS) using a SRI 8610 GC; processed flux data rather than raw concentrations.

## Data collection details
- Measurements: Eight CH4 flux measurements per chamber per day (1-hour chamber closure period; four gas samples analyzed per closure).
- Calibration: Calibration standard analyzed after every fourth gas sample.
- Chamber specifications: 0.25 m2 basal area; chambers 50 cm x 50 cm x 15 cm (L x W x H).

## Data content and quality
- Data included: High-frequency, quality-assessed CH4 flux data.
- Quality assurance: Raw data files and GC chromatograms inspected for anomalies; anomalies removed as needed.
- Data type: Flux data expressed as CH4-C flux (not raw gas concentrations).

## Data structure and headers
- Timestamp format: dd/mm/yy hh:mm
- Flux columns: Columns B to M represent CH4 fluxes (mg CH4-C m-2 h-1).
- Metadata in headers: Information on treatment and chamber/plot numbers.
- Treatments encoded: Control = control treatment, ArtUrine = artificial urine treatment, Urine = real urine treatment.

## Geospatial and GIS considerations
- Spatial units: Chambers/plots embedded within the field site; suitable for spatial mapping of CH4 flux.
- Location context: Site coordinates and elevation provided; data can be linked to GIS layers (plots, plot positions, elevation).

## Practical use for GIS specialists
- Create maps of CH4 flux across plots for specific dates/times.
- Develop time-series visualizations by plot or treatment.
- Integrate with ancillary spatial data (topography, soil type) to explore spatial patterns.
- Use the quality-assured flux data (not raw concentrations) for reliable spatial analyses.

## Notes and caveats
- Data scope: High-frequency flux data for autumn 2016 at a single site.
- Data type limitation: Does not include raw gas concentration data; flux values are pre-processed after QA.