# SAMPLING

- The document enumerates sampling protocols for multiple environmental variables, spanning 1983 to 2001 (with cloud data continuing beyond 1990). It covers rainfall, cloud, stream water, groundwater, throughfall, and stemflow, detailing how each variable was collected, measured, and processed for later analysis and potential GIS mapping.

## Data categories and key attributes

- Rainfall
  - Collection method: Bulk sample
  - Collection device: Continuously open 15 cm diameter PVC collector with anti-bird protection and coarse filter
  - Flow/volume: Total rainfall measured at a site-level rain gauge
  - Field measurements: Air temperature (glass thermometer and thermistor probe)
  - Sampling interval: Weekly to daily
  - Start/Finish: 10 May 1983 to 18 May 1999; then 25 May 1999 to continuous
  - Filtration: Lab

- Cloud
  - Collection method: Bulk sample
  - Collection device: CEH Edinburgh pattern lidded harp-type passive collector
  - Flow/volume: Weight of sample
  - Field measurements: None
  - Sampling interval: Weekly
  - Start/Finish: 25 Sep 1990 to continuous
  - Filtration: Lab

- Stream water
  - Collection method: Grab samples
  - Collection device: Plastic bucket attached to plastic cord; sample taken near middle of stream
  - Flow/volume: CEH stream (flume) gauges; for non-flume streams, flow record provided to nearest flume
  - Field measurements: Stream temperature and electrical conductivity (field meters, 25°C correction)
  - Sampling interval: Weekly to daily
  - Start/Finish: 10 May 1983 to continuous
  - Filtration: Field

- Groundwater
  - Collection method: Grab samples after flushing boreholes
  - Collection device: BGS borehole sampler
  - Flow/volume: Dip level recorder (depth relative to top of borehole cover)
  - Field measurements: Groundwater temperature; electrical conductivity (25°C corrected)
  - Sampling interval: Monthly to weekly/fortnightly
  - Start/Finish: 24 Apr 1994 to 14 Feb 2001
  - Filtration: Field

- Throughfall
  - Collection method: Bulk sample
  - Collection device: Trough collector
  - Flow/volume: Volume of sample
  - Field measurements: None
  - Sampling interval: Fortnightly
  - Start/Finish: 6 Feb 1984 to 2 Sep 1991
  - Filtration: Lab

- Stemflow
  - Collection method: Bulk sample
  - Collection device: Plastic tubing around trees with carboy collector
  - Flow/volume: Volume of sample
  - Field measurements: None
  - Sampling interval: Fortnightly
  - Start/Finish: 6 Feb 1984 to 2 Sep 1991
  - Filtration: Lab

## Spatial and temporal scope

- Temporal coverage varies by variable; rainfall spans two periods (1983–1999, then ongoing from 1999 onward), cloud from 1990 onward (ongoing), and other variables largely 1983–2001 with some stations ending earlier.
- Spatial scope implied by device types and sites (e.g., site-level rainfall gauge, CEH Edinburgh for cloud, BGS boreholes for groundwater, streams and forest-related throughfall/stemflow), but exact coordinates are not provided in the text. GIS work would require geolocating each sampling site or instrument.

## Data quality, standards, and integration considerations

- Multiple sampling methods and devices across variables, which may introduce compatibility and bias considerations when integrating datasets (e.g., bulk vs grab samples, different collection devices, and various flowmeasurement references).
- Field vs laboratory processing (filtration indicates lab vs field data handling) that can affect data comparability.
- Different sampling intervals (daily, weekly, fortnightly) and irregular temporal coverage require harmonization for time-series analyses and map-based visualizations.
- Some measurements rely on site-specific gauges or networked flumes; cross-referencing lineage (which gauge, which flume) is needed for accurate spatial analyses.

## GIS-ready considerations and recommendations

- Geolocate all sampling sites (rainfall gauges, cloud collection points, stream/groundwater stations, throughfall and stemflow plots) to enable map-based visualization and spatial analyses.
- Standardize units and measurement references (e.g., flow/volume definitions, temperature corrections) across variables for consistent mapping.
- Create metadata records for each site with:
  - Variable type and method
  - Collection device and protocol
  - Sampling interval and time window (start/finish)
  - Filtration and data processing notes
  - Any calibration or correction applied (e.g., 25°C conductivity correction)
- Build time-enabled GIS layers to capture temporal coverage and enable time-series visualization.
- Plan for data gaps and discontinuities (e.g., 1984–1991 gaps for throughfall/stemflow) in analyses and storytelling.
- Consider data fusion approaches to combine datasets at differing resolutions, ensuring provenance and uncertainty are retained for end users.