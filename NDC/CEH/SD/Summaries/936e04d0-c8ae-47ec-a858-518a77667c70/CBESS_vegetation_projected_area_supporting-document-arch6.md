# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

## Overview
- Purpose: Projected area estimates of saltmarsh vegetation to quantify vegetation extent and structure, enabling analysis of ecosystem services such as wave height dissipation.
- Outputs: Vegetation area measures from photographic analysis, including raw and normalised metrics.

## Data collection and locations
- Study sites (contrasting habitats and soils):
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) with clay soils
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) with sandy soils
- Habitat context: Saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation; mudflats in Essex are cohesive clays/mud/silt vs. Morecambe mudflats with coarse, mobile sediments.
- Observation period: October 2012 – September 2013
- Sampling design: 22 quadrats sampled in January and August; quadrats along a wave-monitoring transect sampled four times over the period

## Observed variables and dataset structure
- Core variables:
  - Horizontal extent (image subset analyzed, in mm)
  - Veg area (total vegetation pixels converted to area, in mm^2)
  - Normalised area (Veg area normalized by horizontal extent, mm^2 per mm)
- Dataset organization:
  - Quadrats labeled AH, FW, TM (with additional quadrats a1-a8, f1-f8, t1-t8 along the transect)
  - Scale codes to indicate image subset size: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
  - Season: Winter (W) or Summer (S)
  - Site/Location and Habitat fields (Mudflat, Saltmarsh)

## Methods and data processing
- Field photography:
  - Equipment: FujiFilm Finepix XP30, 14 MP, fixed distance, photographs taken through a 20 cm deep vegetation section against a red backboard
  - Selection: For each quadrat, the best image chosen based on contrast and lighting
- Calibration and distortion correction:
  - Calibration using Camera Calibration Toolbox for Matlab
  - Chessboard calibration pattern (1600 x 910 mm) to derive pixel size per focal length; correction of geometric distortions
  - Rotation to horizontal alignment using reference points on the backboard
- Image processing workflow (in MATLAB and Erdas Imagine):
  - Cropping to include full vegetation while maximizing vegetation pixel proportion
  - Apply focal-length-specific masks to generate pixel-area masks
  - Rotate/crop masks to match transformed images; create image-specific masks
  - Import into Erdas Imagine; perform 20-class unsupervised classification
  - Manually attribute classes to vegetation or background; recode to binary (1 = vegetation)
  - Compute vegetation dimensions from the binary classified areas, correcting for geometric distortions
- Assumptions and caveats:
  - Vegetation is treated as flat and in the plane of the backboard
  - Two-class classification balances discrimination with inter-user variability as class count increases
- Quality checks:
  - Visual quality control during processing
- Data formats and outputs:
  - Original images: JPEG; intermediate/processed imagery: Erdas .img and TIFF
  - Outputs stored as ASCII text
  - NA values indicate non-performed measurements

## Dataset fields and descriptions
- Core fields (example structure):
  - Header/Description, Cell Format
  - Row number: sequence index for sorting
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: CS, WS, WP (Morecambe) or AH, FW, TM (Essex)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat: identifier (1–22; a1–a8, f1–f8, t1–t8)
  - Scale: A–D
  - Date: DD.MM.YYYY
  - Horizontal extent: subset width (mm)
  - Veg area: vegetation area (mm^2)
  - Normalised area: mm^2 per mm horizontal extent
- Data quality notes:
  - NA values indicate unperformed measurements
  - Field descriptions and data-type details provided for reproducibility

## Use cases and data exploitation
- Self-serve data products: enable end users to retrieve vegetation area metrics and compare across sites, habitats, and times
- Cross-site analyses: contrast clay vs. sandy soils, inundation regimes, and vegetation structure
- Ecosystem service modelling: provide input metrics for wave dissipation and related coastal dynamics (referencing Möller 2006)
- Data integration: combine with other CBESS datasets for broader analyses of biodiversity, services, and habitat condition

## References and methodological context
- Reference: Möller, I. (2006). Quantifying saltmarsh vegetation and its effect on wave height dissipation: Results from a UK East coast saltmarsh. Estuarine, Coastal and Shelf Science, 69(3-4), 337-351. doi:10.1016/j.ecss.2006.05.003.