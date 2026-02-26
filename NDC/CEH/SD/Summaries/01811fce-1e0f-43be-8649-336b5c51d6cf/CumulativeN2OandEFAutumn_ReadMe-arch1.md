# ReadMe file for CumulativeN2OandEFAutumn.csv

## Overview
- Presents data on cumulative N2O emissions and N2O-N emission factors (EF) measured from three treatments: Control (no urine), ArtUrine ( artificial sheep urine), and Urine (real sheep urine).
- Study conducted on a humic gleysol within an unimproved grazing area in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W), using a randomised block design.
- Emissions and emission factors are calculated from measurements taken over 118 days following treatment application.

## Site, design, and treatments
- Location: Snowdonia National Park, Carneddau mountains, Wales, UK; soil: humic gleysol; elevation 556 m a.s.l.
- Design: randomised block.
- Treatments:
  - Control: no urine applied.
  - ArtUrine: artificial sheep urine applied.
  - Urine: real sheep urine applied.
- N inputs:
  - ArtUrine: 1120 kg N ha-1.
  - N inputs for the nitrate and glucose treatment: 106 kg N ha-1 and 213 kg C ha-1 (note: described in the document; the main N input for ArtUrine is the 1120 kg N ha-1).

## Measurements and calculations
- N2O emissions: cumulative N2O measured from each chamber and reported as Cum_N2O.
- Calculation of Cum_N2O: area under the curve of N2O-N emissions for each replicate chamber, using trapezoidal integration from the time of treatment application onward.
- Emission factors (EF): calculated as the percentage of total N applied that was released as N2O-N, with corrections for the chamber area not treated (because artificial urine was applied in discrete patches within the chamber).
- Timeframe: emissions and EF are based on measurements over 118 days post-treatment.

## Data structure and fields
- Data headers:
  - Treatment: one of 'Control', 'ArtUrine', or 'Urine'.
  - Chamber: chamber identifier number from which N2O emissions were measured.
  - Cum_N2O: cumulative N2O emissions per chamber, units micrograms N2O-N over 118 days.
  - EF: N2O-N emission factor as a percentage of total N applied.
- Units:
  - Cum_N2O: micrograms N2O-N accumulated over 118 days.
  - EF: percent of total N applied.

## Data quality, provenance, and reuse
- Data were visually checked for errors.
- Authors must be acknowledged if data are reused or reproduced.
- The dataset is site-specific (upland Welsh grazing system) and conditions (patch-based application, chamber methodology) should be considered when extrapolating or comparing to other settings.