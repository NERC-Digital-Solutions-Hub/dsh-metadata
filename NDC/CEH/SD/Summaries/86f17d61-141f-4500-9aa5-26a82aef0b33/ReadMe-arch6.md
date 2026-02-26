# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

## Overview
- Provides flow velocity measurements, discharge estimates, and suspended sediment characteristics for the Irrawaddy and Salween rivers, collected during 2017–2019.
- Data are intended to support analysis of sediment flux and river dynamics using a synoptic Rouse-based approach (Baronas et al., 2020).
- Citation required: Baronas, J. J., et al. (2020). Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers. Journal of Geophysical Research: Earth Surface.

## Data collection and processing

### Flow velocity measurements (ADCP)
- Platforms and dates: Two monsoon seasons (Aug 2017, Aug 2018) and two dry seasons (Feb 2018, May 2019).
- Location: Upstream of delta distributary networks for both rivers.
- Instrument: Teledyne Rio Grande II 1200 kHz Acoustic Doppler Current Profiler (ADCP) mounted on a moving boat, down-facing, 40–60 cm depth range.
- Transects: 1–5 per site; discharge reproducibility typically better than 6% per transect (Q_transects.csv).
- Processing workflow:
  - Initial processing in WinRiver II; export to Velocity Mapping Toolbox.
  - Create mean cross-sections (MCS) perpendicular to channel; derive mean along-channel velocity field.
  - MATLAB 2019b: gap filling, outlier removal, and extrapolation to surface and bottom (inpaintnans).
  - Processed velocity data, depth, and cross-sectional area stored in ADCP_processed.
- Additional velocity data: Collected during sediment sampling in Aug 2018 and May 2019 (drifting with current); associated ADCP files listed in samples_data.csv.

### Sediment sampling and processing
- Depth profiles: Aug 2017, Aug 2018, May 2019 (both sites); Feb 2018 (surface only).
- Sampling method: Modified 8.5 L Van Dorn depth sampler; isokinetic conditions achieved via drifting boat and large-diameter sampler.
- Sample handling: 10 L bags; weighed; filtered within 24 h through 0.2 μm PES membrane; sediment washed into opaque containers; freeze-dried later.
- Suspended sediment concentration: computed as dried sediment mass divided by initial water mass (error < ~1%).
- Particle size: Dry samples analyzed with Malvern Mastersizer 2000 (0.35–2000 μm; 20-bin resolution); 10–20% obscuration; 3–5 measurements per sample; typical PSD uncertainty <10%.
- Organic carbon: Carbon removed with HCl; analyzed by EA-IRMS; precision ~0.05% (wt% C); correction for blanks (<5%).

## Data structure and access

### Folder organization
- ADCP_RAW: Per-date site folders; within each, subfolders:
  - Q_transects: Raw ADCP transect data (lateral crossings) for discharge structure.
  - Sed_samples: Hydroacoustic data while drifting and sediment depth samples (some dates lack Sed_samples).
  - Metadata files link raw data to samples and transects via samples_data.csv.
- ADCP_PROCESSED: Derived products (bin-based across cross-sections) for each site/date; three CSV files per site/date:
  - Depth per bin (m)
  - Cross-sectional area per bin (m2)
  - Primary flow velocity per bin (cm/s)

### Key files and headers
- samples_data.csv: Links sediment samples to ADCP data
  - Sample_ID, Site_season, Sample_profile, Sample_depth_m, Sample_time, ADCP_file_prefix, ADCP_Ens_no, Latitude, Longitude, SSC_mgL, OC_wtprc, D50_um, D84_um, ParticleSize_fraction_under_XXX_um
- Q_transects.csv: Transect details and discharge information
  - Crosssection_ID, Magnetic_declination_degrees, Transect_ID, Date, Transect_filename, Start_Bank, Ens_count, Start_Time, Total_Q_m3_per_s, Delta_Q_prc, Top_Q_m3_per_s, Meas_Q_m3_per_s, Bottom_Q_m3_per_s, Left_Q_m3_per_s, Left_Dist_m, Right_Q_m3_per_s, Right_Dist_m, Width_m, Total_Area_m2, Boat_Speed_m_per_s, Flow_Speed_m_per_s, Flow_Dir_degrees, End_Time, Duration_sec, Start_Ens, End_Ens, Velocity_method, Depth_method
- Q_crosssections.csv: Cross-section summaries and linkage to transects
  - Crosssection_ID, Date, Latitude, Longitude, Discharge_m3_per_s, Discharge_uncertainty, Transects_used
- ADCP-related supporting files
  - ADCP_datastructure.pdf: structure/column headers for _ASC.TXT and _GPS.TXT
  - ADCP_datastructure_description.pdf: more detailed file structure for raw ADCP and GPS data
- Notes: NaN used to indicate missing data

## Key variables and how they are derived

- Velocity: From ADCP across binning across the channel; results aggregated to an MCS for each sampling date.
- Discharge: Derived per transect and per cross-section; cross-section discharge is average across used transects with uncertainty (2 standard deviations).
- Sediment characteristics: Depth-resolved suspended sediment concentration (SSC in mg/L); PSD (D50, D84 in μm) and size fractions; organic carbon content (%wt C) after carbonate removal.

## Data quality, limitations, and provenance

- Quality checks: QA/QC steps include alignment of ADCP transects with cross-sections, isokinetic sampling validation, and outlier removal.
- Uncertainty: Discharge uncertainty provided for cross-sections; individual transects show discharge reproducibility typically <6%.
- Data gaps: Some measurement dates do not include Sed_samples data; overall linkage relies on sample_data.csv, ADCP_RAW, and ADCP_PROCESSED to connect data streams.
- Data fidelity: Processed ADCP data include gap-filling and extrapolations (surface/bottom) to generate complete velocity fields.
- Scope: Data cover two rivers (Irrawaddy and Salween) and four seasonal windows (two monsoon, two dry years).

## Usage and citations

- Data is intended for exploration of flow velocity fields, cross-sectional discharge, and suspended sediment dynamics; suitable for self-service analytics, dashboards, and reproducible research in river hydrology and sediment transport.
- Proper citation required: Baronas et al. 2020 JGR Earth Surface for the synoptic model integration and data usage.

## Practical notes for data support

- Helpful for building end-user data products such as:
  - Interactive dashboards of discharge vs. time and across-section velocity profiles
  - Cross-sectional velocity and area visualizations
  - Sediment PSDs and OC trends by site/date
- Ensure proper data linking using sample IDs and cross-section IDs across ADCP_RAW and ADCP_PROCESSED folders, with reference to the provided CSVs and supporting PDFs for structure.