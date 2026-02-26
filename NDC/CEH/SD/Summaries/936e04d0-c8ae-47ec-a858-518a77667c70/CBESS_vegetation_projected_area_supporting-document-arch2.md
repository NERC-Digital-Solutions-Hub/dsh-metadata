# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

## Overview
- Estimates the horizontal area or density of vegetation in saltmarsh habitats from photographic imagery of a 600 × 200 mm section.
- Aimed at supporting coastal ecosystem monitoring by providing standardized vegetation metrics that can be tracked over time.

## Location and personnel
- Staff: Tom Spencer, Ben Evans.
- Study sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) – saltmarsh and mudflat habitats with clay soils.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) – saltmarsh and mudflat habitats with sandy sediments.
- Site descriptions emphasize contrasting sediment types, inundation frequencies, creek structures, and vegetation types.

## Study design and sampling
- Monitoring period: October 2012 – September 2013.
- Quadrat sampling: 22 quadrats sampled in January and August; quadrats along the wave-monitoring transect sampled four times over the period.
- Variables observed: horizontal extent of vegetation, total vegetation area, and normalised area (area per unit horizontal extent).

## Methods and processing
- Data collection:
  - Photographs taken with a FujiFilm Finepix XP30 at full resolution, through a 20 cm deep vegetation section, against a red back board at a fixed distance.
  - Prior calibration used the Camera Calibration Toolbox for Matlab with a checkerboard to correct geometric distortions and to derive pixel dimensions.
- Image processing workflow:
  - Align images to horizontal, crop to include full vegetation, and generate image-specific masks for pixel areas.
  - Software: Matlab for preprocessing; Erdas Imagine for classification.
  - Classification: 20-class unsupervised classification, then manual assignment to vegetation or background (binary: 1 = vegetation).
  - Calculations: derive vegetation area per image subset, adjust for distortions, and account for scale to produce area metrics.
- Key assumption: vegetation is flat and located on the plane of the photo-back board.

## Data products and fields
- Outputs and formats:
  - Images and derived ASCII text outputs; raw formats include JPEG, Erdas .img, and TIFF.
- Dataset fields (examples):
  - Season (Winter, Summer), Location (Morecambe or Essex), Site (e.g., CS, WS, AH, FW, TM), Habitat (Saltmarsh, Mudflat), Quadrat identifiers, Scale (A–D with corresponding ranges), Date.
  - Measurements: Horizontal extent (mm), Veg area (mm^2), Normalised area (mm^2 per mm of horizontal extent).
- Data quality notes:
  - NA values indicate measurements not performed; visual quality control performed during processing.

## Data quality, standards, and references
- QA through visual checks during processing.
- Methodology anchored to established techniques (Möller 2006) for quantifying saltmarsh vegetation and its effect on wave height dissipation.
- Calibration and distortion correction steps documented and replicated per focal length.

## Accessibility, reuse, and implications for environmental monitoring
- Uses standardised data collection and processing methods to enable cross-site and temporal comparisons.
- Outputs are compatible with common geospatial and statistical workflows (images and ASCII data), facilitating integration with other coastal monitoring datasets.
- Aligns with the Analysts Monitoring the Environment archetype’s goals of verifiable, standardised datasets and the potential to combine with additional datasets to enhance value and accessibility of underlying data.