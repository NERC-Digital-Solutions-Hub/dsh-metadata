# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

## Overview
- Dataset estimating the projected horizontal area/density of saltmarsh vegetation from photographs of a 600×200 mm section.
- Focused on two contrasting saltmarsh regions (Essex with clay soils; Morecambe Bay with sandy soils) to capture habitat variation.
- Timeframe: October 2012 – September 2013; 22 quadrats sampled in January and August; additional wave-monitoring transect quadrats sampled four times in total.

## Study design and scope
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Site characteristics:
  - Saltmarsh sites across both regions to represent contrasting soil types, inundation frequency, creek structure, and predominant vegetation.
  - Mudflat sites in Essex represented by cohesive clays, mud, silt versus Morecambe mudflats with coarse, mobile sediments.
- Target variables: Horizontal extent, vegetation area (veg area), normalised area (veg area per horizontal extent).

## Data collection and processing
- Field methods:
  - Photographs taken with a FujiFilm Finepix XP30 (14 MP) through a 20 cm deep vegetation section, against a red backboard at fixed distance.
  - For each quadrat, the most suitable image based on contrast/lighting was selected for analysis.
- Data processing workflow (geospatial/image processing):
  - Camera calibration and distortion correction using the Camera Calibration Toolbox for MATLAB.
  - Pixel size calibration per focal length using a checkerboard reference to derive real-dimension masks for each focal length.
  - Image alignment and preprocessing:
    - Rotate image to horizontal by reference points.
    - Crop to include full vegetation with minimal background, preserving vegetation pixels.
    - Apply focal-length-specific masks, rotate/crop masks accordingly.
  - Image analysis:
    - Import into Erdas Imagine; perform 20-class unsupervised classification.
    - Manually classify classes as vegetation or background; reclassify to binary (1 = vegetation).
    - Derive vegetation structure metrics by referencing the structure from the binary mask and associated masks (pixel and area dimensions).
    - Correct for geometric distortion; assume vegetation lies on the backboard plane.
- Reference methods: Möller (2006) on quantifying saltmarsh vegetation and wave dissipation.

## Data quality and QA
- Calibration and distortion corrections applied per focal length; detailed camera calibration procedures documented.
- Visual quality control during processing (ongoing).
- Assumptions acknowledged: vegetation is flat and on the backboard plane; potential inter-user variability with higher class counts in unsupervised classification.

## Data formats and outputs
- Data formats:
  - Images in JPEG; intermediate/analysis outputs in Erdas .img and TIFF; final outputs stored as ASCII text.
- Outputs include:
  - Dataset fields describing each observation (Season, Location, Site, Habitat, Quadrat, Scale, Date, Horizontal extent, Veg area, Normalised area, etc.).
  - NA values indicate non-performed measurements.

## Metadata and field descriptions
- Season: Winter (W) or Summer (S).
- Location: Morecambe (M) or Essex (E).
- Site: Morecambe – Cartmel Sands (CS), Warton Sands (WS), West plain (WP); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Habitat: Mudflat (MF) or Saltmarsh (SM).
- Quadrat: Quadrant number (1–22; with additional quadrats along transects).
- Scale: A = 1 m; B = 1–10 m; C = 10–100 m; D = 100–upper limit.
- Date: DD.MM.YYYY.
- Horizontal extent: Sub-image width in mm used for analysis.
- Veg area: Total pixel area classified as vegetation (mm^2).
- Normalised area: Veg area per unit horizontal extent (mm^2 per mm).

## References
- Möller, I. (2006). Quantifying saltmarsh vegetation and its effect on wave height dissipation: Results from a UK East coast saltmarsh. Estuarine, Coastal and Shelf Science, 69(3-4), 337-351. doi:10.1016/j.ecss.2006.05.003

## Practical GIS considerations
- The dataset provides geospatially structured vegetation metrics across multiple saltmarsh sites with contrasting habitats, suitable for map-based visualization of vegetation extent and change over time.
- The detailed processing workflow supports reproducibility and potential re-derivation of vegetation metrics from the raw imagery.
- Spatial resolution is defined by the analysis subset (mm-scale) and the scaling provided by the quadrat framework, enabling integration into GIS analyses at the observed sites.