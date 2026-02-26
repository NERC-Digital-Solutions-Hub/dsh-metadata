# Field measurements of alkalinity, chloride-ion, conductivity,   pH   and   nutrients   in   rivers   (2003-2006) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR baseline dataset of river water quality measurements collected 2003–2006.
- Fortnightly sampling at 23 Environment Agency monitoring sites across the Frome/Piddle, Pang/Lambourn, and Tern catchments (2003 November → 2006 June; site-specific durations varied).
- Data intended to support understanding of baseline river chemistry and enable subsequent analyses of water quality trends.

## What was measured (variables and units)
- Alkalinity as CaCO3 (mg/L)
- Ammonia as N (mg/L)
- Chloride-ion (mg/L)
- Conductivity at 20 °C (µS/cm)
- Nitrate as N (mg/L)
- pH (pH units)
- Phosphorus soluble reactive (SRP) (mg/L P)
- Silicate reactive dissolved (SRD) (mg/L SiO2)
- Sulfate (mg/L)
- Note: Nitrate measured as NO3 and converted to mg/L N using X × 14/64.

## Where and when
- Sampling locations: 23 EA monitoring sites; some sites correspond to NRFA stations.
- Catchment codes: FP (Frome/Piddle), PL (Pang/Lambourn), TE (Tern); LCWQ indicates LOCAR water quality sampling site.
- Sampling frequency: every two weeks (fortnightly) from November 2003 to June 2006.
- River sampling point: main flow of the river at each site.

## How measurements were made (sampling and analysis)
- Sampling: single sample per site per event; bottles supplied by Thames Water.
  - pH and alkalinity: glass bottle.
  - SRP: field-filtered.
  - Other determinands: unfiltered.
- Analysis: conducted by Thames Water; site samples collected by Catchment Service Team.
- Detailed methods and quality metrics provided for each parameter (e.g., detection limits, calibration standards, precision indicators).

## Data quality and quality assurance
- Thames Water performed data quality control.
- Weekly QA: duplicate and QC samples sent to Thames Water for result verification.
- Statistical summaries: box-and-whisker plots generated for all variables to display range, median, quartiles, and outliers.
- Data notes: some NRFA station numbers may be missing; site metadata include site codes and catchment associations; nitrate conversion documented.

## Data governance and stewardship implications for Data Stewards
- Metadata requirements:
  - Variable definitions, units, measurement methods, QA/QC procedures.
  - Site codes, site types, and NRFA station mappings; catchment identifiers (FP/PL/TE).
  - Time coverage and sampling frequency; data provenance and data lineage (sampling → analysis → QA).
  - Detection limits, measurement uncertainties, and any conversions (e.g., NO3 to N).
- Data management actions:
  - Ensure consistent metadata schema across LOCAR baseline datasets.
  - Maintain crosswalks for site identifiers, catchment codes, and NRFA mappings.
  - Preserve original methods documentation and QA reports; link to dataset lineage.
  - Store data in a centralized catalogue with versioning and accessible data lineage.
- Data sharing and accessibility:
  - Facilitate discoverability via portals with clear variable definitions and methodological notes.
  - Include documentation on data quality, outliers, and any caveats (e.g., parameter-specific uncertainties).
- Potential constraints and considerations:
  - Some incomplete site metadata (e.g., missing NRFA station numbers) should be resolved or clearly documented.
  - Parameter-specific uncertainties (e.g., SRD uncertainty ~21%) should accompany data records where possible.
  - Nitrate conversions (NO3 to N) must be consistently applied and documented.

## Practical considerations for reuse
- The dataset provides a robust baseline for river water quality, enabling trend analyses and cross-site comparisons.
- Use of detailed method notes and QA information supports reproducibility and audit trails.
- Users should account for site-specific metadata gaps and parameter uncertainties when performing analyses.