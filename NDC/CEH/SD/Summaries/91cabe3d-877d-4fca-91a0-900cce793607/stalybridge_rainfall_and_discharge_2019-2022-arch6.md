# Stalybridge Rainfall and Discharge 2019-2022

## Purpose and scope
- Dataset of rainfall and runoff records from ten experimental microcatchments (A–J) on Stalybridge Moor, upland peatland, UK.
- Collected to assess the impact of gully blocking methods on stormflow responses in peatland catchments.
- Part of the Protect-NFM project (NERC grant NE/R004560/1).
- Time span: 2019–2022 (pre- and post-intervention periods).

## Experimental design
- BACI design: Before (May 2019–Mar 2020), After (post-Mar 2020) with intervention implemented in Mar 2020.
- Microcatchments A, D, G, J: unrestored controls throughout the dataset.
- Interventions:
  - B: 22 standard cobblestone dams
  - C: 7 cobblestone dams (lower gully), 13 peat dams (upper/middle)
  - E: 10 piped-peat dams
  - F: 6 standard peat dams
  - H: 6 standard peat dams
  - I: 20 timber dams
- Post-restoration design changes occurred in E (pipe dam openings changed in 2020–2021) and I (timber dam slot modifications in 2021).

## Data collection and instrumentation
- Discharge: v-notch weirs with pressure transducers in stilling wells; continuous measurements at 5-minute timesteps.
- Rainfall: tip bucket rain gauges (0.2 mm per tip) in B, E, G, I.
- Calibration: barometric correction using an above-water sensor; manual stageboard readings for calibration to discharge.
- Recording period: continuous May 2019–Feb 2022; occasional gaps due to instrument failure.
- Data gaps: missing observations in discharge; rainfall gaps patched from nearest available microcatchment when a gauge failed.

## Data processing and calculations
- Converting water depth behind v-notch to discharge using site-specific calibration:
  - Q = 0.01678 × (100 h)^{2.4331}, where Q is discharge (L/s) and h is head above the v-notch (m).
- Data are corrected to reflect actual water depth and standardised to discharge in litres per second.
- Rainfall recorded as millimetres; rainfall gauge readings converted from tip counts.

## Data structure and access
- Data organized by calendar year and microcatchment, provided as CSV files.
- Filename pattern: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: stalybridge_e_2021_rainfall_discharge.csv
- Columns (consistent across files):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Rainfall (mm): rainfall observations (float64)
  - Discharge (L/sec): discharge observations (float64)

## Quality control and limitations
- Visual checks for spurious discharge events; periods with apparent errors (e.g., vegetation clogging the weir) removed and marked as no data.
- Gaps due to instrument failure; rainfall data gaps patched from nearest microcatchment when possible.
- Some microcatchments lack dedicated rainfall gauges; reliance on patches from other gauges in certain periods.
- Post-intervention data may reflect changes in dam configurations, which influence hydrological responses and comparability across periods.

## Variables and units
- Discharge: litres per second (L/s)
- Rainfall: millimetres (mm)
- Time resolution: 5-minute timesteps
- Geographic references: specific UTM/UK grid coordinates provided for each microcatchment and rainfall gauge

## Spatial and temporal reference
- Microcatchments labeled A–J (west to east) with precise UK grid references.
- Rain gauges positioned at B, E, G, and I with exact coordinates.
- Study period covers pre- and post-gully blocking interventions (May 2019–Feb 2022).

## References
- Shuttleworth, E.L. et al. (2019) Restorations in peat moorlands and their effects on stormflow: Journal of Hydrology X. https://doi.org/10.1016/j.hydroa.2018.100006

## Suggested uses and considerations for data users
- Evaluate the effect of different gully-blocking designs on stormflow peaks and timing across restored and control microcatchments.
- Compare pre- and post-intervention hydrological behavior, leveraging BACI design.
- Use consistent 5-minute data to analyze rainfall–discharge relationships, accounting for post-restoration design changes (especially in E and I).
- Account for data gaps and patching strategies; consider sensitivity analyses excluding periods with data quality concerns.
- Integrate with the Shuttleworth et al. (2019) framework to contextualize observed changes in peak discharge and delay of stormflow.