# The effect of biochar addition on N2O and CO2 emissions from a sandy loam soil - the role of soil aeration

## Overview
- Investigates how biochar addition influences soil N2O and CO2 emissions, focusing on soil aeration effects.
- Study uses bare soil from a Miscanthus field in Lincolnshire, UK, with a dense, compacted sandy loam profile.
- Two experiments:
  - Experiment 1: fully-factorial design across three incubation temperatures (4, 10, 16 °C) and two moisture conditions (field moist and wetted), with/without biochar.
  - Experiment 2: incubations at uniform water holding capacity (WHC) with five biochar amendment levels (0, 1, 2, 5, 10%).
- Data outputs include gas flux time-series (N2O and CO2), soil chemical properties, and biochar characteristics, all analyzed to assess biochar’s impact under varying conditions.

## Datasets and data types
- Gas flux data:
  - Experiment 1: headspace N2O and CO2 fluxes measured at 6, 26, 51, 64, and 127 days across 4 replicates per treatment combination.
  - Experiment 1 includes wetting events with additional sampling post-wetting (0–48 h window).
  - Experiment 2: cumulative gas production tracked over 168 hours after wetting, with measurements at multiple short intervals.
- Chemical and soil property data:
  - Soil pH, extractable NH4+ and NO3−, total C and N.
  - Bulk density and water-filled pore space (WFPS) calculations.
  - Biochar properties: total C and N, pH, cation exchange capacity (CEC), and other properties (supplementary information).
- Experimental metadata:
  - Soil core dimensions, bulk density, moisture status (WFPS), incubation temperatures, biochar application rates, and wetting protocols.
  - Sampling methods and analytical instruments.

## Experimental design and procedures
- Site and soil: Miscanthus-derived bare soil; sandy loam with specified texture and initial chemical characteristics.
- Biochar treatment: hardwood-derived biochar (<2 mm) added to top 7 cm at ~2% by dry soil weight in Experiment 1.
- Experiment 1 protocol:
  - Soil cores prepared and stored at 4 °C for equilibration.
  - Treatments combined: biochar presence/absence, three temperatures, two moisture levels.
  - Wetting: field-moist and wetted conditions with precise WFPS values; headspace gas sampling conducted over time.
- Experiment 2 protocol:
  - Soil from 0–10 cm depth prepared and incubated at 16 °C in darkness.
  - Biochar amendment across five levels (0–10% of dry soil weight) with 3-day equilibration.
  - WHC determined and soils wetted to 87% WHC; headspace gas sampling over 168 hours.
- Gas analysis:
  - CO2 analyzed by GC with dual FID detectors; N2O analyzed by GC with ECD.
  - Calibration against certified standards; detection limits noted (data not shown for limits).
- Chemical analysis:
  - pH, NH4+, NO3− via standard extraction and colorimetric analysis; total C and N by dry combustion.
- Data processing:
  - Gas fluxes calculated from linear accumulation of headspace concentrations or direct differences for Experiment 2.
  - Peak cumulative N2O used at 60 hours post-wetting in Experiment 2.
- Statistical analyses:
  - R (v2.14.0) used; log-transformations applied for normality.
  - Experiment 1: linear mixed-effects models for gas fluxes; three-way ANOVA for cumulative fluxes and chemical properties.
  - Experiment 2: one-way ANOVA with biochar level; Tukey's test for level differences.

## Data quality, uncertainty, and limitations
- Gas measurements calibrated with certified standards; system airtightness pre-tested.
- Initial CO2 flush after mixing acknowledged and equilibrated before data collection.
- Detection limits referenced but not displayed in the data summary.
- Use of standard, cited methods for pH, inorganic N, and CN analyses to support data reliability.
- Data interpretation relies on established flux calculation methods and transformation to improve normality.

## Metadata and data management considerations for Data Stewards
- Essential metadata to accompany datasets:
  - Site coordinates, soil type, and crop history.
  - Detailed biochar characteristics (C, N, pH, CEC, particle size, GMC).
  - Experimental design details: factors (biochar, temperature, moisture), treatment codes, replication, dates.
  - Soil core dimensions, bulk density, WFPS values, and moisture treatment parameters.
  - Sampling times, headspace measurement methods, instrument models, detection limits, calibration procedures.
  - Analytical methods for pH, NH4+, NO3−, total C and N, with units and instrument settings.
  - Data processing steps: flux calculation methods, transformation formulas, statistical models used, software version.
  - Data provenance and versioning, links to supplementary information.
- Quality assurance practices to document:
  - Pre-testing of enclosure gas sampling; calibration against standards; replicate handling; QC checks on chemical analyses.

## Sharing, reuse, and preservation considerations
- Datasets could be prepared for deposition in data repositories or portals with clear metadata and documentation.
- Provide data in machine-readable formats with standardized units; include method references and raw/derived data where appropriate.
- Include data provenance, version history, and links to supplementary information for reproducibility.

## Endnotes and references
- The study references established methods for gas flux measurement, soil chemical analyses, and statistical approaches, supporting robust data interpretation and comparability with other soil-GHG studies.