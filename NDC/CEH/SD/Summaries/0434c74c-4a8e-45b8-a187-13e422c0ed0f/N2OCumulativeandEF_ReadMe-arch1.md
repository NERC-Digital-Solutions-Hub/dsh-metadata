# ReadMe file for N2OCumulativeandEF.csv

## Overview
- Provides annual cumulative N2O emissions and N2O-N emission factors (EF) measured from control (no urine), artificial sheep urine, and real sheep urine applications.
- Experimental system: orthic podzol in a semi-improved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Timeframe: spring and autumn 2016.
- Design: randomised block.
- Data checked visually for errors; authors must be acknowledged if data are reused or reproduced.

## Experimental design and treatments
- Treatments:
  - Control: no urine application
  - ArtUrine: artificial sheep urine
  - RealUrine: real sheep urine
- N application rates (kg N ha-1):
  - Spring: ArtUrine 1066; RealUrine 756
  - Autumn: ArtUrine 1004; RealUrine 1112
- Emissions measured from chambers within discrete urine patches; cumulative emissions calculated per replicate chamber per season.
- Chamber-based measurements with a corrective adjustment for urine-not-applied area.

## Data contents and structure
- Key headers:
  - Treatment: Control, ArtUrine, RealUrine
  - Chamber_no: chamber identifier
  - Season: spring 2016 or autumn 2016
  - Cumulative_N2O: cumulative N2O emissions per chamber (micrograms N2O-N over 1 year)
  - N2O-N_EF: emission factor as a percentage of total N applied
- Data are aligned with two related files for data collection/instrumentation details:
  - SpringN2OData.csv
  - AutumnN2OData.csv

## Calculation methods
- Cumulative_N2O derived from the area under the curve for each replicate chamber in each season.
- N2O-N_EF calculated as a percentage of total applied N.
- Emission factors corrected for patch area not treated by urine within the chamber.

## Data quality and provenance
- Data visually checked for errors.
- Clear attribution: authors must be acknowledged if data are reused or reproduced.
- Dataset deposited with accompanying data collection details (Spring and Autumn datasets).

## Usage notes
- Suitable for comparing N2O emissions across urine types and seasons, and for deriving emission factors.
- Appropriate consideration of local-scale, patch-based application design and the underlying randomised block layout.
- Accurate interpretation requires accounting for N application rates and chamber-area corrections.