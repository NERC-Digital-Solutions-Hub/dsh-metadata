# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

## Purpose and scope
- Long-term monitoring dataset covering surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a from Grasmere, Cumbria, England.
- Sampling frequency ranged from weekly to fortnightly, spanning June 1968 to 2013 for some variables.
- Data intended for assessment of environmental health and long-term policy-relevant trends.

## Data collection and methods
- Origins: initial collection by the Freshwater Biological Association; since 1989, CEH and predecessor Institute of Freshwater Ecology have continued sampling.
- Sampling regime: water samples integrated from 0 to 5 m; measurements taken from a boat at a marked buoy in the deepest part of the lake; when the buoy could not be reached, shore samples were taken (not integrated), marked as Flag 2.
- Variables measured (with units):
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - PH: pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg SiO2 per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Data structure: each row includes sdate (measurement date), variable (with description), value (measured value), sign_if_LT_LOD (indicates detection limit if value is below detection), and flag (1 = buoy location, 2 = shore sample).

## Data quality and limitations
- Status: raw data not quality controlled or calibrated; double entries exist only from 2005 onwards.
- Visual checks conducted; some values below detection limits are indicated with a "<" sign in sign_if_LT_LOD.
- Sampling method differences (buoy-based integrated 0–5 m vs occasional shore samples) may affect comparability over time.

## Data content, structure, and access
- Data format: comma-separated values (CSV) with columns as described above.
- Coverage: June 1968 through 2013 (end date for the dataset varies by variable, with full period for many variables).

## Use cases and relevance
- Demonstrates long-term environmental changes and water quality trends critical for monitoring lake health and informing environmental policy.
- Has been used in publications on:
  - Catchment productivity and lake CO2 emissions
  - Long-term phytoplankton ecology and effects of nutrient enrichment
  - Carbon and silicon geochemical cycles in freshwater systems
  - Lake surface temperature trends

## Practical considerations for analysts
- Because data are raw, plan for quality control, calibration, and homogenization before rigorous analysis.
- Address detection-limit handling using sign_if_LT_LOD and consider imputation or censored data methods where appropriate.
- Account for method changes (buoy vs shore sampling) when constructing time series or performing trend analyses.
- When integrating with other datasets, ensure consistent units and temporal alignment; store and document metadata for reproducibility.

## Key publications and references
- Maberly, S.C., Barker, P.A., Stott, A.W. & De Ville, M.M. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change.
- Reynolds, C.S., Maberly, S.C., Parker, J.E. & De Ville, M.M. (2012). Forty years of monitoring water quality in Grasmere (English Lake District): separating the effects of enrichment by treated sewage and hydraulic flushing on phytoplankton ecology. Freshwater Biology.
- Wang, B., et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
- Woolway, R.I., et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society.