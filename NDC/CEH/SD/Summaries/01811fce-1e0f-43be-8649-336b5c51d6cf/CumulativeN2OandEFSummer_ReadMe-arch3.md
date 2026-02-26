# ReadMe file for CumulativeN2OandEFSummer.csv

- Purpose: Describes a dataset of cumulative N2O emissions and N2O-N emission factors generated from control and urine-application treatments to a grazing land site, intended for supporting environmental monitoring and policy evaluation.

- Authorship and reuse: Authors must be acknowledged if data are re-used or reproduced.

- Study context and design:
  - Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level; 53°22'N, 3°95'W).
  - Experimental setup: Randomised block design assessing artificial and real sheep urine effects against a control (no urine).
  - Treatments:
    - Control: no urine
    - ArtUrine: artificial sheep urine
    - Urine: real sheep urine
  - Nitrogen application rates: 920 kg N ha-1 (ArtUrine) and 930 kg N ha-1 (Urine).

- Measurements and calculations:
  - N2O emissions: Cumulative N2O measured from each chamber as area under the curve, using trapezoidal integration.
  - Emission factors (EF): Calculated as the percentage of total N applied that was released as N2O-N, after correcting for the portion of the area within the chamber not treated with urine (patches).
  - Duration: 144 days.
  - Data quality checks: Visual inspection for errors.

- Data structure (headers and meaning):
  - Treatment: 'Control', 'ArtUrine', or 'Urine'.
  - Chamber: Chamber identifier number for emission measurements.
  - Cum_N2O: Cumulative N2O emissions per chamber (units: micrograms N2O-N over 144 days).
  - EF: N2O-N emission factor (percentage of total N applied).