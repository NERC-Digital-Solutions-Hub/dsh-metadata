# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

## Overview
- A comprehensive metadata schema for environmental chemical analysis data from a monitoring network around Plynlimon, detailing a wide range of analytes across multiple years.
- Documents analytical methods, QA/QC, sample types, and data management to enable policy scrutiny and decision-making.

## Data fields and metadata structure
- For each analyte: FORM, DETERMINAND, UNITS, LQDC, QUOTE TO, START, END, ANALYSIS LOCATION, METHOD QC QUALIFIER, FILTRATION, PRESERVATION, METHOD, DETECTION LIMIT, NOTES.
- Data provenance includes multiple laboratories (e.g., Wallingford, Lancaster, Staylittle, Bangor) and instruments (ICP-OES, ICP-MS, IC, TOC analysers, etc.).
- Pre-concentration and sample preparation details (e.g., evaporation steps, filtration types, field vs lab handling) are specified.
- Data quality indicators and qualifiers are integrated (see QC codes and data qualifier codes).

## Sampling types, timing, and data processing
- Sampling types: grab samples (stream, borehole) and time-integrated inputs (rainfall, throughfall, cloud, stemflow).
- Time stamping conventions emphasize the sampling time and, for inputs, the interval between successive samples; volume-weighted sampling times are calculated to reflect precipitation timing.
- Conversion between flow and water mass metrics is provided (see area-weighted runoff calculations).

## Analytical methods and QA
- A broad spectrum of analytes is covered (major ions, trace metals, nutrients, dissolved organic carbon and nitrogen, DOC/DON, etc.).
- Methods include spectrometry (ICP-OES, ICP-MS), ion chromatography, colorimetry, TOC analysis, and UV/visible techniques; several methods involve pre-concentration and specific preservation requirements.
- Data quality is governed by explicit QC data qualifiers and ISO 17025-related notes, indicating accredited or proficiency-tested analyses.

## Data qualifiers and QC codes
- Includes DATA QUALIFIER CODES (e.g., raw instrument data, detection-limit related flags, quality concerns) and ANALYTICAL METHOD QC CODES (quality assurances, interlaboratory proficiency references).
- Codes indicate data reliability, method changes, and potential uncertainties, enabling policymakers to filter or weight data by confidence.

## Site coverage and analytical locations
- Sites include catchments associated with Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, and Upper Hafren, with catchment areas specified.
- Analyses distributed across multiple labs with site- and time-specific start/end dates, enabling long-term trend analysis.

## Flow-to-runoff conversions and flux calculations
- Explicit formulas to convert streamflow (cumecs) to area-weighted runoff (mm/15 min) and vice versa, using site catchment areas.
- This enables calculation of fluxes and loadings from concentration data, crucial for policy-relevant assessments of pollutant fluxes.

## Sampling times and data interpretation guidance
- Sampling times for different sample types are defined; time-stamped data should be interpreted with volume-weighted sampling times in mind.
- Year mean sampling and volume-weighted time bases are described to support accurate temporal analyses and comparisons.

## Implications for monitoring frameworks and policy
- Provides a blueprint for robust metadata governance necessary for credible monitoring frameworks.
- Demonstrates how to document data provenance, analytical methods, QA, and data processing steps to support transparent policy evaluation.
- Highlights the importance of data completeness, metadata richness, and clear QC flags to enable credible use of historical environmental data in decision-making.