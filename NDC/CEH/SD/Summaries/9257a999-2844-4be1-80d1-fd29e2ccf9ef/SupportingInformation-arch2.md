# Exotic Plantations Increase Risk of Flooding in Mountainous Landscapes

## Overview and purpose
- Describes the dataset used to produce results in the manuscript on how exotic plantations influence flood risk in mountainous terrain.
- Focuses on ecohydrology data to study rain-runoff response, carbon sequestration, and nutrient/sediment discharge in the Upper Nilgiris, Tamil Nadu, a part of the Western Ghats.
- Data collected 2013–2016; dry-season data not included; ongoing data collection through May 2020 by multiple collaborating agencies.

## Dataset composition
- DailyRainDischarge2014to2016.csv
  - Daily rainfall and discharge for eight small catchments and land cover types during May 2014–December 2016.
  - Rainfall from tipping bucket gauges (tips per minute) converted to millimetres; water levels from capacitance-based loggers.
- KSatLandCovers.csv
  - Hydraulic conductivity under major land covers (Shola, Grassland, Pine, Wattle) in the Upper Nilgiris, measured with a mini-disk infiltrometer.
- Location context
  - Data collected in the Upper Nilgiris Reserve Forest, Western Ghats, headwaters of the Bhavani river (a Cauvery tributary).
  - Four research partners: Foundation for Ecological Research, Advocacy and Learning (Pondicherry), Ashoka Trust for Research in Ecology and the Environment (Bangalore), Lancaster Environmental Centre (Lancaster University, UK), National Centre for Biological Sciences (Bangalore).

## Fieldwork and instrumentation
- Rainfall data
  - Tipping bucket rain gauges (Rainwise) deployed on ridges and grasslands in a ~1x1 km grid; data logged every minute and retrieved biweekly.
  - Locations listed with precise coordinates.
- Discharge data
  - Water levels recorded at eleven low-order streams (five-minute intervals) using stilling wells and capacitance loggers.
  - Discharge conversion:
    - Most sites: velocity-area method.
    - Site 101: compound weir with standard discharge equations.
  - Catchment boundaries derived from SRTM DEM.
- Infiltration data
  - Saturated hydraulic conductivity measured with mini-disk infiltrometer at selected land-cover patches; ~20 m GPS accuracy for non-canopy patches.
  - Sites include Shola, Grassland, Pine, and Wattle patches.

## Calibration and quality assurance
- Calibration
  - Rain gauges calibrated yearly (end of dry season) using fixed-volume water pours.
  - Water level loggers calibrated per manufacturer guidelines.
  - Mini-disk infiltrometer used according to the manufacturer’s manual.
- Quality assurance procedures
  - Logs checked for power-related and contact issues; errors timestamped and replaced with NULL values.
  - Stilling wells paired with fixed scales to validate capacitance readings.
  - Salt-dilution gauging (slug and constant-rate) used in parallel with velocity-area methods for QA.
  - Rain and infiltration measurements underwent repeatable sampling with error-discard criteria (air leaks, adequate sampling distance from obstructions).

## Analytical methods and data processing
- Data management
  - Data imported into R and aggregated to daily time steps.
  - Comprehensive processing scripts documented (Workflow and functions described, including calibration, data import, gap-filling, aggregation, and reporting).
- Processing pipeline
  - Tipping Bucket Rain Gauges: data processing scripts to calibrate, fix dates, import raw data, fill gaps, aggregate at multiple time intervals, output CSVs and PNGs.
  - Water Level Recorders: master and specialized scripts for calibration, import, gap-filling, merging nulls, aggregation, and output.
  - Discharge calculations: scripts to manage rating curves, compute discharge from stage, and generate figures and reports.
  - Outputs include daily and aggregated rainfall and discharge data, and associated diagnostic figures.

## Data structure and key variables
- Rain/runoff dataset (Table 5)
  - dt.tm: Timestamp (IST)
  - wlr: Water level recorder number
  - Discharge: Discharge (m3 s-1)
  - DepthDischarge: Depth of discharge (mm)
  - flowD: Daily flow (mm)
  - mm: Daily rainfall (mm)
  - PeakDischarge: Peak daily discharge (m3 s-1)
  - PeakDepthDischarge: Depth at peak discharge (mm)
  - AMI: Antecedent moisture index (past 14 days)
  - area: Catchment area (hectares)
  - CircularityIndex: Basin circularity metric
  - slopeSteep: Slope steepness factor (for Universal Soil Loss Equation)
  - drainDensity: Drainage density
  - catchment: Catchment land cover (e.g., Wattle, grassland, shola)
- Saturated hydraulic conductivity dataset (Table 6)
  - Date: Sample date
  - Land.Cover: Land cover category (wattle, pine, shola, grassland)
  - LSAT: Saturated hydraulic conductivity
  - K: Hydraulic conductivity (m s-1)

## Geographic and ecological context
- Location: Upper Nilgiris, Tamil Nadu, India; part of the Western Ghats biodiversity hotspot.
- Hydrology: Headwaters of Bhavani River, significant for regional water resources and flood risk assessment.
- Land cover focus: Exotic plantations (Wattle, Pine) vs. natural montane grasslands and shola forests; investigation of land cover effects on rainfall-runoff and flood risk.

## Reuse, interoperability, and accessibility
- Data and processing scripts are organized to standardize outputs (CSV and PNG formats) and facilitate reproducibility.
- Emphasizes the need to couple this dataset with additional data sources to enhance utility and policy analysis, aligning with the archetype’s aim to increase dataset value and enable broader access.

## Limitations and notes
- Dry-season data not included; dataset emphasizes extreme rainfall events.
- GPS precision for non-canopy patches ~20 m, which may influence site-specific inferences.
- Some references and sources noted for methods and equipment; standard methodology adhered to (e.g., velocity-area, infiltrometry, salt dilution, rating curves).