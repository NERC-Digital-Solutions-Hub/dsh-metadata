# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

## Overview
- Estimates the projected area or density of vegetation structures in saltmarsh habitats, using horizontal plane views of a 600x200 mm section of salt marsh vegetation.
- Study period: October 2012 – September 2013.
- 22 quadrats sampled in January and August; quadrats along a wave monitoring transect sampled four times.
- Two regional contrasts: Essex (clay soils) and Morecambe Bay (sandy soils), representing different sediment types, inundation patterns, creek structures, and vegetation.
- Included mudflat sites in Essex (cohesive clays, mud, silt; not the primary focus) to contextualize habitat contrasts.

## Data stewardship and governance
- Staff responsible: Tom Spencer, Ben Evans.
- Dataset appears to be prepared with documented processing workflows, calibration procedures, and metadata fields to support discovery and reuse.
- Emphasis on documenting data collection methods, processing steps, calibration, and quality control to enable standards-aligned reuse and reprocessing if needed.
- Includes explicit methodological decisions (e.g., classification approach, handling of NA values) to inform data users and future governance decisions.

## Location and sampling design
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
- Site descriptions highlight contrasting soils (clay in Essex; sand in Morecambe Bay) and differing inundation frequencies, creek structures, and dominant vegetation.
- Sampling schedule: October 2012–September 2013 monitoring; 22 quadrats with targeted sampling in January and August; wave monitoring transect quadrats sampled four times during the period.

## Data collection and processing
- Field method: Photographs taken with a FujiFilm Finepix XP30 at full 14 MP resolution, through a 20 cm deep vegetation section, against a red backboard at a fixed distance.
- Image processing workflow (in Matlab and Erdas Imagine):
  - Camera calibration to correct distortion using the Camera Calibration Toolbox for Matlab with a checkerboard reference pattern.
  - Image rectification and rotation to ensure horizontal alignment; cropping to include full vegetation within a minimal frame.
  - Creation and application of pixel-level masks for vegetation versus background, with focal-length-specific calibration.
  - Selection of the best-quality image per quadrat based on contrast and lighting.
  - Unsupervised 20-class classification in Erdas Imagine, followed by manual attribution of classes to vegetation or background.
  - Recode to two classes (vegetation = 1; background = 0) and calculation of vegetation area and dimensions, correcting for geometric distortions.
  - Assumption notes: vegetation is flat and lies on the plane of the photo-backboard.
- Calibration and QA:
  - Calibration procedures described and repeated for different focal lengths.
  - Data checking performed visually during processing.
- Outputs and formats:
  - Image data stored as JPEG, Erdas .img, and TIFF formats; outputs also stored as ASCII text.
  - Metadata and dataset field definitions accompany the dataset to support reuse and interpretation.

## Variables, data model, and field structure
- Core observed/derived variables:
  - Horizontal extent (in mm)
  - Veg area (mm^2)
  - Normalised area (vegetation area per horizontal extent, mm^2 per mm)
- Dataset fields and coding (examples):
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe Cartmel Sands (CS), Warton Sands (WS), West plain (WP); Essex Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat identifiers: 1–22 (with a1–a8, f1–f8, t1–t8 representing additional quadrats along a wave transect)
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100– upper limit)
  - Date (DD.MM.YYYY)
  - Horizontal extent, Veg area, Normalised area (with corresponding data types)
- Data describe how each image subset is analyzed and how results map to a structured, field-reported dataset.

## Quality assurance and limitations
- Visual QA conducted during processing; classification choices balanced differentiation of vegetation with inter-user variability.
- Key limitations and assumptions:
  - Vegetation treated as flat and lying on the backboard plane; potential distortions if geometry deviates.
  - Two-class vegetation classification introduces potential inter-user variability, mitigated by locking to vegetation/background labels.
  - NA values indicate missing measurements where observations were not performed.
- These factors influence interpretability and comparability across quadrats and dates; appropriate metadata and method notes are provided to support auditability and potential reprocessing.

## Data formats, storage, and accessibility
- Data formats include JPEG, Erdas .img, TIFF images and ASCII text outputs.
- Metadata and field definitions provided to support discoverability, interoperability, and reuse in data portals or catalogues.

## References
- Möller, I. (2006). Quantifying saltmarsh vegetation and its effect on wave height dissipation: Results from a UK East coast saltmarsh. Estuarine, Coastal and Shelf Science, 69(3-4), 337-351. doi:10.1016/j.ecss.2006.05.003.