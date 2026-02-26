# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

## Purpose and significance
- Investigates how climate variability and change influence river water temperature (WT), a key driver of ecology, biogeochemistry, and services (e.g., cooling for power plants, recreation).
- Aims to unravel large-scale spatial and temporal variability in climate-WT relationships and how basin properties modify these relationships to inform water and land management, climate mitigation, and adaptation.

## Dataset scope and coverage
- Temporal coverage: 1984–2007.
- Spatial coverage: 35 WT monitoring sites across 21 rivers within 16 basins in Great Britain.
- Data merged: observed WT with modeled climate data (six variables) at 1-km resolution near each site.
- Data products are provided as 3-month seasonal averages.

## Data columns and definitions
- UID: Unique identifier.
- Year: Year of data collection.
- Season: Seasonal code (1 = winter; 2 = spring; 3 = summer; 4 = autumn).
- Num Days: Number of days used to calculate the 3-month averages.
- WT: 3-month average water temperature (°C).
- AT: 3-month average air temperature (°C).
- SWR: 3-month average short-wave radiation (W m^-2).
- WS: 3-month average wind speed (m s^-1).
- SH: 3-month average specific humidity (kg kg^-1).
- P: 3-month average precipitation (kg m^-2 d^-1; equivalent to mm d^-1).
- LWR: 3-month average long-wave radiation (W m^-2).
- Time: Time index for modelling (e.g., 1.0 = winter 1984; 1.25 = spring 1984; etc.).
- Dataset: Dataset name.
- Basin, River, Site: Geographical identifiers.
- NGR, Easting, Northing: National Grid references.

## Data sources and integration
- Water temperature data (WT) compiled from CEH-led projects and related studies with varying temporal resolutions; examples include Frome, Great Ouse, Tadnoll, Plynlimon catchment studies, UK Acid Water Monitoring Network, and LOCAR.
- Climate data provided by CHESS (Climate Hydrology and Ecology research Support System): six climate variables, serving as forcing data for the JULES model; CHESS downscales MORECS 40-km grids to 1-km cells; daily time series for 1971–2007; each CHESS cell matched to the site(s) it contains.

## Seasonal series derivation and data processing
- Step 1: Sub-daily WT data are averaged to daily values; certain datasets (spot measurements) are treated as representative of their measurement day.
- Step 2: Daily WT data are matched to the corresponding daily climate data.
- Step 3: Seasonal averages are computed from daily data for all seven variables (WT, AT, SWR, WS, SH, P, LWR).
- Season definitions: Winter (December–February), Spring (March–May), Summer (June–August), Autumn (September–November). Winter values for year y use December of year y−1 through February of year y.
- Time indexing: Season codes (1–4) are used to denote winter, spring, summer, autumn.

## Modelling and applications
- The dataset supports analysis of climate-WT associations and their spatial-temporal patterns, aiding climate change impact assessment and water/land management decisions.
- CHESS-derived data provide a consistent, model-based climate backdrop for potential use in JULES or other modelling approaches.

## References
- Best, M. J., et al. (2011). The Joint UK Land Environment Simulator (JULES), model description.
- Broadmeadow, S. B., et al. (2011). Influence of riparian shade on lowland stream temperatures.
- Cris p, D. T. (1997). Water temperature of Plynlimon streams.
- Edwards, F. K., et al. (2009). Re-introduction of Atlantic salmon to Tadnoll Brook.
- Evans, C. D., et al. (2008). Buffering recovery from acidification by organic acids.
- Hough, M. N., & Jones, R. J. A. (1997). MORECS version 2.0 overview.
- Keller, V., et al. (2006). Continuous Estimation of River Flows (CERF) technical report.
- Langan, S. J., et al. (2001). Variation in river WT over a 30-year period.
- Neal, C., et al. (2010). Hydrology and water quality of headwaters of the River Severn.
- Welton, J. S., et al. (1999). Timing of Atlantic salmon migration in the River Frome.
- Wheater, H. S., et al. (2006). Hydro-ecological functioning of Pang and Lambourn catchments.