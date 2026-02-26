# N2O emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (autumn, 2016)

## Overview
- Dataset of N2O emissions from plots with three treatments: Control (no urine), artificial urine, and real sheep urine.
- Location: orthic podzol in semi-improved upland grassland, Henfaes Research Station, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Timeframe: autumn 2016.
- Experimental design: randomised block.
- Data collection methods:
  - Automated greenhouse gas monitoring system (GHH; eight flux measurements per chamber per day; 1-hour closure with four gas samples analyzed per closure).
  - Calibration standard analyzed after every fourth gas sample.
  - Additional monthly flux measurements from smaller manual chambers (40 cm x 20 cm x 20 cm).
- Data scope: quality-assessed flux data (not raw gas concentrations).
- Data authorship note: authors must be acknowledged if data are reused or reproduced.

## Experimental setup and data collection
- Chambers:
  - Automated system chambers: 50 cm x 50 cm x 15 cm (0.25 m2 basal area).
  - Manual system chambers: 40 cm x 20 cm x 20 cm.
- Instrumentation:
  - Automated system: GHH with GC (SRI 8610) for eight measurements per chamber per day.
  - Manual analysis: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler; four gas standards used for calibration.
- Data collection cadence:
  - High-frequency data from automated system (daily flux measurements).
  - Monthly flux measurements from manual chambers.
- Data processing: flux data are provided after quality checks; raw gas concentration data are not included.
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; anomalous data removed as needed. Manual data below detection limit set to zero.

## Data structure and content
- Data headers:
  - Date_Time: format dd/mm/yy hh:mm.
  - Columns B–M: N2O fluxes (units: micrograms N2O-N m-2 h-1).
- Treatments coded in headers: Control, ArtUrine (artificial urine), Urine (real urine).
- Chamber/plot identifiers included in headers.

## Quality assurance and data processing notes
- Data quality ensured by checking chromatograms and raw files for anomalies.
- Non-detect or below-detection-limit values in manual data set to zero.
- Emission flux values represent processed/quality-assessed data, not raw concentrations.

## Metadata and discoverability
- Location details (-site, altitude, coordinates) and experimental design are described.
- Instrumentation and calibration procedures are specified (GC models, calibration standards, frequency).
- Clear treatment labeling and chamber/plot identifiers facilitate cross-study linkage and meta-analysis.

## Usage notes and caveats
- The dataset provides flux data suitable for assessing treatment effects and temporal patterns but not raw concentration traces.
- Users should acknowledge data authors and refer to the study context (site, year, treatments) when reusing.
- Data are organized for ease of integration with other flux datasets but consider potential differences in chamber design and sampling cadence when comparing across studies.

## Reuse and attribution
- Explicit authorization requirement: authors must be acknowledged if data are reused or reproduced.
- Include study context (location, year, treatments) to maintain interpretability in secondary analyses.

## Relevance for Data Leaders (data strategy implications)
- Data system view:
  - Demonstrates end-to-end data lifecycle: from automated high-frequency measurements to curated, quality-checked flux data.
  - Highlights the separation between high-frequency automated data and lower-frequency manual data, with distinct processing pipelines.
- Data availability and discoverability:
  - Well-documented metadata (location, design, instruments, treatments, data headers) supports data discovery and reuse.
  - Clear data structure (flux values with treatment and chamber identifiers) aids integration into broader datasets.
- Data quality and governance:
  - Emphasis on QA procedures and handling of non-detects provides a model for data integrity.
  - Documentation of calibration and methodological details supports reproducibility.
- User needs and co-ownership:
  - Metadata supports policymakers or researchers needing context to interpret N2O flux results in relation to land management practices.
- Gaps and standardization:
  - The dataset distinguishes between automated and manual measurements, signaling the need for consistent data schemas when combining high-frequency and manual datasets.
- Coordination and collaboration:
  - Clear attribution and procedural transparency facilitate cross-institutional reuse and potential integration with wider data networks on soil emissions.