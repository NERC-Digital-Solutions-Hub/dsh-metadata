# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview and aims
- Study to measure nitrous oxide (N2O) fluxes and associated soil properties on Easter Bush Farm Estate, Midlothian, Scotland, for environmental monitoring and policy evaluation.
- Involved strategic, high-precision data collection across multiple fields and seasons to capture management practice variability.

## Monitoring design and measurement approach
- High-precision dynamic closed chamber system used to measure N2O fluxes.
- Mobile setup: chamber connected to a compact quantum cascade laser (QCL) gas analyser mounted in an off-road vehicle; measurements conducted over a 3-minute period.
- Chamber specifics: circular chamber with a 39 cm² base area; collars inserted 5 cm into soil; measurement radius extended ~30 m from the vehicle.
- Four seasonal measurement periods across autumn 2012 to summer 2013, across 20 fields representing arable fodder crops and grazing pastures.
- Equipment and protocol validated against prior methodological work; 95% confidence intervals calculated from regression fitting, air density, and chamber volume.

## Data collected and variables
- Flux measurements: N2O flux (µg N2O-N m⁻² h⁻¹) with Flux_Error (95% CI).
- Soil measurements taken at 457 of the flux measurement locations:
  - Soil temperature (Soil_T, °C)
  - Water-filled pore space (SMAv, %)
  - Bulk density (BD_density, g cm⁻³)
  - Soil porosity (BD_Porosity)
  - Volumetric water content (BD_VWC)
  - Calculated WFPS (BD_WFPS, %)
  - Soil pH (pH)
  - Inorganic nitrogen (NH4N, NO3N) via KCl extraction
  - Total carbon (Tot_C) and total nitrogen (Tot_N)
- Field-level metadata:
  - Date and period of measurement
  - Field identifier and plot type/description
  - GPS coordinates (GPS_E and GPS_N)

## Data processing, quality control, and uncertainty
- Fluxes computed with the HMR package in R, which selects among five methods to best fit each chamber set.
- Individual regression fits inspected to detect chamber leaks via CO2 response; data deemed unstable were discarded.
- Due to log-normal distribution and mixed data sources, outliers in flux and soil variables were retained when not demonstrably unreliable.
- Findings linked to prior methodological work for uncertainty assessment and data interpretation.

## Data structure and units
- Core dataset file: Farm_Flux_and_Soil
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
  - BD_density (g cm⁻³)
  - BD_Porosity
  - BD_VWC
  - BD_WFPS (%)
  - pH
  - NH4N (g N H4-N kg⁻¹)
  - NO3N (g NO3-N kg⁻¹)
  - Tot_C (g C kg⁻¹)
  - Tot_N (g N kg⁻¹)
  - Flux (µg N2O-N m⁻² h⁻¹)
  - Flux_Error (µg N2O-N m⁻² h⁻¹)
- Structure supports linkage between flux measurements and soil properties, enabling integrated analysis.

## Temporal and spatial scope
- Location: Easter Bush Farm Estate, near Penicuik, Midlothian, Central Scotland.
- Timeframe: Measurements from autumn 2012 through summer 2013.
- Spatial coverage: 20 representative fields with diverse management practices (arable fodder crops and grazing pastures).

## Relevance for monitoring frameworks
- Demonstrates an end-to-end data collection and processing workflow for environmental monitoring:
  - Integration of precise gas flux measurements with soil chemistry and physical properties.
  - Explicit data governance elements: standardized measurement protocols, detailed metadata, and transparent uncertainty estimation.
  - Use of established analytical tools (HMR in R) and adherence to validated methodologies.
  - Clear data structure that facilitates replication, verification, and policy-relevant analysis.