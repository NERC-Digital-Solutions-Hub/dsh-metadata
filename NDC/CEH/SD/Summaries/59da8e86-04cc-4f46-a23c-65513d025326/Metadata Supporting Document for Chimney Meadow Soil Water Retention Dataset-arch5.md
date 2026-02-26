# Objective To determine soil characteristics within the top metre of soil to relate to soil moisture and Electrical Resistivity Tomography measurements

## Purpose and scope
- Document the methodology and data characteristics for determining soil properties in the top 1 m of soil at a single representative field site to relate to soil moisture and Electrical Resistivity Tomography (ERT) measurements.

## Study site and sampling design
- Location: Church Field, Chimney Meadow NNR, Berks, Bucks and Oxfordshire Wildlife Trust.
- Sampling strategy: one site chosen to represent soil type around the ERT transect; a soil pit located 13.75 m north and 1.0 m west of the transect to avoid interference with ERT.
- Transect reference points and soil pit coordinates provided (OSGB grid and heights).

## Fieldwork and laboratory instrumentation
- Sampling method: fixed-volume soil cores (769.77 cm3) using stainless steel rings (100 mm depth, 99 mm inner diameter); 10 cm depth increments up to 1.0 m; two samples per depth from a horizontal side cut; end caps used to prevent disturbance during transport.
- Laboratory instruments and stages:
  - Stage 1: Sand to convey suction from drainage system (pF 0 to 2.0).
  - Stage 2: Sand/kaolin box to apply suction from pF 2.0 to 2.7 (−100 hPa to −500 hPa).
  - Stage 3: 5 bar pressure plate extractor.
  - Stage 4: 15 bar pressure plate extractor.
- Equipment brands referenced: Eijkelkamp Sandbox and Sand/Kaolin box; Soil Moisture Equipment Corporation pressure plates.

## Calibration and measurement approach
- Suction application systems calibrated to maintain specified suctions; offset corrections for ambient air pressure applied where needed.
- Calibration principles:
  - Column of water for suction in sand-based devices.
  - Vacuum pump control via certificated transducers; pressure regulation for 5 bar and 15 bar plates.
  - All equipment maintained to certified standards.
- Primary calibration method: determine soil moisture content by gravimetric weighing of a fixed soil volume at each suction step; equilibrium judged by weight stability (< 0.1 g daily difference).

## Analytical methods and data captured
- Process:
  - Samples equilibrated to saturation, then progressively dried under specified suctions.
  - Water-release (retention) curves constructed for each depth, revealing two predominant clay soil types that are interleaved rather than fixed horizons.
- Key calculations:
  - Total weight = soil + water + ring; soil weight = total − ring; water weight = total − ring − dry soil.
  - Moisture Volume Fraction (MVF) = weight of water / volume of soil sample.
- Units and conversions:
  - Weights in grams; 1 bar = 100 kPa; 1 MPa = 1000 kPa.
  - pF scale described; conversion between MPa and pF via water column height (with typical plant-available and wilting-point references provided).
  - pF values linked to suction pressures through standard conversions.

## Data collected and data quality
- Data types: gravimetric soil moisture, suction at multiple pF steps, and derived moisture relationships (water-release curves) by depth.
- Quality control:
  - Duplicate samples per depth to detect procedural anomalies.
  - Large-volume cores to minimize voids and stone-related errors.
  - Cross-checks by plotting paired results to identify inconsistencies.

## Data format and storage
- Data format: comma-separated values (.csv).
- Metadata considerations evident from the record: site, transect references, soil pit location, depth increments, sampling and laboratory methods, equipment stages, and calibration notes.

## Data context and soil characterization
- Soil description: Church Field lies on a clay lens overlying sand and gravel; generally homogeneous in A and B horizons to 1.1 m; classification references include Kelmscott Association (per 1:250,000 map) and Oxford Clay interpretation at finer scales.
- Photographic and supplementary materials:
  - Explanatory images accessible via CEH Image Catalogue (SCWAFL project).
  - References to standard soil physics methods (bulk density, water retention) cited.

## Provenance, limitations, and notes for reuse
- Provenance: study tied to CEH SCWAFL project; uses established methods from recognized standards documents.
- Limitations:
  - Single-site study; results are representative of one location within a clay lens context.
  - Clay types are interleaved rather than fixed horizons, indicating temporal deposition variability.
- Documentation and references provided for replication or audit, including instrument manuals and foundational soil analysis literature.

## Related data and practical implications for data stewardship
- Directly linked to ERT measurements through correlation of soil moisture and water-retention characteristics with resistivity signals.
- Data stewardship considerations:
  - Ensure CSV is accompanied by comprehensive metadata (site coordinates, depth, sample IDs, instrument settings, calibration values, QA flags).
  - Maintain traceability to sampling events, depths, and equipment used to enable reproducibility and re-use in related hydrology or pedology studies.