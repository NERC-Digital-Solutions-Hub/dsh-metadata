# Kinder Scout Rainfall and Discharge 2010-2021

## Overview
- Dataset of rainfall and runoff records from three experimental microcatchments (0.4–0.8 hectares) on Kinder Scout, upland peatland, UK.
- Period: 2010–2021, capturing peatland degradation and restoration.
- Purpose: assess the impact of peatland restoration on storm flow response.
- Part of the Protect-NFM project; data collection by field technicians and researchers.
- Discharge measured at v-notch weirs; rainfall recorded with tip-bucket gauges; occasional instrument-related gaps.

## Experimental design and study sites
- Design: Before-After-Control-Intervention (BACI).
- Firmin: unrestored control throughout the dataset.
- Olaf: restoration via revegetation.
- Nogson: restoration with revegetation and gully blocking, later Sphagnum plug planting.
- Timeframe: pre-intervention 2010–2011; restoration 2011–2012 with additional Nogson planting in 2015.
- Continuous 10-minute measurements from June 2010 to December 2021; occasional data gaps due to instrument failure.

## Data collection and methods
- Discharge measurement: v-notch weirs with pressure transducers; barometric correction using an above-water sensor.
- Calibration: manual stageboard readings used to calibrate pressure-derived depth to v-notch height.
- Rainfall measurement: tip-bucket gauges; 0.2 mm per tip; readings aggregated to 10-minute intervals.
- Data handling: monthly data downloads; if a rain gauge failed, data from the nearest functioning gauge substituted; Alt TBRG notes recorded.
- Location identifiers (UK grid references) provided for each microcatchment.

## Data format and structure
- Output: yearly CSV files per microcatchment and site, named: [site]_[microcatchment]_[year]_rainfall_discharge.csv.
- Columns (in order):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Discharge (L/sec): float64
  - Rainfall (mm): float64
  - Alt TBRG: string (name of alternate rain gauge used when needed)
  - Notes: string (field notes or relevant information)

## Measurement specifics and units
- Discharge: litres per second (L/s)
- Rainfall: millimetres (mm)
- Time resolution: 10-minute timesteps

## Spatial information
- V-notch weir locations (UK grid references):
  - Nogson: SK 08234 89464
  - Olaf: SK 08262 89464
  - Firmin: SK 08972 89442
- Rain gauge locations (UK grid references):
  - Nogson: SK 08236 89456
  - Olaf: SK 08268 89454
  - Firmin: SK 08970 89438

## Calibration and quality control
- Calibration: depth readings at time of downloads used to calibrate sensor depth to water depth above the v-notch.
- Quality control: visual checks for spurious discharge (e.g., vegetation blocking the v-notch); periods identified as erroneous are omitted (no data).
- Rain gauge quality: cross-check among gauges; if one failed, substitute with the functioning gauge and record Alt TBRG accordingly.

## Usage notes and references
- Data collection and analysis aligned with Shuttleworth et al. (2019) on restoration effects on stormflow.
- Data suitable for GIS-based visualization and spatio-temporal analyses of rainfall–discharge relationships across restored and unrestored microcatchments.

## Related project and data provenance
- Project: Protect-NFM (Optimising NFM in headwater catchments to protect downstream communities)
- NERC grant number: NE/R004560/1
- Reference: Shuttleworth, E.L. et al. (2019) Journal of Hydrology X, 2, 100006.