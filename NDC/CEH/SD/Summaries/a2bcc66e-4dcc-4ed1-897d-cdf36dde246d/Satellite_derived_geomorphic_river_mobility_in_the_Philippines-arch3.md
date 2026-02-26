Supporting documentation for 'Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019'

# Overview
- Dataset providing satellite-derived information on geomorphic river mobility for ten catchments in the Philippines (1988–2019).
- Uses a locational probability approach to map the proportion of time a river channel occupies a given location.
- Quantifies locational probabilities for approximately 600 km² of riverbed.
- Aims to support predicting and developing resilience to river-related hazards in dynamic landscapes.
- Includes example codes (Google Earth Engine and MATLAB) to replicate analyses and outputs for each catchment.

# Data scope and purpose
- Data intended for informing policy decisions, monitoring approaches, and future decisions on environmental health and hazard resilience.
- Outputs designed to be reproducible and comparable across catchments and time.
- Supports governance and communication of complex river dynamics through standardized processing and artifacts.

# Methods and processing

## Active channel extraction
- Used Google Earth Engine (GEE) to derive binary active channel masks from Landsat imagery.
- Trunk channel defined with a 3 km buffer to encompass the active channel.
- Time-windows: two-year periods between 1988 and 2019 to maximize cloud-free data.
- Image collections built per time-window; cloud/shadow masked with CFmask; bicubic resampling applied.
- Active channel classified using NDVI and MNDWI; NDVI ≤ 0.2 and MNDWI ≥ −0.4 as thresholds.
- Pixel values rescaled to [0,1], reduced to a single image per time-window using the 10th percentile.
- Final masks converted to binary presence/absence and exported as GeoTIFFs.
- Two code versions: (i) original Landsat Collection 1 code; (ii) updated Landsat Collection 2 code (post-2022) to ensure compatibility with new Landsat data.

## Cleaning and quality checking
- Artefacts (e.g., built-up areas, agricultural fields) removed from binary masks.
- Filtering steps:
  - Remove disconnected areas < 500 pixels.
  - Morphological closing with a 2-pixel disk element.
  - Remove large, isolated features < 2500 pixels away from the trunk channel.
- Manual GIS sense-check to remove connected areas not representing the main trunk channel.
- Some time-windows are data-poor due to variable Landsat imagery and cloud cover, leading to incomplete coverage in certain catchments (e.g., Mindanao).

## Locational probability calculation
- Locational probability (lp) computed from multi-temporal binary active-channel masks:
  - p = sum(Wn * Fn) across time-windows, where Fn is 1 if the pixel is part of the active channel at time-window n, else 0.
  - Weights Wn = 1/x, with x being the total number of time-windows for the catchment (equal weighting across windows).
  - lp ranges from 0 (never occupied) to 1 (always occupied).
- Interpretation:
  - Low lp (0 < lp < 0.25): channel rarely occupies the pixel (high mobility).
  - High lp (0.75 < lp < 1): channel frequently occupies the pixel (stability).

## Spatial reference and resolution
- Spatial reference: EPSG:32651 – WGS 84 / UTM zone 51N.
- Spatial resolution: approximately 10 m × 10 m.

## Data structure and outputs
- Documentation and data files organized with:
  - General overview (README.txt)
  - Subfolder-specific READMEs for GEE code and locational probabilities
  - Processed locational probability rasters and accompanying software
- Outputs include processed locational probability rasters for the ten catchments and example MATLAB code for plotting longitudinal data.

# Reproducibility, code, and data governance

- GEE code provided in two versions:
  - GEE_Code_Abulug_Deprecated.txt (legacy)
  - GEE_Code_Abulug_Migrated.txt (updated for Collection 2)
- Example MATLAB code sets included for processing locational probabilities and plotting longitudinal data.
- Data products are designed for reproducibility and applicability to other rivers using similar approaches.
- The work is supported by the Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund grant NE/S003312/1, underscoring governance and funding considerations for monitoring-focused research.

# Data quality, limitations, and accessibility

- Data quality control involved visual checks against Landsat and Google Earth imagery, with consistent processing steps across catchments.
- Limitations:
  - Cloud cover and varying Landsat data availability lead to data-poor time-windows in some catchments.
  - Geographic data availability biases (e.g., Mindanao) affecting data completeness.
  - Manual editing required to ensure binary masks align with the trunk channel.
- Accessibility:
  - Processed outputs and codes are provided to enable replication and adaptation by the research and policy communities.
  - Underlying raw imagery data may have usage constraints, but the documented workflow and outputs facilitate transparent monitoring.

# Applications for monitoring frameworks and policy

- Provides a quantitative, repeatable metric of river mobility that can inform:
  - Infrastructure risk assessments against bankfull-channel shifts
  - Long-term river dynamics monitoring programs
  - Spatial planning for flood resilience and hazard mitigation
- The combination of open-source tools (GEE) and shareable code enhances transparency, data governance, and collaboration across agencies and researchers.
- The methodology aligns with monitoring framework aims to identify useful environmental health measures, verify data quality, and present findings in accessible formats (rasters, summaries, and longitudinal plots).

# References and context

- The dataset and methodology are described in Boothroyd et al. (2025) Nature Communications: Big data show idiosyncratic patterns and rates of geomorphic river mobility.
- Foundational references cover remote sensing, river morphology analysis, cloud/dataset handling, and locational probability concepts relevant to monitoring and policy use.