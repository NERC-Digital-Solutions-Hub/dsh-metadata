# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Overview
- A data deposit of water chemistry and dissolved organic matter (DOM) composition from UK freshwaters (2018–2019).
- Data collection and generation methods described in the manuscript “A comparison of methods for the extraction of dissolved organic matter from freshwaters” (Water Research, 2020).
- Data are quality controlled, with values below detection limits addressed.
- Contains five CSV files that capture site-level waterbody characteristics, DOM chemistry, replication, recovery, and method scoring.

## Data files and their contents
- DOMextraction SITES
  - Type of waterbody (headwater, stream, lake/loch, reservoir inlet, reservoir, reservoir outlet) and counts.
  - Site numbers for each waterbody type.
  - Elevation (m above sea level) for site groups (min/max).
  - Catchment area (km²) (min/max) for site groups.
  - pH ranges per waterbody category.
  - DOC (mg C L⁻¹) ranges per waterbody category.
  - POC (mg C L⁻¹) ranges per waterbody category.
  - Dominant soil type (peat vs mineral soils) per waterbody category.

- DOMextraction CHN
  - Site number.
  - DOC (mg C L⁻¹) of the initial water sample.
  - Extraction method used (e.g., DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, various dialysis methods).
  - Raw % contents: Total C, Total N, Total H, Organic C.
  - Organic carbon content relative to raw samples.
  - Rate of processing (mL hr⁻¹) and time from start to final DOM sample per volume.
  - Recovery percentage and notes on comparisons relative to RE samples.

- DOMextraction REreps
  - Site number and replication (A, B) for replicates of rotary evaporation.
  - Extraction method designation.
  - Raw % contents: Total C, Total N, Total H.

- DOMextraction RECOVERY
  - Site number and extraction method.
  - Volume processed (mL).
  - DOM mass (mg) and DOM total C (%), DOC mass (mg), DOC mass per volume (mg L⁻¹), and DOC concentration (mg C L⁻¹).
  - Recovery percentage (relative to original DOC concentration in water); note recovery can exceed 100% due to filtration differences.

- DOMextraction SCORES
  - For each method: number of samples (N), mean rate (mL hr⁻¹), mean recovery (%), recovery standard error, cost per sample (£), large equipment cost (£).
  - Scoring: Rate score, Recovery score, Cost score (lower is better).
  - Large equipment penalty (scaled 0–10).
  - Sum of scores and overall rank (1–9).

## Methods and quality control
- Methods aligned with the described extraction approaches in the Water Research 2020 manuscript.
- Quality control applied to all data, including handling detection-limit values and recovery calculations.
- Some recovery values exceed 100% due to methodological specifics (e.g., filtration differences between DOM extraction and direct DOC measurement).

## Metadata, provenance, and usability
- The dataset is structured to support cross-site comparisons, method evaluation, and system-level analyses of DOM in UK freshwaters.
- Comprehensive per-field descriptions enable data discoverability and reuse, with explicit documentation of extraction methods and performance metrics.
- Data are provided as five CSV files with consistent naming and schema to facilitate integration into data systems and pipelines.

## Implications for data strategy and governance
- Provides a clear example of end-to-end data provenance, QC, and method benchmarking that supports data stewardship, standardization, and cross-institution collaboration.
- Highlights importance of metadata richness (method details, processing rates, recovery, and cost) to enable effective data discovery, validation, and reuse.
- Demonstrates handling of complex, multi-step laboratory workflows and their impact on data quality and comparability.