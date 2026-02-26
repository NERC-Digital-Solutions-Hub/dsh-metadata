# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

## Overview
- Long-term, fortnightly monitoring dataset from Bassenthwaite Lake, Cumbria, England (1990–2013).
- Variables tracked: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH (PH), ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples integrated from 0–5 m; collected from a boat at the deepest part of the lake; shore samples used when buoy sampling was not possible.
- Data are provided as raw values (not QC’d/calibrated) with some visual checks; detailed metadata described below.

## Sampling regime and collection methods
- Fortnightly sampling schedule.
- Measurements collected from August 1990 to end of 2013.
- Depth-integrated water samples (0–5 m) taken at the deepest site (buoy); if buoy access was impossible, samples were taken from the shore (Flag 2).

## Quality control and limitations
- Data are raw and not yet quality controlled or calibrated; double entries exist from 2005 onwards.
- Visual checks performed; some data gaps: March–June 2001 due to foot-and-mouth outbreak restricting lake access.
- Detection limits indicated in data (sign_if_LT_LOD column); some values below detection limits shown with a < symbol.
- Some samples not integrated due to sampling constraints (Flag 2).

## Data structure and metadata
- Data delivered as a comma-separated values (CSV) file.
- Core columns:
  - sdate: measurement date.
  - variable: shorthand for each measured parameter (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value: measured value for each variable.
  - sign_if_LT_LOD: indicator if value is below detection limit (presence of <).
  - flag: sampling location indicator (Flag 1 = buoy site; Flag 2 = shore sampling).
- Descriptions provided for each column and variable.

## Notable usage and publications
- Recent examples of dataset usage in research:
  - Bernhardt, Elliott & Jones (2008): modelling phytoplankton responses to changing lake mixing depth and light extinction.
  - Elliott, Jones & Page (2009): influence of nutrient sources and retention time on phytoplankton.
  - Elliott & Bell (2011): potential long-term climate-change impacts on vendace habitat.
  - Jones et al. (2011): climate-driven changes to river flow and phytoplankton biomass.
  - Maberly et al. (2013): catchment productivity controls on lake CO2 emissions.
  - Thackeray et al. (various years 2006–2017) and related works: climate impacts on phytoplankton phenology and related lake ecology.
  - Additional references up to 2017 include broader lake temperature context in climate state reporting.

## Relevance for monitoring frameworks
- Demonstrates long-term, multi-parameter lake monitoring with consistent sampling cadence.
- Provides a clear data schema (variables, units, detection limits, sampling flags) suitable for integration into monitoring dashboards or governance reports.
- Highlights practical challenges for monitoring data: raw data status, need for QC/calibration, data gaps, and metadata completeness.
- Illustrates data governance considerations: openness of underlying data in publications, need for clear metadata, and documentation of detection limits and sampling conditions.

## Caveats for use
- Data are raw and require quality control and calibration for some analytical applications.
- Gaps exist due to disease outbreak and sampling constraints; some data are not integrated (shore samples).
- Interpretation should consider detection limits and flag indicators.