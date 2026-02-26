# SAMPLING

- This document catalogs environmental sampling campaigns across several water-related media, detailing how each dataset was collected, what measurements were taken, how frequently, and the time span of collection.

- Datasets and metadata

  - Rainfall
    - Collection method: Bulk samples from continuously open collectors (15 cm diameter PVC with anti-bird protection and coarse filter).
    - Collection devices: Continuous rain gauge at ground level.
    - Flow/volume: Noted as rainfall flow/volume from the rain gauge.
    - Field measurements: Air temperature (glass thermometer and thermistor probe).
    - Sampling interval: Weekly or daily.
    - Time span: 10 May 1983 to 18 May 1999.
    - Filtration: Lab.

  - Cloud
    - Collection method: Bulk samples from CEH Edinburgh pattern lidded harp-type passive collector.
    - Collection device: Harp-type passive collector.
    - Flow/volume: Weight of sample.
    - Field measurements: None.
    - Sampling interval: Weekly.
    - Time span: 25 Sep 1990 to continuous (ongoing implied).
    - Filtration: Lab.

  - Stream water
    - Collection method: Grab samples.
    - Collection device: Plastic bucket attached to plastic cord; sample taken mid-stream.
    - Flow/volume: CEH stream (flume) gauges; or flow data from nearest flume if not sampled by a flume.
    - Field measurements: Stream temperature and electrical conductivity (field meters corrected to 25°C).
    - Sampling interval: Weekly or daily.
    - Time span: 10 May 1983 to continuous.
    - Filtration: Field.

  - Groundwater
    - Collection method: Grab samples after flushing boreholes.
    - Collection device: BGS borehole sampler.
    - Flow/volume: Dip level recorder (depth relative to top of borehole cover).
    - Field measurements: Groundwater temperature and electrical conductivity (field meters corrected to 25°C).
    - Sampling interval: Monthly, fortnightly, or weekly.
    - Time span: 24 Apr 1994 to 14 Feb 2001.
    - Filtration: Field.

  - Throughfall
    - Collection method: Bulk samples from trough collectors.
    - Collection device: Trough collector.
    - Flow/volume: Volume of sample.
    - Field measurements: None.
    - Sampling interval: Fortnightly.
    - Time span: 6 Feb 1984 to 2 Sep 1991.
    - Filtration: Lab.

  - Stemflow
    - Collection method: Bulk samples with plastic tubing around trees and carboy collectors.
    - Collection device: Plastic tubing and carboy collector.
    - Flow/volume: Volume of sample.
    - Field measurements: None.
    - Sampling interval: Fortnightly.
    - Time span: 6 Feb 1984 to 2 Sep 1991.
    - Filtration: Lab.

- Data integration and management implications for Data Support

  - The datasets span different media (rainfall, cloud, surface water, groundwater, throughfall, stemflow) with distinct collection devices and measurement practices, enabling multi-component hydrological analyses but requiring harmonization of units, intervals, and time stamps.
  - Lab filtration is consistently used across all media, indicating a common post-collection processing step that should be captured in metadata.
  - Some datasets are continuous or ongoing (e.g., rainfall and streamwater), while others have defined ends, which affects longitudinal analyses and data versioning.
  - Field measurements are present for some datasets (temperature, conductivity) and absent for others, impacting how datasets can be correlated without imputing or annotating missing variables.
  - The need to access multiple collection systems and formats suggests a requirement for standardized metadata schemas and clear provenance to support discovery, quality assurance, and end-user self-service exploration.

- Practical data-use considerations

  - Build dashboards or reports that can compare temporal trends across media (e.g., rainfall vs. streamflow) once aligned to common time scales.
  - Implement data quality checks to address patchy data, gaps, and differing sampling intervals.
  - Provide clear documentation on collection methods, devices, and field measurements to aid end-users in interpretation and appropriate usage.
  - Support data discovery by tagging datasets with media type, collection method, instrumentation, sampling interval, and time span.