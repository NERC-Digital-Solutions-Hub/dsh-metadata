# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

- Overview
  - A historical data collection and analysis of bumblebee wing morphology to assess environmental stress signals across Britain, spanning the 19th to 21st centuries.
  - Data drawn from five UK museums and focus on five Bombus species: B. hortorum, B. muscorum, B. lapidarius, B. pascuorum, and B. sylvarum.
  - Wings analyzed via high-resolution images, with wing morphology quantified through landmark-based geometry to derive fluctuating asymmetry (FA).

- Data collection and scope
  - Specimens photographed with label data from Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
  - Labels transcribed; where possible, locations geocoded to latitude/longitude using Google Maps Geocoding API.
  - For each specimen, 13 landmarks plotted on each of the left and right forewings; only specimens with both wings landmarked used in downstream analyses.
  - Wings aligned (Procrustes) to a common scale/position/orientation; FA quantified as Procrustes distance between left and right wings using the geomorph package in R.

- Data processing and measurement
  - Landmarking: dual-collector setup with replication to assess repeatability.
  - Procrustes alignment to control for scale/rotation/translation; FA computed as the difference in wing shape between wings.
  - Orientation data captured for each wing (left/right) and whether the wing was upside down; includes ImageID, Wing, Species, Sex/Caste, Orientation, Flipped status.
  - Data entries include a broad set of associated metadata, including collection decade, location, latitude/longitude, and climate-related variables.

- Quality control and filtering
  - Repeatability: subset (20 B. hortorum drones) landmarked thrice by two collectors; mixed-effects models show no significant inter-collector or repeated-measure differences.
  - Measurement error: wings landmarked twice per specimen; Procrustes ANOVA shows no significant error.
  - Filtering criteria to retain high-quality wings: retained specimens within the 75th percentile for wing shape and within the 75th percentile plus IQR for wing angle differences.
  - Quality-controlled dataset variants exist, with more stringent filtering in updated files (e.g., 20210409_updated_dataset.csv).

- Data files and schema
  - FA_data_with_metadata_3_3.csv: FA values (ProcD) for five species, plus fields such as ImageID, left/right wing angles (L_wing_angle, R_wing_angle), Angle.diff, project ID, species, sex, caste, decade, year/month collected, UK Met Office climate region, location, lat/long, geotag accuracy, ITD, climate variables (temp_ranks and rainfall), and other metadata.
  - 20210409_updated_dataset.csv: QC-filtered FA data with extended climate variables (e.g., raindays, maximum/mean/min temperatures by season and year), queen Type (early/late cohort) for queens, and the same core columns as above.
  - Subsampled_FA_Data_0_1_v3.csv: QC-filtered data with subsampling to ensure >20 specimens per year 1900–2000; complete location/date/caste data; exclusions for certain queen eclosion timing.
  - 01_Filtering_specimens_generating_FA.R and 03_Repeatability_analysis.R: R scripts documenting quality control and repeatability analyses.
  - Key data states: some cells may contain NA; orientation and climate metadata are included where available; geotagging accuracy included for spatial reliability.

- Access, provenance, and governance
  - Data are derived from museum collections and enhanced with geospatial and climate context; provenance is preserved via project IDs and specimen ImageIDs.
  - Multiple data versions exist reflecting quality control status (unfiltered vs. QC-filtered); QC workflow is explicitly documented through associated R scripts.
  - Climate data linked to UK Met Office historic records and supplied as derived fields within the updated datasets.

- Limitations and considerations
  - Data span extensive historical range; sampling density and geographic coverage may be uneven across decades.
  - Some environmental and metadata fields are incomplete (NA in some cells); geotagging accuracy varies.
  - Measurements rely on manual landmarking and Procrustes-based shape analysis, with documented QC to mitigate measurement error.

- Implications for data strategy and reuse
  - Demonstrates end-to-end data lifecycle: from specimen imaging and landmark-based morphometrics to curated, QC-filtered datasets with rich metadata and climate context.
  - Highlights the importance of reproducible workflows (R scripts) and versioned data files for traceability and auditability.
  - Provides a model for long-term, cross-institutional data aggregation, geospatial framing, and integration of environmental context to support large-scale, time-series analyses of biological responses to stress.
  - Useful for data leaders designing data governance around historical biological collections: emphasis on provenance, metadata completeness, quality control, and clear data versioning to enable future reuse.