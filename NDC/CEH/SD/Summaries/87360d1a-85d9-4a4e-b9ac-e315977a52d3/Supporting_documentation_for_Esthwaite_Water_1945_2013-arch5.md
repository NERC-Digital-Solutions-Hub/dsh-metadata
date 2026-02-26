# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Overview
- Long-term monitoring dataset from Esthwaite Water, Cumbria, England, covering 1945 to 2013 for multiple water quality and phytoplankton variables.
- Variables included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data are provided for water sampled from 0–5 m depth; measurements taken from a boat at the deepest part of the lake (buoy) or from shore when buoy sampling was not possible.

## Sampling regime and collection methods
- Frequency: weekly to fortnightly sampling; began in 1945 for some variables.
- History: data collected by the Freshwater Biological Association initially, since 1989 by CEH and its predecessor Institute of Freshwater Ecology.
- Sampling location and method: integrated 0–5 m water samples; buoy-based sampling when possible; shore sampling if buoy visits were not possible.

## Quality control and data provenance
- Data status: raw data not yet quality controlled or calibrated; visual checks have been performed.
- Exceptions: double entries exist from 2005 onwards.
- Data provenance: maintained from 1945 through 2013 with documented collection history (FBA to CEH).

## Data structure and units
- File format: comma separated values (CSV).
- Key columns:
  - sdate: date of measurement.
  - variable: description of the measured variable (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value: measured values.
  - sign_if_LT_LOD: indicates if values are below detection limit (a "<" sign used).
  - flag: sampling location flag (1 = buoy at marked location; 2 = shore sampling when buoy sampling was not possible).
- Units:
  - TEMP: degrees Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - PH: pH
  - NH4N, NO3N: µg N per litre
  - PO4P, TOTP: µg P per litre
  - SIO2: µg SiO2 per litre
  - TOCA: µg per litre

## Data availability and usage
- The dataset is available to download as a CSV file with the described structure and fields.
- Recent publications using the dataset illustrate its value for understanding nutrients, phytoplankton dynamics, and lake carbon and silicon cycles.

## Representative publications (examples)
- Dong et al. (2012). Nutrients exert a stronger control than climate on recent diatom communities in Esthwaite Water.
- Elliott (2010). Seasonal sensitivity of Cyanobacteria and other phytoplankton to flushing rate and water temperature.
- Feuchtmayr et al. (2012). Spring phytoplankton phenology in lakes within the same climatological region.
- Maberly et al. (2013). Catchment productivity controls CO2 emissions from lakes.
- Wang et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes.
- Woolway et al. (2016). Lake surface temperatures in the State of the Climate 2015.

## Data stewardship considerations
- Data are raw and require quality control and calibration before broad reuse; update and document QC processes for future versions.
- Metadata should clearly reflect sampling methods, detection limits, and any deviations (e.g., shore sampling events).
- Maintain and communicate the meaning of QC flags and detection-limit indicators to ensure proper interpretation and interoperability with other datasets.