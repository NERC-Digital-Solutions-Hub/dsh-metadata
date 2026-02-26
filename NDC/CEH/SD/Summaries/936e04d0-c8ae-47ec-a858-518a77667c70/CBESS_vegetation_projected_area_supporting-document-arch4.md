# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) projected area estimates of vegetation in saltmarsh habitats

- Overview: This dataset provides estimates of the projected area or density of vegetation structures in saltmarsh habitats, interpreted from horizontal views through a 600 × 200 mm section of salt marsh canopy.

- Staff responsible: Tom Spencer, Ben Evans.

- Locations and habitats:
  - Essex: Abbotts Hall (AH) 51°47'N, 0°52'E; Fingringhoe Wick (FW) 51°49'N, 0°58'E; Tillingham Marshes (TM) 51°41'N, 0°56'E.
  - Morecambe Bay: Cartmel Sands (CS) 54°10'N, 3°0'W; Warton Sands (WS) 54°08'N, 2°48'W.
  - Habitats and soils:
    - Saltmarsh regions with contrasting soil types: three sites with clay soils (Essex) and three with sandy soils (Morecambe Bay).
    - Essex saltmarsh vs Morecambe saltmarsh differ in inundation frequency, creek structure, and dominant vegetation.
    - Mudflat sites in Essex are cohesive clays/mud/silt; Morecambe mudflats have coarse, mobile sediments.

- Temporal coverage and sampling:
  - Observation period: October 2012 – September 2013.
  - Sampling: 22 quadrats in January and August; quadrats along the wave monitoring transect sampled four times over the period.

- Variables observed:
  - Horizontal extent
  - Vegetation area (Veg area)
  - Normalised area (Veg area normalised by horizontal extent)

- Data collection methods:
  - Photography: FujiFilm Finepix XP30, 14 MP, taken through a 20 cm deep section of vegetation against a red backboard at fixed distance.
  - Field procedures: Selection of quadrat locations where vegetation height exceeded the backboard, ensuring visibility against the backboard.

- Data processing and analysis workflow:
  - Calibration and distortion correction:
    - Camera calibrated with MATLAB Camera Calibration Toolbox.
    - Calibration used a 1600 × 910 mm black/white checkerboard pattern to determine pixel dimensions and rectify geometric distortions.
  - Image processing steps per quadrat:
    - Select the best vegetation image based on contrast and lighting.
    - In MATLAB: correct misalignment, rotate to horizontal, crop to include full vegetation height, generate and apply pixel/area masks for the appropriate focal length, and rotate/crop masks accordingly.
    - Import into Erdas Imagine; perform 20-class unsupervised classification, then manually attribute classes to 'vegetation' or 'background' to create a binary vegetation class (1 = vegetation).
    - Compute vegetation measures (areas, pixel counts) with masks that account for image-specific pixel dimensions and distortions.
  - Assumptions and limitations:
    - Assumes vegetation is flat and lies on the plane of the backboard.
  - Validation and references:
    - Method adapts Möller (2006) for quantifying saltmarsh vegetation and wave height dissipation.
  - Outputs and formats:
    - File formats: JPEG, Erdas .img, and TIFF; outputs stored as ASCII text.
    - Dataset fields/descriptions include: Header, Row number, Season (Winter W or Summer S), Location (Morecambe M or Essex E), Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex), Habitat (Mudflat MF, Saltmarsh SM), Quadrat (1–22, with sub-quadrats), Scale (A-D reflecting 1 m to >100 m), Date (DD.MM.YYYY), Horizontal extent (mm), Veg area (mm^2), Normalised area (mm^2 per mm horizontal extent).

- Data quality and governance:
  - Quality control performed visually during processing.
  - Data include NA values where measurements were not performed.
  - Documentation references the Möller (2006) methodology for context and reproducibility.

- Access and use considerations for data leaders:
  - Clear provenance: staff, dates, sites, and processing workflow documented.
  - Rich metadata: detailed field definitions and calibration steps supporting discoverability and reuse.
  - Potential for cross-site comparison: contrasting clay vs sandy soils and differing inundation regimes across Essex and Morecambe Bay.
  - Reproducibility considerations: explicit calibration, image processing steps, and classification approach enabling replication.