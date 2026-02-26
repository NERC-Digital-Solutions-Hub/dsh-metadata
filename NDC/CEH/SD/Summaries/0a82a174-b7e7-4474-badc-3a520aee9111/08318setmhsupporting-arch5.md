# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

- Overview of the dataset
  - Measurements of sediment elevation using Surface Elevation Table - Marker Horizon (SET-MH) technique and associated environmental metadata.
  - Spans UK coastline across 16 saltmarsh sites, with 48 SET plots and multiple marker horizons.
  - Total of 4104 elevation observations and four related CSV data files.
  - Managed by UK Centre for Ecology & Hydrology (UKCEH) with plans for analysis in R and documentation in future publications.

- Study area and temporal coverage
  - Sites range from Dornoch Firth (north) to Solent (south), including Dornoch Point, Crook of Baldoon, Caerlaverock, Campfield Marsh, Warton Marsh, Banks Marsh, Marshside, Stiffkey, Brancaster Beach, Blakeney, Bulldog Sands East/West, West Itchenor, Pilsey/Thorney Island, and Gutner Point.
  - Data collection occurred over multiple seasons: initial measurements in spring/summer 2023, followed by spring and autumn 2024.
  - UKCEH sites calibrated against LIDAR-derived elevations and GNSS measurements for site-specific elevation.

- Data collection methods and instrumentation
  - Primary method: SET-MH to monitor elevation dynamics; installation based on Lynch et al. (2015) protocol.
  - Installation details:
    - Three SET plots per marsh at similar elevation and mid-marsh plant communities; placement at least 5 m from creek edge.
    - rSET bases and marker horizons installed with standardized procedures; use of external quadrats with feldspar clay to create a consistent measurement surface.
    - Replication across sites: measurements from nine pins (1–9) per SET, across multiple orientations; marker horizons measured in triplicate on multiple plots.
  - Field measurements:
    - Elevation (mm) from rSET plots in collar orientations (1–8) or quadrants (N, E, S, W); depth of feldspar horizons measured with corer and ruler (to nearest 1 mm).
    - Metadata collected: latitude, longitude, rSET depth, LIDAR elevation (year specified), GNSS elevation, plant community (DAFOR/NVC), sediment observations, site features, weather conditions.
  - Sampling cadence and scope:
    - Annual spring measurements with planning for autumn monitoring where possible.
    - 48 SETs across 16 marshes; total of 4104 elevation observations.
  - Instruments and calibration:
    - Tools include dGPS, sediment corers, digital levels; installation torque aided by a petrol-driven postdriver.
    - Instruments calibrated to manufacturer specifications; data recorded with explicit units.

- Data processing and quality control
  - Data processing planned in R; a script will accompany future publications.
  - Elevation estimates derived from LIDAR data (DEFRA and Scottish remote sensing portal) using a representative 20 m diameter circle for each plot; year of LIDAR data recorded.
  - Quality control includes photographic documentation of each plot and linking of metadata, data, photos, and sites via unique ID codes.
  - Data are organized to ensure clear traceability from raw readings to analyzed data through four CSV files with consistent naming and codes.

- Data structure and metadata (four CSV files)
  - 08318setmhsitemetadata.csv: site-related metadata (location codes, site descriptions, SET IDs, coordinates, Depth_rSET, lidar timestamp and elevation, GNSS elevation, plant community codes, NVC, and observational metadata).
  - 08318setmhsamplingmetadata.csv: sampling-related metadata (row_number, metadata codes, timestamps, SET_ID, photo IDs, dominant/abundant/frequent/occasional/rare species codes with NVC, weather and site notes, installation notes).
  - 08318setdata.csv: sediment elevation measurements (row_number, metadata_code, location_code, plot_code, replicate_code, timestamps, orientation, height_pin_mm, notes).
  - 08318mhdata.csv: marker horizon measurements (row_number, metadata_code, location_code, plot_code, replicate_code, timestamp_TN, orientation, depth_to_horizon_m, notes).
  - Data fields and codes:
    - Location_code covers all study sites (e.g., RBMS, SWCB, CHGP, NNSK, NNBB, etc.).
    - Plot identifiers follow the format SETnumber_LocationCode (e.g., SET1_RBMS).
    - Orientation uses standard compass directions; replicate codes distinguish measurement repeats.
    - Species and vegetation codes are defined in accompanying tables (DAFOR, NVC, and Appendix 1).
  - Appendix 2 (locations of SET bases) and Appendix 1 (NVC saltmarsh communities) provide geospatial context and community classifications.

- Vegetation and site context (Appendices)
  - Appendix 1: Saltmarsh vegetation classifications (NVC/Saltmarsh communities) including SM13a, SM13c, SM13d, SM14a, SM16a and their sub-communities.
  - Appendix 2: Coordinates and site assignments for all SET bases across Ribble, Solway, Dornoch Firth, North Norfolk, Wash, and Solent regions, with explicit latitude/longitude data.

- References and contact
  - Method reference: Lynch, J. C., Hensel, P., & Cahoon, D. R. (2015). The Surface Elevation Table and Marker Horizon technique: A protocol for monitoring wetland elevation dynamics.
  - Contact for dataset information: enquiries@ceh.ac.uk; UKCEH offices listed for Bangor, Edinburgh, Lancaster, and Wallingford.

- Governance and forward notes for Data Stewards
  - Clear data provenance with unique IDs linking plots, metadata, and photos to enable traceability and reuse.
  - Metadata-rich structure supports discovery and interoperability, with explicit data collection methods, units, and measurement protocols.
  - Data processing and analysis plans documented (R scripts to accompany future publications) to support reproducibility.
  - Potential interoperability considerations due to site-specific codes and multiple datafiles; alignment with standard naming conventions and thorough documentation mitigate risks.