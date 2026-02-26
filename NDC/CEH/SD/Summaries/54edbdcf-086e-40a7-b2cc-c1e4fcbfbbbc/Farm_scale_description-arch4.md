# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview
- Location and collaboration: Easter Bush Farm Estate, Midlothian, UK; Scotland's Rural College (SRUC) and University of Edinburgh (UoE) for commercial and research purposes.
- Timeframe and scope: four seasonal measurement periods between autumn 2012 and summer 2013; over 500 N2O flux measurements and 457 soil measurements.
- Field selection: 20 fields representing a wide variety of management practices; fields used for arable fodder or grazing pasture.

## Data collection and instrumentation
- Measurement system: dynamic closed chamber with a pump and a compact continuous wave quantum cascade laser (QCL) gas analyser; mobile setup mounted in a vehicle.
- Chamber and sampling: circular chamber (39 cm diameter) placed on soil collars inserted 5 cm deep; 3-minute measurement period; chamber circulates air through inlet/outlet tubing with a 30 m radius for placement.
- Uncertainty handling: 95% confidence interval derived from regression of gas concentration with time (dc/dt), air density, and chamber volume.

## Measurements and variables
- Flux data: N2O flux (µg N2O-N m-2 h-1) with 95% confidence interval.
- Soil measurements (457 locations): soil temperature (°C), water-filled pore space (WFPS %), bulk density (g cm-3), soil porosity, volumetric water content (VWC), WFPS, pH (in H2O), NH4+-N (g NH4-N kg-1), NO3--N (g NO3-N kg-1), total carbon (Tot_C, g C kg-1), total nitrogen (Tot_N, g N kg-1).
- Metadata and site details: Date (dd/mm/yyyy), Period (season and year), Measurement_ID, Field, Plot type, Plot Description, GPS_E, GPS_N.

## Experimental design and sampling
- Field diversity: 20 fields chosen to represent the estate’s management practices.
- Sampling cadence: measurements conducted in four seasonal periods; total measurements exceed 500 flux measurements and 457 soil measurements across arable and grazing fields.

## Data processing and quality control
- Flux calculation: using the HMR package in R to apply up to five methods and select the best fit for each chamber set.
- Quality checks: manual inspection of regression fits to identify chamber leaks via CO2 response; unstable signals discarded.
- Data characteristics: data are log-normally distributed; outliers retained due to lack of evidence they are unreliable.
- Uncertainty: flux uncertainties quantified as 95% CIs based on regression fit, air density, and chamber volume (per Cowan et al., 2014).

## Data structure, units and provenance
- Dataset/file: Farm_Flux_and_Soil.
- Recorded variables (21 total): Date (dd/mm/yyyy), Period, Measurement_ID, Field, Plot type, Plot Description, GPS_E, GPS_N, Soil_T (°C), SMAv (WFPS %), BD_density (g cm-3), BD_Porosity, BD_VWC, BD_WFPS, pH, NH4N (g NH4-N kg-1), NO3N (g NO3-N kg-1), Tot_C (g C kg-1), Tot_N (g N kg-1), Flux (µg N2O-N m-2 h-1), Flux_Error (µg N2O-N m-2 h-1, 95% CI).
- Time and location formats: Date as dd/mm/yyyy; GPS coordinates in easting/northing (BNG).
- Data provenance: methods and related data are documented with multiple references (Cowan et al. 2014, 2015, 2017; Levy et al. 2011; Pedersen et al. 2010; Rowell 1994).

## References and context
- Methodological foundations and prior related studies cited to support measurement approaches, uncertainty quantification, and data structure.