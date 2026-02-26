# This file is for the weir boxes that are measuring drain and overland flow in the bowl. They were installed on 11/04/06.

## Overview
- Document describes field notes from two weir boxes (drain flow and overland flow, OLF) monitoring water height relative to a V-notch crest, including logger and sensor maintenance, calibration, and data issues.
- Components mentioned: pressure transducers (PT) in both weir boxes, loggers, tipping buckets (TB), and later turbidity sensors installed on the OLF outflows (24/11/06).
- Observations include water heights above the V-notch, logger sampling intervals, and adjustments to data processing when sensor readings jumped or appeared unreliable.
- Physical setup notes include V-notch dimensions, and that the weir boxes’ notches and sides may not be perfectly straight, affecting height calculations.

## Equipment, measurements and data streams
- Measurements primarily focus on height above the V-notch for DRAIN and OLF weir boxes, used to estimate flow.
- Weir box dimensions noted: approximate side lengths used to infer notch cross-section (DRAIN ~0.4074 m², OLF ~0.404022 m²); slight non-linearity due to notch geometry.
- Turbidity sensors installed on OLF outflows on 24/11/06; logs include periods of direct height measurements, plus flow estimates from tipping buckets.
- Data issues frequently tied to logger behavior, battery status, and occasional data gaps or jumps in PT readings.

## Data quality, calibration and processing
- Repeated mentions of jumps in PT values (notably 01/11/06, 14/11/06, 16/11/06, 03/03/08) requiring adjustments in calculations of height above the notch; some corrections documented in the accompanying Excel analysis file.
- Data gaps and reliability issues: data loss or incomplete downloads due to “dodgy” loggers or battery problems (e.g., lost data 25/11–05/12; 16/12–27/12; battery voltage around 10.1 V noted on 13/11/09).
- Calibration actions and zero-offset updates:
  - 07/06/07: Weir box dimensions measured to refine flow calculations.
  - 04/06/09: New zero-offset calibration performed after cleaning; OLF zero height 287.3 mm, DRAIN 271.2 mm.
  - During periods when the drain inflow pipe was not reinstalled properly (notably around 20/02/09 to 22/04/09), drain flow data deemed not suitable.
- Calibration approaches used:
  - Adding water to establish base (0 flow) levels for both OLF and DRAIN.
  - Adjusting for observed jumps in PT values to ensure height measurements remain consistent with physical conditions.
- Environmental factors affecting data:
  - Evaporation and diurnal temperature effects causing fluctuating PT readings.
  - Snow, ice, and freezing conditions (e.g., 18/02/08; 13/03/07) impacting measurements and necessitating protective lids or calibration checks.
  - Biological/physical blockages (rodents, voles, mol es) and sediment affecting sensor wells and flow paths.
- Data integrity notes:
  - Some data points later recalibrated or corrected in spreadsheets to align with measured heights and known physical changes.
  - Later notes emphasize the need to verify data post-cleaning and post-calibration due to potential shifts in sensor placement or drift.

## Maintenance, incidents and notable events (highlights)
- 24/11/06: Turbidity sensors installed on OLF outflows.
- 13/03/07: Wooden lids installed on pressure transducer stilling wells to mitigate snow intrusion.
- 27/11/07: Drain pipe shortened to enable water sampling; minor adjustments to plumbing.
- 18/02/08 – 16/02/08: Periods of freezing and snow-related issues affecting readings; inferred ice formation impacting PT data.
- 12/06/08: Weir boxes cleaned; PTs recalibrated; best offset estimates determined (OLF ~291.5 mm; DRAIN ~271 mm after adjustments).
- 04/06/09: New zero-offset calibrations established after cleaning; notes indicate one drain inflow pipe not properly reinstalled during a period, rendering data during that period unsuitable.
- 13/11/09: Logger reconnected after intermittent disconnection, possibly due to windy conditions; batter y situation flagged earlier (10.1 V) and addressed.

## Implications for GIS data products
- Time-series data for two coupled yet distinct flow paths (DRAIN and OLF) require careful synchronization and labeling to avoid mix-ups.
- Data quality flags should accompany records indicating logger health, battery status, calibration events, and known periods of data unreliability (e.g., post-02/09 to 04/09; 25/11–05/12; 16/12–27/12).
- Calibration history is essential for any flow calculations derived from height above V-notch; zero-offset changes and notch geometry corrections directly affect computed flow values.
- Notable environmental and maintenance events (ice, snow, blockages, lid installation) should be captured as contextual metadata for spatial-temporal analyses and for reproducibility of the dataset.
- Data cleaning steps (adjusting jumps, applying offsets, discarding dubious periods) should be documented in GIS-derived products to ensure transparency and reproducibility.