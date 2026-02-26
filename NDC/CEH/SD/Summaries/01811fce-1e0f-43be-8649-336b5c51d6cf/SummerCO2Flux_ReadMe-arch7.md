# ReadMe file for SummerCO2Flux.csv

## Overview
- Metadata for CO2 flux measurements from control, artificial sheep urine, and real sheep urine treatments.
- Location: dystric histosol on unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Experimental context: sheep excluded from plots from 15/05/2017 to avoid confounding effects.
- Data are quality-assessed flux measurements, not raw gas concentrations, collected with an automated greenhouse gas monitoring system.

## Spatial and temporal coverage
- Field site: Carneddau mountains, Snowdonia NP, UK.
- Spatial units: experimental plots with chambers (50 cm x 50 cm x 15 cm; basal area 0.25 m2). Within plots, treatments applied as discrete patches inside chambers.
- Temporal coverage: measurements collected for 80 days following treatment (24/07/2017).
- Data timestamps: Timestamp header in format dd/mm/yy hh:mm; Days header indicates time relative to treatment (pre- or post-).

## Experimental design
- Treatments (n = 4):
  - Control: no urine application.
  - Artificial sheep urine: patches within chamber; N application rate ~920 kg N ha-1; 200 ml artificial urine per patch over 100 cm2.
  - Real sheep urine: patches within chamber; N application rate ~930 kg N ha-1; 200 ml real urine per patch over 100 cm2.
- Application date: 24/07/2017.
- Design: randomized block with triplicate patches per treatment within chambers.

## Data collection and quality assurance
- Instrumentation: automated greenhouse gas monitoring system (QUT) with LI-COR LI-820.
- Data rate: eight flux measurements per chamber per day (1 h chamber closure; four gas samples per closure; calibration standard after every fourth sample).
- QA procedures: review raw data files and GC chromatograms for anomalies; remove anomalous data (e.g., gas peak interferences) as needed.
- Data scope: includes high-frequency flux data; does not include raw gas concentration data.

## Data structure and file contents
- Data covers emissions period analyzed by the automated system (high-frequency data only).
- Data represent quality-assessed CO2 flux values, not raw concentrations.

## Variables and data columns
- Timestamp: dd/mm/yy hh:mm
- Days: days relative to treatment (pre- or post-treatment)
- Columns B–M: CO2 fluxes (mg CO2-C m-2 h-1)
- Column headers indicate treatment and chamber/plot numbers:
  - Control = Control treatment
  - ArtUrine = artificial urine treatment
  - Urine = real sheep urine treatment

## GIS-specific considerations and usage notes
- Suitable for map-based visualization of spatially resolved CO2 flux responses at the chamber/patch level within plots.
- Can be integrated with plot boundaries, chamber locations, and patch locations to create spatio-temporal maps of CO2 flux.
- Temporal resolution: high-frequency daily measurements; use Days and Timestamp to construct time-series maps or animated visualizations.
- Data provenance: attribution required; authors must be acknowledged if data are reused or reproduced.
- Limitations for GIS applications:
  - The dataset provides flux values but not full raw gas concentration traces.
  - Spatial coordinates beyond general site location are not provided in this ReadMe; linking to plot/chamber spatial data is needed for precise mapping.
  - Only the post-treatment monitoring window (80 days) is included; pre-treatment baseline coverage is indicated by Days but may be limited to the experimental design.

## Licensing and authorship
- Authors must be acknowledged if the data are reused or reproduced.