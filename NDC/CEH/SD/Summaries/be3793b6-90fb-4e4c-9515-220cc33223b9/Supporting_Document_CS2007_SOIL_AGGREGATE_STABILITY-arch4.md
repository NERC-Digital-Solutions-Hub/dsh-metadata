# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

## Overview
- Two CSV data files from Countryside Survey 2007 covering soil aggregate stability across 419 soils in 150 1km squares (GB).
- Data types: Particle Size Distribution (PSD) measurements for water-stable aggregates and post-sonication aggregates; derived stability metrics (Mean Weight Diameter and Disaggregation Reduction).

## Data files and schema
- Particle_Size_Distribution_data.csv
  - SQUARE: 1km square site code
  - PLOT: Plot identifier within each square
  - PSIZE: Particle size class (laser granulometry)
  - VOL_WS: Proportional volume for water-stable aggregates
  - VOL_SON: Proportional volume after sonication
- Aggregate_stability_metrics.csv
  - SQUARE, PLOT: As above
  - MWD1: Mean Weight Diameter of water-stable aggregates
  - MWD2: Mean Weight Diameter after sonication
  - DR: Disaggregation Reduction (DR2000; no rescale to 500 µm in this dataset)
  - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric)
  - COUNTRY, COUNTY07, EZ_DESC_07: Location descriptors and environmental zone
- Note: This dataset uses DR2000 (no rescaling to <500 µm); references to DR500 exist but are not included here.

## Sampling design and sample selection
- Based on Countryside Survey methodology: stratified GB-wide sampling by environmental gradients (Land Classes).
- 1km × 1km sample squares; 591 squares surveyed in 2007 (England, Scotland, Wales breakdown provided).
- Soil samples for aggregate stability selected from 424 plots; 419 analysed.
- Samples originate from archived 2007 CS soils; 15 g subsamples analyzed.

## Background and methodology
- Aggregate stability measured via laser granulometry to derive PSD and Mean Weight Diameter (MWD).
- DR (disaggregation reduction) = MWD of water-stable aggregates minus MWD after sonication (fundamental particles).
- Protocol evolution for this dataset:
  - Increased soil mass used (about 1.8× previous mass) and longer PSD measurement (60 s).
  - No rescaling to <500 µm; DR is reported as DR2000 (no rescale) in this dataset.
  - Three texture classes used to set analyzed soil mass: 0.55 g (fine), 1 g (medium), 1.3 g (coarse) with the 7 m pipe added to instrument to increase circulating water volume.
  - Pre-wetting and measurement timing standardized to ensure consistent obscuration and energy input.

## Laboratory protocol
- Pre-wetting: precise mass of 1-2 mm aggregates placed between two filter papers; 1.0 ml RO water applied; aggregates wetted by capillary action for ~30 minutes.
- PSD measurement: laser granulometer (60 s analysis) across 92 size classes (0.375–2000 µm); pump speed fixed to avoid bias.
- Post-sonication: 5 minutes at 100 W; PSD measured again for 60 s; temperature monitored.
- DR calculation: DR2000 = MWD_after_sonication − MWD_before_sonication (for the same sample); obscuration < 30% criteria used to adjust sample mass if needed.
- Quality control: palaeosol reference material and standard PSD materials used; repeat analyses if obscuration exceeded thresholds.

## Quality control and quality assurance
- Field staff trained; use of a field sampling manual.
- Use of Ospringe palaeosol reference material and two standard PSD materials to check accuracy/precision.
- Laboratory QA procedures include re-analysis with smaller sample mass if obscuration high after post-sonication.

## Quality assurance and governance
- UK Centre for Ecology & Hydrology (UKCEH) maintains ISO 9001:2015 certified quality management system; formal QA policy and procedures in place.

## Usage notes and provenance
- Data are from Countryside Survey 2007; designed to support national statistics and cross-regional comparisons.
- Data sources and background detailed in accompanying Countryside Survey publications and cited references (environmental classifications, soil methods, and laboratory protocols).

## Access, provenance, and acknowledgments
- Data are housed under Countryside Survey with acknowledgment required in any use: “Countryside Survey data owned by UK Centre for Ecology & Hydrology; Countryside Survey © UKCEH.”
- Primary references and CEH project details provided for methodological context and reproducibility.

## Data System Implications for Data Leaders
- Data completeness: 419/424 plots analyzed; consider documenting data gaps and reasons for any exclusions.
- Metadata and discoverability: ensure clear definitions of DR, MWD, PSD, and unit conventions; maintain crosswalks to land-class and environmental zone codes.
- Provenance and lineage: capture archival origin (2007 CS soils), processing steps, protocol changes (DR2000 vs DR500), and equipment settings (laser granulometer, sonicator).
- Data quality governance: maintain QA materials (reference soils, standard PSD references) and ISO 9001:2015 alignment; document uncertainty and validation results.
- Reuse and integration: align with other Countryside Survey datasets (soil, land cover, environmental zones) to enable integrated analyses across GB; consider providing data licenses and clear usage terms.
- Access and updates: preserve versioning; communicate protocol amendments (e.g., mass and measurement duration changes) to downstream users to ensure comparability over time.
- Stakeholder alignment: reflect user needs (policy colleagues, researchers) by offering clear data dictionaries, data availability notes, and potential data gaps for granularity or coverage.