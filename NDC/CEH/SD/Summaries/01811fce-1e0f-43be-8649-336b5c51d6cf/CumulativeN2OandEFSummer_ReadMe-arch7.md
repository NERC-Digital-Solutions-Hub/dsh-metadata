# ReadMe file for CumulativeN2OandEFSummer.csv

## Overview
- Provides data on cumulative N2O emissions and N2O-N emission factors from a controlled grazing study in Snowdonia, Wales.
- Focuses on spatially organized measurements across chambers within a randomized block design.

## Study context and location
- Environment: dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Design: randomized block design.
- Treatments:
  - Control: no urine application
  - ArtUrine: artificial sheep urine
  - Urine: real sheep urine
- N application rates: 920 kg N ha-1 for artificial urine; 930 kg N ha-1 for real urine.

## Data content and structure
- Data sources: cumulative N2O emissions measured from chambers over 144 days.
- Variables (headers):
  - Treatment: 'Control', 'ArtUrine', or 'Urine'
  - Chamber: chamber number from which emissions were measured
  - Cum_N2O: cumulative N2O emissions per chamber (units: micrograms N2O-N over 144 days)
  - EF: N2O-N emission factor as a percentage of total N applied

## Calculations and processing
- Cumulative N2O emitted per chamber calculated from the area under the time-course curve using trapezoidal integration.
- Emission factors (EF) computed as a percentage of the total N applied, corrected for chamber area not covered by urine (urine applied in discrete patches within the chamber).
- Data quality: visually checked for errors.

## Timeframe
- Emissions summarized over a 144-day measurement period.

## Usage notes for GIS applications
- Each chamber provides spatially resolveable unit-level data that can be mapped or joined with spatial features (e.g., chamber locations, treatment zones).
- Suitable for visualisation of emissions intensity by location, treatment, and across blocks.
- EF values enable spatial comparison of emission efficiency relative to N input across treatments.

## Attribution and data hygiene
- Authors must be acknowledged if data are reused or reproduced.

## Data schema summary
- Key fields: Treatment, Chamber, Cum_N2O, EF
- Related context: location, elevation, grazing land characteristics, and randomized block design inform GIS interpretation and integration with other spatial datasets.