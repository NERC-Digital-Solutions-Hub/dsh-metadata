# ReadMe file for SummerCH4Flux.csv

## Overview
- CH4 flux measurements from a field experiment in Snowdonia National Park, Wales, UK.
- Study site: dystric histosol within unimproved grazing land in the Carneddau mountains; site elevation ~556 m a.s.l.; coordinates 53°22'N, 3°95'W.
- Exclusion of sheep from plots starting 15/05/2017 to avoid recent excretal confounding effects.
- Data focus on fluxes (not raw concentrations) collected using an automated greenhouse gas monitoring system.

## Experimental design and treatments
- Treatments (n = 4, described): Control (no urine), Artificial sheep urine, Real sheep urine. Each treatment implemented in triplicate discrete patches within the chamber.
- Nitrogen application rates: Artificial urine ~920 kg N ha-1; Real sheep urine ~930 kg N ha-1.
- Treatment patches were applied on 24/07/2017.
- Experimental layout: randomised block design with multiple chambers/plots per treatment.

## Data collection and instrumentation
- Monitoring system: automated gas monitoring system (gas flux measurements) paired with a SRI 8610 GC.
- Measurement cadence: eight CH4 flux measurements per chamber per day (1-hour chamber closure; four gas samples per hour).
- Calibration: standard analyzed after every fourth gas sample.
- Chamber specifications: basal area 0.25 m2; dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Data scope: high-frequency flux data period; not raw gas concentration data.
- Quality assurance: inspection of raw data files and GC chromatograms to identify and remove anomalies (e.g., gas peak interference).

## Data structure and contents
- Data headers (example): Timestamp (dd/mm/yy hh:mm); Days (time relative to treatment, in days); Columns B–M: CH4 flux values (µg CH4-C m-2 h-1).
- Treatment and chamber/plot identifiers embedded in column headers:
  - Treatments: Control, ArtUrine (artificial urine), Urine (real urine).
  - Each patch/chamber has an assigned plot/chamber number.
- Data are presented as flux values tied to time and spatial unit (chamber/patch within a treatment).

## Spatial and temporal coverage
- Spatial: discrete chambers/patches arranged within the experimental plots at the field site (0.25 m2 chambers).
- Temporal: observations span up to 80 days post-treatment application (with data focusing on the high-frequency period captured by the automated system after treatment dates).

## Data quality and processing notes
- Data represent quality-assessed CH4 flux values (not raw concentration data).
- Anomalies identified via examination of raw files and GC chromatograms; affected data removed as needed.
- Data are suitable for GIS-based visualization of spatial patterns and temporal trends in CH4 flux across treatments.

## Usage, attribution, and limitations
- Authors must be acknowledged if data are reused or reproduced.
- GIS applicability: enables map-based visualization of CH4 flux spatial distribution across patches and temporal dynamics after urine amendments.
- Key limitations to consider:
  - Exact geographic projection/CRS not specified.
  - Flux units are CH4-C per area per time; requires consistent unit handling when integrating with other datasets.
  - The dataset reflects a controlled field experiment with specific treatment conditions; caution needed when extrapolating beyond the study site or timeframe.

## Related notes
- The dataset includes a high-frequency flux subset and explicitly notes it does not include raw gas concentration data.