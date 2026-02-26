# Kinder Scout Rainfall and Discharge 2010-2021

## Overview
- Dataset of rainfall and runoff from three experimental microcatchments (0.4–0.8 ha) on Kinder Scout, UK, spanning 2010–2021.
- Purpose: assess impact of peatland restoration on storm flow response in upland peatlands.
- Experimental setup includes one non-restored control microcatchment and two restoration-treated microcatchments.

## Experimental design and regime
- BACI design: before-after-control-intervention.
- Microcatchments:
  - Firmin: unrestored control (no treatment throughout).
  - Olaf: restoration with revegetation.
  - Nogson: restoration with revegetation and gully blocking, later Sphagnum plug planting.
- Timeline:
  - Pre-intervention: 2010–2011.
  - Restoration: 2011–2012.
  - Additional Sphagnum planting at Nogson: 2015.
- Data collection: 2010–2021, continuous measurements at 10-minute timesteps; some gaps due to instrument failure.

## Data collection and processing
- Discharge measurement: v-notch weirs with pressure transducers in stilling wells; barometric compensation using a reference sensor above water to convert to water depth and discharge.
- Rainfall measurement: tip bucket rain gauges; each tip ≈ 0.2 mm rainfall; rainfall per 10-minute timestep derived from tip counts.
- Calibration: manual stageboard readings used to calibrate depth to v-notch height; data downloaded monthly.
- Data handling in-field: if a rain gauge failed in a microcatchment, rainfall data from a nearest microcatchment substituted; alt gauge used is documented.
- Equation for discharge:
  - Q = 0.01678 × (100 × h)^2.4331 (Q in litres per second, h in metres).

## Field equipment and calibration details
- Discharge: AquiStar SDI-12 pressure transducers.
- Rainfall: HOBO RG3-M rain gauges (186 cm² orifice; resolution 0.2 mm).
- Calibration approach: manual depth readings taken at download used to calibrate sensor depth to water height behind the V-notch.

## Data structure and format
- Timeframe: 2010–2021, continuous discharge and rainfall measurements; some irregular gaps.
- File organization: yearly CSV files named [site name]_[microcatchment name]_[year]_rainfall_discharge.csv (e.g., kinder_nogson_2015_rainfall_discharge.csv).
- Columns (same order in every CSV):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Discharge (L/sec): float64
  - Rainfall (mm): float64
  - Alt TBRG: string (name of alternative rain gauge used when needed)
  - Notes: string (field notes relevant to data)

## Data quality and limitations
- Quality checks: visual assessment of discharge records against rainfall to identify spurious observations (e.g., vegetation blocking the V-notch); such periods omitted and marked as no data.
- Rainfall substitutions: if a gauge failed, rainfall data from a functioning gauge substituted and the alternative gauge noted in Alt TBRG.
- Limitations: incomplete discharge records due to instrument failure; irregular gaps; patching of rainfall data across microcatchments may affect some analyses.

## Provenance and usage
- Data collection and processing managed by the Protect-NFM project (NERC grant NE/R004560/1).
- Experimental design and interpretation linked to published work:
  - Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge.
- Data intended to support analyses of how peatland restoration influences hydrological responses to rainfall, enabling self-contained examination of treatment effects across microcatchments.

## References
- Shuttleworth, E.L. et al. (2019). Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. Available at: https://doi.org/10.1016/j.hydroa.2018.100006.