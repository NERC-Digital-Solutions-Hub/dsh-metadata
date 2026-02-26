# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

## Overview
- Timeframe: 2017–2019, with sampling during two monsoon seasons (Aug 2017, Aug 2018) and two dry seasons (Feb 2018, May 2019).
- Location: Irrawaddy and Salween rivers, sampled just upstream of delta distributary networks.
- Purpose: Record flow velocity, discharge, suspended sediment concentrations and compositions to support understanding and modeling of sediment flux; used to inform a synoptic Rouse-based model (Baronas et al., 2020).

## Data collection and methods
- Flow velocity
  - Instrument: Acoustic Doppler Current Profiler (ADCP) Rio Grande II 1200 kHz, mounted on a moving boat.
  - Procedure: Transects across the river channel perpendicular to flow; GPS for position with <5 m accuracy.
  - Sampling: 1–5 transects per site; discharge reproducibility typically better than 6%.
  - Data processing: WinRiver II → Velocity Mapping Toolbox → MATLAB 2019b; gap filling and outlier removal; extrapolation to surface and bottom; data stored in ADCP_processed.
- Sediment sampling
  - Depth profiles of suspended sediments collected at multiple depths in Aug 2017, Aug 2018, May 2019; surface samples in Feb 2018.
  - Sampling tool: Modified 8.5 L depth sampler; isokinetic conditions ensured during drifting.
  - Processing: Filtration (0.2 μm PES), drying, and weighing to calculate suspended sediment concentration (SSC).
  - Particle size: Malvern Mastersizer 2000; 20-bin distribution (0.35–2000 μm); multiple measurements with ~<10% uncertainty.
  - Organic carbon: carbonate removal via HCl; EA-IRMS analysis; precision ~0.05%.
- Data files and organization
  - ADCP_RAW: raw hydroacoustic data and accompanying GPS data; organized by site/date; Subfolders include Q_transects (flow transects) and Sed_samples (sediment depth samples).
  - ADCP_PROCESSED: derived data per site/date; three CSV types per date: depth per bin, cross-sectional area per bin, and primary flow velocity per bin (across the cross-section from left to right).
  - Data linkage: samples_data.csv links sediment samples to corresponding ADCP data files; Q_transects.csv and Q_crosssections.csv describe transects and cross-sections with discharge calculations.

## Data structure and key files
- samples_data.csv
  - Header fields include: Sample_ID, Site_season, Sample_profile, Sample_depth_m, Sample_time, ADCP_file_prefix, ADCP_Ens_no, Latitude, Longitude, SSC_mgL, OC_wtprc, D50_um, D84_um, and particle size fractions.
- Q_transects.csv
  - Header fields include: Crosssection_ID, Magnetic_declination_degrees, Transect_ID, Date, Transect_filename, Start_Bank, End_Time, Total_Q_m3_per_s, Top_Q_m3_per_s, Bottom_Q_m3_per_s, Left_Q_m3_per_s, Right_Q_m3_per_s, Width_m, Total_Area_m2, Boat_Speed_m_per_s, Flow_Speed_m_per_s, Flow_Dir_degrees, Start_Time, End_Ens, End_Ens, Velocity_method, Depth_method.
- Q_crosssections.csv
  - Header fields include: Crosssection_ID, Date, Latitude, Longitude, Discharge_m3_per_s, Discharge_uncertainty, Transects_used.
- ADCP_RAW and ADCP_PROCESSED folders
  - ADCP_RAW: per-date site data with raw _ASC.TXT (hydroacoustic) and _GPS.TXT (GPS) files; descriptions reference ADCP_datastructure_description.pdf.
  - ADCP_PROCESSED: bin-based data for depth, cross-sectional area, and velocity; aligned with the same site/date naming convention as ADCP_RAW.

## Data quality, uncertainties, and processing notes
- Uncertainties and QC
  - Discharge reproducibility across transects typically better than 6%.
  - Grain-size distributions: typical uncertainty <10% per size bin; largely driven by subsampling of coarse particles.
  - SSC calculations assume complete transfer during filtration and drying; carbonate removal handled with procedural blanks (~<5% of sample carbon mass).
- Data processing workflow
  - Raw ADCP data processed in WinRiver II, then Velocity Mapping Toolbox, then MATLAB for gap filling and extrapolation.
  - Depth and cross-sectional area per bin, plus velocity per bin, form the primary processed outputs.
  - Cross-section discharge derived from multiple transects, with uncertainty estimates included.
- Metadata and data accessibility
  - Files use NaN to indicate missing data.
  - Data structure descriptions and file headers are documented (e.g., ADCP_datastructure.pdf).
  - Full dataset is linked to a published modeling study (Baronas et al., 2020, JGR: Earth Surface).

## Relevance for monitoring and policy decisions
- Enables assessment of suspended sediment flux and its drivers in two major rivers, informing riverine health and sediment management decisions.
- Provides a comprehensive, traceable data workflow from field collection to processed products, suitable for monitoring frameworks that require reproducible data pipelines and open data practices.
- The dataset highlights governance considerations for monitoring programs:
  - Metadata completeness and standardization are critical for data reuse and cross-site comparability.
  - Public sharing of underlying data is valuable but may require governance, licensing, and quality-control processes.
  - Inter-organizational data silos and data format transformation can impede timely use; a standardized data governance approach helps mitigate this.

## Notes for usage and potential challenges
- Use in policy and monitoring contexts requires attention to data provenance, processing steps, and uncertainty propagation.
- The dataset is well-documented with accompanying metadata, but users should verify alignment between raw and processed data via the linked CSV files and PDFs.
- When integrating into broader monitoring frameworks, consider establishing metadata standards, data access policies, and data governance mechanisms to address common barriers (data gaps, access delays, silos, and data-sharing constraints).