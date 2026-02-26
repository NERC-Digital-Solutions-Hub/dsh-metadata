# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

## Aim
- Combine observed river water temperatures with a consistent set of modeled climate data to study climate–water temperature relationships.
- Analyze spatio-temporal variability and the influence of basin properties to inform water and land management, climate change mitigation, and adaptation strategies.

## What it covers
- 35 water temperature monitoring sites on 21 rivers across 16 basins in Great Britain.
- Time period: 1984–2007.
- Data: six climate variables (from CHESS) matched within 1 km of each site.
- Temporal resolution: three-month seasonal averages (winter, spring, summer, autumn).

## Dataset structure and variables
- Core fields
  - UID, Year, Season (1=winter, 2=spring, 3=summer, 4=autumn), Num Days, Time (season index), Dataset, Basin, River, Site, NGR, Easting, Northing.
- Measurements
  - WT: 3-month average Water Temperature (°C).
  - AT: 3-month average Air Temperature (°C).
  - SWR: 3-month average Short Wave Radiation (W/m^2).
  - WS: 3-month average Wind Speed (m/s).
  - SH: 3-month average Specific Humidity (kg/kg).
  - P: 3-month average Precipitation (kg/m^2 d^-1; unit equivalent to mm d^-1).
  - LWR: 3-month average Long Wave Radiation (W/m^2).
- Time and location
  - Time: index used for modelling (e.g., 1.0 = winter 1984, 1.25 = spring 1984, etc.).
  - NGR/Easting/Northing: National Grid references for site localization.

## Data sources and provenance
- Water temperature data
  - Collected from CEH-led and related projects with varying temporal resolutions; examples include Frome, Great Ouse, Tadnoll, Plynlimon, UK Acid Water Monitoring Network, and LOCAR.
- Climate data
  - CHESS dataset: UK-wide 1-km gridded climate data derived from MORECS (precipitation based on gauge data) and daily time series for 1971–2007, used as forcing data for JULES.

## Seasonal series derivation and processing
- Steps
  - Sub-daily WT data are averaged to daily values (some sites’ data are treated as representative of the measurement day).
  - Daily WT data are matched to daily CHESS climate data by date.
  - Seasonal (three-month) averages computed for all variables using standard season definitions.
- Season definition specifics
  - Winter: December of year y-1 to February of year y (e.g., 1976 winter uses Dec 1975 + Jan-Feb 1976).
  - Season codes: 1=winter, 2=spring, 3=summer, 4=autumn.

## Applications and interpretation
- Enables examination of large-scale spatial and temporal variability in climate–water temperature relationships.
- Helps identify the relative influence of climate and basin properties on WT, informing climate change mitigation and adaptation strategies, river management, and ecological understanding.

## Data quality, accessibility, and reuse considerations
- The dataset emphasizes standardized outputs (maps, charts) and consistent data handling across sites.
- Datasets are designed for storage and uploading to appropriate data portals, supporting broader access and reuse.
- Aligns with monitoring aims by providing verified, cleaned, and comparable temperature and climate metrics across multiple basins and time periods.

## References and context
- References include foundational papers on JULES (CHESS as forcing data), the influence of riparian shade on stream temperatures, and long-term river temperature studies, underscoring methodological and ecological contexts for the dataset.