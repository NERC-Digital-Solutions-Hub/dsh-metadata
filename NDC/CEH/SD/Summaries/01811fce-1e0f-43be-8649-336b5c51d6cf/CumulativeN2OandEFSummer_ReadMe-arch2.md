# ReadMe file for CumulativeN2OandEFSummer.csv

## Purpose and scope
- Documentation for a dataset of cumulative N2O emissions and N2O-N emission factors (EF) measured under three treatments.

## Study context
- Location: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK
- Soil: dystric histosol
- Elevation: 556 m above sea level
- Design: randomised block design

## Treatments and nitrogen inputs
- Control: no urine applied
- ArtUrine: artificial sheep urine
  - N applied: 920 kg N ha-1
- Urine: real sheep urine
  - N applied: 930 kg N ha-1

## Data and calculations
- Measurements: N2O emissions recorded per chamber
- Timeframe: 144 days
- Cumulative N2O: calculated as area under the curve for each replicate chamber using trapezoidal integration
- Emission factor (EF): percentage of total N applied that was released as N2O-N
  - EF is corrected for the chamber area not occupied by urine (urine applied in discrete patches)

## Data structure and quality
- Data headers:
  - Treatment: 'Control', 'ArtUrine', 'Urine'
  - Chamber: chamber number for N2O measurement
  - Cum_N2O: cumulative N2O emissions per chamber (µg N2O-N over 144 days)
  - EF: N2O-N emission factor (percent of N applied)
- Data were visually checked for errors
- Authors should be acknowledged if data are reused or reproduced

## Practical use for environmental monitoring
- Provides standardized outputs showing environmental impact of urine-derived N2O under different urine treatments
- Enables cross-treatment comparisons and integration with other monitoring data
- Facilitates transparent calculation methods (area under the curve, trapezoidal integration) and quality checks for reproducibility