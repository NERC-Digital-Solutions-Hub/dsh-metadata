# ReadMe file for CumulativeN2OandEFAutumn.csv

## Overview
- Dataset of cumulative N2O emissions and N2O-N emission factors (EF) measured from control (no urine), artificial sheep urine (ArtUrine), and real sheep urine (Urine) applications.
- Location: humic gleysol, unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Experimental design: randomised block.
- Data include calculations of cumulative emissions and emission factors, with outputs corrected for patchy application within chamber areas.

## Data content and measurements
- Focuses on cumulative N2O emissions (Cum_N2O) and emission factors (EF) as percentages of total N applied.
- Timeframe: emissions measured and integrated over 118 days after treatment application.
- Units:
  - Cum_N2O: micrograms N2O-N per chamber (over 118 days).
  - EF: percentage of total N applied emitted as N2O-N.
- Data are accompanied by a ReadMe-style description to aid reuse and interpretation.

## Treatments and application rates
- Treatments:
  - Control: no urine application.
  - ArtUrine: artificial sheep urine application.
  - Urine: real (extracted) sheep urine application.
- N application rates:
  - ArtUrine: 1120 kg N ha-1.
  - Nitrate and glucose treatment: 106 kg N ha-1 and 213 kg C ha-1 (for comparison/context in the study design).
- Note: Artificial urine was applied in discrete patches within the greenhouse gas chamber, with EF calculations adjusted accordingly.

## Calculations and data processing
- Cum_N2O calculated by area under the curve of each chamber’s N2O measurements, using trapezoidal integration from treatment application onward.
- EF calculated as the N2O-N emission factor (percentage of total N applied), with corrections for the portion of chamber area not treated due to patchy application.
- Data were visually checked for errors as part of quality control.

## Data structure and headers
- Headers in the dataset:
  - Treatment: 'Control', 'ArtUrine', 'Urine'.
  - Chamber: chamber number from which N2O emissions were measured.
  - Cum_N2O: cumulative N2O emissions (μg N2O-N) per chamber over 118 days.
  - EF: N2O-N emission factor as a percentage of total N applied.

## Quality control and caveats
- Data underwent visual error checking.
- Patchy urine application requires adjustment to EF calculations to account for un-treated chamber areas.
- The study design is a randomised block, which informs interpretation and comparative analyses across treatments.

## Usage, attribution, and limitations
- Data are suitable for comparing cumulative N2O emissions and EF across treatments, and for assessing the impact of artificial versus real urine on N2O emissions in this soil/landscape context.
- Attribution: authors must be acknowledged if data are reused or reproduced.
- Practical considerations: real-world applicability may be influenced by the patchy application approach and specific site characteristics (humic gleysol, high-altitude Welsh grazing land).