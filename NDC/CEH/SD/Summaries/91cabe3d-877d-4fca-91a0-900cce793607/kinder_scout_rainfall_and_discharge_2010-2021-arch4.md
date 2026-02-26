# Kinder Scout Rainfall and Discharge 2010-2021

## Overview
- Dataset of rainfall and runoff from three experimental microcatchments (0.4–0.8 ha) on Kinder Scout, upland peatland, UK, spanning 2010–2021.
- Purpose: determine the impact of peatland restoration on storm flow response.
- Study design includes a BACI framework with a non-restored control and restored treatments to evaluate restoration effects.

## Experimental design / sampling regime
- Microcatchments:
  - Firmin: unrestored control (no treatment throughout the dataset).
  - Olaf: revegetation during restoration.
  - Nogson: revegetation and gully blocking, later with Sphagnum plug planting.
- Timeline:
  - Pre-intervention: 2010–2011.
  - Restoration: 2011–2012.
  - Additional Sphagnum planting at Nogson: 2015.
- Data collection: continuous discharge and rainfall from June 2010 to December 2021 at 10-minute timesteps.
- Data gaps: instrument failures causing missing observations; where a rain gauge failed, a nearby gauge’s data were substituted with an alt gauge noted.

## Data collection / generation / transformation
- Discharge measurement: v-notch weirs with pressure transducers in a stilling well; barometric correction applied.
- Rainfall measurement: tip bucket gauges; 0.2 mm per tip; replacements used if a gauge failed.
- Calibration: manual readings of stage height used to calibrate pressure transducer depth to actual water depth; stage height used to estimate discharge via a specified conversion.
- Location references: v-notch weirs and rain gauges identified by UK grid references for Nogson, Olaf, and Firmin.

## Fieldwork equipment
- Discharge: AquiStar SDI-12 pressure transducers.
- Rainfall: HOBO RG3-M gauges with ~0.2 mm resolution.

## Calibration steps and values
- Manual stageboard readings obtained at data download were used to calibrate sensor depth to water height above the v-notch.

## Nature and units of recorded values
- Discharge: litres per second (L/sec).
- Rainfall: millimetres (mm).

## Analytical methods
- Not specified (N/A).

## Quality control
- Discharge data checked against rainfall to identify spurious observations (e.g., vegetation blocking the v-notch); erroneous periods removed and marked as no data.
- Rain gauges visually compared; if a gauge failed, data from a functioning gauge substituted; alt gauge used is recorded in the Alt TBRG field.
- Field observations used to validate data integrity during downloads.

## Details of data structure
- Data organized by calendar year for each microcatchment and stored in CSV format.
- Filename pattern: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv (e.g., kinder_nogson_2015_rainfall_discharge.csv).
- Columns (in order): 
  - 'DateTime (GMT)' (YYYY-MM-DD HH:MM:SS, string)
  - 'Discharge (L/sec)' (float64)
  - 'Rainfall (mm)' (float64)
  - 'Alt TBRG' (name of any alternative rain gauge used)
  - 'Notes' (field notes relevant to the data)

## Miscellaneous
- N/A.

## References
- Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge, Journal of Hydrology X, 2, p. 100006.