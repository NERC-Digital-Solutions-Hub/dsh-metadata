# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018.

## Purpose and scope
- Long-term, fortnightly monitoring dataset from Bassenthwaite Lake, Cumbria, England.
- Records multiple limnological variables to assess environmental health and trends over time.

## Sampling regime and collection methods
- Measurements collected from January 2014 to the end of 2018; long-term monitoring ended early 2019 due to funding shortages.
- Parameters measured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L^-1), pH, ammonium (NH4N, µg N L^-1), nitrate (NO3N, µg N L^-1), soluble reactive phosphate (PO4P, µg P L^-1), total phosphorus (TOTP, µg P L^-1), dissolved reactive silicon (SIO2, µg L^-1), phytoplankton chlorophyll a (TOCA, µg L^-1).
- Integrated water samples from 0–5 m; sampling conducted from a boat at the deepest-lake buoy; if buoy access was not possible, samples collected from the shore (Flag 2).
- Data represent a mix of buoy-based and shore-based sampling where required.

## Data quality and limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Double entered and visually checked; some missing data due to weather or staff shortages.
- Flag indicators: Flag 1 = sample taken at buoy; Flag 2 = shore sample due to buoy inaccessibility.

## Data structure and format
- Stored as comma-separated values (CSV) with columns:
  - Date: measurement date
  - Variable: each measured parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value for each variable
  - Sign (if<LOD): indicates values below detection limit with a < symbol
  - Flag: 1 = buoy location; 2 = shore location when buoy sampling not possible

## Temporal coverage and status
- Timeframe: January 2014 – end of 2018
- Long-term monitoring halted in early 2019 due to funding shortages

## Data usage and provenance
- Example publications using the dataset:
  - Wang et al. (2016) Scientific Reports on carbon and silicon cycles
  - Winfield, Fletcher & James (2017) Fundamental and Applied Limnology on vendace reappearance
  - Woolway et al. (2016) Bulletin of the American Meteorological Society on lake surface temperatures
- Overview reference: Maberly et al. (2017) on long-term ecological informatics and knowledge generation

## Relevance to the Analysts Monitoring the Environment
- Provides standardized, time-series data to assess environmental health and policy-relevant trends.
- Raw data with clear metadata support transparency and reproducibility.
- Datasets are suitable for integration with other environmental datasets to enhance monitoring value, with explicit data structure and quality notes.

## Practical notes for analysts
- Treat data as raw; plan quality-control and calibration steps before formal analysis.
- Consider using the Flag and Sign fields to handle sampling location differences and detection-limit issues.
- Acknowledge the end of the monitoring program in 2019 when interpreting long-term trends.