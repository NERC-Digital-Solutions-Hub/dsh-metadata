# ReadMe file for AutumnSoilWFPS_pH_EC.csv

- This ReadMe describes a dataset containing soil properties: water-filled pore space (WFPS), pH, and electrical conductivity (EC).
- Treatments studied: Control (no urine), Artificial sheep urine, and Nitrate+Glucose (CandN).
- Experimental context: conducted on a humic gleysol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK; sampling occurred after treatment applications with plots excluded from sheep for a defined period to avoid confounding excreta effects.
- Data ownership and attribution: authors must be acknowledged if data are reused or reproduced.
- Source reference for methods: Rowell (1994) cited for porosity calculations.

## Location, timing, and sampling context

- Site: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level).
- Coordinates provided: 53°22'N, 3°95'W.
- Key temporal details:
  - Sheep excluded from plots from 15/05/2017 to reduce confounding by recent excretal events.
  - A treatment application date for the CandN treatment was 25/10/2017.
  - Soils were sampled from replicated areas adjacent to greenhouse gas sampling chambers, processed within 24 hours of collection.
- Sampling design suggests replication at the plot level (n = 4 per treatment).

## Treatments and experimental design

- Control: no urine application.
- Artificial sheep urine (ArtUrine): applied in triplicate discrete patches per plot; each patch delivers 1120 kg N ha⁻¹. Each patch received 200 mL of artificial urine over 100 cm² soil surface.
- Nitrate + Glucose (CandN): 1 L of nitrate and glucose solution applied across a 40 × 40 cm square adjacent to the chamber; application rate of 106 kg N ha⁻¹ and 213 kg C ha⁻¹.
- Experimental replication: four plots per treatment (n = 4 for treatments).

## Measurements and calculations

- Parameters measured:
  - WFPS: soil water-filled pore space (%), calculated as volumetric water content divided by soil porosity.
  - pH: measured in 1:2.5 soil-to-distilled water suspensions with standard electrodes.
  - EC: electrical conductivity measured in µS cm⁻¹, from the same suspensions as pH.
- Porosity calculation:
  - Porosity derived using particle densities: 2.65 g cm⁻³ (mineral fraction) and 1.4 g cm⁻³ (organic fraction).
  - Method follows Rowell (1994) for soil science methods.
- Data headers and definitions:
  - Date: date of soil sample collection (dd/mm/yyyy).
  - Days: days after treatment application.
  - Treatment: Control, ArtUrine, CandN.
  - Plot: plot identifier.
  - WFPS: percent soil water-filled pore space.
  - pH: soil pH.
  - EC: soil electrical conductivity (µS cm⁻¹).

## Data structure and usage notes

- File/database focuses on three variables (WFPS, pH, EC) across three treatments and multiple plots over time.
- Metadata completeness:
  - Clear treatment descriptions, plot identifiers, sampling dates, and days-after-treatment are provided.
  - Authors request attribution for reuse.
- Potential considerations for data leaders:
  - Data are tied to a specific field site with clear methodology, aiding reproducibility.
  - Spatial and temporal replication exists (n = 4 plots per treatment; dates include 25/10/2017 for CandN and ongoing sampling around treatment events).
  - Ensure unit consistency (WFPS in percent; EC in µS cm⁻¹; pH unitless) when integrating with other datasets.
  - Metadata references: provenance to Rowell (1994) for porosity methodology.

## Reference

- Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman Group UK Ltd., London, United Kingdom (1994).