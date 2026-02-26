# Supporting information for 'Cunliffe et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020.'

- Data access and citation
  - Data are available under the Open Government Licence at the provided DOI link.
  - Citation: Cunliffe, A. et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020. NERC Environmental Information Data Centre. (Dataset).
  - Dataset organized by survey, with a 15-digit survey_ID linking image data, ground control markers, and biomass observations.

- Introduction
  - Data collected following the protocol described in Cunliffe & Anderson (2019) and linked to ongoing Work on drone-derived biomass prediction.
  - For each drone survey, there are 38 directories containing aerial images and a markers file; metadata and biomass data are in drone_allometry_observations.csv, with units in an accompanying text file.

- Site and species selection
  - Focus on low-stature, non-forest ecosystems (grasslands, open/closed shrublands, woody savannas) to complement forest biomass work in literature.
  - Regionally widespread, accessible species; excluded highly artificial vegetation (e.g., managed hedges).
  - Sampling during peak canopy cover to minimise phenophase differences; allometric relationships may vary with more water-limited ecosystems.
  - Protocol described in Cunliffe & Anderson (2019).

- Aerial imaging surveys
  - Drones conducted two flight sets per site: nadir imagery (~5 mm per pixel at canopy top) and oblique imagery (~20°) from ~3–4 m higher.
  - Typical survey altitude ~20 m; both flights achieved ~75% forward/side overlap, capturing at least 30 images per area.
  - Wind speeds recorded prior to surveys.
  - Photogrammetric accuracy supported by 13 ground control markers per site (markers 20 cm x 20 cm) with high-precision GNSS coordinates (±0.015 m horizontal, ±0.03 m vertical).
  - Ground control expectations and future improvements noted (reduced need for markers with better camera geolocation/orientation).

- Vegetation harvests
  - Harvest plots selected to represent the natural canopy height range; aim for plots at least 0.5 m x 0.5 m.
  - Plot corners GNSS-located before harvest; biomass dried to constant weight (50–80°C); moisture content measured for some large taxa.
  - Plot areas calculated from corner coordinates unless a frame was used during harvesting.

- Image-based modelling
  - SfM photogrammetry workflow using Agisoft PhotoScan (v1.4.3); data converted to UTM coordinates.
  - Image quality controlled (sharpness score ≥ 0.5); high-quality alignment with specified parameters; dense point clouds exported in laz format with RGB attributes.
  - Camera parameters enabled (f, cx, cy, distortion terms, etc.); marker locations constrained the reconstruction; accuracy assessed using dedicated markers.
  - Sparse point clouds reviewed and cleaned; markers used for spatial constraint and for independent accuracy evaluation.

- Digital terrain models
  - DTMs created to support canopy height derivation; terrain models interpolated with inverse distance weighting (power term = 1) using GNSS harvest plot corners.
  - Alternatives suggested for high topographic variation (e.g., post-harvest UAV surveys, LiDAR, or walkover GNSS).

- Analysis of dense point clouds
  - PDAL used to analyze plot point clouds; non-vegetation points removed where obvious.
  - Height above ground computed relative to a surface interpolated from plot corners; negative heights coerced to zero.
  - 0.01 m resolution grid used to compute maximum height per cell; gaps interpolated with inverse distance weighting across a 7x7 cell neighborhood; remaining cells left empty if no neighbors.
  - Plot-level mean canopy height derived from grid of local maximum elevations.

- References
  - Includes foundational methodological and related works on UAV photogrammetry, accuracy considerations, biomass estimation, and related photogrammetric and remote sensing practices.