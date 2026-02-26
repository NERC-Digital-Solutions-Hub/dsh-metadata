# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018

## What this dataset is
- Long-term monitoring dataset collected from Bassenthwaite Lake, Cumbria, England.
- Fortnightly sampling conducted from 2014 to 2018; dataset ends in 2018 due to funding shortages (long-term monitoring ended early 2019).
- Variables captured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).

## Sampling regime and collection methods
- Sampled from 0 to 5 m depth; water samples are an integrated sample from this depth interval.
- Measurements taken from a boat at the deepest marked location (buoy); when the buoy could not be visited, samples were taken from the shore (Flag 2).
- When buoy sampling was possible, data reflect buoy location; otherwise shore sampling occurred.
- Timeframe: January 2014 through end of 2018.

## Data quality and limitations
- The data are raw and have not yet been quality controlled or calibrated.
- Data have been double entered and visually checked.
- Missing data primarily due to weather conditions or staff shortages.
- Some measurements below detection limit are indicated with a < sign in the Sign (if<LOD) column.
- Documentation notes are included to help interpret the dataset (e.g., Flag values, measurement method).

## Data structure and file format
- Delivered as comma-separated values (CSV).
- Core columns include:
  - Date: Date of measurement.
  - Description (Variable): The variable measured (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value (Value): Measured value for each variable.
  - Sign (if<LOD): Indicates if the value is below detection limit (presence of <).
  - Flag (Flag): 1 = sample taken at the buoy location; 2 = sample taken from the shore.
- Data are baseline, raw measurements with the specified structure and flags to indicate sampling context.

## Usage context and example publications
- The dataset has been used in publications exploring aquatic geochemical cycles and ecological responses, including:
  - Coupling of carbon and silicon geochemical cycles in rivers and lakes (Scientific Reports, 2016).
  - The reappearance of vendace in Bassenthwaite Lake under multiple stressors (Fundamental and Applied Limnology, 2017).
  - Lake surface temperatures referenced in broader climate summaries (Bulletin of the American Meteorological Society, 2016).
- An overview reference: From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District (Ecological Informatics, 2017).