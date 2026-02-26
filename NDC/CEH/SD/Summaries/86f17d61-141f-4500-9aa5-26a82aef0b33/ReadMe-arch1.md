# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

- The dataset combines flow velocity, discharge, and suspended sediment (SS) composition data for the Irrawaddy and Salween rivers, collected during 2017–2019. It is intended to support analyses of suspended sediment flux using a synoptic Rouse-based model (Baronas et al., 2020).

## What the dataset includes

- Flow velocity measurements across river cross-sections using Acoustic Doppler Current Profiler (ADCP) and corresponding SS samples.
- SS depth profiles and particle-size distributions, plus organic carbon content for sampled sediments.
- Metadata linking ADCP data, transects, cross-sections, and sediment samples, enabling construction of cross-sectional flux estimates.

## Data collection and sampling design

- Locations and timing:
  - Two monsoon seasons: August 2017 and August 2018.
  - Two dry seasons: February 2018 and May 2019.
  - Sampling upstream of delta distributary networks for both rivers.
- ADCP data collection:
  - Teledyne Rio Grande II 1200 kHz ADCP mounted on a moving boat, with the transducer 40–60 cm below the surface.
  - Transects perpendicular to flow to capture lateral velocity structure; GPS used for positioning.
  - Typical discharge reproducibility better than 6%.
- Sediment sampling:
  - Depth profiles collected in August 2017, August 2018, and May 2019; surface-only samples in February 2018.
  - Sediments collected with a modified Van Dorn-style sampler, drift-boat sampling for isokinetic conditions.
  - Sediment processing included drying, filtration (0.2 μm), and storage in dark conditions; SS concentration calculated from dried mass over original water mass.
  - Particle-size distributions measured with Malvern Mastersizer 2000; size range 0.35–2000 μm with ~10–20% obscuration targets; repeat measurements with ~<10% uncertainty.
  - Organic carbon (%wt) measured after carbonate removal via HCl; analysis by EA-IRMS with calibration standards; procedural blanks accounted for (<5% of sample carbon).
- Data notes:
  - Some dates (XXX17_Aug_XXX and XXX18_Feb_XXX) lack Sed_samples data.

## Data structure and organization

- Folder structure:
  - ADCP_RAW: raw hydroacoustic data and accompanying GPS data, organized by date/site. Subfolders include Q_transects (cross-channel transects), Sed_samples (sediment depth samples) when available.
  - ADCP_PROCESSED: processed data derived from raw ADCP and sediment data, organized by date/site. Three CSV types per site-date: water depth per bin, cross-sectional area per bin, and velocity per bin (cm/s).
- Core data links:
  - samples_data.csv: metadata for each sediment sample (Sample_ID, Site_season, Sample_profile, depth, time, SS concentration, OC content, particle sizes D50/D84, etc.), plus ADCP file references and spatial coordinates.
  - Q_transects.csv: per-transect details (Crosssection_ID, Date, Transect_ID, discharge components, cross-section geometry, velocities, instrument settings, start/end times, etc.).
  - Q_crosssections.csv: per-cross-section discharge estimates and uncertainties, with coordinates and transect references.
- Data dictionaries and structure:
  - ADCP_datastructure.pdf documents the data layout for _ASC.TXT and _GPS.TXT files.
  - NaN indicates missing data in all files; headers and column structures are specified in the associated PDFs.

## Key data fields (highlights)

- Sediment samples (samples_data.csv):
  - Sample_ID, Site_season, Sample_profile, Sample_depth_m, SSC_mgL, OC_wtprc, D50_um, D84_um, ParticleSize_fraction_under_XXX_um
  - Spatial coordinates (Latitude, Longitude) and ADCP associations (ADCP_file_prefix, ADCP_Ens_no)
- Transects (Q_transects.csv):
  - Crosssection_ID, Date, Transect_ID, Total_Q_m3_per_s, Meas_Q_m3_per_s, Top_Q_m3_per_s, Bottom_Q_m3_per_s, Left_Q_m3_per_s, Right_Q_m3_per_s, Width_m, Total_Area_m2, Boat_Speed_m_per_s, Flow_Speed_m_per_s, Flow_Dir_degrees, Start_Time, End_Time, Duration_sec, Velocity_method, Depth_method
  - Extrapolation components and uncertainties (e.g., Delta_Q_prc, Left_Dist_m, Right_Dist_m)
- Cross-sections (Q_crosssections.csv):
  - Crosssection_ID, Date, Latitude, Longitude, Discharge_m3_per_s, Discharge_uncertainty, Transects_used

## Data processing and quality control

- Processing workflow:
  - Raw ADCP data processed with WinRiver II; export to Velocity Mapping Toolbox; MATLAB 2019b used to interpolate gaps, remove outliers, and extrapolate to surfaces/bottom (handled with inpaintnans).
  - MCS (mean cross-section) created for each sampling date to obtain a perpendicular cross-section and average velocity field across the channel.
  - Processed data stored in ADCP_PROCESSED as bin-based data: depth, cross-sectional area, and primary velocity per bin.
- Sediment processing:
  - Isokinetic sampling during drifting flow; hydrodynamic conditions recorded with ADCP and sediment depths.
  - Particle size distributions measured in 20 bins (0.35–2000 μm) with 3–5 repeats per sample.
  - OC measured after carbonate removal; precision ~0.05% (relative to measured OC), with calibration standards and blanks accounted for.

## Usage and citation

- Data accompany the publication: Baronas, J. J., Tipper, E. T., Bickle, M. J., Hilton, R. G., Stevenson, E. I., Hackney, C. R., et al. (2020). Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers. Journal of Geophysical Research: Earth Surface.
- Users should cite Baronas et al. (2020) when employing the dataset in analyses or publications.

## Practical notes and caveats

- The dataset is designed for cross-sectional flux analyses and model validation; cross-referencing between ADCP_RAW, ADCP_PROCESSED, and the metadata CSVs is required to reconstruct specific transects and sediment samples.
- Some dates lack sediment-depth samples, which may limit certain downstream analyses for those dates.
- Data are organized with explicit metadata to facilitate discovery and reuse, but researchers should consult the provided PDFs (ADCP_datastructure.pdf, related documentation) to ensure correct interpretation of file formats and column headers.