# Exotic Plantations Increase Risk of Flooding in Mountainous Landscapes

- Purpose and context
  - Dataset used to derive results for the manuscript examining how exotic plant plantations influence flood risk in mountainous landscapes.
  - Focus on ecohydrology: how land cover affects rain-runoff response, carbon sequestration, and nutrient/sediment discharge.
  - Data collected 2013–2016 in the Upper Nilgiris Reserve Forest, Tamil Nadu, within the Western Ghats (Bhavani river headwaters). Dry-season data are not included.
  - Collaborative program across four organizations to sustain data collection (2013–May 2020).

- Data components
  - DailyRainDischarge2014to2016.csv
    - Daily rainfall and discharge for eight small catchments and land cover types during May 2014–Dec 2016.
    - Rainfall: tipping bucket gauges (tips per minute) converted to mm.
    - Water levels: stilling wells with capacitance-based loggers (converted to discharge via velocity-area methods).
  - KSatLandCovers.csv
    - Hydraulic conductivity (saturated) under major land covers in Upper Nilgiris.
    - Measured with mini-disk infiltrometer (2013–2016).

- Study area and collaborators
  - Upper Nilgiris Reserve Forest, Tamil Nadu; Nilgiris part of the Western Ghats, an important biodiversity hotspot and headwaters region.
  - Partner institutions: Foundation for Ecological Research, Advocacy and Learning (Pondicherry), Ashoka Trust for Research in Ecology and the Environment (Bangalore), Lancaster Environmental Centre (Lancaster University, UK), National Centre for Biological Sciences (Bangalore).

- Field instrumentation and data collection
  - Rainfall
    - Tipping bucket rain gauges (Rainwise) deployed on ridges in grasslands and clearings, arranged roughly 1x1 km grid.
    - Data captured at 1-minute intervals; retrieved about every two weeks.
    - Calibration performed annually (at end of dry season and before monsoon) to convert tips to mm.
  - Discharge
    - Water levels recorded at five-minute intervals across eleven low-order streams (1–3).
    - Stilling wells with capacitance probes; discharge calculated via velocity-area; unit 101 used a compound weir with standard discharge equations.
    - Catchment boundaries estimated from SRTM digital elevation model.
  - Infiltration
    - Saturated hydraulic conductivity measured at selected land-cover patches (grasslands, shola, pine, wattle) using mini-disk infiltrometer.
    - GPS positional accuracy around 20 m for non-grassland patches; coordinates provided for sampling sites.

- Calibration and quality assurance
  - Calibration and calibration checks per instrument:
    - Rain gauges calibrated with fixed volumes at known tip rates (3–4 tips/min).
    - Water level recorders calibrated per manufacturer guidelines.
    - Mini-disk infiltrometer procedures followed per manufacturer manual.
  - Quality assurance measures
    - Data logs checked for power interruptions and sensor errors; battery-change intervals recorded; erroneous readings replaced with NULL.
    - Stilling wells paired with permanent scales to correct placement errors.
    - Salt-dilution gauging (slug and constant-rate methods) used in parallel with velocity-area calculations for cross-validation.
    - Infiltrometer readings filtered to exclude air-leak errors; samples taken away from obstructions (stones, sticks).

- Analytical workflow and reproducibility
  - Data processing
    - Data imported into R and aggregated to daily time steps.
    - Detailed scripts and functions exist to process rain gauge, water level, and discharge data; daily, 15-day, and monthly aggregations produced; outputs include CSVs and plots.
    - Master scripts coordinate the processing; multiple specialized scripts handle calibration, import, gap-filling, aggregation, and plotting.
  - Data processing outputs
    - Rain/runoff dataset with timestamped observations, daily rainfall, daily discharge, peak discharges, and derived metrics (e.g., Antecedent Moisture Index).
    - Land-cover and catchment descriptors for each observation (area, circularity, slope, drain density, catchment type: Wattle, grasslands, shola).
  - Discharge and rating-curve components
    - Discharge calculations include rating-curve-based methods, flume/weir options, and plotting of discharge curves and outlier checks.

- Data structure and key variables
  - Rain/runoff dataset (Table 5)
    - dt.tm: timestamp (IST).
    - wlr: water level recorder identifier.
    - Discharge: discharge in m3 s-1.
    - DepthDischarge: depth of discharge in mm.
    - flowD: daily flow in mm.
    - mm: daily rainfall (mm).
    - PeakDischarge: daily peak discharge (m3 s-1).
    - PeakDepthDischarge: depth of discharge at peak flow (mm).
    - AMI: Antecedent Moisture Index (past 14 days rainfall-to-flow).
    - area: catchment area (ha).
    - CircularityIndex (CI): Ab/Ac, where Ab is basin area and Ac is area of a circle with the same perimeter.
    - slopeSteep: slope steepness factor (UN Soil Loss Equation).
    - drainDensity: drainage density (m/m^2).
    - catchment: land-cover category (Wattle, natural montane grasslands, shola).
  - Saturated hydraulic conductivity dataset (Table 6)
    - Date: sample date.
    - Land.Cover: land-cover type (wattle, pine, shola, grasslands).
    - LSAT: saturated hydraulic conductivity (m s^-1).
    - K: hydraulic conductivity (m s^-1).

- Limitations and notes for analysis
  - Dry-season data are excluded; dataset emphasizes extreme rain events.
  - Spatial scale includes 1x1 km rainfall grid with low-order catchments; boundaries estimated from SRTM DEM.
  - GPS accuracy for canopy patches is reduced (~20 m), which may affect precise localization of hydrological properties.
  - Data and methods are designed for exploring relationships between land cover and flood risk under extreme rainfall, suitable for developing and validating predictive models.

- Potential analytic opportunities for data-driven questions
  - Quantify how land-cover types (Wattle, grasslands, Shola) influence rainfall-runoff response and daily/peak discharges.
  - Assess relationships between hydraulic conductivity (K) and observed infiltration/runoff metrics across land covers.
  - Explore how Antecedent Moisture Index (AMI) modulates discharge behavior during extreme rainfall events.
  - Compare observed discharge from velocity-area methods with alternative rating-curve or weir-based calculations.
  - Integrate land-cover descriptors (area, slope, drainage density) to model flood risk at local scales.

- References
  - Includes supporting manuals and literature on instrumentation and hydrology methods (guidance from data loggers, infiltrometry, SRTM, and standard hydrology texts).