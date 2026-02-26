# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013

## Overview
- Long-term, fortnightly monitoring dataset from Derwent Water, Cumbria, England (Aug 1990–2013).
- Variables measured: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), phytoplankton chlorophyll a (TOCA).
- Purpose aligned with assessing environmental health indicators to inform policy and decision-making.

## Sampling regime and collection methods
- Measurements taken from a boat at a marked buoy location (deepest part of the lake); when unavailable, sampling from shore (Flag 2).
- Integrated water samples from 0–5 m depth.
- Sampling frequency: fortnightly (regular long-term time series).

## Data quality, limitations, and metadata
- Data are raw (not quality-controlled or calibrated) except for double entries from 2005 onward; visually checked.
- Some missing data:
  - March–June 2001 due to foot-and-mouth disease restricting access.
  - 2009 data gaps due to weather conditions.
- Values below detection limits indicated with a < sign (sign_if_LT_LOD column).
- Data structure includes: Date, Variable, Value, Sign_if_LT_LOD, Flag (1 = buoy sample, 2 = shore sample).

## Data structure and metadata
- File format: comma-separated values (CSV).
- Columns:
  - Date: measurement date.
  - Variable: parameter (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value: measured value.
  - Sign_if_LT_LOD: indicator if below detection limit.
  - Flag: sampling location indicator (1 buoy, 2 shore).
- Units specified for each variable (e.g., TEMP in °C, OXYG in % air-saturation, SECC in metres, ALKA in µg CaCO3 per litre, etc.).

## Data availability and usage
- Data provided to download; raw and uncalibrated except for documented double entries.
- Frequently cited in literature for climate and lake ecosystem studies; examples include:
  - Climate change impacts on physical characteristics of large lakes (Freshwater Biology, 2007).
  - Catchment productivity and lake CO2 emissions (Nature Climate Change, 2013).
  - Fisheries and lake ecology under climate stress (various proceedings and journals).

## Relevance to monitoring frameworks (policy evaluation and decision-making)
- Demonstrates a long-term, multi-parameter monitoring approach to evaluate environmental health indicators.
- Provides baseline metrics for temperature, oxygen, clarity, nutrient status, and phytoplankton – essential for assessing ecosystem condition and responses to environmental change.
- Highlights practical aspects of data collection, management, and dissemination critical to monitoring governance.

## Practical considerations for monitoring governance
- Data accessibility and openness: raw data availability is important but may be limited by lack of full quality control and metadata completeness.
- Metadata and standardization: clear documentation of units, detection limits, sampling methods, and locations is crucial for data reuse and comparability.
- Data quality and calibration: for robust policy insights, timely quality control and calibration, with transparent QA/QC records, are needed.
- Handling data gaps: plan for and document gaps due to access, weather, or outbreaks; strategies to mitigate and annotate such gaps are important.
- Governance and sharing: balancing openness with data provenance and governance to ensure data are stored, updated, and shared appropriately.

## Key takeaways for authors of monitoring frameworks
- Longitudinal, multi-parameter datasets enable rigorous evaluation of environmental health indicators and policy outcomes.
- Clear documentation of sampling design, units, detection limits, and data flags is essential for interpretability and reuse.
- Anticipate data gaps and access barriers; incorporate metadata standards and QA/QC protocols from the outset.
- Facilitate data sharing while maintaining data provenance and governance to maximize utility for decision-makers and researchers.