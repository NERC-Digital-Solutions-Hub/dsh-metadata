# Dataset: Flow velocity, discharge, and suspended sediment compositions of the Irrawaddy and Salween Rivers (2017-2019)

## Overview
- A comprehensive dataset of flow velocity, discharge, and suspended sediment characteristics for the Irrawaddy and Salween rivers collected across two monsoon seasons (Aug 2017, Aug 2018) and two dry seasons (Feb 2018, May 2019).
- Data collected upstream of delta distributary networks using a Teledyne Rio Grande II ADCP on a moving boat, with supporting suspended sediment samples and laboratory analyses.
- Includes raw and processed data, extensive metadata, and documentation to enable reuse and replication of analyses (notably used in Baronas et al., 2020).

## Data Content
- Flow velocity data
  - Collected with ADCP across multiple transects per sampling date; mean cross-sections (MCS) created perpendicular to the river channel.
  - Processing steps include gap interpolation, outlier removal, and extrapolation to the surface and bottom; MATLAB and Velocity Mapping Toolbox used.
  - Cross-section and discharge information derived from transects; additional fields for discharge components (Top/Bottom/Left/Right/Total).
- Sediment sampling and analysis
  - Depth profiles of suspended sediments at multiple depths; surface samples in February 2018 only.
  - Sampling method designed for near-isokinetic conditions; samples processed via filtration, freezing, and laboratory analyses.
  - Particle size distributions (0.35–2000 μm) measured with Malvern Mastersizer 2000; organic carbon (OC) content measured by EA-IRMS after carbonate removal; typical uncertainties and procedural blanks reported.
- Data products and structure
  - ADCP_RAW: raw hydroacoustic data (files ending in _ASC.TXT and _GPS.TXT) and sediment sampling data folders (Sed_samples).
  - ADCP_PROCESSED: bin- or cell-based data across cross-sections, with separate files for water depth, cross-sectional area, and primary flow velocity per bin; data organized by site/date.
  - Metadata files describing data relationships and timing:
    - samples_data.csv: Sample_ID, Site_season, Sample_profile, depth, time, coordinates, SSC_mgL, OC_wtprc, D50, D84, and particle-size fractions.
    - Q_transects.csv: transect-level metadata (dates, start/end times, discharge components, vessel and instrument settings, transect IDs, cross-section references, etc.).
    - Q_crosssections.csv: cross-section-level discharge and location data (Discharge_m3_per_s, Discharge_uncertainty, Transects_used, coordinates, etc.).
- Data contents and formats
  - Data stored as plain text CSV files; NaN denotes missing data.
  - Detailed data structures documented in ADCP_datastructure.pdf and ADCP_datastructure_description.pdf.
  - Units and column headers standardized across files; files within ADCP_PROCESSED contain depth bins (rows) and across-channel positions (columns).

## Data Structure and Access
- Directory organization
  - ADCP_RAW: per-date/site folders; within each, Q_transects and Sed_samples subfolders; Sed_samples may be absent on some dates.
  - ADCP_PROCESSED: per-date/site CSV triplets for depth, area, and velocity per cross-section/date.
- Data types and file naming
  - _ASC.TXT: hydroacoustic data with instrument settings.
  - _GPS.TXT: external GPS data in NMEA 0183 format.
  - Processed files reflect the same site/date naming convention as raw data.
- Documentation and references
  - Primary methodological framework described in Baronas et al. (2020) JGR-Earth Surface.
  - Additional documentation referenced for internal data structure (ADCP_datastructure.pdf, ADCP_datastructure_description.pdf).

## Data Processing and Quality Assurance
- Processing workflow
  - Raw ADCP data processed in WinRiver II; then velocity fields generated with Velocity Mapping Toolbox.
  - Cross-sections aligned to channel perpendiculars; MCS constructed; gaps interpolated; outliers removed.
  - Data further processed in MATLAB (2019b) to fill gaps and extrapolate to surface/top and bottom/below sidelobe interference.
- Data quality indicators
  - Discharge reproducibility across transects typically better than 6%.
  - Uncertainty estimates provided for cross-section discharges (Discharge_uncertainty = 2 standard deviations of used transects).
  - Sediment measurements include precision notes for OC and grain-size measurements (typical uncertainties <10% for size bins; procedural blanks accounted for in OC).
- Provenance and traceability
  - Data derivation explicitly linked to the Baronas et al. (2020) publication.
  - Clear linkage between samples_data.csv and corresponding raw ADCP files via ADCP_Ens_no and Transect IDs.

## Metadata and Documentation
- Sample metadata
  - Sample_ID, Site_season, Sample_profile, Sample_depth_m, Sample_time, coordinates, SSC_mgL, OC_wtprc, D50_um, D84_um, and size-fraction markers.
- Transect and cross-section metadata
  - Crosssection_ID, Date, Latitude/Longitude, Discharge_m3_per_s, Uncertainty, Transects_used, and related timing and geometry fields.
  - Instrument settings (Velocity_method, Depth_method) indicating whether external GPS or ADCP-based depth detection was used.
- Data quality and structure notes
  - NaN used for missing data; detailed file structure described in accompanying PDFs.
- Governance and discoverability
  - Documentation enables reproducibility and reuse; data are designed for discovery and cross-dataset integration within large river sediment transport studies.

## Provenance and Citation
- Usage note: When using this dataset, cite Baronas, J. J., Tipper, E. T., Bickle, M. J., Hilton, R. G., Stevenson, E. I., Hackney, C. R., et al. (2020). Integrating suspended sediment flux in large alluvial river channels: Application of a synoptic Rouse-based model to the Irrawaddy and Salween rivers. Journal of Geophysical Research: Earth Surface.

## File Organization, Access, and Reuse
- Access model
  - Raw data (ADCP_RAW) and processed data (ADCP_PROCESSED) separated to preserve provenance and reusability.
  - Crosswalks between sample events, ADCP transects, and cross-sections carefully documented via samples_data.csv, Q_transects.csv, and Q_crosssections.csv.
- Reuse considerations
  - Data are complex and large; require careful integration across multiple CSVs and alignment with the published methodology.
  - Metadata completeness and documentation are essential for discoverability and interoperability with other river hydrology and sediment transport datasets.

## Challenges and Considerations for Data Stewards
- Incomplete picture of user needs and priorities for downstream data consumers.
- Timely acquisition of data from field campaigns; consistent metadata capture.
- Encouraging data creators to adhere to metadata and documentation standards (e.g., consistent site naming, date formatting, and cross-referencing IDs).
- Interoperability across multiple systems and formats; handling large, multi-file datasets.
- Managing legacy data and ensuring interoperability with newer data infrastructures.
- Ensuring update mechanisms and versioning for processed data and documentation.