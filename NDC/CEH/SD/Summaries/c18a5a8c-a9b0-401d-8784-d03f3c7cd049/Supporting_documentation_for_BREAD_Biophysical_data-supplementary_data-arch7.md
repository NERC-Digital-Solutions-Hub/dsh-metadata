# IPORE Soil Measurements Protocol

- Purpose and GIS relevance
  - Describes a randomized, multi-site soil sampling regime designed for mapping and analysis of soil water content, pore water conductivity, and soil temperature across smallholder farms.
  - Data are organized for integration into GIS workflows (spatial units, hierarchical design, temporal series).

## Experimental and sampling design

- Sampling framework
  - Within each household, soil sampling occurs in three fertility zones: Home (near the house), Near (between home and far field), and Far (far from house).
  - Two kebeles (districts) sampled: Konicha and 1st Choroko.
- Hierarchical structure and replication
  - Replication planned at multiple levels with three to six replicates per fertility zone depending on tier.
  - Measurements taken from multiple measurement sites per household and across fertility zones.
- Spatial and depth resolution
  - Depths sampled in each site: 0-5 cm, 5-10 cm, and 10-15 cm.
  - Each fertility zone includes three replicates per site.
- Temporal resolution
  - Monthly measurements recorded from January through July for each parameter.

## Data collection and measurement details

- Sampling locations and randomization
  - Randomly positioned measurements within each fertility zone and area to capture spatial variability.
- Field measurement protocol
  - Measurements collected with the W.E.T sensor, calibrated for the soil type in use.
  - Randomized placement of samples and three replicates per area to account for spatial variability.
- Sensor and field setup
  - W.E.T sensor used to measure soil water content, pore water electrical conductivity, and temperature.
  - Calibration and field setup steps provided to ensure consistency across sites and users.

## Calibration procedures (W.E.T sensor)

- Soil water content calibration
  - Two-point calibration using damp and dry soil samples.
  - Steps include measuring soil permittivity at wet/dry states, weighing damp/dry soil, and calculating calibration constants (b0, b1) for custom soil types.
  - Calibration values loaded as Custom 1 in the sensor, ensuring field measurements reference the correct soil type.
- Pore water electrical conductivity calibration
  - Calibration involves preparing a soil-water solution, measuring conductivity and permittivity in solution, and deriving parameters to estimate EC in field conditions.
  - Calibration constants loaded into the sensor (Custom 1) for field use.
- Operational notes
  - After calibration, select Custom 1 soil type in the sensor's soil type menu during field measurements.
  - Sensor can provide water content, temperature, and EC readings with predefined accuracy targets.

## Quality control and data management

- Field QA/QC
  - Random replicates (three per area) used to address spatial variability.
  - Periodic calibration checks in saline solutions to ensure sensor accuracy.
  - Data collected by experienced field scientists; immediate data upload to tablet via ODK to minimize data loss and mislabeling.
- Data handling and labeling
  - Soil samples labeled and stored; note: some label-related losses (<5%) occurred.
  - Strict adherence to SOPs for all laboratory and field procedures.
- Data quality and distribution
  - Sensor accuracy: ~5% for water content, ~1.5°C for temperature, ~10 mS/m for EC.
  - Data checked for statistical distribution; results reported as normally distributed.

## Data files and column structures

- IPORE-Soil EC.csv
  - Columns include: Sample number, Household number, District (Kebele), Household ID, Fertility Zone (Home/Near/Far), Top depth (cm), Bottom depth (cm), Replicate number, and monthly pore water conductivity (mS/m) columns for January–July.
- IPORE-Soil water.csv
  - Columns include: Sample number, Household number, District (Kebele), Household ID, Fertility Zone, Top depth, Bottom depth, Replicate number, and monthly volumetric water content (%) columns for January–July.
- IPORE-Soil temperature.csv
  - Columns include: Sample number, Household number, District (Kebele), Household ID, Fertility Zone, Top depth, Bottom depth, Replicate number, and monthly soil temperature (°C) columns for January–July.

- Common metadata across files
  - Each row represents a measurement site within a fertility zone of a specific household, with depth range and replicate identifier.
  - Monthly measurements span January to July, enabling temporal GIS analyses of soil moisture, EC, and temperature at varying depths.

## GIS considerations and recommended data products

- Spatial units and join keys
  - Use kebele (district), household ID, fertility zone, and measurement site to join field data to GIS layers (household points, parcel polygons, and zone buffers).
- Temporal dimension
  - Integrate monthly measurements as time-series layers or as attributes with time indexes for dynamic mapping.
- Depth stratification
  - Represent depth as a discrete attribute (Top depth / Bottom depth) or as separate layers per depth interval for soil property maps.
- Data standards and interoperability
  - Ensure consistent units (EC in mS/m, WC in %, Temperature in °C, depths in cm) and consistent categorical codes for fertility zones.
- Potential GIS products
  - Maps of spatial variability in soil moisture, EC, and temperature across households and zones.
  - Temporal dashboards showing changes from January to July by depth and fertility zone.
  - Layered datasets suitable for interpolations (e.g., kriging) or for integration with other soil/land-use layers.

Appendix notes (practical for GIS deployment)
- Data are organized by household and zone across two kebeles, enabling hierarchical analyses.
- Randomized sampling and multiple replicates support robust GIS-based assessments of spatial heterogeneity.
- Data quality control measures and calibration details should be documented in metadata accompanying GIS datasets.