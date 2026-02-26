# CumulativeN2OandEFSummer.csv

- Aim and scope
  - Dataset provides cumulative N2O emissions and N2O-N emission factors (EF) measured from different treatments on a dystric histosol in unimproved grazing land.
  - Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
  - Study design: randomised block.

- Treatments and rates
  - Treatment groups: Control (no urine), ArtUrine (artificial sheep urine), Urine (real sheep urine).
  - Nitrogen application rates: 920 kg N ha-1 for ArtUrine; 930 kg N ha-1 for Urine.

- Measurements and time frame
  - N2O emissions collected in replicate chambers over 144 days.
  - Cumulative N2O (Cum_N2O) calculated per chamber by area under the curve (trapezoidal integration).

- Emission factors
  - EF represents the percentage of applied urine-N released as N2O-N.
  - EF values are corrected for the fraction of the area within the chamber that did not receive urine (patches).

- Data structure and headers
  - Treatment: 'Control', 'ArtUrine', or 'Urine'.
  - Chamber: chamber identifier for emission measurement.
  - Cum_N2O: cumulative N2O-N emissions per chamber (µg N2O-N over 144 days).
  - EF: N2O-N emission factor as a percentage of total N applied.

- Data quality and provenance
  - Visual checks performed to identify errors.
  - Authors must be acknowledged if the data are reused or reproduced.

- Practical notes
  - Data capture is specific to a single site, soil type (dystric histosol), and discrete urine-application patches, which may affect generalisability.
  - Useful for analysing relationships between urine treatment type, cumulative N2O emissions, and emission factors, and for informing modelling or comparisons across treatments.