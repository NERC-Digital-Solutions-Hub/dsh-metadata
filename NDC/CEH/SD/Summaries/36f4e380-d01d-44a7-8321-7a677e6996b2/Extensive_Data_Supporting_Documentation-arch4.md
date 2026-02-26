# Extensible_Vegetation_and_Soil_Data.csv

- Overview
  - A stratified survey of ecological and soil states conducted at sites in Yukon (2013) and Northwest Territories (2014), Canada.
  - Aims to map extensive variability and covariation between vegetation and edaphic characteristics at fine spatial scales (24–30 x 1 m2 plots per site).
  - Data support analyses of boreal vegetation–soil interactions and active-layer conditions in permafrost regions.

- Data collected and key variables
  - ALD: Late August thaw depth (active layer thickness) measured from the moss layer bottom.
  - Slope: Ground surface incline in degrees along the steepest slope.
  - Tree_LAI: Leaf Area Index of the tree canopy.
  - Understorey_LAI (LAI U): Understory vegetation LAI (vascular plants only; moss layer excluded).
  - OM_thick: Thickness of the organic matter layer.
  - Moss_thickness: Total moss layer thickness (live + dead).
  - OM_and_Moss_thickness: Combined thickness from moss surface to the mineral layer.
  - DeepMoist: Deeper soil moisture (11–16 cm below surface) in the moss/organic layer.
  - SurfMoist: Surface soil moisture (upper 6 cm) in late August.
  - Height: Mean maximum understory vegetation height from multiple measurements.
  - Region, Site, Plot: Categorical/location identifiers for each plot.
  - GPS.N, GPS.W: Geographic coordinates (degrees north, degrees west).
  - LAI: Total Leaf Area Index (general descriptor).
  - Additional context from Table 2 includes site-specific descriptors such as location, elevation, vegetation zone, disturbance history, and permafrost zone.

- Data collection and processing methods
  - Tree_LAI: Calculated from nine 1 m above-plot photographs using a Nikon D5000 with hemispherical lens; CAN-EYE software outputs LAI Tree, with thresholding to standardize light conditions.
  - Understorey_LAI: Measured with a LI-COR LAI-2000 Plant Canopy Analyzer; measurements above and around the plot center to isolate vascular plant contribution; shading control to minimize sun condition effects.
  - Understorey height: Height measured at five points (four corners + center) within a 0.5 x 0.5 m quadrat; mean used in analyses.
  - Moss thickness: Determined by removing a moss/organic section and measuring depth to where dead moss loses discernible structure.
  - Surface and deeper moisture: Measured with ML3 ThetaKit probes; surface moisture in upper moss/soil layer; deeper moisture at ~11 cm depth (volume ~11–16 cm below surface); multiple readings per plot averaged.
  - OM thickness: Measured with a 1.8 cm diameter soil corer to the base of the O horizon; moss thickness subtracted to yield organic matter depth.
  - Slope and ALT: Slope measured with a 50 cm plank and digital angle meter; ALT measured with a stainless steel rod to point of refusal, with a temperature probe confirming 0 °C for frozen conditions; plots where temperatures exceeded 0 °C were excluded from analysis.
  - Quality and calibration notes: Moisture readings relied on factory calibrations due to within-plot variability; data collection times and procedures were standardized to minimize daylight and cloud-condition effects.

- Site details (Table 2)
  - Sites span Whitehorse, Yukon Territory, and Yellowknife, Northwest Territories, with multiple site names indicating post-fire and unburned conditions.
  - Key attributes captured: latitude, longitude, elevation, vegetation zone (boreal/tundra boreal), vegetation description, disturbance/hydrology, permafrost zone (sporadic or discontinuous), and specific data collection time windows for vegetation and soil sampling.

- Metadata, codes, and documentation
  - Data codes are explained in Table 1 (e.g., ALD, LAI, etc.) to clarify measurement descriptions and units.
  - Site details are recorded for reproducibility and cross-study comparability, including precise coordinates and environmental context.
  - The study and methods are linked to external publication for detailed methodology and validation: Fisher et al. 2016, Global Change Biology, on vegetation and soil influences on active-layer thickness in boreal forests.

- Data governance and interoperability considerations for Data Leaders
  - Comprehensive, system-wide metadata enabling discoverability and reuse (variables, units, collection methods, sampling times, site identifiers).
  - Clear data provenance with tool-specific measurement protocols and calibration remarks for reproducibility.
  - Potential data gaps to consider: regional coverage limited to two Canadian boreal regions; variability in site disturbance histories may affect comparability; calibration considerations for moisture probes noted due to within-plot variance.
  - Opportunities for co-ownership with policy colleagues and partners by sharing standardized data codes, measurement protocols, and site-context metadata (facilitating cross-network analyses and integration with broader data ecosystems).

- Practical implications and potential uses
  - Enables analysis of relationships between vegetation structure (LAI, height) and soil properties (moisture, organic matter thickness, active-layer depth) across boreal sites.
  - Provides a framework for benchmarking data collection methods and metadata schemas across networks, supporting data quality, standardization, and discoverability.
  - Supports studies of post-disturbance recovery (e.g., post-fire conditions) and their impact on vegetation–soil dynamics and permafrost stability.