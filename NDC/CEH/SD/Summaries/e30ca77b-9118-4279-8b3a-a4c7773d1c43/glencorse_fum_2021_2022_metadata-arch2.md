# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Purpose and scope
- Studying effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Located at Glencorse woodland near Edinburgh (55.8539 N, -3.2151 W; altitude 200 m); Birch plantation experimental site established in 2021.
- Data intended to support understanding of NH3 deposition and environmental responses, with standardized monitoring outputs.

## Study design and location
- NH3 enhancement system controlled by wind conditions; NH3 released only when wind direction is 275–345 degrees and wind speed is 0.3–10 m/s.
- NH3 released from three horizontal PVC tubes (each 20 m long, 110 mm diameter) at elevations 0.5, 1.35, and 2.2 m above ground.
- NH3 delivered from a cylinder through a manifold using a mass flow controller (MFC) and solenoid valve; release occurs into the fan airflow to dilute NH3.
- Wind data collected below the canopy to determine release conditions.

## Data collection and parameters
- Monitoring period: 16 September 2021 to 5 January 2023; all times in GMT.
- Data collected every 20 seconds and averaged to 15-minute intervals.
- Data file contains 45,538 measurements across 5 parameters.
- Parameters and metadata include:
  - NH3_status: release status (0 = OFF, >0 = ON)
  - NH3_flow_set: NH3 flow set point (slpm) for release
  - NH3_flow: actual NH3 flow through the MFC into the release manifold (slpm)
  - Wind_speed: below-canopy wind speed (ms^-1)
  - Wind_direction: below-canopy wind direction (degrees)
- Additional metadata fields in the CSV include Timestamp, Instrument, Manufacturer, and Description for each parameter.

## Data structure and format
- CSV dataset with clearly defined columns and 15-minute timestamp format: dd/mm/yyyy hh:mm.
- Each row corresponds to a 15-minute interval within the monitoring period.
- File design supports integration into standard environmental monitoring workflows and portals.

## Quality control and data gaps
- Visual quality checks performed; removal of obvious instrument malfunctions, datalogger programming issues, and power-cut artifacts.
- Some gaps remaining due to replacement of faulty gas control components.

## Temporal coverage and location details
- Timeframe: 16 Sep 2021 – 5 Jan 2023.
- Location: Glencorse woodland, near Edinburgh, UK; coordinates 55.8539 N, -3.2151 W; altitude 200 m.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.

## Relevance for environmental monitoring and policy
- Demonstrates standardized NH3 enhancement data collection suitable for monitoring environmental health and nitrogen deposition.
- Data quality control and metadata support reproducibility and cross-study comparisons.
- Designed for integration with other datasets and potential publication, reports, maps, and policy-relevant analyses.
- Emphasizes the importance of making underlying data accessible and usable beyond single outputs.