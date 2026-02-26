# ReadMe file for N2OCumulativeandEF.csv

## Overview
- Documents annual cumulative N2O emissions and N2O-N emission factors for control, artificial urine, and real sheep urine treatments.
- Study conducted in spring and autumn 2016 at Henfaes Research Station, North Wales, using a randomized block design.
- Emissions calculated from chamber data; emission factors expressed as percent of urine-N applied.

## Site, design, and treatments
- Location: Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Environment: Orthic podzol within a semi-improved upland grassland.
- Design: Randomised block.
- Treatments:
  - Control (no urine)
  - ArtUrine (artificial sheep urine)
  - RealUrine (real sheep urine)
- Seasons: Spring 2016 and Autumn 2016.

## Data structure and headers
- Primary dataset: N2OCumulativeandEF.csv
- Key columns:
  - Treatment: Control, ArtUrine, RealUrine
  - Chamber_no: Chamber identifier
  - Season: Spring or Autumn 2016
  - Cumulative_N2O: Cumulative N2O emissions (micrograms N2O-N per chamber over 1 year)
  - N2O-N_EF: N2O-N emission factor as a percentage of total N applied

## Experimental details and calculations
- N application rates (kg N ha-1):
  - Spring: ArtUrine 1066; RealUrine 756
  - Autumn: ArtUrine 1004; RealUrine 1112
- Emissions were derived from the area under the chamber emission curve for each replicate per season.
- Emission factors were calculated after correcting for the chamber area not covered by urine (urine applied in a discrete patch within the chamber).
- Data were visually checked for errors.

## Related data files
- AutumnN2OData.csv and SpringN2OData.csv: data collection and instrumentation details; deposited alongside N2OCumulativeandEF.csv.

## Data provenance and usage
- Authors must be acknowledged if the data are reused or reproduced.

## GIS and spatial context
- Although chamber-level data are provided, coordinates and site details enable contextual GIS mapping of treatments and seasons.
- Potential analyses include spatial visualization of emissions by treatment and season, and integration with soil/geomorphology layers for enhanced interpretation.

## Notes and cautions
- Cumulative_N2O units: micrograms N2O-N per chamber over one year.
- N2O-N_EF units: percent of total applied N.
- Emission factors include patch-area corrections due to discrete urine application within chambers.