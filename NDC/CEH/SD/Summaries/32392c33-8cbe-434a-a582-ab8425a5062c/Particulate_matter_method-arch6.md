# Determination of Suspended Particulate Matter (SPM) in Water by Filtration and Ignition

- Purpose
  - Quantify suspended particulate matter in water and, if needed, separate organic and inorganic fractions by ignition at 500 °C.
  - Provide SPM concentration in mg/L (and convert to mg/m³ if required).

- Data and outputs
  - Key measurements: W1 (initial filter + dish weight), W2 (filter + particulate matter weight), W3 (filter + inorganic fraction after ignition), V (volume of water filtered, in liters).
  - Calculations:
    - Blank correction X: X = mean(W2_blank) − mean(W1_blank); ensure |X| ≤ 0.5 mg.
    - SPM concentration: CSMP = (W2 − W1 + X) / V (mg/L); multiply by 1000 to convert to mg/m³ if needed.
    - If determining fractions: CI = (W3 − W1) / V (mg/L); CO = (W2 − W3) / V (mg/L).
  - Data units: weights in mg; volumes in L; convert from g to mg where necessary (×1000).

- Equipment and consumables
  - Drying oven, muffle furnace, 47 mm glass fibre filters, filtration manifold, vacuum pump
  - Forceps, balance (0.01 mg, 5 decimals), wash bottle, aluminum trays, desiccator
  - Measuring cylinders (1–2 L), sample bottles, plastic bags
  - Distilled water, storage containers; ensure surfaces and tools are clean to avoid contamination

- Filter preparation (to obtain W1)
  - Harden glass fibre filters by ignition at 500 °C.
  - Soak filters in distilled water ~5 minutes; handle with forceps.
  - Dry at 75 °C for ~1 h; cool in a desiccator.
  - Weigh each filter with its aluminium dish to obtain W1 (to 0.01 mg); minimize moisture uptake by keeping desiccators closed.
  - Store weighed filters in Ziploc bags until sampling.

- Filtration procedure (to obtain W2 and handle samples)
  - Collect water samples in bottles; filter as soon as possible; store at <4 °C if delay is necessary.
  - Place weighed filter on filter base; homogenize sample by inverting bottle; load filtered volume until filter begins to clog (typical aim ~2 mg material; open ocean 2–5 L; coastal waters 0.5–1 L); denote volume as V.
  - Rinse solids from measuring cylinder into filter; rinse filter/manifold with three 10 mL distilled water rinses; remove salt by washing filter margins.
  - Remove filter, return to aluminum tray, place in Ziploc, and freeze until ready to dry.

- Determination of blanks (to correct for filter hygroscopicity)
  - Prepare at least three blank filters, not used for filtration.
  - Weigh to obtain W1 (initial). Redry and reweigh to obtain W2 (blank second weight).
  - Compute X = mean(W2) − mean(W1); X may be positive or negative but should not exceed ±0.5 mg.

- Field duplicates
  - Collect two separate samples at the same time under identical conditions to assess precision of field collection, preservation, storage, and laboratory procedures.

- Filter drying and SPM calculation (final data processing)
  - Dry filtered filters in their aluminium trays for ~1 h at 75 °C; cool in a desiccator.
  - Weigh to obtain W2 (filter + all particulate matter) to 0.01 mg.
  - Calculate CSMP = (W2 − W1 + X) / V (mg/L). For mg/m³, multiply CSMP by 1000.
  - If organic/inorganic fractions are needed:
    - Ignite filters at 500 °C for 3 h; cool and weigh to obtain W3 (filter + inorganic fraction).
    - Compute CI = (W3 − W1) / V and CO = (W2 − W3) / V (mg/L).
  - Conversions:
    - W1, W2, W3 in mg; V in L; if weights were recorded in g, multiply by 1000 to convert to mg.
    - If volume was recorded in mL, convert to L by dividing V by 1000.

- References
  - Strickland, J.D.H., Parsons, T.R. (1972) A Practical Handbook of Seawater Analysis.
  - Radojevic, M., Bashkin, V.N. (1999) Practical Environmental Analysis.