# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Overview
- Long-term monitoring dataset from Esthwaite Water, Cumbria, England, covering 1945–2013 for multiple water quality variables.
- Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data collected weekly to fortnightly; initially by the Freshwater Biological Association, since 1989 by CEH and its predecessor.
- Sampling site: water samples from a marked buoy at the deepest part of the lake; shore samples used if buoy access was not possible (Flag 2).

## Sampling regime and collection methods
- Water samples are integrated from 0 to 5 m depth.
- Conducted from a boat at the buoy location; occasionally from shore when the buoy could not be visited.
- Measurement modes and units per variable are standardized in the dataset.

## Quality control
- The dataset consists of raw data and has not been quality controlled or calibrated (except for double entries from 2005 onward).
- Visual checks have been performed to validate data.

## Data structure and format
- Data provided as comma-separated values (CSV).
- Core columns:
  - sdate, Description: Date of measurement and variable description (e.g., TEMP, OXYG, etc.).
  - value, Description: Measured value for each variable.
  - sign_if_LT_LOD, Description: Indicates if the value is below detection limit with a "<" sign.
  - flag, Description: 1 = sample taken at buoy location; 2 = sample taken from shore (visit to buoy not possible).
- Variables included with units:
  - TEMP: degrees Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - PH: pH
  - NH4N: µg N per litre
  - NO3N: µg N per litre
  - PO4P: µg P per litre
  - TOTP: µg P per litre
  - SIO2: µg SiO2 per litre
  - TOCA: µg per litre

## Accessibility and potential use
- Data are downloadable as CSV files.
- Raw data offer opportunities for cleaning, calibration, integration with other datasets, and development of data products to enable self-service analyses.

## Example usage and publications
- The dataset has been used in multiple studies, such as:
  - Nutrients vs. climate impacts on diatom communities in Esthwaite Water (Freshwater Biology, 2012).
  - Seasonal sensitivity of Cyanobacteria and phytoplankton to flushing rate and temperature (Global Change Biology, 2010).
  - Spring phytoplankton phenology and drivers across lakes (Freshwater Biology, 2012).
  - Connections between catchment productivity and CO2 emissions from lakes (Nature Climate Change, 2013).
  - Studies on carbon and silicon cycles in rivers and lakes (Scientific Reports, 2016).
  - Contributions to state-of-climate discussions (Bulletin of the American Meteorological Society, 2015).