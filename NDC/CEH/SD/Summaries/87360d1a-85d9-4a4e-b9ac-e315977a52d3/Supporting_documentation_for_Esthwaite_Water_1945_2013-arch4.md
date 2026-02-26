# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013.

## Overview
- Long-term monitoring dataset from Esthwaite Water, Cumbria, England, covering surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data span from 1945 to 2013 (April 1945 onward for many variables).
- Initial data collection by the Freshwater Biological Association; since 1989 collected by CEH and its predecessor institutes.
- Available data are downloadable in CSV format with clearly defined units and variable descriptions.

## Sampling regime and collection methods
- Sampling frequency ranges from weekly to fortnightly.
- Water samples are integrated from 0 to 5 meters.
- Measurements taken from a boat at the deepest part of the lake (buoy); when not possible, samples taken from shore (Flag 2 indicates shore sampling).
- Data columns include sdate (measurement date) and value for each variable, with contextual fields.

## Data quality and limitations
- The dataset consists of raw data that have not been quality controlled or calibrated (except for double entries from 2005 onwards).
- Visual checks have been performed to ensure data plausibility.
- Some values below detection limits are indicated with a < sign in sign_if_LT_LOD.

## Data structure and variables
- Provided as a comma-separated values (CSV) file.
- Key columns:
  - sdate, variable, value, sign_if_LT_LOD, flag.
- Variables and units:
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation in % air-saturation.
  - SECC: Secchi depth in metres.
  - ALKA: alkalinity in µg CaCO3 per litre.
  - PH: pH.
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.
- Flags:
  - sign_if_LT_LOD indicates below detection limit with a < sign.
  - flag indicates sampling location: 1 = buoy, 2 = shore.

## Usage and references
- Recently used in multiple publications, including:
  - Dong et al. (2012) Nutrients exert a stronger control than climate on diatom communities in Esthwaite Water.
  - Elliott (2010) Seasonal sensitivity of cyanobacteria and phytoplankton to flushing rate and temperature.
  - Feuchtmayr et al. (2012) Spring phytoplankton phenology in lakes of the same region.
  - Maberly et al. (2013) Catchment productivity and CO2 emissions from lakes.
  - Wang et al. (2016) Coupling of carbon and silicon cycles in water bodies.
  - Woolway et al. (2016) Lake surface temperatures (cited in State of the Climate 2015).

## Implications for data leadership and governance
- Data is raw and not yet quality controlled or calibrated; prior QC steps are minimal, highlighting a need for formal calibration, validation, and provenance tracking.
- Rich, multi-parameter time-series spanning several decades, suitable for longitudinal analyses, trend detection, and cross-variable studies, provided proper metadata and quality controls are established.
- Clear data structure and documentation (units, detection limits, sampling methods, location flag) support data discoverability and re-use; however, fuller metadata and data dictionaries would enhance interoperability across networks.
- Opportunities for data product development include improved QC pipelines, standardized metadata schemas, and collaborative data-sharing practices to support wider network analyses and user-centered data products.