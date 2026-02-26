# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

- The dataset comprises sediment elevation measurements using the Surface Elevation Table - Marker Horizon (SET-MH) method, plus environmental metadata (soil composition, plant cover, installation details such as rSET depth).
- Collected along the UK coastline across 16 saltmarsh sites, with unique plot and SET identifiers linked to metadata and data files.
- Data collection occurred in multiple seasons: initial measurements spring/summer 2023 and follow-up in spring and autumn 2024.
- Analysis and processing planned in R; quality control includes photographs and metadata checks; outputs linked via unique IDs.

## Study area and sampling design

- Geographic coverage: UKCEH sites from Dornoch Point (north Scotland) to the South Coast of England, including Dornoch Firth, Solway, Ribble, North Norfolk, Wash, and Solent regions.
- Sites (examples): Dornoch Point, Crook of Baldoon, Caerlaverock, Campfield Marsh, Warton Marsh, Banks Marsh, Marshside, Stiffkey, Brancaster, Blakeney, Bulldog Sands East/West, West Itchenor, Pilsey/Thorney Island, Gutner Point.
- Plot and replication:
  - Three SET plots per marsh at similar elevation with mid-marsh plant communities.
  - SETs positioned across marsh (5 m from creek edge); four peripheral orientations (N, E, S, W) around each SET; nine measurement pins per orientation (or 3 cores for horizons).
  - Replication across multiple marshes to capture variability.
- Monitoring regime: initial spring/summer 2023 measurements; annual spring measurements; autumn monitoring when possible.

## Data collected and structure

- Primary data: sediment elevation measurements (mm) from rSET plots; depth of feldspar horizons (marker horizons) from cores.
- Environmental and installation metadata:
  - Location coordinates (latitude, longitude), depth of rSET, LIDAR-based elevation, GNSS elevation, plant community codes (DAFOR and NVC), sediment observations, site weather and conditions.
  - Installation details include rSET bases, calibration notes, and plotting layout (quadrat size, external edge, replication coordinates).
- Data units and formats: measurements in millimetres; metadata and measurements linked by unique IDs and codes.

## Data collection methodology and instrumentation

- Installation methodology:
  - rSET bases and marker horizons installed per Lynch et al. (2015) protocol; components designed/adjusted by UKCEH workshop; sites chosen to include three SET plots per marsh with mid-marsh communities.
  - Replicated placements at 1.5 m N, E, S, W of SET center; feldspar clay layer applied and lightly set to prevent dispersal.
- Data collection details:
  - Elevation readings from SETs (using collar orientations 1-8 or quadrants N/E/S/W) via 9 pins per SET/reading sequence.
  - Depths of at least three feldspar horizons per core (three measurements per core, mm resolution).
  - Metadata fields include precise geolocation, rSET depth, LIDAR-derived elevations, GNSS elevations, and vegetation classification.
- Periodicity and samples:
  - Annual spring measurements; potential autumn monitoring when feasible.
  - Total coverage: 48 SETs across 16 marshes, with 4104 elevation observations.
- Instrumentation and calibration:
  - Tools: dGPS, sediment corers, digital levels; calibration per manufacturer specs; post installation measures to reduce disturbance.
  - Data processing planned in R; LIDAR elevations calculated in QGIS; elevation year recorded.

## Data processing, quality control, and provenance

- Quality assurance:
  - Photographs taken for each plot; metadata and data reformatted and linked by unique IDs.
  - Data checked for consistency and recorded with clear units and descriptions.
- Provenance and reproducibility:
  - Data linked across four CSV files via unique IDs; cross-referenced with site and plot metadata.
  - LIDAR elevations sourced from DEFRA/Scottish remote sensing portals; GNSS elevations captured on-site.
- Analysis guidance:
  - Future analyses to be performed in R with provided scripts; compatibility with GIS tools (QGIS) for elevation estimation.

## Dataset files and data dictionaries

- 08318setmhsitemetadata.csv
  - Site-related metadata: Location_code, Location, SET_ID, Latitude, Longitude, Depth_rSET, timestamp_lidar, LIDAR_elevation, timestamp_elevation, Elevation_m, GCS_notes, Instrument, Comment, etc.
- 08318setmhsamplingmetadata.csv
  - Sampling metadata with structure: row_number, metadata_code, timestamp_TN, SET_ID, photo_id, dominant/abundant/frequent/occasional/rare species codes, NVC, notes_conditions, notes_sediment, notes_site, notes_installation.
  - Species codes include Ap, At, Ca, Fr, Gm, Hp, Lv, Plm, Pm, Se, Spartina, Tm, Sm, Sum, Sp, Tr; NVC codes as applicable.
- 08318setdata.csv
  - Sediment elevation readings: row_number, metadata_code, location_code, plot_code (SETnumber_LocationCode), replicate_code, timestamp_T0, timestamp_TN, orientation_num, orientation, height_pin_mm.
- 08318mhdata.csv
  - Marker horizon measurements: row_number, metadata_code, location_code, plot_code, replicate_code, timestamp_TN, orientation, depth_to_horizon_m, notes.
- Data structure references:
  - Tables outlining location codes, plot identifiers, replication schemes, time stamps, and measurement orientation.
  - Tables include descriptions of variables, units, and permissible values.

## Appendices and references

- Appendix 1: NVC Saltmarsh Community Floristic Tables
  - Communities include SM13a/SM13c/SM13d (Puccinellia maritima), SM14a/SM14c (Atriplex portulacoides), SM16a (Festuca rubra) and associated sub-communities.
- Appendix 2: Locations of SET bases
  - Detailed site-by-site coordinates for SET bases (RBMS, RBBS, RBWM; SWCF, SWCB, SWCV; DFDP; WSBW, WSBE, WSWM; NNSK, NNBB, NNBN; CHGP, CHWI, CHPS) with estuary, marsh, latitude, and longitude values.
- References:
  - Lynch, J. C., Hensel, P., & Cahoon, D. R. (2015). The surface elevation table and marker horizon technique: A protocol for monitoring wetland elevation dynamics. Natural Resource Report NPS/NCBN/NRR.

## Access and contact

- Enquiries: enquiries@ceh.ac.uk
- UK Centre for Ecology & Hydrology locations (Bangor, Edinburgh, Lancaster, Wallingford) and general contact information.