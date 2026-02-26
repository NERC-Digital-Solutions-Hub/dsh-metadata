# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

- This document describes two CSV datasets from the Countryside Survey 2007, covering soil aggregate stability metrics derived using laser granulometry on 419 soils across 150 1km squares in Great Britain.
- Core measurements include particle size distributions (PSD) for water-stable aggregates and post-sonication particles, and derived stability metrics (Mean Weight Diameter and Disaggregate Reduction).
- Two data products are provided to enable analysis and self-service exploration, with careful attention to sampling design, laboratory protocol, quality control, and data provenance.

## Datasets and key fields

- Particle_Size_Distribution_data.csv
  - Content: PSD data for water-stable aggregates (WS) and post-sonication (SON) across 419 soils.
  - Columns:
    - SQUARE: 1km square site code
    - PLOT: Plot identifier within square
    - PSIZE: Particle size class (laser granulometry)
    - VOL_WS: Proportional volume for water-stable aggregates
    - VOL_SON: Proportional volume after sonication
  - Scope: 419 soils from 150 squares; 1km square sampling framework

- Aggregate_stability_metrics.csv
  - Content: Derived aggregate stability metrics for water-stable and post-sonication aggregates.
  - Columns:
    - SQUARE, PLOT: Identifiers (as above)
    - MWD1: Mean Weight Diameter (water-stable aggregates)
    - MWD2: Mean Weight Diameter (post-sonication aggregates)
    - DR: Disaggregation Reduction (MWD1 minus MWD2)
    - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric)
    - COUNTRY: England/Scotland/Wales
    - COUNTY07: County or Council
    - EZ_DESC_07: Countryside Survey Environmental Zone description
  - DR notation: DR 2000 (no rescaling) used for this dataset; earlier DR 500 is referenced but not included here.

## Sampling design and scope

- Based on Countryside Survey methodology with stratification by Land Classes across environmental gradients.
- Great Britain stratified into land classes; 591 sample squares were surveyed in 2007 (England 289, Wales 107, Scotland 195).
- Plot selection: Randomly selected 1km squares within land classes; 424 plots selected; 419 plots analysed for aggregate stability.
- Soil sampling: From archived 2007 samples, collected from the top 0-15 cm, stored as air-dried and 2 mm sieved material; 15 g subsamples used for analysis.

## Background and measurement approach

- Measurement method: Laser granulometry to obtain PSD; Mean Weight Diameter (MWD) calculated from PSD.
- Stability metric: Disaggregate Reduction (DR) = MWD after pre-wetting (water-stable) minus MWD after sonication (fundamental particles).
- Protocol evolution: This dataset uses an updated protocol with larger aggregate mass and longer PSD measurement (60 s) without rescaling to <500 µm; DR 2000 refers to measurements without rescaling, while DR 500 (not included) refers to original rescaled values.
- Context: The method was developed and refined in Rawlins et al. (2013, 2015); a short lab video is available for the test procedure.

## Laboratory protocol highlights

- Sample preparation:
  - Determine approximate mass of 1-2 mm aggregates per soil; avoid excessive obscuration in PSD analysis.
  - Pre-wetting: Approximately 1 g of aggregates wets on a two-filter paper setup with 1 ml RO water; capillary wetting for 30 minutes.
- Instrumentation and measurement:
  - Instrument: Beckman Coulter LS 13320 laser granulometer.
  - PSD measurement: 60 seconds per run across 92 size classes (0.375 µm to 2000 µm).
  - Pre- and post-sonication measurements to derive DR.
  - Sonication: UP100H, 100 W, 5 minutes; temperature recorded to monitor energy input.
- Quality control during measurement:
  - Pump speed set to 60 (approx. 45 ml/s) to minimize bias from large aggregates.
  - If post-sonication obscuration > 30%, adjust sample mass and repeat.
  - Rinse vessel between analyses; use palaeosol reference material for QA, and standard PSD materials to check accuracy and precision.

## Quality control and assurance

- Field and laboratory QA:
  - Field staff trained with a detailed sampling manual; standardized processing from core logging to archiving.
  - Palaeosol reference material and standard PSD materials used to ensure measurement accuracy and precision across sessions.
  - Repeated PSD measurements if obscuration exceeded thresholds.
- Quality management:
  - UKCEH operates an ISO 9001:2015 certified Quality Management System with related QA policy and procedures.

## Data provenance, usage, and acknowledgements

- Data origin: Countryside Survey, UK Centre for Ecology & Hydrology (UKCEH).
- Version: 1 (dated 24-02-2020); Countryside Survey data © UKCEH.
- Usage notes:
  - All use of Countryside Survey data should include formal acknowledgement of UKCEH and Countryside Survey.
  - Data and publications should credit the Countryside Survey as the data source.
- References and supporting materials:
  - Key methodological and contextual references from the Countryside Survey program and Rawlins et al. publications.
  - Additional materials and data context linked in the document (LC07 land classification, etc.).

## Acknowledgements

- Funded through the NERC Soil Security Programme (Project NE/P014364/1).
- Data produced under the Countryside Survey program; acknowledgement and copyright notice required in all copies and outputs.

## Practical notes for data users

- DR interpretation:
  - DR 2000 values are included in this dataset (no rescaling to <500 µm); DR 500 values (older method) are not included here but may be referenced for comparability.
- Data integration considerations:
  - Align SQUARE and PLOT identifiers across both datasets to join PSD and stability metrics.
  - Consider country/lab class context (COUNTRY, LC07, EZ_DESC_07) when aggregating by region or land class.
- Citation guidance:
  - When publishing analyses or findings, acknowledge UKCEH Countryside Survey data as the data source.