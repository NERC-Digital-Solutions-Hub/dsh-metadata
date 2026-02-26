# ReadMe file for SummerSoilWFPS_pH_EC.csv

## Overview
- Dataset of soil percent water-filled pore space (WFPS), pH, and electrical conductivity (EC) under three treatments: control (no urine), artificial sheep urine, and real sheep urine.
- Collected from a dystric histosol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Site details: 556 m above sea level; coordinates ~53°22'N, 3°95'W.
- Sheep excluded from 15/05/17 to avoid confounding recent excretal events; samples processed within 24 hours of collection.

## Dataset scope and location
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK.
- Soils: dystric histosol in unimproved grazing land.
- Sampling approach: replicated areas adjacent to green-house gas sampling chambers within each experimental plot.

## Treatments and experimental design
- Treatments (n = 4 per treatment; real urine n = 3): 
  - Control: no urine application.
  - Artificial sheep urine: patches applied with N application rate of 920 kg N ha^-1; 200 mL urine-equivalent per patch over 100 cm^2 soil surface.
  - Real sheep urine: patches applied with N application rate of 930 kg N ha^-1; 200 mL urine per patch over 100 cm^2 soil surface.
- Treatment application date: 24/07/17.
- Each plot contains discrete patches representing the treatments.

## Sampling and measurements
- Soil sampling method: from replicated areas adjacent to the greenhouse gas sampling chambers using an auger.
- Processing: samples processed within 24 hours of collection.
- Measurements:
  - WFPS: calculated as volumetric water content divided by soil porosity.
  - pH and EC: determined in 1:2.5 soil-to-distilled water suspensions using standard electrodes.

## Data structure and headers
- Date: date of soil sample collection (dd/mm/yyyy).
- Days: days after treatment application.
- Treatment: "Control", "ArtUrine" (Artificial urine), or "RealUrine" (Real sheep urine).
- Plot: plot identifier.
- WFPS: percent soil water-filled pore space.
- pH: soil pH.
- EC: soil electrical conductivity (µS cm^-1).

## Calculation methods
- WFPS calculation: WFPS = volumetric water content / soil porosity.
- Porosity: estimated using particle densities of 2.65 g cm^-3 (mineral fraction) and 1.4 g cm^-3 (organic fraction) per Rowell (1994).
- pH and EC: determined from 1:2.5 soil-to-distilled water suspensions.

## Temporal and spatial considerations
- Temporal: data captured as Days after treatment, with sampling on 24/07/17.
- Spatial: plots represent discrete treatment patches within the experimental area; data can be joined to spatial locations of plots for map-based visualization.

## Provenance and usage notes
- Authors must be acknowledged if data are reused or reproduced.
- Location and sampling specifics allow GIS-based mapping of soil properties by treatment and time.
- Dataset suitable for map-centric analysis of treatment effects on soil moisture (WFPS), acidity (pH), and salinity (EC).

## References
- Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman Group UK Ltd., London, UK.