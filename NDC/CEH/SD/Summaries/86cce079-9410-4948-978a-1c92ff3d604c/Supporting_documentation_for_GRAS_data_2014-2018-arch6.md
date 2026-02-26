# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018

## Overview
- Long-term, fortnightly monitoring dataset from Grasmere, Cumbria (Jan 2014 – end of Mar 2018) measuring multiple limnological parameters.
- Data intended for download and use in ecological analyses, trend assessment, and integration with broader datasets.

## Sampling regime and collection methods
- Sampling conducted fortnightly as part of an ongoing monitoring program.
- Water samples collected from a boat at the deepest lake location (buoy); when not possible, samples taken from the shore (Flag 2).
- Integrated 0–5 m water column samples; when buoy access was unavailable, no integration occurred.

## Variables and units
- Surface temperature (TEMP): degrees Celsius (°C)
- Surface oxygen saturation (OXYG): % airsaturation
- Secchi depth (SECC): metres (m)
- Alkalinity (ALKA): µg CaCO3 per litre
- pH: (unitless)
- Ammonium (NH4N): µg N per litre
- Nitrate (NO3N): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre

## Data collection timing and context
- All data collected between January 2014 and end-March 2018.
- Long-term monitoring ended in March 2018 due to funding shortages.

## Data quality and limitations
- Data are raw and have not been quality controlled or calibrated yet.
- Double-entered and visually checked; some missing data due to weather or staff shortages.
- Values below detection limits are indicated in the Sign (if<LOD) column.

## Data structure and format
- Provided as comma-separated values (CSV).
- Key columns:
  - Date: measurement date
  - Variable: name of the parameter
  - Value: measured value
  - Sign (if<LOD): indicates if below detection limit with a < symbol
  - Flag: 1 = sample from buoy at marked location; 2 = shore sample when buoy visit was not possible

## Usage and how outputs have been or can be used
- Dataset has been used in publications examining carbon and silicon cycles and lake surface temperatures.
- Overview and context provided for long-term ecological research and data integration efforts.
- Suitable for creating self-serve data products (e.g., dashboards) once quality control and calibration are applied.

## Publications and references
- Examples:
  - Wang et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports 6, 35832.
  - Woolway et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society, 97(8), S17-S18.
- Overview: Maberly et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. In Ecological Informatics, 455-482.