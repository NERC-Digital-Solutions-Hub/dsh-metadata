# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

- A multi-year, GIS-relevant dataset describing flow velocity, river discharge, and suspended sediment characteristics for the Irrawaddy and Salween rivers, collected 2017–2019.
- Includes raw and processed hydrodynamic and sediment data, plus comprehensive metadata to support spatial analysis and map-based visualisations.
- Cited work for usage: Baronas, J. J., et al. (2020). Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers. Journal of Geophysical Research: Earth Surface.

## What’s in the dataset

- Flow velocity data
  - Collected with an Acoustic Doppler Current Profiler (ADCP) on a moving boat.
  - Sampling campaigns: August 2017, August 2018 (monsoon seasons) and February 2018, May 2019 (dry seasons).
  - Measurements taken just upstream of delta distributaries; GPS position with <5 m horizontal accuracy.
  - Data processed to produce mean cross-sections and mean along-channel velocity fields; includes gap filling and surface/bottom extrapolation.
  - Additional velocity data during sediment sampling in August 2018 and May 2019 (drifting with current).

- Sediment sampling and analysis
  - Depth profiles of suspended sediments (Aug 2017, Aug 2018, May 2019) and surface samples (Feb 2018).
  - Depth sampling with Van Dorn-style sampler under isokinetic conditions; samples filtered and processed for sediment concentration.
  - Particle-size distribution measured with laser diffractometry (0.35–2000 μm; 20-bin resolution).
  - Organic carbon concentration (%wt) determined after carbonate removal; precision ~0.05%.

- Metadata and data organization
  - Data structured to support GIS use, with cross-sections, transects, and sample locations linked to timestamps and positions.
  - Files and folders:
    - ADCP_RAW: per-date site folders containing Q_transects (velocity across channel) and Sed_samples (drifting sediment data). Some dates lack Sed_samples data.
    - ADCP_PROCESSED: derived cross-sectional bins with depth (rows) and lateral position across the channel (columns). Three CSV types per site/date: water depth per bin, cross-sectional area per bin, primary flow-velocity per bin.
  - Metadata CSVs:
    - samples_data.csv: per-sample metadata including Sample_ID, site, profile, depth, time, ADCP linkage, latitude/longitude, SSC (suspended sediment concentration), OC, and particle-size metrics (D50, D84, and size fractions).
    - Q_transects.csv: transect-level data including location, time, discharge components (Meas, Top, Bottom, Left, Right), cross-section width/area, velocities, and methods.
    - Q_crosssections.csv: cross-section summaries including date, location, total discharge, and transect IDs used.
  - Data structure notes:
    - NaN denotes no data across files.
    - Suffixes _ASC.txt and _GPS.txt for raw ADCP and GPS data; detailed structure described in ADCP_datastructure.pdf.

## Key data fields (highlights)

- Samples and sediment
  - Sample_ID, Site_season, Sample_profile, Sample_depth_m, Sample_time
  - SSC_mgL, OC_wtprc, D50_um, D84_um, ParticleSize_fraction_under_XXX_um
- ADCP and transects
  - Crosssection_ID, Transect_ID, Date, Start_Time, End_Time, Total_Q_m3_per_s, Meas_Q_m3_per_s, Top_Q_m3_per_s, Bottom_Q_m3_per_s, Left_Q_m3_per_s, Right_Q_m3_per_s
  - Width_m, Total_Area_m2, Flow_Speed_m_per_s, Flow_Dir_degrees, Velocity_method, Depth_method
  - Discharge_uncertainty (for cross-sections), Transects_used
- Processed data (ADCP_PROCESSED)
  - Bin-based water depth (m), cross-sectional area (m2), and primary flow velocity (cm/s) per site/date

## How this data is structured for GIS use

- Spatial references
  - Latitude/Longitude coordinates captured for samples and cross-sections (decimal degrees).
  - Cross-sections represent perpendicular transects across the river channel; processed data are arranged as bins from left bank to right bank.
- Temporal scope
  - Multiple dates across 2017–2019 enabling temporal GIS analyses of flow and sediment dynamics.
- Data links
  - ADCP raw data (ADCP_RAW) linked to processed outputs (ADCP_PROCESSED) via site/date naming conventions.
  - Metadata files (samples_data.csv, Q_transects.csv, Q_crosssections.csv) provide linkage between raw data, processed outputs, and sample observations.

## Considerations for GIS analysts

- Data completeness
  - Note that some dates in the ADCP_RAW/Sed_samples structure do not include Sed_samples data.
- Data quality and processing
  - Raw ADCP data are paired with GPS; velocity fields are interpolated and gap-filled; surface and bottom extrapolations are applied.
  - Sediment data include isokinetic sampling, filtration, drying, and laboratory analyses with quantified uncertainties.
- Data integration
  - Use samples_data.csv to join sediment properties with ADCP transects and cross-sections.
  - Use Q_transects.csv and Q_crosssections.csv to compute site-level discharges and to create spatially explicit representations of river hydraulics.
- Potential GIS products
  - Per-date cross-section velocity and discharge maps across the channel.
  - Gridded velocity fields across cross-sections for synoptic modelling or visualization.
  - Spatial distribution of suspended sediment concentration, grain-size statistics, and organic carbon along the channel.

## Usage and citation

- Data are tied to the publication: Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers (Baronas et al., 2020, JGR Earth Surface).
- Follow the citation guidance provided in the dataset notes when using the data.