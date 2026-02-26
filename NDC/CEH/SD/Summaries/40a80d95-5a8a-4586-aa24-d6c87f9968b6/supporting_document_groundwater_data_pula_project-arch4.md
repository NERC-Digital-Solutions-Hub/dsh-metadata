# A brief description/overview of the data being described

- Dataset: PULA Groundwater folder containing 25 files with in situ groundwater measurements from the Gaborone catchment, Botswana.
- Time period: May 2017 – June 2018.
- Collaborators and funding: Botswana Department of Water Affairs, Botswana International University of Science and Technology, University of Aberdeen; NERC PULA project funding.
- Purpose: Understand long-term groundwater response to the 2016–2017 floods, assess spatial variability and impacts on water quality across groundwater and surface water systems.
- Sampling design: Combines spatial coverage (22 boreholes) with high-temporal-resolution monitoring (3 boreholes) to capture flood-drought-flood cycles and spatial heterogeneity.
- Data quality and constraints: Logistical and budget constraints caused incomplete near-monthly datasets and some equipment failures; data quality controlled with cleaning of obvious errors.

## Data content and structure

- Data files: 25 total; split into two data collection strategies.
  - Strategy 1: 22 near-monthly manual measurements (PULA_GW_level_physicochem_*.csv) across boreholes.
  - Strategy 2: 3 high-temporal-resolution timeseries (PULA_GW_timeseries_*.csv) at 5-minute intervals.
- Parameters measured:
  - Strategy 1: groundwater depth (GWD), pH, temperature (T), electrical conductivity (EC), total dissolved solids (TDS).
  - Strategy 2: groundwater depth (GWD), temperature (T), and EC (when available).
- Data structure:
  - Strategy 1 files: 7 columns — measurement date, time, GWD (m), pH, T (°C), EC (µS/cm), TDS (ppm).
  - Strategy 2 files: 5 columns — measurement date, time, GWD (m), T (°C), EC (µS/cm).

## Experimental design and field methods

- Strategy 1 (spatial mapping):
  - 22 boreholes distributed to cover spatial variability around the catchment.
  - Monthly or coarser sampling; multiple measurement parameters per borehole.
  - Campaigns aligned with flood-drought-flood cycles.
- Strategy 2 (high-temporal monitoring):
  - 3 boreholes instrumented with automatic dataloggers for 5-minute time steps.
  - Parameters recorded: GWD, T, and EC (EC in some wells).
- Locations and borehole details are provided in a Table 1 (names, coordinates, measurement periods, and parameters).

## Instruments, calibration and data processing

- Strategy 1 instruments:
  - GWD: Hydrotechnik dipmeter (accuracy 0.01 m).
  - pH, T, EC, TDS: Hanna HI-98129 portable tester (calibration with factory settings; pH δ 0.01; T 0.1 °C; EC 1 µS/cm; TDS 1 ppm).
- Strategy 2 instruments:
  - GWD: Solinst Levelogger (Model 3001; accuracy 0.001 m).
  - T: Solinst Levelogger (accuracy 0.001 °C).
  - EC: Solinst Levelogger (accuracy 0.1 µS/cm).
- Calibration and data processing:
  - GWD: calibrated with manual dipmeter during download; Strategy 2 uses barometric-corrected water head.
  - All other variables: factory calibration.
  - Barometric compensation and conversion to freshwater head performed using a Barologger (at Otse-ramotswa landfill BH2) and linear interpolation with Strategy 1 dates.
  - Depth corrections applied using Strategy 1 measurements and interpolation.
- Data processing timeline: eight download occasions spanning 2017–2018.

## Quality control and data documentation

- Quality checks: screened for obvious measurement errors and anomalies (field notes, datalogger issues).
- Cleaning: erroneous records removed manually.
- Calibration and units: clearly documented per parameter and strategy; consistent units across files.

## Data accessibility and context

- Geographic context: measurements scattered across the Gaborone Reservoir catchment, southwest Botswana; variable geology and land use.
- Data provenance: collected by a collaborative project involving national and academic institutions; data curated for long-term groundwater and water-quality assessment.
- Potential uses: evaluating groundwater response to extreme rainfall and floods, comparing surface and groundwater responses, supporting data-driven water management and policy analysis for diverse audiences.

## Key limitations and considerations for use

- Data gaps: near-monthly (Strategy 1) datasets are incomplete due to logistical and equipment issues.
- Temporal coverage: Strategy 2 provides high-frequency data for only three boreholes, limiting broad temporal generalization.
- Metadata completeness: Table 1 and sampling details are provided, but users should verify borehole-specific timings and parameters when integrating datasets.
- Suitability for analysis: data require barometric and depth-correction steps; ensure consistent processing when combining Strategy 1 and Strategy 2 records.