# Supporting information for 'Cunliffe et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020.'

- Data access and citation
  - Open Government Licence; dataset available at the provided DOI.
  - Please cite Cunliffe et al. (2020) in NERC Environmental Information Data Centre.

- Purpose and scope
  - Data collected to support allometric modelling of aboveground biomass from drone imagery.
  - Focus on non-forest, low-stature ecosystems (grasslands, open/closed shrublands, woody savannas).
  - Data linked to broader work on drone-derived canopy height predicting biomass; protocol described in accompanying publications.

- Data structure and organization
  - Data are organized per drone survey, identified by a 15-digit survey_ID (date, investigator initials, site code).
  - 38 survey directories, each containing:
    - a _markers.csv file with ground control marker data
    - a subdirectory with image files
  - Metadata and biomass data for each survey’s harvest plots are in drone_allometry_observations.csv; units documented in an accompanying text file.
  - Ground control markers: 13 markers per site, 20 cm x 20 cm, geolocated with GNSS;  typical horizontal/vertical precision provided.
  - Marker locations and survey metadata are provided in UTM coordinates; EPSG codes listed in the dataset spreadsheet.

- Site and species selection
  - Targeted 90% representation of biomass and canopy within plots for target taxa.
  - Minimum harvest plot size of 0.5 m x 0.5 m.
  - Seasonal peak canopy cover to minimise phenological variation.

- Aerial imaging surveys
  - Two drone flight sets per site: nadir (≈5 mm/pixel at canopy top) and oblique (~20°) at 3–4 m above canopy.
  - Typical survey altitude around 20 m; 75% forward/side overlap; ≥30 images per area.
  - Wind speeds recorded prior to surveys.
  - Photogrammetry requires adequate spatial control: 13 ground control markers (20 cm x 20 cm) deployed and precisely geolocated.
  - Future improvements anticipated to reduce ground control needs with better geolocation/orientation.

- Vegetation harvests
  - Harvest plots chosen to cover the natural canopy height range; focus on target taxa.
  - Independent GNSS corner geolocation before harvest.
  - Biomass dried to constant weight; moisture content subsampling for largest taxa.
  - Plot area calculated from corner coordinates unless a harvest frame was used.

- Image-based modelling workflow
  - SfM photogrammetry using Agisoft PhotoScan (v1.4.3).
  - Data georeferenced to UTM; image sharpness scores retained (≥ 0.5).
  - Camera alignment with high-quality settings; detailed camera parameters enabled (f, principal point, distortion terms, etc.).
  - Dense point clouds produced with multi-view stereopsis; colours captured; exported as laz.

- Digital terrain models (DTMs)
  - DTMs created from GNSS-based harvest corners via inverse distance weighting (power = 1).
  - DTMs essential for canopy height modelling; alternatives include leaf-off UAV surveys, LiDAR, or walkover GNSS methods.

- Analysis of dense point clouds
  - PDAL used to subset plots by GNSS corners.
  - Noise points (e.g., posts/flags) manually removed when visible.
  - Height above ground calculated relative to a DTW-interpolated surface; negative heights coerced to zero.
  - 0.01 m resolution grid; maximum height per grid cell computed; empty cells interpolated from neighboring cells using inverse distance weighting; local maxima used to derive plot-level mean canopy height.

- Data products and reuse
  - All data and methods described to support reproducibility and reuse for allometric analyses linking canopy height to biomass.
  - Units and methodological details provided in the accompanying txt file; coordinates provided in UTM with corresponding EPSG codes.

- Key considerations for analysts
  - Data are best suited for cross-site, non-forest biomass allometry using canopy-height proxies.
  - Ground control requirements and image geometry influence accuracy; higher vegetation or dense canopies may require adjustments to flight height and spacing.
  - The dataset supports modelling and validation of biomass estimates from drone-derived photogrammetry, with provenance and processing steps explicitly documented for reproducibility.