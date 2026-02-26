# ReadMe file for CumulativeN2OandEFSummer.csv

## Overview
- Dataset reports cumulative N2O emissions and N2O-N emission factors measured from three treatments: Control (no urine), ArtUrine (artificial sheep urine), and Urine (real sheep urine).
- Experiment conducted on a dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W), using a randomised block design.
- N application rates: 920 kg N ha-1 for artificial urine and 930 kg N ha-1 for real urine.
- Emissions calculated from the area under the time-series curve of chamber measurements; EF derived after correcting for the chamber area not treated by urine patches.

## Experimental context
- Purpose: quantify cumulative N2O emissions and corresponding emission factors from different urine sources under grazing land conditions.
- Design: randomised block with discrete urine patches measured using gas chambers.

## Data content and structure
- Measurements cover 144 days.
- Outputs include:
  - Cum_N2O: cumulative N2O-N emissions per chamber (units: micrograms N2O-N over 144 days).
  - EF: emission factor as a percentage of the total N applied.
  - Treatment indicating the experimental group (Control, ArtUrine, Urine).
  - Chamber indicating the chamber number used for measurement.

## Data processing and quality checks
- Cumulative N2O emissions calculated by trapezoidal integration of chamber time-series data.
- EF computed after correcting for the portion of chamber area not treated by urine patches.
- Data visually checked for errors.

## Headers and field definitions
- Treatment: 'Control' = no urine, 'ArtUrine' = artificial sheep urine, 'Urine' = real sheep urine.
- Chamber: chamber identifier.
- Cum_N2O: cumulative N2O emissions per chamber (micrograms N2O-N, over 144 days).
- EF: N2O-N emission factor as a percentage of total N applied.

## Usage notes and provenance
- Authors must be acknowledged if the data are reused or reproduced.
- Data enable comparison of emissions between artificial and real urine applications, as well as against a no-urine control, within a patchy application and chamber-based measurement framework.