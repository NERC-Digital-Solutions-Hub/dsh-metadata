# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P., Mackay, E.B., Thackeray, S.J., Maberly, S.C. (2021)

## Overview for GIS specialists
- Long-term, fortnightly water-quality monitoring dataset for Derwent Water, Cumbria, England (2014–2018; funded ended early 2019).
- Parameters include surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH, nutrients and phytoplankton chlorophyll a (NH4N, NO3N, PO4P, TOTP, SIO2, TOCA; all in µg/L except SECC and TEMP).
- Water samples are integrated from 0–5 m, taken from a boat at the deepest lake location (buoy). If the buoy was inaccessible, shore samples were collected (Flag 2).
- Data can support map-based analyses of spatially explicit water quality changes over time, with emphasis on the buoy location and shore sampling.

## Data structure and access
- Format: CSV with columns:
  - Date: measurement date
  - Variable: which parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measurement value with units
  - Sign (if<LOD): indicates values below detection limit with a “<” sign
  - Flag: 1 = sample from buoy, 2 = sample from shore
  - Descriptions: metadata for each field
- Full dataset covers January 2014 to end of 2018.
- Units per variable are specified in the data description for accurate GIS mapping and unit consistency.

## Quality control and data preparation
- Raw data are provided and have not been fully quality controlled or calibrated.
- Double-entered and visually checked for errors; missing data attributed to weather or staff shortages.
- For GIS use, plan for local QC steps, calibration where possible, and careful handling of detections below the limit of detection (LOD).

## Spatial and temporal considerations for mapping
- Sampling locations:
  - Primary: marked buoy at the deepest point of the lake.
  - Secondary: shore samples when buoy sampling was not possible.
- Spatial scope is effectively point-based (single lake location with occasional shore observations); suitable for time-series mapping and trend analysis at the lake scale, with caution on broader spatial extrapolations.
- Temporal resolution is fortnightly; dataset supports time-enabled GIS analyses, including animated maps and trend surfaces when combined with auxiliary layers.

## Practical GIS workflows and tips
- Create a time-enabled point layer with two main geometry types: buoy location and shore sampling points (where available).
- Join each observation to the corresponding coordinates, date, variable, and value; store Flag and Sign (LOD) fields to filter or flag incomplete or below-detection data.
- Normalize units if integrating with other datasets; document any unit conversions in the metadata.
- Visualize:
  - Time slider to show changes in TEMP, OXYG, SECC, and nutrients/chlorophyll over 2014–2018.
  - Separate maps for each variable or a multi-attribute map with color ramps and transparency to compare parameters.
- Analytical options:
  - Time-series analyses of individual variables (e.g., TEMP trends) and comparisons between buoy vs shore samples.
  - Correlation mapping between variables (e.g., temperature and chlorophyll a) over time.
  - Integrate with environmental layers (weather, lake depth profiles) to contextualize results.
- Data processing notes:
  - Treat values with <LOD as censored where appropriate; document handling method in GIS workflows.
  - Acknowledge the raw nature of data and plan QC/calibration steps before formal decision-making.

## Usage references and provenance
- Example publications utilizing the dataset:
  - Winfield, I.J., Fletcher, J.M. & James, J.B. (2017). The 'reappearance' of vendace (Coregonus albula) in the face of multiple stressors in Bassenthwaite Lake, U.K. Fundamental and Applied Limnology 189, 227-233.
  - Woolway, R.I. et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society, 97(8), S17-S18.
- Overview context:
  - Maberly, S.C. et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District (Ecological Informatics, pp. 455-482).

## Metadata and accessibility
- Dataset is part of a long-term monitoring program for Derwent Water.
- Data described as raw but with documented measurement regime, sampling locations, and unit definitions.
- Access indicated as downloadable CSV; end-of-monitoring timeline noted (funding-driven end in 2019).