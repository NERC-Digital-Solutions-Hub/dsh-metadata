# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview
- Study conducted on Easter Bush Farm Estate (Midlothian, UK) to measure soil nitrous oxide (N2O) fluxes and related soil properties.
- Farm comprises arable fodder crops and grazing pasture; monitored across four seasonal periods between autumn 2012 and summer 2013.
- Data include >500 flux measurements across 20 selected fields and 457 accompanying soil measurements, enabling analysis of management practices on N2O emissions.

## Experimental Design and Setting
- High-precision flux chamber system used to measure N2O fluxes.
- Site: Easter Bush Farm Estate, SRUC and University of Edinburgh collaboration.
- 20 representative fields chosen to capture management diversity and accessibility for equipment.
- Measurements aligned with prior work (Cowan et al., 2017) to account for field heterogeneity.

## Measurement System and Procedures
- Dynamic closed chamber with a pump (SH-110) and a compact quantum cascade laser gas analyser (CW-QC-TILDAS-76-CS) for real-time N2O monitoring.
- Chamber details: circular chamber of 39 cm diameter, inserted 5 cm into soil via stainless steel collars.
- 30 m radius around the measurement vehicle to place the chamber; measurements collected over a 3-minute period.
- N2O fluxes calculated from the rate of change in gas concentration (dc/dt) with adjustments for air density and chamber volume.
- Quality control included inspection of CO2 response to detect leaks; data with unstable signals discarded.

## Soil Measurements and Analyses
- Soil samples collected at 457 flux measurement locations (5 cm depth) immediately after flux measurement.
- Soil samples stored at -18°C and analyzed later for:
  - pH (in water) using standard soil methods.
  - Available nitrogen: ammonium (NH4+) and nitrate (NO3−) using 1 M KCl extraction.
  - Total carbon (Tot_C) and total nitrogen (Tot_N) via grinding and analysis.
  - Bulk density and soil moisture measures: soil moisture content via oven-drying; calculated bulk density and porosity; water-filled pore space (WFPS) derived.
- Soil analyses performed with established protocols and calibrated instruments (AutoAnalyser for NH4+/NO3−; Vario EL cube for C and N; standard pH measurement).

## Data Processing, Quality Control, and Uncertainty
- Fluxes calculated with the HMR package for R, which tests five estimation methods and selects the best fit per chamber set.
- Data validation included checking for chamber leaks via CO2 response; unstable signals led to data discard.
- Given log-normal distribution of fluxes and soil variables, outliers were retained when there was no evidence they were unreliable measurements.
- Uncertainty considerations referenced through standard methods for flux quantification (e.g., Cowan et al., 2014; 2011–2017 related work).

## Data Structure and Content
- File: Farm_Flux_and_Soil
- Key fields:
  - Date (dd/mm/yyyy)
  - Period (season and year)
  - Measurement_ID
  - Field
  - Plot type
  - Plot Description
  - GPS_E, GPS_N
  - Soil_T (°C)
  - SMAv (WFPS %)
  - BD_density (g cm-3)
  - BD_Porosity
  - BD_VWC
  - BD_WFPS
  - pH
  - NH4N (g NH4-N kg-1)
  - NO3N (g NO3-N kg-1)
  - Tot_C (g C kg-1)
  - Tot_N (g N kg-1)
  - Flux (µg N2O-N m-2 h-1)
  - Flux_Error (µg N2O-N m-2 h-1, 95% CI)
- The dataset encompasses 500+ flux measurements and 457 concurrent soil measurements across a diversity of field management practices (arable fodder crops and grazing pastures).
- Four seasonal measurement periods and field-level descriptions provide context for environmental and management influences on N2O emissions.

## References
- Cowan et al. 2014, 2015, 2017 (methods for N2O flux measurement, spatial variability, and emissions sources)
- Levy et al. 2011; Pedersen et al. 2010 (uncertainty quantification in trace gas fluxes and comprehensive flux estimation approaches)
- Rowell 1994 (soil methods and applications)