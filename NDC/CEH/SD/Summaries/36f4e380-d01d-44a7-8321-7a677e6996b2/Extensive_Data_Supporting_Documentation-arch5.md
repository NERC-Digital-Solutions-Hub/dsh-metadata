# Extentive_Vegetation_and_Soil_Data.csv

## Overview
- A stratified ecological and soil dataset describing covariation between vegetation and edaphic characteristics.
- Collected at sites in the Yukon (2013) and Northwest Territories (2014), Canada.
- 24–30 × 1 m² plots per site to map extensive vegetation and soil variability.

## Data Collected
- Vegetation and soil variables (data codes described in Table 1):
  - ALD: Late August thaw depth (cm) from moss layer bottom
  - slope: Ground slope in degrees
  - Tree_LAI: Canopy leaf area index (LAI) via hemispherical photography
  - Understorey_LAI (LAI U): Understory vascular LAI via LAI-2000
  - OM_thick: Organic matter layer thickness (cm)
  - Moss_thickness: Moss layer thickness (cm)
  - OM_and_Moss_thickness: Total organic/moss thickness (cm)
  - DeepMoist: Deeper soil moisture (11–16 cm)
  - SurfMoist: Surface soil moisture (0–6 cm)
  - Height: Mean understory height (cm)
  - Region/Site/Plot: Geographical identifiers
  - GPS.N / GPS.W: Coordinates
  - LAI: Total Leaf Area Index
- Site and plot identifiers, and time stamps:
  - Time of vegetation data; Time of soil sampling
  - Region descriptions and per-site metadata (e.g., boreal region)

## Measurements and Methods
- LAI Tree:
  - Measured with Nikon D5000 DSLR and hemispherical lens; nine photos per plot
  - Processed with CAN-EYE; LAI2000 output for comparability
  - Sunlight control via thresholding and, when possible, measurements taken later in the day
- Understorey LAI (LAI U):
  - Measured with LI-COR LAI2000 Plant Canopy Analyser
  - One measurement above, four below the understory canopy (20 × 20 cm center plot)
  - Shading and sky conditions controlled using 90° cap and tarps as per manual
- Height:
  - Measured at five points (four corners + center) within a 0.5 × 0.5 m quadrat; mean used
- Moss Thickness:
  - Measured by careful removal of moss/organic layer; thickness from moss surface to base of decomposed moss
- Moisture (Surface and Deeper):
  - SurfMoist: Upper 0–6 cm using ML3 ThetaKit; readings reflect moss/soil surface
  - DeepMoist: 11–16 cm depth; probe inserted after parting moss/organic layer
  - Four readings per plot; mean used
  - Factory calibration used due to small-scale variability; multiple readings per plot/site
- Soil Organic Matter (OM) Thickness:
  - Measured with 1.8 cm diameter corer to base of O horizon
  - Moss thickness subtracted to yield OM thickness
- Slope:
  - Measured along steepest gradient with a 50 cm plank and digital angle meter
- Active-Layer Thickness (ALT):
  - Measured with a stainless steel rod; confirm frozen conditions with a temperature probe
  - Plots where soil >0°C excluded from analysis
- Additional notes:
  - Data codes and variable descriptions are provided in Table 1
  - Site details and per-site metadata are provided in Table 2
  - Related publication for methods and context: Fisher et al. 2016, Global Change Biology

## Site Details
- Site codes and locations:
  - FFB, FFU: Whitehorse, Yukon Territory
  - BF: Whitehorse, Yukon Territory
  - MB, MU: Yellowknife, Northwest Territories
  - BB, BS: Yellowknife, Northwest Territories
- Site attributes:
  - Latitude/Longitude and Elevation (varies by site)
  - Vegetation Zone: Boreal
  - Vegetation Description: Varied post-fire and understorey composition
  - Disturbance/Hydrology: Ranged from upland with recent fire to unburned areas
  - PF Zone: Permafrost zone statuses (sporadic or discontinuous)
- Time of data collection:
  - Vegetation data dates vary by site (e.g., 4–6 August 2013 for some, 27 July–25 August for others)
  - Soil sampling dates span August 2013 and August 2014 depending on site

## Data Coding, Metadata, and Documentation
- Data identified by codes described in Table 1 (e.g., ALD, slope, LAI Tree, LAI U, etc.)
- Detailed site metadata provided in Table 2 (location, elevation, vegetation, disturbance, permafrost zone, and sampling times)
- Connection to publication:
  - Fisher et al. (2016) The influence of vegetation and soil characteristics on active-layer thickness of permafrost soils in boreal forest, Global Change Biology

## Data Quality and Governance Considerations for Data Stewards
- Metadata richness and traceability:
  - Clear data codes, units, and per-site metadata enable interoperability and re-use
- Standardization and reproducibility:
  - Documented measurement methods, calibration approaches, and sampling protocols
- Update and sharing readiness:
  - Data described for potential upload to data portals and catalogues; workflow and documentation aid discoverability and reuse
- Compliance and limitations:
  - Exclusion of plots with unfrozen soils (>0°C) ensures data quality for ALT analyses
  - Acknowledge potential small-scale variability in moisture readings and calibration choices

## Reference
- Fisher, J. P., et al. 2016. The influence of vegetation and soil characteristics on active-layer thickness of permafrost soils in boreal forest. Global Change Biology, 22: 3127-3140