# ReadMe file for CumulativeN2OandEFAutumn.csv

- Purpose: Provides data on cumulative N2O emissions and N2O-N emission factors (EF) to support evaluation of environmental health policies and monitoring approaches.
- Scope: Measurements from control (no urine), artificial sheep urine (ArtUrine), and real sheep urine (Urine) applied to a humic gleysol in unimproved grazing land.

## Experimental design and treatments
- Study design: Randomised block design conducted in Snowdonia National Park, Wales, UK.
- Location details: Carneddau mountains, 556 m above sea level; coordinates 53°22'N, 3°95'W.
- Treatments and N inputs:
  - Control: no urine application.
  - ArtUrine: artificial sheep urine application, 1120 kg N ha-1.
  - Urine: real sheep urine application, 106 kg N ha-1 and 213 kg C ha-1 (nitrate and glucose treatment referenced for comparative nutrient inputs).

## Measurements and calculations
- Emission measurement: N2O emissions monitored using chambers.
- Calculation of cumulative emissions: Area under the curve of N2O emissions from the time of treatment onwards, using trapezoidal integration; results expressed as cumulative N2O-N (µg N2O-N) per chamber over 118 days.
- Emission factors (EF): Calculated as percent of total N applied; corrected for portions of chamber area not treated due to discrete patch application of artificial urine.

## Data fields
- Treatment: Categorical variable with values Control, ArtUrine, Urine.
- Chamber: Numeric identifier for each gas measurement chamber.
- Cum_N2O: Cumulative N2O-N emissions per chamber (µg N2O-N over 118 days).
- EF: N2O-N emission factor as a percentage of N applied.

## Data quality and processing
- Quality checks: Data visually inspected for errors.
- Data handling: Emissions calculated from chamber data with area-correction for patch applications; EF computed from total N applied.

## Location and site context
- Environment: Humic gleysol soil within unimproved grazing land.
- Geographic context: Snowdonia National Park, Carneddau mountains, Wales, UK.

## Usage and attribution
- Attribution: Authors must be acknowledged if the data are reused or reproduced.