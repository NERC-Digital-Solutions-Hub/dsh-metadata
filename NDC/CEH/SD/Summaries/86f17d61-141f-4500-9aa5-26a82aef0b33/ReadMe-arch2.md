# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

## Overview
- Measurements collected on the Irrawaddy and Salween rivers during two monsoon seasons (Aug 2017, Aug 2018) and two dry seasons (Feb 2018, May 2019).
- Sampling sites were upstream of delta distributary networks.
- Goals align with understanding flow dynamics and suspended sediment characteristics for environmental monitoring and policy support.

## What was measured
- Flow velocity profiles across the river channel using an Acoustic Doppler Current Profiler (ADCP) Rio Grande II (1200 kHz) on a moving boat.
- Discharge across cross-sections derived from multiple transects.
- Suspended sediment characteristics: concentration (SSC), particle-size distribution (D50, D84, and fractions), and organic carbon content (wt%).

## Equipment and data collection approach
- ADCP data collected with the boat moving perpendicular to flow; GPS used for positioning with accuracy <5 m.
- Additional flow-velocity sampling conducted while drifting during suspended-sediment sampling.
- Sediment depth profiles collected with a modified Van Dorn sampler to ensure near-isokinetic sampling conditions.
- Depth and total sediment mass determined through careful weighing, filtration (0.2 μm PES), and lab processing.

## Sediment processing and analyses
- Particle size: laser diffraction (Malvern Mastersizer 2000), 20-bin resolution (0.35–2000 μm), 3–5 repeats per sample, typical uncertainty <10%.
- Organic carbon: carbonate removed with acid (HCl) before EA-IRMS analysis; precision ~0.05%.
- Samples kept in dark, transported under controlled conditions, and freeze-dried for analysis.

## Data processing workflow
- Raw ADCP data processed initially in WinRiver II, then exported for further processing.
- Velocity fields converted into a mean cross-section (MCS) per sampling date using Velocity Mapping Toolbox.
- MATLAB (2019b) used to interpolate gaps, remove outliers, and extrapolate to surface and bottom where necessary (inpaintnans).
- Processed velocity data and cross-sectional areas uploaded as ADCP_processed data.

## Data structure and file organization
- NaN used to denote missing data across all files.
- ADCP_RAW: raw hydroacoustic data organized by date/site.
  - Subfolders: Q_transects (flow-velocity transects) and Sed_samples (drifting sediment sampling data).
  - _ASC.TXT files: hydroacoustic data (Teledyne Rio Grande Workhorse 1200 kHz); detailed structures described in ADCP_datastructure_description.pdf.
  - _GPS.TXT files: external GPS data in NMEA 0183 format.
- ADCP_PROCESSED: derived data with three CSV types per site/date:
  - Water depth per bin (m)
  - Cross-sectional area per bin (m2)
  - Primary flow velocity per bin (cm/s)
- Q_transects.csv: transect-level discharge data and metadata (e.g., Start/End times, measurements, extrapolations, boat speed, flow direction, cross-section width, etc.).
- Q_crosssections.csv: cross-section discharge estimates and uncertainties (Discharge_m3_per_s, Transects_used, etc.).
- samples_data.csv: sediment sample metadata and measurements (Sample_ID, Site_season, Sample_profile, Sample_depth_m, SSC_mgL, OC_wtprc, D50_um, D84_um, etc.).
- Data structure references: ADCP_datastructure.pdf and ADCP_datastructure_description.pdf describe file headers and data organization.

## Data content highlights
- Cross-sections and transects provide spatially distributed velocity and discharge information across river channels.
- Sediment samples incorporate depth profiles, organic carbon content, and grain-size distributions, enabling integrated sediment flux analysis.
- Data quality practices include isokinetic sampling, careful filtering, calibration standards, and explicit handling of missing data.

## Usage and access considerations for analysts
- Data are standardized and stored with explicit metadata to facilitate integration with other environmental datasets.
- Outputs are designed for clear visualization (maps, charts, cross-sections) and for informing environmental health and policy performance assessments.
- For re-use, cite Baronas et al. (2020) when applying the synoptic Rouse-based model to compute suspended sediment flux.

## Relevant citations
- Baronas, J. J., Tipper, E. T., Bickle, M. J., Hilton, R. G., Stevenson, E. I., Hackney, C. R., et al. (2020). Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers. Journal of Geophysical Research: Earth Surface.