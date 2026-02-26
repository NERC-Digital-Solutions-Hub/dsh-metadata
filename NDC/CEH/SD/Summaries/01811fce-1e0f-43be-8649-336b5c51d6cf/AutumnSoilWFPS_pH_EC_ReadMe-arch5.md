# ReadMe file for AutumnSoilWFPS_pH_EC.csv

## Overview
- Dataset contains soil measurements of water-filled pore space (WFPS), pH, and electrical conductivity (EC).
- Treatments include control (no urine), artificial sheep urine, and nitrate plus glucose (CandN) applied to plots.
- Location: humic gleysol in unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sampling context: sheep excluded from 15/05/2017 to avoid confounding excretal input; soils sampled adjacent to greenhouse gas sampling chambers.
- Sampling cadence: measured with respect to days after treatment; data collection processed within 24 hours of collection.

## Experimental design and treatments
- Treatments (n = 4 as noted in the document; described below):
  - Control: no urine application.
  - Artificial sheep urine (ArtUrine): applied in triplicate discrete patches per plot (each patch with 1120 kg N ha^-1; 200 mL artificial urine over 100 cm^2 soil surface per patch).
  - CandN: nitrate and glucose treatment applied at 106 kg N ha^-1 and 213 kg C ha^-1; 1 L solution applied across a 40 × 40 cm square adjacent to the chamber.
- Treatment timing:
  - ArtUrine patches applied as part of the experimental setup.
  - CandN treatment applied on 25/10/2017.
- Replication details: measurements taken from plots adjacent to chambers; specific replication counts per treatment implied by the description (art urine in triplicate patches, across plots).

## Data collection and processing
- Soil sampling method: replicated areas adjacent to greenhouse gas sampling chambers; auger sampling; processed within 24 hours of collection.
- WFPS calculation: ratio of volumetric water content to soil porosity.
  - Porosity estimation: based on particle densities of 2.65 g cm^-3 for mineral fraction and 1.4 g cm^-3 for organic fraction (Rowell, 1994).
- pH and EC measurement: determined in 1:2.5 soil-to-distilled water suspensions using standard electrodes.

## Data schema and headers
- Date: date of soil sample collection (dd/mm/yyyy).
- Days: days after treatment application.
- Treatment: code for treatment per plot ('Control', 'ArtUrine', 'CandN').
- Plot: plot identifier.
- WFPS: percent soil water-filled pore space.
- pH: soil pH value.
- EC: soil electrical conductivity in µS cm^-1.

## Data quality and provenance
- Data provenance: field measurements with explicit treatment mapping and collection timing; processing within 24 hours.
- Documentation includes calculation method for WFPS and porosity assumptions.
- Authors must be acknowledged in any reuse or reproduction of the data.

## Location and scope
- Geographic coordinates and altitude provide spatial context for data stewardship and potential cross-site comparisons.
- Units and scales are specified (WFPS in percent, pH unitless, EC in µS cm^-1).

## Usage, attribution, and references
- Appropriate acknowledgment required for data reuse.
- Key reference for methodology: Rowell, D.L. (1994). Soil Science: Methods and Applications. Longman UK Ltd.
- Dataset-oriented governance: clear linkage between treatment definitions, timing, sampling, and data headers to support discoverability and reuse.