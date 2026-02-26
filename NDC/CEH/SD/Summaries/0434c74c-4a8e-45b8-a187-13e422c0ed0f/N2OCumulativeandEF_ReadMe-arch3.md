# ReadMe file for N2OCumulativeandEF.csv

## Overview
- Provides annual cumulative N2O emissions and N2O-N emission factors (EF) for different urine treatments applied to an orthic podzol in semi-improved upland grassland.
- Study context: Henfaes Research Station, North Wales (270 m above sea level; coordinates 53°13'N, 4°0'W) during Spring and Autumn 2016.
- Design: randomised block design.

## Experimental site and design
- Location: Henfaes Research Station, Abergwyngregyn, North Wales.
- Environment: upland grassland with a discrete urine patch applied within a greenhouse gas chamber.
- Design: randomised block.

## Treatments and application rates
- Treatments:
  - Control: no urine application.
  - ArtUrine: artificial sheep urine.
  - RealUrine: real sheep urine.
- Nitrogen application rates (kg N ha-1):
  - Spring: ArtUrine 1066; RealUrine 756.
  - Autumn: ArtUrine 1004; RealUrine 1112.

## Measurements and calculations
- Emissions measurement: cumulative N2O emissions calculated from the area under the concentration-time curve for each chamber replicate per season.
- Emission factors: N2O-N_EF calculated as the percentage of total N applied, corrected for the portion of chamber area not receiving urine (patch area).
- Data processing: data visually checked for errors.

## Data structure and headers
- Key headers:
  - Treatment: Control, ArtUrine, RealUrine.
  - Chamber_no: chamber identifier.
  - Season: Spring or Autumn 2016.
  - Cumulative_N2O: cumulative N2O emissions (micrograms N2O-N per year) per chamber.
  - N2O-N_EF: emission factor (% of total N applied).

## Data provenance and related files
- Authorship and reuse: Authors must be acknowledged if data are reused or reproduced.
- Related datasets: AutumnN2OData.csv and SpringN2OData.csv contain data collection and instrumentation details for the respective seasons.
- Data origin: measurements taken from discrete patches within chambers; details on data collection methods are linked to the accompanying seasonal files.

## Data quality and limitations
- Quality checks: data visually checked for errors.
- Limitations: single-site, two-season dataset with patch-based urine application; EF depends on accurate patch area correction and site-specific conditions.