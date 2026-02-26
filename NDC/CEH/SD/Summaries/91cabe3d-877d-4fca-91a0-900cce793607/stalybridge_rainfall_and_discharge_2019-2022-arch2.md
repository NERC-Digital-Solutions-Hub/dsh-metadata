# Stalybridge Rainfall and Discharge 2019-2022

- Dataset of rainfall and runoff from ten experimental microcatchments (A–J) on Stalybridge Moor, an upland peatland in the UK.
- Timeframe spans 2019–2021/2022, including pre- and post-gully blocking to assess storm-flow responses; six microcatchments were blocked (treatment) and four remained as unrestored controls.
- Part of the Protect-NFM project; data collection led by field technicians with analysis by researchers.
- Discharge measured with v-notch weirs and pressure transducers; rainfall recorded by tip bucket gauges.
- Irregular data gaps occurred due to instrument failures; where rainfall gauges failed, nearby microcatchment observations patched in.

## Experimental design and interventions

- BACI (Before-After-Control-Intervention) design.
- Controls: microcatchments A, D, G, J (no gully blocking).
- Treatments: microcatchments B, C, E, F, H, I (gully blocking varied by site).
  - B: 22 standard cobblestone dams.
  - C: 7 cobblestone dams (lower gully) + 13 peat dams (middle/upper).
  - E: 10 piped-peat dams.
  - F: 6 standard peat dams.
  - H: 6 standard peat dams.
  - I: 20 timber dams.
- Gully blocking occurred 16–25 March 2020; post-intervention records begin April 2020.
- Post-restoration dam design changes:
  - E (pipeds-peat dams): 25/03/2020–22/02/2021 had open pipes (150 mm), lower dam had 64 mm; from 22/02/2021 all piped-peat dams capped to 64 mm open orifice.
  - I (timber dams): 25/03/2020–27/01/2021 timber dam slots 150 × 40 mm; 27/01/2021 lower dam slot constricted to 50 × 40 mm; 29/03/2021 remaining timber dam slots reduced to 50 × 40 mm.

## Data collection and processing

- Continuous rainfall and discharge data collected from May 2019 to February 2022 at 5-minute timesteps.
- Discharge: measured behind v-notch weirs via pressure transducers; depth converted to discharge.
- Rainfall: tip bucket gauges; 0.2 mm per tip.
- Calibration and corrections:
  - Barometric compensation using a separate barometer above water.
  - Manual stageboard readings to calibrate sensor depth to v-notch height.
  - Data loggers downloaded monthly; depth-to-discharge calibration applied.
- Data gaps:
  - Instrument failures caused missing observations; rainfall gaps patched from nearest microcatchment if needed.

## Data structure and access

- Data are provided per calendar year for each microcatchment in CSV format.
- Filename convention: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv (e.g., stalybridge_e_2021_rainfall_discharge.csv).
- Columns (in all files):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Rainfall (mm): rainfall observations (float64)
  - Discharge (L/sec): discharge observations (float64)

## Measurement methods and equations

- Discharge calculation: Q = 0.01678 × (100 × h)^{2.4331}, where Q is in litres per second and h is the head above the v-notch in metres.
- Equipment:
  - V-notch weirs with HOBO U20-001-04 pressure transducers (for water depth behind weirs).
  - Rainfall: HOBO RG3-M gauges with 186 cm² orifice delivering 0.2 mm resolution.

## Location and data quality

- Microcatchment locations labeled A–J with precise UK grid references provided for each site.
- Rain gauge locations provided for B, E, G, I microcatchments.
- Quality control:
  - Visual checks for spurious discharge observations.
  - Cross-checks with rainfall data (e.g., vegetation in the weir affecting readings).
  - Erroneous periods removed and flagged as no data.

## Related reference

- Shuttleworth, E. L. et al. (2019) Rest restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. DOI: https://doi.org/10.1016/j.hydroa.2018.100006

## Relevance for environmental monitoring and policy evaluation

- Provides standardized, longitudinal rainfall and discharge records suitable for assessing how restoration (gully blocking) and dam-type interventions influence stormflow in upland peatlands.
- Supports comparative analysis between treated and control microcatchments to evaluate effectiveness of nature-based flood management (NFM) strategies.
- Data quality measures and BACI design enhance reliability for monitoring environmental health and informing policy performance over time.