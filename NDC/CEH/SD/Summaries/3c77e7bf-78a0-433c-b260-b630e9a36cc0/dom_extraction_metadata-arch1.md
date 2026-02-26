# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Overview
- A data deposit accompanying a study on dissolved organic matter (DOM) extraction from UK freshwaters (2018–19).
- Data quality controlled (e.g., values below detection limits handled).
- Five CSV files cover site metadata, chemical composition, processing replicates, recovery calculations, and method-based scoring.
- Method descriptions and broader context are provided in the referenced manuscript: A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020.
- Designed to enable reproducibility, cross-method comparisons, and meta-analytic use.

## Data files and what they contain
- DOMextraction SITES
  - Type of waterbody (headwater, stream, lake/loch, reservoir inlet/outlet, etc.)
  - Site numbers for each waterbody type
  - Elevation (m a.s.l.)
  - Catchment area (km²)
  - Waterbody chemistry: pH, DOC (mg C L⁻¹), POC (mg C L⁻¹)
  - Dominant soil type (peat vs mineral)
  - Provides minimum and maximum values across waterbody types

- DOMextraction CHN
  - Site (site number)
  - DOC concentration (mg C L⁻¹) of the original water sample
  - Method (extraction method used; e.g., DRY-6, RE, RO-DF, RO-RE, SPE, etc.)
  - Raw %C, %N, %H and OrganicC% (DOM composition)
  - Rate (mL hr⁻¹) of processing
  - Time to final DOM sample (per volume processed)
  - Recovery% (relative to original DOC)
  - Relative measurements vs RE samples (Relative to RE: Total%C, Total%N)

- DOMextraction REreps
  - Site and Method
  - Replicates A and B for rotary evaporation (RE)
  - Raw %C, %N, %H for replicates

- DOMextraction RECOVERY
  - Site and Method
  - Volume used (mL)
  - DOM mass (mg) and DOM total%C
  - DOC mass (mg) and DOC mass per volume (mg L⁻¹)
  - DOC concentration (mg C L⁻¹)
  - Recovery% (as defined by comparison of DOMC content to measured DOC)

- DOMextraction SCORES
  - Method (extraction method used)
  - N (number of samples)
  - Rate (mean processing rate, mL hr⁻¹)
  - Recovery% (mean recovery)
  - Recovery SE (standard error)
  - Cost per sample (£) and Large equipment cost (£)
  - Score components: Rate score, Recovery score, Cost score
  - Large equipment penalty
  - Sum of scores and final Rank (1–9)

## Processing methods and QC
- Core extraction methods include various dry-down, RO, RE, SPE, dialysis, and related sequences
- Full methodological details and definitions are in the Water Research 2020 manuscript
- QC notes: values below detection limits addressed; recovery calculations account for differences in processing steps (e.g., filtration sizes) that can yield Recovery% > 100%

## Core variables and metrics
- DOC concentration and POC concentration in original water and DOM
- DOM elemental composition: C, N, H contents; Organic C fraction
- DOM recovery percentage and its relation to original DOC
- Processing rate and total processing time
- Method-specific performance indicators: recovery, rate, cost, and required equipment
- Data across waterbody types and site characteristics (elevation, catchment area, pH)

## Analytical opportunities and how analysts might use this
- Compare extraction methods to identify the most efficient balance of rate, recovery close to 100%, and cost
- Explore how DOM composition (C/N/H and OrganicC%) varies by waterbody type, site characteristics (pH, elevation, catchment area), and initial DOC
- Assess replicate variability using REreps to understand method precision
- Investigate relationships among processing rate, time, and recovery across methods
- Calibrate or harmonize DOM extraction results for cross-study comparisons
- Track data lineage and metadata for reproducibility and reuse in meta-analyses

## Caveats and notes
- Recovery can exceed 100% due to differences in pre-processing steps (e.g., filtration sizes between DOM processing and DOC measurement)
- Data are specific to UK freshwaters for 2018–2019; use with awareness of geographic and temporal scope
- Minimum/maximum values in SITES provide range context rather than site-specific distributions
- Detailed methodological nuances are in the cited Water Research 2020 manuscript; refer to it for implementation details

## End goal
- The dataset supports robust data-driven evaluation of DOM extraction methods, enabling evidence-based method selection, comparative analyses, and reproducible scientific conclusions.