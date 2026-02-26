# Supporting information for 'Cunliffe et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020.'

## Aim
- Provide and describe a comprehensive dataset to support allometric modelling of above-ground biomass from drone-acquired photographs, including drone imagery, ground control marker coordinates, and biomass data from 36 sites collected between 2016 and 2020.
- Complement ongoing work on predicting biomass from drone-derived canopy height in non-forest ecosystems.

## Data access and citation
- Data available under the Open Government Licence.
- DOI: https://doi.org/10.5285/1ec13364-cbc6-4ab5-a147-45a103853424
- Citation: Cunliffe, A. et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/1ec13364-cbc6-4ab5-a147-45a103853424

## Data structure and contents
- Data organized per drone survey, identified by a 15-digit survey_ID (date YYYYMMDD + investigator initials + 3-character site code).
- 38 directories (survey flights) containing:
  - A markers.csv file
  - A subdirectory with image files
- Metadata and biomass data from harvest plots are in drone_allometry_observations.csv, with units in an accompanying txt file.
- Dataset focuses on 36 sites; 38 survey directories indicate multiple flights per site or overlapping surveys.

## Site and species selection
- Target ecosystems: low-stature, non-forest environments (grasslands, open/closed shrublands, woody savannas).
- Excluded highly artificial vegetation (e.g., managed hedges) and forests (reserved for active remote sensing methods in other literature).
- Sampling timed to seasonal peak canopy cover to minimise phenophase variability; plant development and allometry may still vary in water-limited systems.

## Aerial imaging surveys
- Surveys conducted with unmanned aerial systems (UAS):
  - Nadir imagery at ~5 mm per pixel for canopy top
  - Oblique imagery (~20° from nadir) from ~3–4 m higher
- Typical survey altitude: ~20 m above canopy
- Image overlap: ~75% forward and side overlap; at least 30 images per study area
- Environmental data: wind speeds recorded with handheld anemometers prior to surveys
- Ground control: 13 markers (20 cm × 20 cm) deployed per site, geolocated with high-precision GNSS (typical accuracy ±0.015 m horizontal, ±0.03 m vertical)
- Future directions: improved camera geolocation/orientation may reduce need for ground control in certain settings
- Survey data references: drone images geotagged in WGS84; ground control marker locations provided in meters with UTM zone specifics and EPSG codes in the spreadsheet

## Harvests (biomass sampling)
- Harvest plots sampled to represent the natural canopy height range; aim for plots where ~90% of biomass and canopy are from target taxa
- Minimum harvest plot size: 0.5 m × 0.5 m
- Corners geolocated with high-precision GNSS prior to harvest
- Biomass processed by air-drying to constant weight (50–80°C)
- For large taxa, field weighing followed by subsampling for moisture content
- Plot area calculated from corners unless a harvesting frame was used (frame area used to minimize GNSS-derived errors)

## Image-based modelling
- Processing workflow: structure-from-motion (SfM) photogrammetry using Agisoft PhotoScan (v1.4.3)
- Data imported: geotagged images and ground-control coordinates converted to UTM
- Image quality: sharpness score ≥ 0.5
- Camera alignment: high-quality settings, with specific point limits and preselection enabled
- Lens parameters and corrections enabled (f, principal point, distortion, tangential distortion, etc.)
- Bundle adjustment: optimized with provided marker constraints
- Marker strategy: 13 ground control points; ten markers constrain reconstruction; three markers reserved for independent accuracy assessment
- Output: dense point clouds exported as laz format with coordinates and RGB values

## Digital terrain models (DTMs)
- Canopy height modelling requires accurate DTMs
- DTMs created by interpolating GNSS corner coordinates of harvest plots using inverse distance weighting (power = 1)
- In dense or discontinuous canopies, DTMs can also be derived from the photogrammetric point cloud or alternative data sources (e.g., leaf-off UAV surveys, LiDAR, or walkover GNSS)

## Analysis of dense point clouds
- Point clouds subset to harvest plot extents using GNSS corners
- Noise removal: manually excluded any non-vegetation points (n = 18 plots where infrastructure appeared)
- Height-above-ground calculation:
  - Relative to a surface interpolated between plot corners (inverse distance weighting, power = 1)
  - Height above ground (HAG) computed per grid cell with 0.01 m resolution
  - Maximum height per cell extracted
  - For empty cells, heights interpolated using IDW from a 7 × 7 neighborhood; cells without neighbors remain empty
- Plot-level mean canopy height derived from grid of local maxima elevations

## Data quality and methodological notes
- Image sharpness and alignment quality controls described to ensure reliable reconstructions
- Ground control markers provide spatial constraints and accuracy assessment
- Authoritative references accompany methods for context and reproducibility

## Potential uses for environmental monitoring
- Standardised, repeatable biomass estimates from drone imagery across diverse non-forest ecosystems
- Supports validation and calibration of canopy height–biomass allometric relationships
- Can be integrated with other environmental datasets to enhance monitoring of ecosystem productivity and carbon dynamics

## Related references and context
- Protocols and prior SfM methodologies cited to support data collection and processing decisions
- Context for ongoing work on drone-derived canopy height and biomass in non-forest ecosystems
- Acknowledgement of alternative remote-sensing approaches for forest biomass and higher-structure vegetation

## How this aligns with the Analysts Monitoring the Environment archetype
- Data verification and quality assurance through standardized protocols (survey design, GNSS accuracy, image sharpness thresholds)
- Systematic data transformation and analysis to produce outputs (biomass estimates and canopy-height relationships)
- Clear data products and citations enabling reuse, with datasets stored under a formal licence and accessible via DOIs
- Emphasis on data accessibility and interoperability (survey IDs, directory structure, and accompanying spreadsheets)
- Consideration of data reuse and value extension through integration with related datasets and ongoing research outputs