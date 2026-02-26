# Digestate_HF_and_NW_NH3_v2.csv

## Overview
- Supplementary data description for a dataset on ammonia (NH3) emissions from digestate-treated plots in two sites (Henfaes, HF; North Wyke, NW).
- Data supports evaluating environmental health impacts of digestate management and informing monitoring decisions.

## Dataset content and structure
- 8 columns and 304 rows.
- Sites: HF (Henfaes) and NW (North Wyke).
- Measurements collected from two digestate trials using wind tunnels and acidified NH3 trapping methods.
- Treatments represented as:
  - D = digestate
  - AD = acidified digestate (pH 5.5 at HF; pH 3 at NW)
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with DMPP
- Key data columns:
  - Site: HF or NW
  - Midpoint_time: midpoint of NH3 measurement period
  - Hours_since_digestate_app: hours since digestate application
  - Block: blocking factor (1–4) of the randomized block design
  - Plot: experimental plot identifier
  - Treatment: D, AD, DNI, ADNI
  - NH3_qa1: NH3-N emissions over the 7-day measurement period (kg NH3-N ha⁻¹)
  - NH3_qa2: same as NH3_qa1 but negative NH3 fluxes replaced with 0

## Measurement methodology
- NH3 captured using gas traps with phosphoric acid to convert NH3 to NH4+ for measurement.
- Air drawn from wind tunnels to traps via pipes located at plot midpoints on both sides of the tunnels.
- Trap changes: NH4 traps were replaced 2–3 times per day on the first day at HF/NW due to expected higher volatilization.
- Detection limit: 0.01 mg NH4-N L⁻¹ (lowest detection limit used).

## Sampling schedule and timing
- HF: NH3 emissions measured over 7 days at 4 h, 24 h, and days 2–7 after application.
- NW: NH3 emissions measured over 7 days at 1 h, 3 h, 6 h, 24 h, and days 2–7 after application.
- The dataset’s Midpoint_time and Hours_since_digestate_app capture these timepoints.

## Data quality, metadata, and governance considerations
- Metadata is provided for each field (column explanations and units).
- Data provenance includes digestate sources:
  - HF digestate from anaerobic digestion of food waste (Fre-energy, Wrexham)
  - NW digestate from anaerobic digestion of food waste (Holsworthy)
- Data quality considerations:
  - Negative NH3 flux values are replaced with zero in NH3_qa2.
  - Potential data governance barriers highlighted in related monitoring frameworks include data accessibility, metadata adequacy, and the need for data sharing and governance at source.
- Data format requires interpretation of treatment codes and alignment with metadata to enable cross-study comparisons.

## Relevance for monitoring frameworks
- Provides a structured, comparable dataset to assess environmental emissions from different digestate management strategies (D, AD, DNI, ADNI).
- Enables evaluation of policy-relevant questions such as the impact of acidification and nitrification inhibitors on NH3 emissions.
- Supports transparency and reproducibility through clear data fields, measurement methods, and treatment definitions, aligning with governance and data-quality expectations for monitoring programs.

## Potential considerations for use
- Ensure alignment of site-specific pH treatments when aggregating HF and NW data.
- Verify any updates to treatment codes or measurement protocols when integrating with other datasets.
- Assess metadata completeness and consider augmenting with dataset provenance, measurement notes, and data-cleaning steps if used for official reporting or decision-making.