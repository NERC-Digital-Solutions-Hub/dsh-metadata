Supporting information for 'Cunliffe et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020.'

## Data access and citation
- Open Government Licence data available via DOI: 10.5285/1ec13364-cbc6-4ab5-a147-45a103853424
- Citation: Cunliffe, A. et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/1ec13364-cbc6-4ab5-a147-45a103853424

## Introduction
- Data collected following the protocol described in Cunliffe & Anderson (2019).
- Linked to Cunliffe et al. (In Review) on drone-derived canopy height predicting aboveground biomass.
- Organization: 38 drone survey directories, each named by a 15-digit survey_ID (date, investigator initials, site code).
- Contents per survey: a markers.csv, image subdirectory, and a metadata/biomass spreadsheet (drone_allometry_observations.csv) with units described in an accompanying txt file.

## Site and species selection
- Focus on low-stature, non-forest ecosystems (grasslands, shrublands, woody savannas); forests reserved for other methods.
- Species chosen for regional prevalence and accessibility to inform ongoing research; highly artificial vegetation excluded.
- Sampling during peak canopy cover to minimize phenophase effects, with acknowledgment of residual variation in some ecosystems.

## Aerial imaging surveys
- Drone surveys used two flight sets per site: nadir imagery (~5 mm per pixel at canopy top) and oblique imagery (~20° at ~3–4 m higher).
- Typical survey altitude ~20 m above canopy; 75% forward/side overlap; minimum 30 images per area.
- Wind conditions recorded prior to surveys.
- Photogrammetry relies on 13 ground control markers (GCPs), each 20 cm × 20 cm, geolocated with high-precision GNSS (typical ±0.015 m horizontal, ±0.03 m vertical).
- Ground control markers and imagery referenced to WGS84; GCP coordinates provided in meters in corresponding UTM zones; EPSG codes documented in the spreadsheet.
- Recommendation for higher-altitude surveys in taller, texturally complex vegetation to reduce parallax.
- Protocol optimized for plants up to ~3 m; future improvements anticipated with better camera geolocation/orientation reducing GCP needs.

## Vegetation harvests
- Harvest plots selected to represent canopy height range; aim for 90% of biomass and canopy from target taxa within each plot.
- Minimum harvest plot size: 0.5 m × 0.5 m to minimize co-registration errors.
- Corners geolocated with high-precision GNSS before harvest to ground level; biomass dried to constant weight (50–80°C).
- For largest taxa, field weights and subsamples dried to determine moisture content.
- Plot areas computed from corner coordinates unless a harvesting frame was used (frame area used to minimize GNSS-derived errors).

## Image-based modelling
- Photogrammetry performed in Agisoft PhotoScan (v1.4.3) with geotagged images and GCPs converted to UTM.
- Image quality checked (sharpness score ≥ 0.5).
- High-quality alignment with stringent settings (max 40,000 key points, 8,000 tie points, predefined pair preselection, adaptive model fitting disabled).
- Lens parameters configured (f, cx, cy, distortion terms, etc.); bundle adjustment optimized.
- Sparse point cloud reviewed; obviously erroneous tie points removed; 10 markers projected on 10 images per GCP for spatial constraint.
- 13 GCPs constrained the reconstruction; 3 markers used for accuracy assessment and deselected from final use.
- Multiview stereo produced dense point clouds; colors captured; mild depth filtering to preserve fine vegetation detail.
- Output dense clouds exported in laz format (with coordinates and RGB).

## Digital terrain models (DTMs)
- Canopy height modelling requires accurate DTMs.
- Terrain DTMs created by inverse distance weighting (IDW, power = 1) between GNSS corner observations of harvest plots.
- For discontinuous canopies, high-quality DTMs can be derived from photogrammetric point clouds; alternative sources include leaf-off UAV surveys, LiDAR, or walkover GNSS surveys.

## Analysis of dense point clouds
- Point clouds subset to harvest plot extents using GNSS corner coordinates.
- Noise points (e.g., posts, flags) removed where present (n ≈ 18 plots).
- Height above ground calculated per point relative to a surface interpolated between plot corners via IDW (power = 1).
- Negative heights coerced to zero.
- Grid at 0.01 m resolution; maximum height per grid cell computed.
- For empty cells, heights interpolated with IDW over a 7 × 7 neighbourhood; cells with no neighbors remained empty.
- Plot-level mean canopy height extracted from the grid of local maxima elevations.

## Coordinate systems and references
- Imagery geolocated in WGS84; ground control and plot coordinates provided in their respective UTM zones.
- EPSG codes and coordinate references documented within the dataset’s metadata/spreadsheet.

## Data structure and availability
- 38 survey directories; each includes:
  - a markers.csv (GCP locations)
  - a subdirectory of drone images
  - biomass and metadata in drone_allometry_observations.csv
  - units described in an accompanying txt file
- Data curated to support GIS analyses and map-based visualisations of canopy height and biomass relationships.