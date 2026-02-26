# Kinder Scout Rainfall and Discharge 2010-2021

## Overview
- Dataset of rainfall and runoff records from three experimental microcatchments (0.4–0.8 hectares) on Kinder Scout, an upland peatland in the UK, spanning 2010–2021.
- Collected to determine the impact of peatland restoration on storm flow response; includes one non-restored control microcatchment.
- Data collection and processing managed by the Protect-NFM project; discharge measured at v-notch weirs with pressure transducers; rainfall recorded by tip bucket gauges.
- Occasional gaps due to instrument failure; when a rain gauge failed, a neighbouring gauge’s data were substituted and the alternate gauge named in the records.

## Experimental design
- BACI (Before-After-Control-Intervention) design:
  - Firmin: unrestored control (no treatment throughout).
  - Olaf: treated with revegetation during restoration.
  - Nogson: treated with revegetation and gully blocking, later with Sphagnum plug planting.
- Timeline:
  - Pre-intervention: 2010–2011
  - Restoration: 2011–2012
  - Additional Sphagnum planting at Nogson: 2015
- Data collection period: June 2010–December 2021; continuous discharge and rainfall at 10-minute timesteps; some data gaps due to instrument failure.

## Data collection, generation, and processing
- Equipment and measurements:
  - V-notch weirs across erosional gullies; pressure transducers behind weirs; barometric compensation for depth readings.
  - Rainfall measured with tip bucket gauges; each tip equals 0.2 mm.
- Processing:
  - Depth of flow converted to discharge using a calibration equation related to the V-notch geometry.
  - Monthly downloads of data; manual calibration using stageboard readings to relate sensor depth to water depth over the V-notch.
- Locations:
  - Nogson (UK grid reference: SK 08234 89464)
  - Olaf (UK grid reference: SK 08262 89464)
  - Firmin (UK grid reference: SK 08972 89442)
- Units:
  - Discharge: litres per second (L/s)
  - Rainfall: millimetres (mm)

## Data structure and file naming
- Data organized per calendar year for each microcatchment; CSV filenames follow:
  - [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: kinder_nogson_2015_rainfall_discharge.csv
- Columns (in order):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS
  - Discharge (L/sec): float64
  - Rainfall (mm): float64
  - Alt TBRG: name of any alternative rainfall gauge used
  - Notes: field notes relevant to the data

## Quality control and data notes
- Discharge data visually inspected for spurious observations and compared across the three discharge records; periods with potential overestimation (e.g., obstruction at the V-notch) omitted and marked as no data.
- Rain gauges compared; if a gauge failed, data substituted from a functioning gauge and the alternate gauge noted in Alt TBRG.
- Irregular data gaps present due to instrument failures; substitutions and notes documented to maintain traceability.

## Miscellaneous and references
- Related methodological context: Shuttleworth, E. L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. Available at the provided DOI.