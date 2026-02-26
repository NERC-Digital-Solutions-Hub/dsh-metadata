# Field Study Sites:

- This dataset compiles CO2 efflux and hydraulic measurements from six field sites across Scotland and the Amazon, collected over multiple years to capture a range of seasons and flow conditions. Sampling locations within each site were chosen to represent different flow intensities.

## Study sites and sampling design

- Scotland
  - River Kelvin (RK): 335 km2 semi-urban catchment; coordinates 55°52'06"N, 4°17'16"W; 18 m.a.s.l.; land use ~23% urban, ~70% agricultural, ~6% forestry; sampling within a 30 m reach ~1.2 km upstream of Clyde Estuary confluence; bankfull width 15–20 m; bed with large pebbles and exposed bedrock.
  - Drumtee Water (DW): headwater, 9.6 km2; peat-dominated; coordinates 55°41'16"N, 4°23'37"W; 197 m.a.s.l.; rough grazing; max elevation 260 m; sampling in a 19 m reach; channel width 4–5 m.
- Amazon
  - Main Trail (MT): catchment ~5 km2; active mainly during the rainy season; sampling point channel width 4–7 m; influenced by surface runoff and throughflow.
  - New Colpita (NC): perennial small stream, ~7 km2; channel width 4–7 m; seasonal variation in width/flow.
  - La Torre river (LT): catchment ~2000 km2; sampling point near confluence with Tambopata river; channel width 40–80 m.
  - Tambopata river (TP): catchment ~14,000 km2; sampling point ~200 m wide; catchment includes small-scale agriculture and gold mining; predominantly rainforest.
- Periodicity
  - RK and DW: regularly from June 2012 to December 2013, weekly to every three weeks, covering four seasons and diverse flow conditions.
  - MT, NC, LT, TP: field campaigns Feb–Apr 2011, Sept–Dec 2011, and Mar–May 2012; multiple campaigns to capture wet and dry seasonal variation.
- Sample counts (as per Table 1)
  - CO2 efflux samples: DW 79, RK 83, MT 42, NC 46, LT 37, TP 26.
  - Mean flow velocity samples: DW 75, RK 87, MT 41, NC 46, LT 37, TP 26.
  - Water depth samples: DW 77, RK 87, MT 42, NC 45, LT 34, TP 26.
  - pCO2 samples: DW 57, RK 58, MT 42, NC 46, LT 36, TP 26.
  - [DIC] samples: DW 57, RK 58, MT 42, NC 37, LT 36, TP 26.
  - pH measurements: DW 79, RK 87, MT 42, NC 46, LT 37, TP 26.
  - Water temperature: DW 79, RK 86, MT 42, NC 46, LT 37, TP 26.

## Measurements and methods

- CO2 efflux
  - Measured as the rate of CO2 accumulation in a floating chamber (volume 0.0029 m3) with a closed-loop system; reactor: Licor LI-840A for CO2/H2O; flow rate 0.3–1.0 L/min; measurement over four minutes, repeated three times.
  - Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)), where δCO2/δt is the slope of CO2 accumulation (μatm s-1), V is chamber volume (m3), R is gas constant, T is air temperature (K), and S is chamber surface area (m2).
  - Surface state during measurement was qualitatively assessed as smooth, medium, or rough; wind speed not directly measured.
  - Amazon sites lacked contemporaneous Re and Fr calculations due to data limitations.
- Hydraulic parameters
  - Velocity measured with a Valeport flow meter (50 mm impeller), 60 s averaging, at 20% and 80% of flow depth, plus at least three other depths for outlier detection to derive depth-averaged mean velocity (ū).
  - Fr (Froude number) and Re (Reynolds number) calculated to characterize surface disturbance and turbulence, indicative of gas transfer and mixing.
  - In UK sites, the field measurements included depth-averaged hydraulic parameters; Amazon sites did not provide Re and Fr data.
- Water chemistry
  - pH, conductivity, and temperature measured in situ with Troll instruments (9000 for DW and RK, 9500 for MT/NC, LT/TP) with calibration frequencies noted.
  - pH: continuous logging at DW (30-minute resolution) to minimize post-sampling alteration; RK pH was calculated from a discharge–pH relationship due to instrument issues.
  - Dissolved inorganic carbon ([DIC]) analyzed from water samples collected within 15 minutes of flux measurements, stored in pre-acidified exetainers, and analyzed later with a Thermo-Fisher Gas Bench/Delta V Plus.
  - pCO2 calculated from [DIC], pH, and temperature.
- Instrument calibration
  - Troll 9000: calibrations ~every 5 weeks (two-point: pH 4 and 7).
  - Troll 9500: calibrations ~monthly (two-point: pH 4 and 7); electrolyte top-up if needed; field cleaning weekly.
- Data collection and QA
  - Water chemistry data collected contemporaneously with CO2 flux measurements; samples for DIC analyzed within six months.
  - Data gaps due to equipment failure, high flow, or dry-season stream drying (MT).
  - DIC and pCO2 missing for June 2012–January 2013 at DW/RK due to late start of DIC sampling; MT dried during dry season, prohibiting sampling Sept–Nov 2011.

## Data structure and quality control

- Dataset format: 11 columns in a single Excel spreadsheet titled “CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13.csv” (NA indicates missing values).
- Columns include:
  - Date (dd/mm/yyyy)
  - Region (Amazon or Scotland)
  - Site (stream name)
  - Mean CO2 efflux (μmol CO2 m-2 s-1)
  - SD of mean CO2 efflux
  - Flow (m s-1)
  - Water depth (m)
  - pCO2 (μatm)
  - [DIC] (mM C)
  - pH
  - Water temperature (°C)
- Data quality notes:
  - All measurements were within method detection limits when available.
  - Some datasets have missing values due to planned sampling gaps, equipment malfunction, or environmental conditions (e.g., MT drying up).
  - Missing data indicated as NA.

## Data usage and relevance for environmental monitoring

- The dataset provides a standardized, cross-site representation of CO2 efflux and hydraulic conditions across diverse catchments (semi-urban/peat-dominated Scotland; tropical Amazonian rivers).
- Enables analysis of hydraulic controls (Fr, Re, ū) on CO2 exchange with the atmosphere and the potential influence of water chemistry (pH, [DIC], pCO2) on fluxes.
- The inclusion of seasonal campaigns and repeated measurements supports temporal trend assessment and policy/performance scrutiny for environmental monitoring programs.
- Data management emphasis: careful QA, calibration, and documentation of methods to ensure reproducibility and integration with other standardized monitoring datasets.

## References and instrumentation details

- Key methodological references and instrument calibrations are provided for CO2 flux calculations, pH/chemistry measurements, and [DIC] analyses.
- Instrument examples: Licor LI-840A for CO2/H2O, Troll 9000/9500 for pH and water chemistry, Valeport flow meter for velocity.
- Data source file: CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13.csv.