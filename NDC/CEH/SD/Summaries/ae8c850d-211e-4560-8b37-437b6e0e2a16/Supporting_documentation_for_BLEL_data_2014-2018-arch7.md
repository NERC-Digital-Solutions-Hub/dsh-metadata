# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2014 to 2018

## Overview
- Long-term, fortnightly monitoring dataset from Blelham Tarn, Cumbria, England (2014–2018).
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples collected from 0–5 m; sampling location is the deepest part of the lake at a buoy when accessible; shore samples taken when buoy visits were not possible.
- Data are provided as raw measurements with no calibration/quality-control applied yet.

## Sampling regime and collection methods
- Fortnightly sampling schedule with measurements taken from a boat at the buoy or from the shore when the buoy could not be visited.
- Water chemistry values reflect integration from 0 to 5 meters depth.
- Some samples labeled as Flag 2 indicate shore sampling without buoy access; all other samples taken at the marked buoy location.

## Data quality and limitations
- Data are raw and not yet quality controlled or calibrated.
- Visual double-entry checks performed; residual issues may arise.
- Missing data due to weather conditions or staff shortages.

## Data structure and fields
- Delivered as CSV with the following columns:
  - Date: Date of measurement.
  - Variable, Description: One of TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA, with units as described.
  - Value, Description: Measured value for each variable.
  - Sign (if<LOD), Description: Indicates if the value is below the detection limit (a "<" sign if applicable).
  - Flag, Description: 1 = sample taken at the buoy location; 2 = sample taken from the shore (buoy visit not possible).

## Spatial considerations for GIS
- Sampling tied to a fixed buoy location at the deepest part of the lake; shore samples provide an alternate spatial reference when needed.
- Units and depth integration are specified, enabling consistent map-based visualization across variables and time.
- Data can be joined with auxiliary spatial layers (lake boundaries, buoy location, shoreline sampling points) for map products and trend analyses.

## Funding and usage references
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Related publications and context:
  - Gray et al. 2019; modelling lake cyanobacterial blooms.
  - Wang et al. 2016; carbon and silicon geochemical cycles in water bodies.
  - Woolway et al. 2016; lake surface temperatures in climate summaries.
  - Overview reference: Maberly et al. 2017; long-term ecological informatics in the English Lake District.

## Practical notes for map-based data products
- Consider creating time-series visualizations for each variable (per variable maps or faceted panels).
- Distinguish buoy-based vs shore-based samples via the Flag field when mapping spatial coverage.
- Be mindful of raw data status; apply appropriate quality-control and calibration steps before final map products if possible.
- Link to metadata (sampling regime, detection limits, units) to aid secondary users in interpretation.