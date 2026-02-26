# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

- A GIS-ready dataset linking observed river water temperatures with modeled climate drivers across Great Britain.
- Spans 1984–2007 for 35 monitoring sites on 21 rivers within 16 basins; extent covers Great Britain.
- Integrates water temperature data (WT) with six climate variables (modelled at 1-km resolution) derived from CHESS.

## Spatial and temporal scope

- Spatial: 35 sites mapped with precise coordinates (NGR, Easting, Northing) across 21 rivers and 16 basins in Great Britain.
- Temporal: Seasonal data aggregations (three-month averages) across multiple years within 1984–2007.
- Seasons encoded as: 1 = winter, 2 = spring, 3 = summer, 4 = autumn.
- Time index for modelling: 1.0 = winter 1984, 1.25 = spring 1984, 1.5 = summer 1984, 1.75 = autumn 1984, 2.0 = winter 1985, etc.

## Data columns and meanings

- UID: Unique identifier for each record.
- Year: Year of data collection.
- Season: Season code (1–4) corresponding to winter, spring, summer, autumn.
- Num Days: Number of days used to calculate the 3-month averages.
- WT: 3-month average Water Temperature (°C).
- AT: 3-month average Air Temperature (°C).
- SWR: 3-month average Short Wave Radiation (W/m²).
- WS: 3-month average Wind Speed (m/s).
- SH: 3-month average Specific Humidity (kg/kg).
- P: 3-month average Precipitation (kg/m²/day; unit equivalent to mm/day).
- LWR: 3-month average Long Wave Radiation (W/m²).
- Time: Time index used for modelling (see above).
- Dataset: Dataset name.
- Basin: Basin name.
- River: River name.
- Site: Site name or code.
- NGR: British National Grid reference.
- Easting, Northing: British National Grid coordinates.

## Data sources and integration

- Water temperature data (WT) collated from CEH and related projects; temporal resolution varies by source.
- Climate data (six variables) from CHESS, the forcing dataset for JULES:
  - CHESS provides daily time series (1971–2007) on a 1-km grid across the UK.
  - Six climate variables derived for each 1-km cell: Air Temperature (AT), Short Wave Radiation (SWR), Wind Speed (WS), Specific Humidity (SH), Precipitation (P), Long Wave Radiation (LWR).
  - Precipitation is based on rain-gauge data.
- Spatial matching: Each CHESS 1-km cell was matched to the study temperature sites contained within it.

## Season derivation and processing steps

- Sub-daily WT data (where available) were averaged to daily values; some datasets used spot measurements representing daylight conditions.
- Daily WT and daily CHESS climate data were date-matched.
- Seasonal averages were computed for all variables using standard definitions:
  - Winter: December–February (note: winter data for year y use December of year y−1 plus Jan–Feb of year y).
  - Spring: March–May.
  - Summer: June–August.
  - Autumn: September–November.
- Season codes (1–4) reflect the order above, and the Time index encodes year-season progression.

## Data use and GIS applications

- Enables analysis of spatial patterns in river water temperature and its climatic drivers across GB.
- Facilitates exploration of relationships between WT and climate variables (AT, SWR, WS, SH, P, LWR) at 1-km resolution proximity to sites.
- Supports coastal/river management, ecological studies, and climate-change impact assessments by providing seasonally resolved, multi-source data integrated at site level.
- Useful for map-based visualizations of seasonal WT and its drivers, and for modelling efforts (e.g., assessing thermal sensitivity to climate variability).

## Considerations and limitations

- Temporal resolution of WT data varies by contributing project; seasonal aggregation mitigates some variation but can still influence interpretation.
- Data integration relies on proximity within 1-km CHESS cells to sites; microclimate effects beyond this resolution may be underrepresented.
- Some WT data reflect daylight conditions or site-specific sampling nuances; users should consider these when performing fine-scale analyses.
- Data completeness depends on the availability of source datasets across all sites and years.

## References and related works

- CHESS climate dataset and JULES model framework references (contextual background for climate drivers and downscaling approach).
- Site-specific hydrology and ecology studies contributing WT data (e.g., Frome, Great Ouse, Tadnoll, Plynlimon, UKAWMN, LOCAR, Pang and Lambourn catchments).