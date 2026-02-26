# Digestate_HF_and_NW_NH3_v2.csv

## Overview
- Supplementary dataset detailing NH3 emissions from a digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Treatments include digestate variants (digestate, acidified digestate, with and without DMPP) measured using wind tunnels.
- 8 columns, 304 rows.

## Dataset scope and origin
- Sites: Henfaes (HF) and North Wyke (NW).
- Experiments involve plots amended with:
  - Digestate (from anaerobic digestion of food waste)
  - Acidified digestate
  - Digestate with nitrification inhibitor (DMPP)
  - Acidified digestate with DMPP
- Measurements conducted over 7 days following digestate application.
- HF and NW used different timing schedules for NH3 measurement (HF: 4 h and 24 h, then days 2–7; NW: 1 h, 3 h, 6 h, 24 h, then days 2–7).

## Data structure and columns
- Columns (8 total):
  - Site: HF or NW
  - Midpoint_time: midpoint of the NH3 measurement period
  - Hours_since_digestate_app: hours since digestate application
  - Block: randomised block design factor (1–4)
  - Plot: experimental plot identifier
  - Treatment: D (digestate), AD (acidified digestate, pH 5.5 HF / pH 3 NW), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP)
  - NH3_qa1: NH3-N emissions over 7-day period (kg NH3 ha^-1)
  - NH3_qa2: NH3_qa1 with negative fluxes replaced by 0

## Measurement methods
- NH3 captured using gas traps with phosphoric acid to convert NH3 to NH4.
- Air circulated from wind tunnels to traps via pipes placed at plot extremes; extraction used to move air through the system.
- NH4 traps changed 2–3 times per day on the first day at HF/NW due to high volatilization rates.

## Treatments and site details
- Digestate sources mentioned:
  - HF: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham)
  - NW: digestate from anaerobic digestion of food waste (Holsworthy)
- Acidified digestate and nitrification inhibitors (DMPP) included to assess impact on NH3 emissions.

## Temporal coverage and measurement schedule
- HF NH3 measurements: 4 h and 24 h; days 2, 3, 4, 5, 6, and 7 after digestate application.
- NW NH3 measurements: 1 h, 3 h, 6 h, 24 h; days 2, 3, 4, 5, 6, and 7 after application.

## Data quality, units, and caveats
- NH3 measurements expressed as NH3-N emissions; units in kg NH3 ha^-1.
- Detection limit: 0.01 mg NH4-N L^-1.
- Data represent a supplement to the CINAg experiment documentation; structure supports standardised environmental monitoring outputs.

## Relevance to environmental monitoring aims
- Demonstrates environmental health indicators using a consistent data format across sites.
- Supports scrutiny of environmental health and policy performance over time through standardised NH3 emission data.
- Data handling emphasizes verification, cleaning, transformation, and storage for accessibility and reuse.