# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' HF_NW_herbage_yield.csv '

## Overview
- Supplement detailing the data structure of the HF_NW_herbage_yield.csv dataset.
- Dataset is used in grassland fertiliser trials from 2016, contributed by Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).
- Part of supporting documentation for CINAg experiments.

## Dataset characteristics
- Size: 7 columns and 96 rows.
- Content: Herbage yield data from grassland fertiliser trials.
- Sites: HF (Henfaes) and NW (North Wyke).

## Column definitions
- Date: Date of grass cut.
- Site: HF or NW indicating trial location.
- N_app: Fertiliser application number (1, 2, or 3).
  - 1st and 2nd applications are 90 kg ha-1.
  - 3rd application is 60 kg ha-1.
- Block: Blocking factor of randomised block design (1–4).
- Plot: Plot identifier within a block (1–16).
- Treatment: Fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control).
- Dry_tonnes_ha: Dry matter yield of grass in tonnes per hectare.