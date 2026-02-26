# Exotic Plantations Increase Risk of Flooding in Mountainous Landscapes

- The dataset described supports the manuscript on ecohydrology and flood risk, focusing on how land cover affects rain-runoff response, carbon sequestration, and nutrient/sediment discharge.
- Location: Upper Nilgiris Reserve Forest, Tamil Nadu, in the Western Ghats (global biodiversity hotspot); headwaters of the Bhavani River.
- Timeframe: Data collected 2013–2016, with ongoing data collection through May 2020 for the broader program.
- Collaborators: Foundation for Ecological Research, Advocacy and Learning (Pondicherry), Ashoka Trust for Research in Ecology and the Environment (Bangalore), Lancaster Environmental Centre (UK), National Centre for Biological Sciences (Bangalore).

## Dataset contents

- DailyRainDischarge2014to2016.csv
  - Daily rainfall and discharge for eight small catchments; land cover data included.
  - Rainfall recorded with tipping bucket gauges (tips per minute converted to mm); discharge derived from water levels in streams.
- KSatLandCovers.csv
  - Hydraulic conductivity values under major land-cover types (Saturated hydraulic conductivity, Ks) measured with mini-disk infiltrometer.
- Dry-season data is excluded to emphasize extreme rain-event response.

## Fieldwork and instrumentation

- Rainfall
  - Tipping bucket rain gauges (Rainwise) deployed in grasslands and ridges on a ~1x1 km grid.
  - Data at 1-minute intervals; retrieved ~every two weeks.
  - Locations provided (latitude/longitude and elevation).
- Discharge
  - Eleven streams instrumented with stilling wells and capacitance-based water level recorders.
  - Water levels logged at 5-minute intervals; discharge calculated via velocity-area method (except unit 101, which uses a weir-based standard).

- Infiltration
  - Saturated hydraulic conductivity measured at multiple land-cover patches using a mini-disk infiltrometer.
  - GPS accuracy noted (~20 m) due to canopy and obstacles.
  - Site coordinates provided for Shola, Grassland, Pine, and Wattle patches.

## Calibration and quality assurance

- Rain gauge calibration annually; measuring tips per minute translated to mm per tip.
- Water level recorders calibrated per manufacturer guidelines; periodical calibration and validation.
- Mini-disk infiltrometer data quality controlled by multiple readings per sample; errors from air leaks discarded.
- Salt-dilution gauging (slug and constant-rate) used as parallel QA for discharge calculations.
- Data logs monitored for power interruptions; erroneous timestamps replaced with NULL values; cross-checks against a permanent scale for water levels.

## Data processing and reproducibility

- Data imported into R and aggregated to daily time steps.
- Comprehensive script suite documented (with detailed processing steps for rain gauges, water levels, and discharge):
  - Rain gauge processing: data import, calibration, null-value handling, aggregation to multiple time intervals, error checks.
  - Water level recorder processing: calibration, import, gap filling, merging nulls, aggregation.
  - Discharge processing: rating curves, velocity-area calculations, discharge calculation scripts.
  - Master control scripts coordinating all processing steps and reporting outputs.
- Outputs include CSVs and plots; scripts are organized to enable reproducible analysis and potential re-use for similar datasets.

## Data structure and variables

- Rain/runoff dataset (Table 5 description)
  - dt.tm: Timestamp (IST)
  - wlr: Water level recorder number
  - Discharge: Discharge (in appropriate units)
  - DepthDischarge: Depth of discharge
  - flowD: Daily flow (mm)
  - mm: Daily rainfall (mm)
  - PeakDischarge: Peak daily discharge
  - PeakDepthDischarge: Peak discharge depth
  - AMI: Antecedent moisture index (past 14 days)
  - area: Catchment area (hectares)
  - CircularityIndex: Basin geometry metric
  - slopeSteep: Slope steepness (UNESCO/SSLE)
  - drainDensity: Drainage density
  - catchment: Land cover category (Wattle, natural montane grasslands, shola)

- Saturated hydraulic conductivity dataset (Table 6)
  - Date: Sample collection date
  - Land.Cover: Land-cover type (wattle, pine, shola, grasslands)
  - LSAT: Measured LSAT value
  - K: Hydraulic conductivity (ms-1)

## Accessibility and usage

- The dataset and accompanying R scripts enable:
  - Reproducible processing of rainfall, water level, and discharge data
  - Creation of self-serve data products (tables, charts, dashboards)
  - Comparative analysis across land-cover types and catchments
- Addresses typical data-support challenges by providing:
  - Clear documentation of data collection, calibration, QA, and processing
  - A transparent pipeline to transform raw observations into daily metrics and outputs

## References

- The data collection and methods align with established instruments and protocols (RainWise tipping buckets, Dataflow Systems WLRs, mini-disk infiltrometer) and standard hydrological practices (velocity-area, weir-based discharge).