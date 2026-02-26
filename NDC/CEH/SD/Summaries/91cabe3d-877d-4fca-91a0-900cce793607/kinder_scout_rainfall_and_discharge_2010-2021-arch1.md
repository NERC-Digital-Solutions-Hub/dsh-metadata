# Kinder Scout Rainfall and Discharge 2010-2021

- Dataset of rainfall and runoff records from three experimental microcatchments (0.4-0.8 ha) on Kinder Scout, upland UK peatland
- Time period: 2010–2021, capturing peatland degradation and restoration phases
- Purpose: determine impact of peatland restoration on storm flow response in upland peatlands

## Experimental design

- Study design: Before-After-Control-Intervention (BACI)
- Firmin: unrestored control microcatchment
- Olaf: revegetation during restoration works
- Nogson: revegetation + gully blocking, later with Sphagnum plug planting
- Intervention timeline:
  - Pre-intervention: 2010–2011
  - Restoration: 2011–2012
  - Additional Sphagnum planting at Nogson: 2015
- Data collection period for all three: June 2010–December 2021

## Data collection and processing

- Measurements:
  - Discharge recorded at v-notch weirs with pressure transducers in stilling wells
  - Rainfall recorded with tip-bucket rain gauges
- Sampling: continuous measurements at 10-minute timesteps
- Gaps: irregular gaps due to instrument failure; when rain gauge failed, data patched from the nearest alternative gauge
- Calibration: barometric compensation applied to sensor depth to convert to water depth; manual stageboard readings used for calibration
- Data management: monthly data logger downloads; depths used to calibrate discharge heights

## Methods and calculations

- Discharge conversion:
  - Q = 0.01678 (100 h)^{2.4331}, where Q is discharge (L/s) and h is water depth above the v-notch (m)
- Rainfall measurement: tip bucket counts converted to millimeters (each tip = 0.2 mm)
- Data validation: visual checks for spurious discharge (e.g., vegetation blocking the weir); periods with erroneous data omitted
- Alternative rainfall data: if a gauge failed, rainfall from a functioning gauge substituted; the alternate gauge name recorded in Alt TBRG

## Equipment and calibration details

- Discharge measurement: AquiStar SDI-12 pressure transducers; v-notch weirs
- Rainfall measurement: HOBO RG3-M rain gauges with 186 cm² orifice
- Calibration: manual stageboard readings used to align sensor depth with measured water depth; barometric correction applied using an above-water pressure transducer

## Data structure and access

- Data format: rainfall and discharge records per calendar year for each microcatchment
- File naming convention: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: kinder_nogson_2015_rainfall_discharge.csv
- CSV columns (in order):
  - DateTime (GMT): timestamp (YYYY-MM-DD HH:MM:SS, string)
  - Discharge (L/sec): discharge observations (float64)
  - Rainfall (mm): rainfall observations (float64)
  - Alt TBRG: name of any alternative rain gauge used (if applicable)
  - Notes: field notes relevant to data

## Data quality and limitations

- Strengths:
  - BACI framework enabling assessment of restoration impacts on stormflow
  - Continuous high-resolution (10-minute) data over a long period
  - Local calibration and manual checks to improve data reliability
- Limitations:
  - Gaps due to instrument failure; some periods omitted or patched with alternative gauges
  - Rainfall data can be substituted from neighboring microcatchments when a gauge fails
  - Potential local-scale measurement challenges (e.g., weir blockages) requiring manual verification

## References

- Shuttleworth, E.L. et al. (2019) Restorations of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, p. 100006. https://doi.org/10.1016/j.hydroa.2018.100006