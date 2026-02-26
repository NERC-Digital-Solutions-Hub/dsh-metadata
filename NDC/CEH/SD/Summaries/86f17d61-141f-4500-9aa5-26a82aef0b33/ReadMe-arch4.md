# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

## Overview
- Multiyear dataset of flow velocity, river discharge, and suspended sediment composition for the Irrawaddy and Salween rivers, collected 2017–2019.
- Data support integration of suspended sediment flux modeling; tied to Baronas et al. (2020) JGR: Earth Surface.
- Measurements taken upstream of delta distributary networks; includes both hydrodynamic and sediment chemical/size properties.

## Data collection methods

- Flow velocity
  - ADCP measurements using Teledyne Rio Grande II 1200 kHz, boat-mounted, down-facing, transects across the channel.
  - Sampling dates: August 2017, August 2018 (monsoon seasons); February 2018, May 2019 (dry seasons).
  - GPS positioning with accuracy <5 m; typically 1–5 transects per site; discharge reproducibility better than 6%.
  - Processing: WinRiver II initial processing; Velocity Mapping Toolbox; MATLAB (2019b) for gap filling, outlier removal, and extrapolation to surface and bottom.

- Sediment sampling
  - Depth profiles of suspended sediments collected August 2017, August 2018, May 2019; surface-only samples in February 2018.
  - Depth sampling with a modified 8.5 L Van Dorn depth sampler; drifting boat sampling to approximate isokinetic conditions.
  - Samples filtered (0.2 μm PES), dried, and weighed to determine suspended sediment concentration (SSC).
  - Particle size distribution measured with Malvern Mastersizer 2000 (0.35–2000 μm, 20-bin resolution); repeat measurements with ~10% overall uncertainty.
  - Organic carbon (wt%) measured after carbonate removal via HCl; EA-IRMS analysis with calibration standards; precision ~0.05%.

- Data organization and cross-referencing
  - ADCP_RAW contains raw hydroacoustic and GPS data; ADCP_PROCESSED contains derived, bin-based cross-sectional data.
  - Samples and transects linked through sample metadata files (samples_data.csv, Q_transects.csv, Q_crosssections.csv).

## Data processing and modeling steps

- Hydrodynamic data
  - Initial ADCP data processed to generate mean cross-sections per sampling date, perpendicular to channel axis.
  - Gap interpolation and outlier removal; extrapolation to surface and bottom to complete profiles.

- Sediment data
  - Mass-based SSC calculations from dried sediment to the pre-filter water mass.
  - Particle size distributions derived from laser diffraction (3–5 repeats per sample).
  - Organic carbon corrected for carbonate removal; QA/QC against blanks and standards.

## Data structure and files

- ADCP_RAW
  - Subfolders per date/site; includes Q_transects (transect-level velocity/discharge data) and Sed_samples (drifting sediment samples).
  - Files titled with _ASC.TXT (hydroacoustic data) and _GPS.TXT (GPS data) per standard descriptions; data tab-delimited.
  - Metadata and file structure described in ADCP_datastructure_description.pdf.

- ADCP_PROCESSED
  - Three CSV files per site/date:
    - Water depth per bin (m)
    - Cross-sectional area per bin (m2)
    - Primary flow velocity per bin (cm/s)
  - Data organized as cross-sections across the channel, with rows representing depth and columns across the channel width.
  - Consistent naming with ADCP_RAW folders.

- samples_data.csv
  - Header fields include: Sample_ID, Site_season, Sample_profile, Sample_depth_m, Sample_time, ADCP_file_prefix, ADCP_Ens_no, Latitude, Longitude, SSC_mgL, OC_wtprc, D50_um, D84_um, and ParticleSize_fraction_under_XXX_um.

- Q_transects.csv
  - Header fields include: Crosssection_ID, Magnetic_declination_degrees, Transect_ID, Date, Transect_filename, Start_Bank, Ens_count, Start_Time, Total_Q_m3_per_s, Delta_Q_prc, Top_Q_m3_per_s, Meas_Q_m3_per_s, Bottom_Q_m3_per_s, Left_Q_m3_per_s, Left_Dist_m, Right_Q_m3_per_s, Right_Dist_m, Width_m, Total_Area_m2, Boat_Speed_m_per_s, Flow_Speed_m_per_s, Flow_Dir_degrees, End_Time, Duration_sec, Start_Ens, End_Ens, Velocity_method, Depth_method.

- Q_crosssections.csv
  - Header fields include: Crosssection_ID, Date, Latitude, Longitude, Discharge_m3_per_s, Discharge_uncertainty, Transects_used.

- Data conventions
  - NaN indicates missing data across all files.
  - Cross-referenced by site/date via folder naming conventions.

## Variables, units, and data quality

- Velocity, discharge, and cross-sectional measurements
  - Discharge: m3/s; cross-sectional areas: m2; velocities: cm/s or m/s depending on file.
  - Uncertainties provided for cross-sections; top/bottom/edge extrapolations documented.

- Sediment properties
  - SSC: mg/L; OC: wt%; particle sizes: D50 and D84 in μm; distribution fractions per size bin.

- Data quality notes
  - ADCP-derived discharges include extrapolations to unmeasured portions of the water column.
  - Sediment measurements include small sample uncertainties (~0.05% for OC, ~10% for grain-size bins).
  - Metadata files enable traceability between transmitted ADCP data, samples, and processed outputs.

## Access, citation, and usage notes

- Publication basis
  - Data underpin the synoptic sediment flux model described in Baronas et al., 2020 (JGR: Earth Surface).
- Citation
  - When using the dataset, cite Baronas, J. J., et al. (2020) Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers.

## Practical implications for data leadership

- Data system view
  - Rich, multi-faceted dataset spanning hydrodynamics and sedimentology with clear cross-references across raw and processed files.
- Discoverability and standards
  - Structured folder conventions, comprehensive metadata, and explicit file headers support discoverability; reliance on external PDFs for schema descriptions (ADCP_datastructure_description.pdf) suggests need for centralized metadata standardization.
- Gaps and challenges
  - Some sampling dates lack Sed_samples data; extrapolated discharge components introduce modeled elements with documented uncertainty.
  - Potential for broader data standardization across platforms to enhance reuse and cross-site comparability.
- Opportunities for collaboration
  - The dataset aligns with broader freshwater sediment flux research and could benefit from community-wide data-sharing practices and standardized metadata schemas.