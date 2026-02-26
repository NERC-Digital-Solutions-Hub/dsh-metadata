# Extensive_Vegetation_and_Soil_Data.csv

## Purpose and scope
- Stratified ecological and soil survey focusing on covariation between vegetation and edaphic (soil) characteristics.
- Data collected at sites in the Yukon (2013) and Northwest Territories (2014), Canada.
- 24–30 x 1 m^2 plots per site to enable extensive mapping of vegetation and soil variability.
- Key variables include leaf area index (LAI), moss and organic matter thickness, surface and deeper soil moisture, and related measurements.

## Data content and structure
- Data are organized with data codes described in Table 1 (e.g., ALD, Tree_LAI, Understorey_LAI, OM_thick, Moss_thickness, DeepMoist, SurfMoist, Height, Region, Site, Plot, GPS coordinates, LAI).
- Primary measurements:
  - ALD: Late August thaw-depth (active layer thickness) beneath the moss layer.
  - Tree_LAI: canopy leaf area index.
  - Understorey_LAI (LAI U): understory vascular plant LAI, measured separately from tree canopy LAI.
  - OM_thick: thickness of the organic matter layer.
  - Moss_thickness and OM_and_Moss_thickness: total moss layer thickness and combined moss/organic layer thickness, respectively.
  - Surface moisture (SurfMoist) and deeper moisture (DeepMoist) in specified soil layers.
  - Height: mean understory vegetation height within plots.
  - Region/Site/Plot: hierarchical identifiers; GPS.N and GPS.W coordinates; LAI (total leaf area index).
- Data collection context and site details provided in accompanying tables (Table 1 for data codes; Table 2 for site details).

## Methods and measurement protocols
- Tree canopy LAI (LAI Tree):
  - Photography-based approach using a Nikon D5000 with hemispherical lens; nine photos per plot taken ~1 m above ground.
  - CAN-EYE software used; LAI2000 output used for comparability; shading corrections applied; measurements scheduled to minimize sun impact.
- Understorey LAI (LAI U):
  - Measured with a LI-COR LAI2000 Plant Canopy Analyser.
  - One above-canopy and four below-canopy readings within a 20 x 20 cm square at the center of each 1 m^2 plot.
  - 90° field of view to limit sunlight effects; shading via tarpaulin when needed.
- Plant height:
  - Maximum understory height measured at five points (four corners and center of a 0.5 x 0.5 m quadrat); mean used in analyses.
- Moss thickness:
  - Measured by removing moss/organic layer with a knife; thickness from moss surface to base of decomposed fibric material.
- Moisture measurements:
  - Surface moisture: upper 6 cm using ML3 ThetaKit; four per plot; typical accuracy ~1%.
  - Deeper moisture: ~11–16 cm depth; measured after parting moss/organic layer; four measurements per plot; standard factory calibration used due to small-scale variability.
- Soil organic matter (OM) thickness:
  - Measured to the base of the O horizon with a soil corer; moss thickness subtracted to obtain OM thickness.
- Slope:
  - Steepest gradient measured with a 50 cm wooden plank and a digital angle meter.
- Thaw depth (ALT/ALD):
  - ALT measured with a stainless steel rod; temperature confirmed near 0°C at the point of refusal.
  - Plots with temperatures > 0°C excluded from analysis.

## Site details and context
- Sites span Whitehorse, Yukon Territory (FFB Firefox burned, FFU Firefox unburned, BF Blackfox) and Yellowknife, Northwest Territories (MB Mosquito Creek burned, MU Mosquito Creek unburned, BB Boundary Creek Birch, BS Boundary Creek Spruce).
- Site attributes include:
  - Elevation (160–970 m) and geographic coordinates (latitude/longitude).
  - Vegetation zone: Boreal across all sites.
  - Vegetation descriptions vary by site (post-fire recovery, understorey composition, etc.).
  - Disturbance/hydrology: notes on upland or wetland status; recent fires at some sites.
  - Permafrost zone (PF Zone): Sporadic or Discontinuous across sites.
  - Time windows for vegetation data collection (dates in 2013–2014) and for soil sampling (Aug 17–Sep 6, 2013; Aug 28–Sept 1, 2014).

## Data usage and related resources
- The dataset supports analysis of how vegetation and soil properties influence active-layer thickness in boreal permafrost soils.
- Related publication: Fisher et al. (2016) Global Change Biology, “The influence of vegetation and soil characteristics on active-layer thickness of permafrost soils in boreal forest.”
- Data can be used to:
  - Compare across sites and disturbance histories (burned vs. unburned; different tree/overtop vegetation).
  - Explore covariation between LAI (tree and understory), moss/OM thickness, soil moisture, slope, and active-layer thickness.
  - Build self-serve data products (dashboards, pivot-like reports) for stakeholders interested in boreal ecosystem conditions and permafrost dynamics.