# ReadMe file for SummerN2OFlux.csv

## Overview
- Dataset records N2O fluxes from three treatments applied to a dystric histosol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Treatments: Control (no urine), Artificial sheep urine, Real sheep urine (each applied in triplicate patches within chambers). Note: text states “Treatments (n = 4)” but lists three treatments.
- Sheep were excluded from plots from 15/05/2017 to avoid recent excretal influence.
- Monitoring duration: 177 days post-treatment.
- Data collected with an automated greenhouse gas monitoring system (QUT) and a SRI 8610 GC; followed by monthly manual flux measurements from the same chambers.
- Data provided are quality-assessed flux values, not raw gas concentrations.

## Experimental design and site
- Experimental design: randomised block.
- Chamber specifications: basal area 0.25 m2; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
- Treatments applied on 24/07/2017.
- Site conditions: grazing land with unimproved vegetation; the soil is a dystric histosol.
- Purpose: assess N2O flux responses to urine-derived nitrogen inputs.

## Treatments and sampling details
- Artificial urine: applied in triplicate patches within a chamber; N application rate 920 kg N ha-1; 200 ml artificial urine per patch over 100 cm2.
- Real urine: urine from ewes grazing the same vegetation; applied in triplicate patches; N application rate 930 kg N ha-1; 200 ml real urine per patch over 100 cm2.
- Sampling schedule:
  - High-frequency period: automated measurements using the QUT system (eight flux measurements per chamber per day; 1-hour closure; four gas samples per closure; calibration after every fourth sample).
  - Post high-frequency period: monthly manual flux measurements from the same chambers using a Perkin Elmer 580 GC with Turbo Matrix 110 autosampler and four gas standards.

## Data content and structure
- Data format: CSV (SummerN2OFlux.csv); readme notes accompany dataset.
- Headers and fields:
  - Timestamp: format dd/mm/yy hh:mm.
  - Days: days pre- or post-treatment application.
  - Columns B to M: N2O fluxes in µg N2O-N m-2 h-1.
  - Column headers encode treatment (Control, ArtUrine for artificial urine, Urine for real urine) and chamber/plot identifiers.
- Data scope: flux measurements covering high-frequency automated data and subsequent monthly manual measurements.
- Data quality: QA involved inspecting raw data files and GC chromatograms for anomalies; contaminated or anomalous data removed.

## Data processing and quality assurance
- Quality assurance steps:
  - Review raw data files and chromatograms for anomalies.
  - Remove anomalous data (e.g., gas peak interference) as needed.
- Output data represent quality-assessed flux measurements rather than raw gas concentrations.

## Usage, attribution, and documentation
- Licensing/acknowledgement: Authors must be acknowledged if data are reused or reproduced.
- Documentation included within the readme to facilitate interpretation and reuse, including:
  - Site details and treatment descriptions.
  - Instrumentation and analytical methods (automated system and GC setups).
  - Data structure, units, and time-related fields.

## Data governance and stewardship considerations
- Metadata completeness: provides site location, treatment definitions, experimental design, measurement cadence, and data processing steps.
- Versioning and updates: dataset includes two measurement regimes (high-frequency and monthly); clear timestamps and Days field support temporal alignment and updates.
- Standards and interoperability: uses clear units (µg N2O-N m-2 h-1) and explicit headers; aligns with typical GHG flux datasets but note potential minor labeling inconsistency in treatment count (n = 4 vs 3 treatments) for governance review.
- Accessibility and discoverability: dataset includes a ReadMe with methodological transparency; ensure future updates maintain consistent metadata and header conventions.
- Potential governance actions for Data Stewards:
  - Verify and document treatment count consistency (n=4 vs three treatments) to avoid misinterpretation.
  - Maintain explicit provenance (instrumentation, calibration standards, data processing steps) for audit trails.
  - Ensure proper citation guidance is provided in dataset records and portals.
  - Consider linking to raw concentration data if ever released, given that current data are processed flux values.