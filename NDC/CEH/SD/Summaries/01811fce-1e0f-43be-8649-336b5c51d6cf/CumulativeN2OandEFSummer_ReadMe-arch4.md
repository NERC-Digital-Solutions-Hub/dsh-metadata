# ReadMe file for CumulativeN2OandEFSummer.csv

## Overview
- Dataset on cumulative N2O emissions and N2O-N emission factors (EF) measured from control (no urine), artificial sheep urine, and real sheep urine applied to a dystric histosol in unimproved grazing land.
- Study design: randomised block.

## Experimental setup and location
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Treatments:
  - Control: no urine application
  - ArtUrine: artificial sheep urine
  - Urine: real sheep urine
- Nitrogen application rates:
  - 920 kg N ha-1 (artificial urine)
  - 930 kg N ha-1 (real urine)
- Design: randomised block
- Emissions measured in chambers; urine applied in discrete patches within the greenhouse gas chamber.

## Data content and structure
- Headers: Treatment, Chamber, Cum_N2O, EF
- Cum_N2O: cumulative N2O-N emissions from each chamber, units in micrograms N2O-N over 144 days
- EF: N2O-N emission factor as a percentage of total N applied

## Calculations and processing
- Cumulative emissions derived from the area under the curve using trapezoidal integration.
- EF corrected for the portion of chamber area not receiving urine due to patchy application.
- Data visually checked for errors.

## Quality, usage, and attribution
- Authors must be acknowledged if data are re-used or reproduced.

## Notes on interpretation and application
- Data reflect a single site and season (summer) with emissions over 144 days.
- Provides a comparison between no urine, artificial urine, and real urine to understand N2O emission responses and EF under controlled conditions.