# Extensible_Vegetation_and_Soil_Data.csv

- A stratified survey of ecological and soil states conducted at sites in Yukon (2013) and Northwest Territories (2014), Canada.
- Aims to map covariation between vegetation and edaphic characteristics across fine spatial scales.
- Core measurements include leaf area index (LAI) for trees and understory, moss and organic matter thickness, surface and deeper soil moisture.
- Each site contains 24–30 plots of 1 m² for extensive mapping of vegetation-soil variability.
- Data are organized with data codes described in Table 1 and cover multiple environmental and site descriptors.

## Data content and codes

- Key variables (data codes): ALD (Active Layer Depth), slope, Tree_LAI, Understorey_LAI, OM_thick, Moss_thickness, OM_and_Moss_thickness, DeepMoist, SurfMoist, Height, Region, Site, Plot, GPS.N, GPS.W, LAI.
- Data descriptions indicate units (e.g., LAI in m²/m²; depth in cm; soil moisture in m³/m³; elevation in m; coordinates in degrees; etc.).
- Site and plot identifiers distinguish locations and sampling contexts.

## Methods and measurements

- Tree canopy LAI (LAI Tree):
  - Measured with a Nikon D5000 DSLR and hemispherical lens.
  - Nine photos per plot, processed with CAN-EYE; LAI2000-based outputs used for comparability.
  - Sunlight effects controlled by per-image thresholding and sampling late in the day when possible.
- Understory LAI (LAI U):
  - Measured with LI-COR LAI-2000 Plant Canopy Analyser.
  - One above-canopy measurement and four below-canopy measurements in a 20 cm × 20 cm central square.
  - Specific caps and shading used to minimize solar angle effects; measurements designed to be independent of Tree LAI.
- Maximum understory height:
  - Measured at five points (four corners + centre) within a 0.5 m × 0.5 m quadrat per 1 m² plot; mean used in analyses.
- Moss thickness:
  - Determined by removing moss and organic material; thickness from moss surface to base of decomposed material.
- Surface moisture:
  - Measured in the upper 6 cm of moss/soil using ML3 ThetaKit; accuracy ~1% for 0–50% volumetric moisture content range.
  - Readings reflect moss layer moisture; readings reflect measurements within surface layer.
- Deeper soil moisture:
  - Measured at ~11 cm depth (volume 11–16 cm below surface); four measurements per plot across the growing season; mean used.
  - Factory calibration used due to variability in millivolt readings; emphasis on multiple measurements rather than plot-specific calibrations.
- Soil organic matter (OM) thickness:
  - Measured with a 1.8 cm diameter corer to the base of the O horizon; moss thickness subtracted to obtain OM thickness.
- Slope:
  - Measured along steepest gradient using a 50 cm plank and digital angle meter.
- Active Layer Thickness (ALT):
  - Measured with a 1.5 cm diameter stainless steel rod; confirmed frozen conditions (0°C) with a temperature probe.
  - Plots with temperatures >0°C excluded from analysis.
- Calibration and data quality:
  - For moisture, factory calibrations used; multiple readings per plot and site to improve reliability.
  - Documentation notes on data processing steps, light conditions, and measurement timing to ensure comparability.

## Site details and structure

- Sites include combinations of post-fire and unburned conditions within boreal landscapes, across two main regions:
  - Whitehorse, Yukon (WH) and Yellowknife, Northwest Territories (YK)
- Site codes and descriptions:
  - FFB: Firefox burned; FFU: Firefox unburned
  - BF: Boundary Creek (peninsula; well drained)
  - MB: Mosquito Creek burned
  - MU: Mosquito Creek unburned
  - BB: Boundary Creek Birch
  - BS: Boundary Creek Spruce
- Common attributes recorded per site:
  - Location (City, Country)
  - Latitude and Longitude
  - Elevation (meters above sea level)
  - Vegetation Zone: Boreal
  - Vegetation Description (site-specific notes on dominant species and post-fire status)
  - Disturbance/Hydrology (upland vs. wetland; fire status)
  - PF Zone (permafrost zone: sporadic, discontinuous, etc.)
  - Time of vegetation data collection (dates vary by site)
  - Time of soil sampling (2013 and 2014 ranges)
- Representative vegetation and disturbance contexts:
  - Examples include post-fire recolonization by Betula glandulosa, Vaccinium spp., and moss-dominated ground layers; presence of black spruce (Picea mariana); varying understory compositions.

## Data availability and references

- Data are linked to a published study for methodological context:
  - Fisher et al. (2016) The influence of vegetation and soil characteristics on active-layer thickness of permafrost soils in boreal forest, Global Change Biology, 22: 3127-3140.
- Site-level and measurement details are documented in the accompanying Table 2 (Site details) and Table 1 (Data code explanations).

## Practical notes for analysts

- The dataset is designed to elucidate correlations between vegetation structure and edaphic properties at fine scales, suitable for predictive modeling of active-layer dynamics in boreal permafrost ecosystems.
- Be mindful of:
  - Scale alignment and cross-site comparability due to site-specific timing and micro-site conditions.
  - Data provenance and metadata for reproducibility (Tables 1 and 2 provide essential context).
  - Exclusion of plots with non-freeze conditions during ALT measurement.
  - Potential gaps or variability in moisture calibration across plots and years.