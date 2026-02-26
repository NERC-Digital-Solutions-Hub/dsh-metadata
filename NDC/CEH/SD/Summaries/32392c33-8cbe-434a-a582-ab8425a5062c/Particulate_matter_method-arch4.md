# Overview

- This document describes a method to quantify suspended particulate matter (SPM) in water by filtering a measured volume, weighing the filter with captured material, and optionally partitioning the material into organic and inorganic fractions via ignition at 500 °C.
- Outputs include total SPM concentration (mg/L or mg/m³) and, if desired, inorganic and organic fractions (CI and CO).

## Data and evaluation context for Data Leaders

- Emphasizes exact weighing and control of moisture/airborne water effects (hygroscopic filters) to ensure accurate measurements.
- Requires blank corrections, field duplicates, and consistent sample handling to assess data quality and precision.
- Uses explicit volumes (V) and weights (W1, W2, W3) with clear unit conversions to ensure traceability and comparability.
- Supports data governance needs: documentation of procedures, calibration, and correction factors (e.g., blank correction X).

## Equipment and consumables (key items)

- Drying oven, muffle furnace, 47 mm glass fibre filters (GF/F, 0.8 µm)
- Filtering manifold, vacuum pump, forceps
- Balance (0.01 mg precision), measuring cylinders, sample bottles
- Aluminium trays, desiccator, Ziploc bags
- Distilled water, general lab supplies for cleaning and storage

## Filter preparation (to ensure data quality)

- Harden filters by ignition at 500 °C.
- Soak in distilled water (~5 min) to remove soluble material; handle with forceps.
- Dry at 75 °C for ~1 h, then cool in a desiccator.
- Weigh each filter with aluminium dish (W1) promptly and store in a sealed bag until filtering.
- Desiccator use is important to minimize moisture-related weight changes.

## Filtration procedure (consistency and traceability)

- Collect samples in bottles and filter as soon as possible; store at <4 °C if delayed.
- Place weighed filter on filter base; mix sample to homogenize particulates.
- Filter a volume until the filter begins to clog, aiming for ~2 mg total particulate matter; typical volumes: open ocean 2–5 L, coastal waters 0.5–1 L (volume V).
- Rinse solids from cylinder into filter; rinse filter/manifold with distilled water; remove salt from filter margins to reduce crystallization artifacts.
- After filtration, store the filter in its aluminium tray and Ziploc bag in a freezer until drying.

## Determination of blanks (quality control)

- Use at least three blank filters to account for hygroscopic weight changes.
- Weigh blanks after redrying (W2); calculate blank correction X = mean(W2) − mean(W1).
- X can be positive or negative, but should not exceed 0.5 mg.

## Field duplicates (precision assessment)

- Collect two separate samples simultaneously under identical conditions.
- Process identically to measure precision from field collection, preservation, and laboratory procedures.

## Filter drying and SPM calculation (final data outputs)

- Dry filters at 75 °C for 1 h, then cool in a desiccator.
- Weigh to 0.01 mg (W2: filter plus total particulate matter).
- Calculate total SPM concentration:
  - C_SPM = (W2 − W1 + X) / V
  - If needed, multiply by 1000 to convert to mg/m³ (depending on units used for V).
- If organic/inorganic fractions are desired:
  - Ignite filters at 500 °C for 3 h to burn off organic material.
  - Weigh ashed filters (W3: filter plus inorganic fraction).
  - Inorganic concentration:
    - C_I = (W3 − W1) / V
  - Organic concentration:
    - C_O = (W2 − W3) / V
- Unit notes:
  - W1, W2, W3 are in mg; V is in litres.
  - To convert between original g weights to mg, multiply by 1000; to convert volume to litres, convert accordingly.
  - Final concentrations are reported in mg/L (or mg/m³ after appropriate scaling).

## References

- Strickland, J.D.H., Parsons, T.R. (1972) A Practical Handbook of Seawater Analysis.
- Radojevic, M., Bashkin, V.N. (1999) Practical Environmental Analysis.