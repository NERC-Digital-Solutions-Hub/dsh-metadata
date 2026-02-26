# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Water, Cumbria, England (2014–2018).
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH, ammonium (NH4N, µg N L−1), nitrate (NO3N, µg N L−1), soluble reactive phosphate (PO4P, µg P L−1), total phosphorus (TOTP, µg P L−1), dissolved reactive silicon (SIO2, µg L−1), and phytoplankton chlorophyll a (TOCA, µg L−1).

## Sampling regime and collection methods
- Part of ongoing long-term monitoring; samples collected fortnightly.
- Sampling integrated from 0 to 5 m depth.
- Measurements taken from a boat at the deepest part of the lake (buoy); when buoy access was not possible, samples were taken near shore along with surface temperature and oxygen.
- Data cover January 2014 to end of 2018.
- Some occasions did not include integrated water samples (Flag 2).

## Data quality and quality control
- The dataset provided is raw and not yet quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data are attributed to weather conditions or staff shortages.

## Data structure and access
- Data provided as a CSV with columns: Date, Variable (Description), Value, Sign (if <LOD), Flag (1 = buoy site, 2 = near shore).
- Values provided for each variable as described above; sign <LOD indicates values below detection limit.

## Limitations and considerations for analysis
- Raw data and lack of full calibration may require quality control and validation before rigorous analysis.
- Occasional non-integrated samples (Flag 2) may affect comparability to fully integrated 0–5 m measurements.
- Detection-limit indicators (< sign) and potential missing values need handling in statistical analyses.

## Potential uses for analysts
- Explore correlations and trends among physical, chemical, and biological parameters (e.g., TEMP, OXYG, SECC, nutrients, TOCA).
- Develop predictive models linking environmental variables to phytoplankton chlorophyll a or Secchi depth.
- Assess inter-annual variability and drivers of water quality in Esthwaite Water.

## Funding
- Data collection supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Related publications and usage
- Pilotto F et al. (2020). Meta-analysis of multidecadal biodiversity trends in Europe, Nature Communications.
- Wang, B. et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
- Woolway, R.I. et al. (2016). Lake surface temperatures in State of the Climate 2015. Bulletin of the American Meteorological Society.
- Maberly, S.C. et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. Ecological Informatics.