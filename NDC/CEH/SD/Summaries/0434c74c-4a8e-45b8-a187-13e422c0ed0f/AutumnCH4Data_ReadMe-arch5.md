# CH4 emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) in autumn, 2016.

## Overview
- Dataset describes methane (CH4) emissions from plots subjected to different urine treatments: Control (no urine), artificial urine (ArtUrine), and real urine (Urine).
- Experimental site: orthic podzol in a semi-improved upland grassland at Henfaes Research Station, North Wales, collected autumn 2016.
- Emissions were measured using an automated greenhouse gas monitoring system connected to a gas chromatograph (GC).

## Experimental setup and data collection
- Design: randomised block experimental design.
- Measurement system: automated GHG monitoring system (SRI 8610 GC, Torrance, USA) operated with eight flux measurements per chamber per day.
- Sampling regime: 1-hour chamber closure period per measurement; 4 gas samples analysed per closure period; calibration standard analysed after every fourth sample.
- Chamber dimensions: basal area 0.25 m2; chambers sized 50 cm x 50 cm x 15 cm (L x W x H).
- Data period: high-frequency data collected during the period analyzed by the automated system.

## Data structure and headers
- Data represent CH4 flux measurements, not raw gas concentrations.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Columns B to M: CH4 fluxes (mg CH4-C m-2 h-1)
- Treatment and plot/chamber identifiers are embedded in column headers (e.g., Control, ArtUrine, Urine; associated chamber/plot numbers).

## Quality assurance and processing
- Quality assurance (QA) procedures:
  - Inspect raw data files and GC chromatograms for anomalies.
  - Remove anomalous data (e.g., gas-peak interferences) as needed.
- Data provided are the quality-assessed flux values, not raw concentration data.
- Data may have undergone cleaning and transformation prior to sharing.

## Metadata, provenance, and documentation
- Site and sampling details are specified (Henfaes Research Station, Abergwyngregyn, North Wales; coordinates and altitude provided).
- Data provenance includes the measurement system, calibration procedures, and QA steps.
- Documentation indicates data authorship and the obligation to acknowledge authors in any reuse or reproduction.

## Data sharing, reuse, and governance
- Reuse policy: Authors must be acknowledged if data are re-used or reproduced.
- Data publication pathway: Data are intended for upload to relevant portals and catalogues, with accompanying dataset-level metadata and documentation to support discovery and reuse.
- Scope for data stewards:
  - Ensure metadata completeness (site, methods, units, treatments, timestamps).
  - Verify alignment of data formats with accepted standards (e.g., timestamp format, unit conventions).
  - Maintain traceability of QA decisions and any data transformations.
  - Facilitate discoverability and appropriate attribution in line with publishing/archiving practices.

## Limitations and scope
- Data reflect quality-assessed CH4 flux measurements from autumn 2016 rather than raw gas concentration data.
- High-frequency nature and treatment-specific design may entail larger file sizes and potential bespoke processing for interoperability.
- Some datasets (e.g., raw chromatograms) are not included in this data release; QA notes indicate potential exclusions due to anomalies.