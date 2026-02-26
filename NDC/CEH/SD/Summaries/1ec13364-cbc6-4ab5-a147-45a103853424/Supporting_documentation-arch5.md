# Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020.

## Data access and citation
- Data are available under the Open Government Licence.
- Access/DOI: https://doi.org/10.5285/1ec13364-cbc6-4ab5-a147-45a103853424
- Citation: Cunliffe, A. et al. (2020). Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/1ec13364-cbc6-4ab5-a147-45a103853424

## Data organization and contents
- Data are organized by each drone survey into 38 directories, each containing:
  - A markers.csv file with ground control marker coordinates.
  - A subdirectory of image files.
- Metadata and biomass data for harvest plots within each drone survey are in drone_allometry_observations.csv.
- Units for data are provided in an accompanying txt file.
- Survey identifiers (survey_ID) link image directories to the corresponding data spreadsheet.

## Site and species selection
- Focused on low-stature, non-forest ecosystems (grasslands, open/closed shrublands, woody savannas).
- Highly artificial vegetation types (e.g., managed hedges) were excluded.
- Sampling conducted at seasonal peak canopy cover to minimize phenophase effects; allometric relationships may still vary in drier ecosystems.
- Protocol description and considerations are detailed in Cunliffe & Anderson (2019).

## Aerial imaging surveys
- Use of unmanned aerial systems (UAS) for two survey flights per site:
  - Nadir imagery for ~5 mm per pixel at canopy top.
  - Oblique ~20° imagery from about 3–4 m higher.
- Typical altitude around 20 m above canopy; 75% forward/side overlap and minimum 30 images per area.
- Wind speeds recorded prior to surveys.
- Ground control: thirteen 20 cm x 20 cm markers deployed per site, GNSS-located to precision ~±0.015 m horizontal, ±0.03 m vertical.
- Future improvements anticipated: reduced need for ground control with improved geolocation/orientation.

## Vegetation harvests
- Harvest plots chosen to represent canopy height range; target of at least 0.5 m x 0.5 m.
- Corners geolocated with high-precision GNSS before harvest to ground level (or moss level for some species).
- Biomass dried at ~50–80°C to constant weight; moisture content measured for largest taxa.
- Plot areas computed from corner coordinates (or frame area when used).

## Image-based modelling and processing
- Photogrammetry workflow using Agisoft PhotoScan (v1.4.3):
  - Import geotagged images and ground-control coordinates; convert to UTM.
  - Image sharpness: score ≥ 0.5 used as quality filter.
  - High-quality settings for tie points, camera alignment; default parameters adjusted for accuracy.
  - Lens parameters enabled; bundle adjustment optimized; manual removal of obviously erroneous points.
  - Ground control markers constrained photogrammetric reconstructions; dense point clouds exported (laz format) with RGB attributes.
- Camera positions reviewed by an operator; ten ground control markers used to constrain reconstruction; three markers reserved for independent accuracy assessment.

## Digital terrain models (DTMs) and canopy height
- DTMs generated from GNSS-corner-derived locations using inverse distance weighting (power = 1).
- When canopies are discontinuous, high-quality DTMs may be derived from the photogrammetric point cloud; alternatives include leaf-off UAV surveys, LiDAR, or walkover GNSS surveys.

## Dense point cloud analysis and canopy height
- Point clouds processed with PDAL (v2.0.1):
  - Plot subsetting via GNSS corner coordinates; artifacts removed manually if present.
  - Height above ground computed relative to a surface interpolated between plot corners (IDW, power = 1).
  - 0.01 m resolution grid used to compute maximum height per cell; for empty cells, height interpolated using IDW from surrounding cells (7x7 neighborhood).
  - Plot-level mean canopy height extracted from the grid of local maxima elevations.

## Data quality, accuracy, and context
- Comprehensive calibration and parameter settings documented (camera, marker, tie-point accuracy, reprojection error).
- Dense point clouds and canopy height derived with quality controls, including accuracy assessments via reserved ground-control markers.
- References and methodological context provided to support reproducibility and comparison with related work.

## Related materials and context
- Protocols and prior methods cited (e.g., Cunliffe & Anderson 2019; related drone photogrammetry and biomass studies) to support data collection, processing, and interpretation.
- Data underpin ongoing work: “Drone-derived canopy height predicts aboveground biomass in non-forest ecosystems across the globe” (In Review) with additional processing details in supplementary materials.

## Usage and governance notes
- Data are openly licensed under the Open Government Licence; proper citation requested.
- Metadata, data structure, and units are documented to facilitate reuse, integration with other datasets, and reproducibility of analyses.
- Acknowledges potential limitations related to ground-control dependency and the applicability of methods to taller or more complex vegetation types; notes future workflow improvements to reduce or eliminate ground control reliance.