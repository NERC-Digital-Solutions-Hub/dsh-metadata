# Kinder Scout Rainfall and Discharge 2010-2021

## Overview
- Dataset of rainfall and runoff from three experimental microcatchments (0.4–0.8 ha) on Kinder Scout, an upland peatland in the UK, 2010–2021.
- Projects' aim: determine the impact of peatland restoration on storm flow response in upland peatlands.
- Restoration occurred during the period; one microcatchment served as a non-restored control.

## Experimental design and scope
- BACI design: Before-After-Control-Intervention.
  - Firmin: unrestored control throughout the study.
  - Olaf: restoration (revegetation) implemented.
  - Nogson: revegetation, gully blocking, and later Sphagnum plug planting.
- Pre-intervention period: 2010–2011; restoration: 2011–2012; additional Sphagnum planting at Nogson in 2015.
- Data collection: continuous discharge and rainfall from June 2010 to December 2021 at 10-minute timesteps; some gaps due to instrument failure.

## Data collection, instrumentation, and processing
- Discharge measured with v-notch weirs; water depth behind weir recorded by pressure transducers; barometric correction applied using outdoor pressure sensor data.
- Rainfall recorded with tip-bucket gauges; one gauge per microcatchment.
- Data loggers downloaded monthly; field readings used to calibrate depth-to-discharge.
- In case of rain gauge failure, data from the nearest alternative gauge used; the alternative gauge name noted.

## Calibration, calculations, and data handling
- Depth behind the v-notch converted to discharge via an empirical calibration equation (based on stage measurements and weir geometry).
- Normalization and calibration steps included manual stage readings during data downloads.
- Units: Discharge in litres per second (L/sec); Rainfall in millimetres (mm).

## Data quality, gaps, and validation
- Visual quality control of discharge data against rainfall to identify spurious values (e.g., vegetation interfering with the v-notch).
- Erroneous periods omitted from final dataset.
- Rain gauge cross-checks performed; if a gauge failed, data substituted from a functioning gauge with Alt TBRG noted.
- Some irregular gaps remained due to instrument failure; missing observations also occur in discharge data.

## Data structure, access, and metadata
- Data provided per calendar year for each microcatchment in CSV format.
- Filename convention: [site]_[microcatchment]_[year]_rainfall_discharge.csv (e.g., kinder_nogson_2015_rainfall_discharge.csv).
- Columns (in order):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Discharge (L/sec): float64
  - Rainfall (mm): float64
  - Alt TBRG: name of any alternative rain gauge used
  - Notes: field notes or relevant information
- Sensor and site locations given as UK grid references.
- Data management and provenance were handled by the Protect-NFM project team; data are structured for reproducibility and transparency, though explicit public sharing constraints are not detailed in the dataset description.

## References
- Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, p. 100006.