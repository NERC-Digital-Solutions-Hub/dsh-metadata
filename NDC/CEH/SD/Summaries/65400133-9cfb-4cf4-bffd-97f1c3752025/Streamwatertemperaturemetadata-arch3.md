# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

## Purpose and relevance
- Combines observed river water temperatures with modeled climate data to study how water temperature is controlled by climate drivers.
- Aims to understand spatial and temporal variability in climate-water temperature relationships to inform water and land management, climate change mitigation, and adaptation strategies.
- Addresses interest in large-scale patterns and basin modifiers of temperature-climate relationships, which are not fully understood.

## Dataset overview
- Time period: 1984–2007.
- Spatial scope: 35 water temperature monitoring sites on 21 rivers across 16 basins in Great Britain.
- Data integration: Observed water temperature data linked with a consistent set of modeled climate variables.

## Spatial and temporal scope
- Basins: 16; Rivers: 21; Sites: 35.
- Seasonal data: 3-month averages (winter, spring, summer, autumn) derived for each site-season-year.
- Spatial resolution for climate data: 1-km grid matching CHESS dataset to study sites.

## Variables and data columns
- Core measurements: Water Temperature (WT; °C), Air Temperature (AT; °C), Short Wave Radiation (SWR; W.m-2), Wind Speed (WS; m s-1), Specific Humidity (SH; kg kg-1), Precipitation (P; kg m-2 d-1).
- Derived/time-related: Time index (season mapping; e.g., 1 = winter 1984, 1.25 = spring 1984, etc.), Num Days (days used for 3-month averages).
- Metadata: UID (unique id), Year, Season, Dataset, Basin, River, Site, NGR, Easting, Northing.
- Climate forcing: Six climate variables from CHESS (downscaled for 1-km cells); precipitation based on gauge data.

## Data sources and climate data
- Water temperature data contributed by the Centre for Ecology and Hydrology (CEH) and linked projects (e.g., Frome, Great Ouse, Tadnoll, Plynlimon, UKAWMN, LOCAR).
- Climate data: CHESS (six climate variables) as the forcing dataset for JULES; CHESS downscaled from MORECS with precipitation from rain gauges.
- CHESS time series: Daily 1971–2007, matched to study sites via spatial overlap.

## Data processing and seasonal derivation
- Seasonal series construction:
  - Sub-daily WT data aggregated to daily values where possible; some datasets are spot measurements representing the day observed.
  - Daily WT data matched to daily climate data.
  - Seasonal averages computed for winter (Dec–Feb), spring (Mar–May), summer (Jun–Aug), autumn (Sep–Nov); winter season uses Dec of previous year through Feb of the year.
- Data coding: Season codes 1–4 correspond to winter, spring, summer, autumn for consistent modeling.

## Data integration and matching
- Spatial matching: CHESS grid cells aligned with the study site locations (1-km resolution).
- Temporal alignment: Daily climate series linked to daily water temperature observations before computing 3-month seasonal means.

## References and provenance
- Key references detailing the CHESS dataset, JULES model integration, and supporting hydrology/ecology studies across UK catchments (e.g., Best et al. 2011; Hough & Jones 1997; Keller et al. 2006; Neal et al. 2010; Wheater et al. 2006; and others).

## Data governance and accessibility considerations for monitoring frameworks
- Data provenance is explicit (multiple contributing projects and datasets); integration relies on consistent processing rules and seasonal definitions.
- Metadata and data sharing considerations are evident through standardized columns (UID, Year, Season, Site identifiers) and explicit documentation of data sources and processing steps.
- Potential barriers noted in related monitoring contexts (e.g., data gaps, inconsistent metadata, diverse data resolutions) are addressed by harmonizing data via standardized seasonal derivation and spatial-temporal matching, though underlying data resolution and provenance remain essential for transparency and reuse.

## Limitations and caveats
- Temporal resolution varies across input WT datasets; some measurements are spot-based rather than continuous.
- Temperature data are not always the primary focus of the original projects, which may affect sampling design and coverage.
- Seasonal derivation relies on certain assumptions (e.g., winter season spanning December to February) and daylight-only representations for some data points.

## Applications for monitoring and policy
- Enables assessment of river thermal sensitivity to climate drivers across multiple basins and years.
- Supports climate adaptation and water resource management planning by identifying key climatic controls on WT.
- Provides a framework for integrating observed biophysical measurements with climate forcing data to inform monitoring program design and data governance in environmental health surveillance.