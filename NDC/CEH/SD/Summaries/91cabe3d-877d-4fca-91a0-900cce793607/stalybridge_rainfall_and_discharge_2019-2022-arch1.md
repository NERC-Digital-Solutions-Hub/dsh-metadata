# Stalybridge Rainfall and Discharge 2019-2022

## Overview
- Dataset of rainfall and runoff records from ten experimental microcatchments (A–J; 0.4–3.9 ha) on Stalybridge Moor, upland peatland, UK.
- Covers 2019–2022 with a Before-After-Control-Intervention (BACI) design to assess how different gully-blocking methods affect storm-flow response.
- Microcatchments include four unrestored controls (A, D, G, J) and six intervention sites with varying dam types and configurations.
- Data collection and processing conducted under the NERC Protect-NFM project; records span before and after gully-blocking interventions, with post-intervention design changes in specific microcatchments.

## Experimental design and interventions
- Control microcatchments: A, D, G, J (no gully blocking throughout the dataset).
- Intervention microcatchments and dam types:
  - B: 22 standard cobblestone dams.
  - C: 7 cobblestone dams (lower gully) + 13 peat dams (mid-upper reaches).
  - E: 10 piped-peat dams.
  - F: 6 standard peat dams.
  - H: 6 standard peat dams.
  - I: 20 timber dams.
- Pre-intervention period: May 2019–March 2020.
- Gully blocking works: 16–25 March 2020.
- Post-intervention: April 2020 onward, with subsequent design adjustments (notably in E and I) during 2020–2022 (details below).

- Post-restoration design changes (examples):
  - Microcatchment E: 25/03/2020–22/02/2021—open pipe diameters of 150 mm for piped-peat dams (except the lowest dam with 64 mm). From 22/02/2021, all piped-peat dams capped to a 64 mm open orifice.
  - Microcatchment I: 25/03/2020–27/01/2021—lower-most timber dam slot width changed from 150×40 mm to 50×40 mm; 27/01/2021 to 29/03/2021—further reductions of remaining timber dam slots to 50×40 mm.

## Data collection and measurement methods
- Continuous discharge measurement at 5-minute timesteps using v-notch weirs across erosional gullies; pressure transducers measure water depth behind the weir.
- Barometric pressure used to compensate transducer readings; depth converted to water height to compute discharge.
- Rainfall measured with tip bucket rain gauges (0.2 mm per tip).
- Field equipment: HOBO U20-001-04 pressure transducers; HOBO RG3-M rain gauges (186 cm² orifice; resolution 0.2 mm).
- Data collection frequency: May 2019–February 2022; occasional gaps from instrument failure; rainfall gaps filled with observations from the nearest microcatchment when needed.

## Data processing and calculations
- Depth readings calibrated against manual stageboard measurements at downloads.
- Discharge calculated from head using the empirical equation: Q = 0.01678 × (100 × h)^{2.4331} (Q in L/s; h in metres).
- Spatial references: v-notch weirs with UK grid references provided for A–J; rain gauges located in B, E, G, I with corresponding grid references.
- Data logged and downloaded monthly; rainfall and discharge stored per calendar year.

## Data structure and formats
- Data grouped by calendar year and microcatchment; CSV files named as: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: stalybridge_e_2021_rainfall_discharge.csv
- Columns (in each CSV, same order):
  - DateTime (GMT)
  - Rainfall (mm)
  - Discharge (L/sec)

## Quality control and limitations
- Visual checks of discharge data against rainfall to flag spurious readings (e.g., vegetation blocking the weir), with identified periods omitted (no data).
- Gaps due to instrument failure; some rainfall data patched from the nearest microcatchment when a gauge failed.
- Data notes include the potential for local-scale variability and management-induced changes in dam configurations influencing hydrological responses.

## Uses and potential analyses
- Designed to quantify how different gully-blocking methods alter stormflow response in upland peatland catchments.
- Suitable for BACI analyses to compare pre- and post-intervention responses between controls and interventions.
- Enables exploration of relationships between rainfall input and discharge output, and assessment of the influence of dam type and dam-slot modifications on peak discharge and timing.

## References
- Shuttleworth, E.L. et al. (2019). Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. https://doi.org/10.1016/j.hydroa.2018.100006