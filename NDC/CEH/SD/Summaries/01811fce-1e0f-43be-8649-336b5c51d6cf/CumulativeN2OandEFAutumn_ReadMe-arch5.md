# ReadMe file for CumulativeN2OandEFAutumn.csv

## Dataset scope and context
- Contains cumulative N2O emissions and N2O-N emission factors (EF) measured from three treatments: Control (no urine), ArtUrine (artificial sheep urine), and Urine (real sheep urine) in a greenhouse gas chamber setup.
- Study site: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Experimental design: randomised block design.

## Data content and variables
- Key headers: Treatment, Chamber, Cum_N2O, EF.
  - Treatment: 'Control', 'ArtUrine', or 'Urine'.
  - Chamber: chamber identifier from which emissions were measured.
  - Cum_N2O: cumulative N2O emissions per chamber, in micrograms N2O-N over 118 days.
  - EF: N2O-N emission factor as a percentage of total N applied.
- N application context:
  - ArtUrine treatment: 1120 kg N ha-1.
  - Urine treatment: data tied to real sheep urine; reference to 106 kg N ha-1 and 213 kg C ha-1 in related nitrate/glucose treatments appears as contextual detail.
- Calculation methods:
  - Cum_N2O derived from the area under the N2O-N emission curve using trapezoidal integration from treatment application onward.
  - EF calculated as the percentage of total N applied released as N2O-N, with adjustments to account for chamber areas not treated (patch application in ArtUrine).

## Methods and calculations
- Emissions integration: area under the curve for each replicate chamber.
- EF calculation: accounts for non-applicable chamber area due to discrete patch application of artificial urine.
- Data quality checks: data were visually checked for errors.

## Experimental design and site details
- Site characteristics: humic gleysol soil, location in Snowdonia National Park.
- Plot design: randomised blocks; treatments applied to discrete patches within the chamber.
- Timeframe: 118 days post-treatment.

## Data quality, provenance, and metadata
- Header definitions provided and explicit: Treatment, Chamber, Cum_N2O, EF.
- Units: Cum_N2O in micrograms N2O-N; EF in percent.
- Data were visually checked for errors, indicating basic QA steps.
- ReadMe notes authorship acknowledgment required if data are reused or reproduced.

## Data governance, usage, and attribution
- Usage note: Authors must be acknowledged in any reuse or reproduction of the data.
- Provenance: measurements originate from a controlled greenhouse gas chamber experiment tied to a field site description and randomised block design.
- Limitations and caveats highlighted by the readme include the patch-based application and the necessary corrections for chamber area in EF calculations.