# ReadMe file for N2OCumulativeandEF.csv

## Overview
- Describes a dataset of annual cumulative N2O emissions and N2O-N emission factors (EF) measured from control (no urine), artificial sheep urine, and real sheep urine applied to an orthic podzol in semi-improved upland grassland at Henfaes Research Station, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) during spring and autumn 2016.
- Study design: randomised block design with two seasonal trials (spring 2016 and autumn 2016).

## Study design and location
- Location: Henfaes Research Station, Abergwyngregyn, North Wales.
- Altitude and coordinates: 270 m above sea level; 53°13'N, 4°0'W.
- Treatments: Control, ArtUrine (artificial urine), RealUrine (real sheep urine).
- N application rates:
  - Spring 2016: ArtUrine = 1066 kg N ha-1; RealUrine = 756 kg N ha-1.
  - Autumn 2016: ArtUrine = 1004 kg N ha-1; RealUrine = 1112 kg N ha-1.
- Emission calculation basis: cumulative emissions derived from area under the curve of each replicate chamber in each season.

## Data collection and calculation
- Emissions: Cumulative N2O emissions per chamber (units: micrograms N2O-N over 1 year).
- Emission factors: N2O-N EF expressed as a percentage of the total N applied, with correction for chamber area not covered by urine (urine applied to a discrete patch within the chamber).
- Data quality checks: Data visually checked for errors.

## Data structure and headers
- Treatment: 'Control', 'ArtUrine', or 'RealUrine'.
- Chamber_no: identifier for the chamber from which emissions were measured.
- Season: Spring 2016 or Autumn 2016.
- Cumulative_N2O: cumulative N2O emissions per chamber (micrograms N2O-N per year).
- N2O-N_EF: emission factor as a percentage of total N applied.

## Related and supporting data
- AutumnN2OData.csv and SpringN2OData.csv contain data collection and instrumentation details; N2OCumulativeandEF.csv provides the calculated cumulative emissions and EF.

## Usage and provenance notes
- Authors must be acknowledged if data are reused or reproduced.
- Dataset presents a transparent calculation approach (area under the chamber emission curve and patch-area correction) suitable for reproducibility and cross-study comparisons.

## Potential data products and analyses
- Create dashboards or pivot tables to compare treatments and seasons by Cumulative_N2O and N2O-N_EF.
- Self-serve analyses of treatment effects on cumulative emissions and emission factors.
- Documentation of data provenance and calculation steps to support transparency and reuse.