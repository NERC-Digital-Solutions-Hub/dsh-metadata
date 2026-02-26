# Extensive_Vegetation_and_Soil_Data.csv

## Overview
- A stratified ecological and soil survey focusing on covariation between vegetation and edaphic characteristics.
- Data collected at sites in Yukon (2013) and Northwest Territories (2014), Canada.
- Key measurements include leaf area index (LAI), moss and organic matter thickness, and surface and deeper soil moisture.
- Data are organized by 24–30 x 1 m² plots per site and identified by data codes described in Table 1.
- Site and plot details (location, coordinates, elevation, vegetation type, disturbance status) are provided (Table 2).

## Spatial coverage and data structure
- Sites represented: Firefox burned (FFB), Firefox unburned (FFU), Boundary Creek Birch (BB), Boundary Creek Spruce (BS), Mosquito Creek burned (MB), Mosquito Creek unburned (MU), Blackfox (BF).
- Each site has GPS coordinates (Latitude, Longitude) and elevation; vegetation zone consistently boreal.
- Data codes and their descriptions are organized in Table 1 (data dictionary).
- Core variables include: ALD (thaw depth), slope, Tree_LAI, Understorey_LAI, OM_thick, Moss_thickness, OM_and_Moss_thickness, DeepMoist, SurfMoist, Height, Region, Site, Plot, GPS.N, GPS.W, LAI.

## Data collection methods and instruments
- Tree canopy LAI (LAI_Tree): 9 photographs per plot taken ~1 m above ground with a hemispherical lens; processed with CAN-EYE; sunlit conditions controlled via thresholding and shading as needed; measurements taken late in the day when possible.
- Understory LAI (LAI_U): measured with LI-COR LAI2000; one above canopy, four at plot corners; 90° FOV cap minimizes cloud effects; shading used when necessary.
- Understorey height: mean of five measurements across a 0.5 x 0.5 m quadrat.
- Moss thickness: measured by removing moss/organic layer and determining the moss thickness from moss surface to base of dead moss.
- Surface moisture (SurfMoist): measured in upper ~6 cm using ML3 ThetaKit; readings target moss/soil surface; factory calibration used for deeper readings.
- Deeper soil moisture (DeepMoist): measured at ~11–16 cm depth; four readings per plot across the growing season; mean used; calibration relies on factory settings due to variability.
- Organic matter thickness (OM_thick): measured to base of O horizon with a soil core; moss thickness subtracted.
- Slope: measured along the steepest gradient using a 50 cm plank and a digital angle meter.
- Active-layer thaw depth (ALT): measured with a stainless steel rod; temperature confirmed at 0°C; plots with >0°C excluded from analysis.
- All methods emphasize consistency and attempts to minimize environmental and measurement biases.

## Table-based data references
- Table 1: Explanation of data codes used in the data file.
- Table 2: Site details, including location, elevation, vegetation description, disturbance/hydrology, permafrost zone, and time stamps for vegetation and soil sampling.

## Site details (Table 2 highlights)
- Site names and locations: 
  - Firefox burned (FFB) – Whitehorse, Yukon; boreal vegetation; sporadic permafrost zone.
  - Firefox unburned (FFU) – Whitehorse, Yukon; boreal; sporadic permafrost zone.
  - Blackfox (BF) – Whitehorse, Yukon; boreal; sporadic permafrost zone.
  - Mosquito Creek burned (MB) – Yellowknife, Northwest Territories; boreal; discontinuous permafrost.
  - Mosquito Creek unburned (MU) – Yellowknife, Northwest Territories; boreal; discontinuous permafrost.
  - Boundary Creek Birch (BB) – Yellowknife, Northwest Territories; boreal; discontinuous permafrost.
  - Boundary Creek Spruce (BS) – Yellowknife, Northwest Territories; boreal; discontinuous permafrost.
- For each site: precise latitude, longitude, elevation, vegetation description (e.g., Betula glandulosa with certain post-fire characteristics; black spruce with understory moss), disturbance/hydrology (upland, recent fire, etc.), and permafrost zone (sporadic or discontinuous).
- Time of vegetation sampling and time of soil sampling are listed per site (e.g., early August 2013 for vegetation; August–September 2013 and August–September 2014 for soil).

## Temporal coverage
- Vegetation sampling: primarily early August 2013 (with some sites around late July 2013 or early August 2013 windows).
- Soil sampling: August 17 to September 6, 2013; August 28 to September 1, 2014.
- The study design provides seasonal cross-checks across the boreal sites to relate vegetation structure to soil moisture and organic layer properties.

## Data quality, standards, and limitations
- LAI measurements require careful control of sunlight; steps taken to standardize conditions (thresholding, shading).
- LAI_U aims to separate vascular understory from moss layer; method attempts to minimize sunlight effects via narrow FOV and shading.
- DeepMoist readings rely on factory calibration due to small-scale variability; multiple readings per plot averaged to reduce noise.
- ALT measurements exclude plots where thaw is not at 0°C to ensure comparability of active-layer assessments.
- Data description emphasizes that additional details and context are provided in the accompanying references (e.g., Fisher et al., 2016) for the influence of vegetation and soil characteristics on active-layer thickness.

## GIS applications and data products
- Per-plot geospatial dataset suitable for map-based visualization of vegetation structure, soil moisture regimes, and organic layer thickness across boreal sites.
- Facilitates exploration of spatial relationships between LAI (tree and understory), moss/organic layers, moisture profiles, slope, and thaw depth.
- Data can be linked to site polygons or raster layers to support ecological modelling, climatology studies, land management decisions, and policy analyses in northern Canada.
- The accompanying data dictionary (Table 1) and site details (Table 2) support consistent coding and integration into GIS workflows.

## References and notes
- Primary methodological reference: Fisher et al. 2016, Global Change Biology, on the influence of vegetation and soil characteristics on active-layer thickness in boreal forests.
- The dataset includes Table 1 (data codes) and Table 2 (site details) for reproducibility and integration into GIS analyses.