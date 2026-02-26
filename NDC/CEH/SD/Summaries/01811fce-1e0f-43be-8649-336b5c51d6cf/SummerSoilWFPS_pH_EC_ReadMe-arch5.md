# ReadMe file for SummerSoilWFPS_pH_EC.csv

## Project/context and dataset purpose
- Document accompanying a CSV dataset of soil measurements: water-filled pore space (WFPS), pH, and electrical conductivity (EC).
- Study setting: dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Experimental context: treatments applied include a control (no urine), artificial sheep urine, and real sheep urine.
- Sampling rationale: sheep were excluded from 15/05/2017 to avoid confounding recent excretal events; samples collected from replicated areas adjacent to greenhouse gas sampling chambers.

## Experimental design and treatments
- Treatments (n = 4 per treatment; real urine n = 3):
  - Control: no urine application.
  - Artificial sheep urine: patches with an N application rate of 920 kg N ha-1; 200 ml applied over 100 cm2 soil surface per patch.
  - Real sheep urine: patches with an N application rate of 930 kg N ha-1; 200 ml applied over 100 cm2 soil surface per patch.
- Treatment application date: 24/07/2017.
- Plot context: samples taken from plots adjacent to greenhouse gas sampling chambers.

## Sampling and processing
- Soil sampling method: cores collected with an auger and processed within 24 hours of collection.
- Replication: multiple plots per treatment; specific n values provided (Control and Artificial Urine typically 4 plots; Real Urine 3 plots).
- Measurements collected: WFPS (%), soil pH, soil EC (µS cm-1).
- Sampling date format: dd/mm/yyyy; “Days” field denotes days after treatment.

## Data fields and units
- Date: date of soil sampling (dd/mm/yyyy).
- Days: days after treatment application.
- Treatment: category – Control, ArtUrine (Artificial Urine), RealUrine (Real Urine).
- Plot: plot identifier.
- WFPS: percent soil water-filled pore space.
- pH: soil pH value.
- EC: soil electrical conductivity in µS cm-1.

## Methodology and calculations
- WFPS calculation: ratio of volumetric water content to soil porosity.
- Porosity calculation: assumes mineral particle density 2.65 g cm-3 and organic particle density 1.4 g cm-3 (per Rowell, 1994).
- pH and EC determination: measured from 1:2.5 soil-to-distilled water suspensions using standard electrodes.

## Metadata, provenance, and data quality
- Data provenance: measurements taken on a dystric histosol in a highland grazing system; sampling aligned with treatment patches.
- Processing and timing: samples processed within 24 hours; consistent protocol across plots.
- Documentation requirements for reuse: authors must be acknowledged if data are reused or reproduced.
- References: Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman UK Ltd.

## Governance and usage notes for Data Stewards
- Data governance considerations:
  - Ensure clear linkage between Date, Days, Treatment, Plot, and corresponding WFPS/pH/EC values to maintain data integrity.
  - Maintain consistent units and formats (date, Days, treatment labels ArtUrine/RealUrine/Control, EC in µS cm-1).
  - Preserve replication counts per treatment and plot identifiers for traceability.
  - Capture site metadata (location, elevation, coordinates, land-use context) for interoperability with other soil and GHG datasets.
- Potential data quality aspects:
  - Small uneven replication (RealUrine n=3) should be documented in downstream datasets to avoid misinterpretation.
  - Porosity-based WFPS calculations rely on assumed densities; document these assumptions for reproducibility.
- Data sharing and attribution:
  - Include proper author acknowledgment in any reuse or reproduction of the dataset.
  - Reference the Rowell 1994 method for porosity calculations to maintain methodological transparency.