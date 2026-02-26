# Stalybridge Rainfall and Discharge 2019-2022

## Overview
- Rainfall and runoff data from ten experimental microcatchments (0.4–3.9 ha) on Stalybridge Moor, upland UK peatland.
- Timeframe: 2019–2022, covering periods before and after gully blocking in six microcatchments; four microcatchments serve as unrestored controls.
- Purpose: assess impact of different gully blocking methods on storm flow response in upland peatlands.
- Data collection and processing led by the Protect-NFM project team; microcatchment discharge measured at v-notch weirs; rainfall recorded with tip bucket gauges. Instrument failures caused irregular data gaps.

## Experimental design and scope
- BACI design:
  - Controls (no gully blocking): A, D, G, J
  - Treatments: B (22 cobblestone dams), C (7 cobblestone + 13 peat dams), E (10 piped-peat dams), F (6 peat dams), H (6 peat dams), I (20 timber dams)
- Intervention timeline:
  - Pre-intervention: May 2019–March 2020
  - Gully blocking: 16–25 March 2020
  - Post-intervention: April 2020 onward
- Post-restoration design changes:
  - Microcatchment E: piped-peat dam openings changed 25/03/2020–22/02/2021; uniform 64 mm open orifice from 22/02/2021
  - Microcatchment I: timber dam slot adjustments from 25/03/2020–27/01/2021 and 29/03/2021
- Study outputs: used to evaluate how blocking methods influence stormflow and peak discharge.

## Data collection and measurement methods
- Discharge:
  - Continuous monitoring at 5-minute intervals using v-notch weirs and pressure transducers
  - Barometric compensation applied using a reference pressure sensor
  - Manual calibration against stage boards during downloads
  - Data logger downloads occur monthly
- Rainfall:
  - Tip bucket rain gauges (0.2 mm per tip) in microcatchments B, E, G, I
  - Rainfall data patched from nearest available microcatchment when a gauge failed
- Instrumentation:
  - Discharge sensors: HOBO U20-001-04 pressure transducers
  - Rain gauges: HOBO RG3-M with 186 cm² orifice
- Location details:
  - Microcatchment coordinates A–J provided; rain gauge locations listed for B, E, G, I

## Data processing, calibration, and units
- Conversion:
  - Water depth behind the weir translated to discharge via a stage-discharge relationship
  - Depth measurements calibrated against manual readings at each download
- Calibration context:
  - Absolute pressure corrected for barometric pressure
  - Depth-to-discharge calibration performed in-field
- Recorded values:
  - Discharge: litres per second (L/sec)
  - Rainfall: millimetres (mm)

## Data structure and file organization
- Data are provided per calendar year for each microcatchment in CSV format
- Filename convention: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: stalybridge_e_2021_rainfall_discharge.csv
- Column order and content:
  - DateTime (GMT): string in YYYY-MM-DD HH:MM:SS
  - Rainfall (mm): float64
  - Discharge (L/sec): float64

## Quality control and data limitations
- Quality checks:
  - Visual review of discharge records against rainfall to identify spurious values (e.g., vegetation blocking the V-notch)
  - Periods with suspected errors are omitted and marked as no data
- Data gaps:
  - Irregular gaps due to instrument failure
  - Rainfall data may be patched from nearby microcatchments when gauges fail
- Notes on scope:
  - Data capture spans pre- and post-intervention periods with design changes in some microcatchments
  - Data are suitable for hydrological analysis of the effects of gully blocking on stormflow in upland peatland settings

## Data governance and stewardship notes
- Project and provenance:
  - Project: Protect-NFM; NERC grant NE/R004560/1
  - Author: Adam Johnston
  - Reference: Shuttleworth et al. (2019) on restoration and stormflow impacts
- Metadata and discoverability:
  - Clear naming conventions, units, and coordinate references enhance reusability and discoverability for data stewards
  - Data are structured to support reproducibility and cross-year aggregation
- Considerations for custodians:
  - Maintain and update metadata to reflect any reprocessing or corrections
  - Track versioning and data provenance across yearly CSVs
  - Ensure alignment of post-intervention periods when comparing treatment vs control microcatchments

## References
- Shuttleworth, E.L. et al. (2019) Restoroation of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge, Journal of Hydrology X, 2, p. 100006.