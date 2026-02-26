# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats.

## Overview
- Dataset provides projected area estimates of vegetation in saltmarsh habitats, focusing on horizontal vegetation extent within a 600x200 mm section of salt marsh.
- Field coverage includes two regions: Essex (saltmarsh habitats with clay soils) and Morecambe Bay (saltmarsh habitats with sandy soils), representing contrasting sediment types and inundation regimes.
- Monitoring period: October 2012 – September 2013; 22 quadrats sampled in January and August, with additional sampling along a wave monitoring transect.
- Primary outputs: Horizontal extent, vegetation area (Veg area), and vegetation area normalized by image extent (Normalised area).

## Location and sampling design
- Sites and locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Site characteristics: Two contrasting habitat soils (clay in Essex; sand in Morecambe Bay) and differing inundation, creek structure, and dominant vegetation.
- Habitat types: Saltmarsh (SM) and Mudflat (MF); seasonal sampling across Winter (W) and Summer (S) periods; quadrats designated (AH, FW, TM; CS, WS).
- Observational methods include wave monitoring transects alongside vegetation quadrats.

## Variables and data products
- Observed/derived variables:
  - Horizontal extent (mm)
  - Veg area (mm^2)
  - Normalised area (mm^2 per mm horizontal extent)
- Dataset fields include seasonal and location metadata, site/habitat classifications, quadrat identifiers, scale, date, and measurement results.

## Data collection and processing methods
- Field methods:
  - Photographs captured with FujiFilm Finepix XP30 at full 14 MP resolution, through a 20 cm deep vegetation section against a red backboard.
  - Vegetation height criteria: photographs taken only where vegetation exceeded the height of the frame backboard (25 mm).
- Data processing workflow:
  - Camera calibration and distortion correction using MATLAB Camera Calibration Toolbox.
  - Calibration targets included a 1600x910 mm checkerboard for pixel-size determination per focal length.
  - Image preprocessing: rotation to horizontal, cropping to include full vegetation height while maximizing vegetation pixels.
  - Mask generation to obtain pixel- and area-based vegetation measures.
  - Image analysis: unsupervised classification (20 classes) in Erdas Imagine, then manual reclassification to two classes (vegetation vs background).
  - Final outputs: vegetation dimensions and positions computed relative to the reference backboard plane, with distortion corrected.
- Assumptions/limitations:
  - Assumes vegetation lies flat on the plane of the backboard.
  - Two-class classification balances differentiation with inter-user variability; more classes increase subjectivity.

## Data formats and metadata
- File formats used: JPEG, Erdas .img, TIFF for images; ASCII text for outputs.
- Data quality and checks: Visual quality control during processing.
- Dataset fields (examples): Season, Location (Essex/Morecambe), Site (AH, FW, TM, CS, WS), Habitat (Saltmarsh, Mudflat), Quadrat, Scale (A-D with defined extents), Date, Horizontal extent, Veg area, Normalised area.
- NA values indicate measurements not performed.

## Data governance, access and quality
- Emphasizes careful calibration, distortion correction, and transparent processing steps to ensure data quality and comparability across sites.
- Metadata-rich structure facilitates data provenance and re-use for ecological monitoring and policy evaluation.
- Underlying data accessibility and public sharing considerations align with broader monitoring framework requirements, including openness and data management standards.

## Limitations and considerations for monitoring
- Method relies on photographic measurement and image processing, requiring substantial technical resources (MATLAB, Erdas Imagine) and calibration rigor.
- The planar-vegetation assumption may introduce bias in non-flat vegetation patches or variable backboard alignment.
- Classification choices (two-class) trade off differentiation detail against inter-user variability; consistency in methodology is critical for long-term monitoring.

## References
- Möller, I. (2006). Quantifying saltmarsh vegetation and its effect on wave height dissipation: Results from a UK East coast saltmarsh. Estuarine, Coastal and Shelf Science, 69(3-4), 337-351. doi:10.1016/j.ecss.2006.05.003.