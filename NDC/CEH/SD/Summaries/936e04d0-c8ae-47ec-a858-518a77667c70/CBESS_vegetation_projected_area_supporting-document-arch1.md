# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

## Aim and what is measured
- Estimates of the projected horizontal area or density of saltmarsh vegetation within a 600×200 mm section of vegetation.
- Two key outputs per analysed image subset: total vegetation area (Veg area) and a normalised area (Veg area per unit horizontal extent).

## Study sites and design
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Site characteristics:
  - Contrasting soil types: clay soils in Essex; sandy soils in Morecambe Bay
  - Distinct inundation frequencies, creek structures, and dominant vegetation
  - Mudflats differ: Essex with cohesive clays; Morecambe with coarse, mobile sediments
- Temporal scope: October 2012 – September 2013
- Sampling: 22 quadrats sampled in January and August; quadrats along a wave monitoring transect sampled four times over the period
- Habitats observed: Saltmarsh (SM) and Mudflat (MF)

## Data collection and processing workflow
- Data collection:
  - Photographs of vegetation using a FujiFilm Finepix XP30 (14 MP) through a 20 cm deep section of vegetation
  - Backboard and fixed distance; photos captured when vegetation height exceeded 25 mm
- Calibration and correction:
  - Camera calibration and distortion correction using the Camera Calibration Toolbox for Matlab
  - Pixel size calibration with a checkerboard pattern (1600×910 mm, 50.4×50.5 mm squares)
  - For each focal length, generation of masks for pixel dimensions and areas; geometric distortion corrected
- Image processing steps:
  - Align images to horizontal, crop to include full vegetation and minimize background
  - Apply focal-length specific masks to obtain area measurements
  - Use Erdas Imagine for 20-class unsupervised classification; manually recode to two classes: vegetation and background
  - Convert to binary vegetation maps and compute vegetation area per image subset
- Quality control:
  - Visual checks during processing
  - Calibration and distortion corrections documented
- Outputs and formats:
  - File formats: JPEG, Erdas .img, TIFF; outputs stored as ASCII text

## Variables and dataset fields
- Seasonal and location fields:
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe (CS, WS, WP); Essex (AH, FW, TM)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat: 1–22 plus additional a1–a8 (AH, f1–f8 at FW, t1–t8 at TM)
  - Scale: A=1 m; B=1–10 m; C=10–100 m; D=100–upper limit
  - Date: DD.MM.YYYY
- Measurements:
  - Horizontal extent (mm)
  - Veg area (mm^2): total vegetation area in analysed image subset
  - Normalised area (mm^2 per mm horizontal extent)

## Data provenance, quality, and documentation
- Data provenance:
  - Staff: Tom Spencer, Ben Evans
  - Based on field observations and image-based vegetation extraction following the methodology of Möller (2006)
- Quality control:
  - Visual data checks; calibration and distortion corrections applied prior to analysis
- Documentation:
  - Detailed methodological description of calibration, image processing, and classification
  - References provided for methods (Möller, 2006)

## Limitations and considerations for analysis
- Assumptions:
  - Vegetation is flat and lies on the plane of the photo backboard
  - Two-class vegetation vs. background classification may oversimplify complex structures
- Data scope:
  - Limited to specific sites, seasons, and quadrats; four-time sampling along the wave transect
- Data completeness:
  - Some fields may contain NA values where measurements were not performed
- Accessibility:
  - Data are documented with extensive metadata but access to primary datasets and processing scripts may require additional portals or permissions

## Potential uses for analysts
- Correlation analyses between vegetation area and site characteristics (soil type, inundation, sediment) across Essex and Morecambe Bay
- Temporal comparisons of vegetation area between winter and summer within and across sites
- Modelling of vegetation density as a proxy for wave dissipation or ecosystem service provision in saltmarsh habitats
- Integration with wave monitoring data to assess how vegetation structure affects coastal processes
- Reproducibility: methodology enables replication with similar image-based vegetation quantification in other saltmarsh contexts