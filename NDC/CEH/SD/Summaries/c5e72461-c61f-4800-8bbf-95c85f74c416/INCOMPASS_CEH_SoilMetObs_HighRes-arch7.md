# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

## Overview
- Time series of meteorological and soil physics variables logged at one-minute resolution.
- Data collected at three INCOMPASS Land Surface Stations in India (Berambadi, Dharwad, Kanpur) from 2016-01-01 to 2019-01-01 (Kanpur data ends 2018-08-28 06:23).
- Purpose: support studies on convective organization and monsoon precipitation, atmosphere, surface processes, and related soil-physics interactions.
- Data provided as separate CSV files per station, with complete time series and standard QC.

## Study sites and characteristics
- Berambadi, Southern Karnataka
  - Location: 11.760633°N, 76.585361°E; 873 m amsl; semi-arid tropical monsoon (Aw).
  - Land use: Mixed agriculture; Alfisol soils; mean annual temp ~24.4°C; rainfall ~600 mm.
- Dharwad, Northern Karnataka
  - Location: 15.498393°N, 74.985730°E; 692 m amsl; tropical savannah (Aw).
  - Land use: Agriculture; Vertisol soils; mean annual temp ~24.3°C; rainfall ~885 mm.
  - Surrounding field has a crop rotation/intercropping schedule.
- Kanpur, Uttar Pradesh
  - Location: 26.509072°N, 80.223765°E; 129 m amsl; humid subtropical (Csa).
  - Land use: Semi-natural grassland; Fluvisol soils; mean annual temp ~25.6°C; rainfall ~820 mm.
  - Grassland experiences seasonal flooding and dynamic vegetation height (0.2–2.5 m).

## Data collection and instrumentation
- Instruments identical across all stations.
- Meteorology: 10 m mast; sensors for barometric pressure, air temperature, relative humidity, net radiation and components (SWin, SWout, LWin, LWout, Rnet), wind speed and direction, precipitation (1.0 m aperture height).
- Soil physics: duplicated measurements at two locations per site; soil heat flux at 0.03 m, soil moisture and soil temperature at 0.05 and 0.15 m depths.
- Sampling: data logged at 0.1 Hz and reported as one-minute means; precipitation summed per minute.
- Kanpur dataset ends earlier (2018-08-28 06:23) compared with 2019-01-01 end date for others.

## Quality control and data validation
- QC includes basic range checks and visual inspection for spikes/dropouts.
- Cross-checks between paired soil observations at the same depth.
- Large soil moisture changes checked against rainfall and known flooding at Kanpur.
- Clearly erroneous data removed; non-physical values flagged as missing.

## Data structure and variables
- Format: one CSV file per station; time series from 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur ends 2018-08-28 06:23).
- Time stamps: DateTime in Indian Standard Time (UTC + 5.5); end-of-minute period.
- Missing data: denoted by -9999.
- Core variables and units:
  - Pa: Barometric pressure (kPa)
  - Ta: Air temperature (°C)
  - RH: Relative humidity (%)
  - SWin: Incoming shortwave radiation (W/m^2)
  - SWout: Outgoing shortwave radiation (W/m^2)
  - LWin: Incoming longwave radiation (W/m^2)
  - LWout: Outgoing longwave radiation (W/m^2)
  - Rnet: Net radiation (W/m^2)
  - Precipitation: Total precipitation per minute (mm/min)
  - WS: Wind speed at 10 m (m/s)
  - WD: Wind direction (degrees from north)
  - G1, G2: Soil heat flux at 0.03 m (W/m^2) – location 1 and 2
  - Tsoil_0.05_1, Tsoil_0.15_1: Soil temperature at 0.05 m and 0.15 m (°C) – location 1
  - Tsoil_0.05_2, Tsoil_0.15_2: Soil temperature at 0.05 m and 0.15 m (°C) – location 2
  - VWC_0.05_1, VWC2_0.15_1: Soil volumetric water content at 0.05 m and 0.15 m (%, location 1)
  - VWC1_0.05_2, VWC2_0.15_2: Soil volumetric water content at 0.05 m and 0.15 m (%, location 2)

## Temporal coverage and accessibility
- Coverage: 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur ends 2018-08-28 06:23).
- Data are suitable for high-resolution GIS analyses of surface energy fluxes, meteorology, and soil moisture dynamics over the three sites.
- CSV format facilitates integration with GIS and other spatial-temporal datasets; note IST timestamps for alignment with local data.

## Usage considerations for GIS specialists
- Use the station coordinates and depths to map spatial variability in surface energy fluxes and soil moisture.
- Be mindful of the -9999 missing values when computing aggregates or performing interpolation.
- Temporal granularity (1-minute) enables detailed event-based analyses but may require down-sampling for certain GIS visualizations.
- Data quality improvements were applied during QC; consider additional validation if merging with other regional datasets.

## Acknowledgments and provenance
- INCOMPASS Project funded by UK and Indian agencies; additional support from related UK-India initiatives.
- Acknowledges site owners, collaborators, and contributing institutions.