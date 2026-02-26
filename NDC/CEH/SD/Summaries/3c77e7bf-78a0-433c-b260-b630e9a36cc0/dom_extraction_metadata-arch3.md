# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Overview
- Data deposit accompanying the Water Research 2020 manuscript on methods for extracting dissolved organic matter (DOM) from freshwaters.
- Covers UK freshwater water chemistry and DOM elemental content for 2018–2019.
- Data are quality controlled (e.g., values below detection limits addressed).

## Data collection and quality control
- Data collection and generation methods are described in the associated manuscript.
- Quality control applied; examples include treatment of values below detection limits.
- Includes a comparative assessment of multiple DOM extraction methods.
- Data are organized to support transparent evaluation of methods, processing, and outcomes.

## Data structure and content
- Five CSV files, each with detailed metadata and field descriptions:
  - DOMextraction SITES
    - Waterbody types (headwater, stream, lake/loch, reservoir inlet, reservoir, reservoir outlet)
    - Site numbers, elevation (m asl), catchment area (km²)
    - Water chemistry: pH, DOC (mg C L⁻¹), POC (mg C L⁻¹)
    - Dominant soil type (peat vs mineral)
  - DOMextraction CHN
    - Site number; DOC concentration; extraction method (DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, DIA-FD, DIA-FH)
    - Raw %C, %N, %H; Organic carbon content; processing rate (mL h⁻¹); processing time; recovery percentage
    - Relative data vs. rotary evaporated (RE) sample for C, N, H and OrganicC%
  - DOMextraction REreps
    - Site number; replicates A/B; extraction method (replicates of RE)
    - Raw %C, %N, %H per replicate
  - DOMextraction RECOVERY
    - Site number; extraction method
    - Volume used; DOMmass; DOM total C; DOC mass; DOC mass per volume; DOC concentration; recovery percentage
  - DOMextraction SCORES
    - For each method: rate score, recovery score, cost score; large equipment cost
    - Sum of scores and rank (1–9)
    - Notes on scoring: faster rate, closer to 100% recovery, and lower cost yield better scores; large equipment penalty lowers method ranking
    - Methods include DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, DIA-FD, DIA-FH

## Quality, metadata and data governance
- Explicit metadata and method descriptions accompany each dataset to facilitate interoperability.
- Recovery values can exceed 100% due to methodological details (e.g., filtration differences between DOM extraction and direct DOC measurement).
- The SCORES dataset provides a transparent, replicable framework to compare methods by speed, recovery, and cost, aiding governance over monitoring approaches.

## Implications for monitoring frameworks and policy evaluation
- Provides a transparent basis to select DOM sampling and processing workflows balancing speed, accuracy, and cost.
- Enables policy bodies to compare waterbody types (headwaters, streams, lakes/loch, reservoirs) in terms of DOM metrics and sampling demands.
- The embedded scoring framework supports evidence-based decision-making on monitoring investments and methodological standardization.

## Practical considerations for use
- Ensure alignment of dataset metadata with internal data standards when integrating into monitoring dashboards or policy analyses.
- Use the SITES and CHN data to interpret DOM composition across UK freshwater categories, considering method-specific biases highlighted in RECOVERY and SCORES.
- Be mindful of the potential for recovery values >100% and factor this into interpretation and reporting.

## Summary of key measures for evaluation
- Data availability and comparability across waterbody types and extraction methods.
- Quality assurance status and explicit method details to support reproducibility.
- Quantitative metrics for method evaluation: rate, recovery, and cost, aggregated into a final ranking to inform method selection for ongoing monitoring.