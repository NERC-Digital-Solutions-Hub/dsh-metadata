# N2O emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (autumn, 2016)

## Overview
- Study location: semi-improved upland grassland on orthic podzol at Henfaes Research Station, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Experimental design: randomised block with treatments including Control (no urine), artificial urine, and real urine.
- Data focus: high-frequency N2O flux measurements from chambers, plus monthly manual flux measurements from smaller chambers.
- Application for GIS: enables spatial mapping of N2O flux by plots/chambers over time, suitable for integration with other site geospatial data.

## Data collection and design
- Automated high-frequency measurements:
  - Instrument: automated greenhouse gas monitoring system linked to a SRI 8610 GC.
  - Schedule: eight flux measurements per chamber per day; 1-hour chamber closure with four gas samples per closure.
  - Calibration: standard analysed after every fourth gas sample.
- Chamber specifications:
  - Large chambers: 50 cm x 50 cm x 15 cm (area 0.25 m2).
- Manual measurements:
  - Smaller chambers: 40 cm x 20 cm x 20 cm.
  - Frequency: monthly flux measurements after the high-frequency period.
  - Instrument: Perkin Elmer 580 GC with Turbo Matrix 110 auto sampler; calibrated with four gas standards (BOC gases).
- Data type:
  - Flux data are quality-assessed outputs (not raw gas concentrations).

## Data structure and metadata
- Time format: Date_Time = dd/mm/yy hh:mm.
- Flux data columns: Columns B to M contain N2O fluxes (micrograms N2O-N m-2 h-1).
- Treatments encoded in headers: Control, ArtUrine (artificial urine), Urine (real urine).
- Plot and chamber identifiers included in headers to support spatial linking.

## Data quality and processing
- Quality assurance:
  - Visual inspection of raw data files and GC chromatograms for anomalies; flagged data removed as needed.
- Handling of detection limits:
  - Manual data fluxes below detection limit replaced with zero.

## GIS-specific considerations
- Spatial linkage: data can be joined to plot-level and chamber-level geospatial identifiers for mapping emissions.
- Temporal resolution: combination of high-frequency (daily) and monthly measurements enables time-series analyses and seasonal emission pattern mapping.
- Units and comparability: fluxes expressed as micrograms N2O-N per square meter per hour, suitable for integration with environmental rasters and covariates (soil type, management, urine treatment).

## Limitations and notes
- Data represent quality-assessed flux values, not raw gas concentration traces.
- Explicit site-level coordinates beyond general location are not provided in the summary; integration with GIS requires plot/chamber georeferencing within the Henfaes site.

## Attribution
- Authors must be acknowledged if the data are re-used or reproduced.