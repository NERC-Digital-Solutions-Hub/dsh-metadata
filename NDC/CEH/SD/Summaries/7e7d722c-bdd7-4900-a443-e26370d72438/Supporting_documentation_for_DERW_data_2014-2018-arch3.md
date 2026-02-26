# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018

## Overview and Purpose
- Part of an ongoing long-term monitoring dataset for Derwent Water (Cumbria, England) covering surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a from 2014 to 2018.
- Provides multi-parameter indicators of environmental health to support scrutiny of policy, trend analysis, and future decision-making.
- Demonstrates how long-term environmental data can inform assessments of stressors and ecosystem responses (as cited by example publications).

## Sampling Regime and Methods
- Fortnightly sampling at a marked buoy in the deepest part of the lake; when buoy visits were not possible, samples were taken from shore.
- Water samples integrated from 0 to 5 meters.
- Measurements include:
  - Surface temperature (TEMP, °C)
  - Surface oxygen saturation (OXYG, % air-saturation)
  - Secchi depth (SECC, m)
  - Alkalinity (ALKA, µg CaCO3 per L)
  - pH
  - Ammonium (NH4N, µg N per L)
  - Nitrate (NO3N, µg N per L)
  - Soluble reactive phosphate (PO4P, µg P per L)
  - Total phosphorus (TOTP, µg P per L)
  - Dissolved reactive silicon (SIO2, µg per L)
  - Phytoplankton chlorophyll a (TOCA, µg per L)

## Data Quality, Metadata, and Structure
- Data provided as raw (not yet quality controlled or calibrated) but have been double entered and visually checked.
- Missing data attributed to weather conditions or staff shortages.
- Flag system:
  - Flag = 1: sample taken at the buoy location
  - Flag = 2: shore sample (buoy visit not possible)
- Detection limits indicated with a “<” sign in the Sign (if<LOD) column.
- Data are organized in a CSV with fields: Date, Variable Description, Value, Sign, Flag.

## Data Coverage and Accessibility
- Timeframe: January 2014 through the end of 2018.
- Data available for download; long-term monitoring concluded in early 2019 due to funding shortages.
- Cited usage in publications demonstrates applicability for evaluating ecological responses to multiple stressors and long-term lake monitoring.

## Usage in Monitoring Frameworks
- Provides a suite of environmental health indicators suitable for policy scrutiny and evaluation.
- Supports data governance considerations: documentation of data collection methods, unit consistency, handling of non-detects, and transparent data sharing (subject to QA/QC enhancements).
- Highlights need for ongoing QA/QC, metadata completeness, and harmonized data management to ensure datasets remain usable for policy assessment and decision-making.

## Context and Limitations
- End of long-term monitoring in 2019 limits continuity and trend analysis beyond 2018.
- Raw nature of data requires QA/QC processes before formal use in policy reporting.
- Some measurements depend on access to the buoy, introducing potential spatial-temporal gaps (shore sampling as a fallback).

## References and Context
- Example publications showcase the dataset’s relevance for understanding responses to stressors (e.g., vendace reappearance in Bassenthwaite Lake).
- Related overview of long-term ecological research in the English Lake District provides broader context for continuing ecological informatics and knowledge generation.