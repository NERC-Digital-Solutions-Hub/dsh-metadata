# Bulk density, carbon and nitrogen content in soil profiles from permafrost in subarctic Canada

## Overview
- Dataset detailing bulk density, and carbon and nitrogen content in soil profiles from permafrost in subarctic Canada.
- Collected from soil cores in 2013 and 2014, comparing peatland plateau vs thawing features and burnt vs unburnt black spruce forests, plus additional sites.
- Site codes include FFU, FFB, BLF, WHF, TPP, TW, TWM, MCU, MCB, WTP, WTM, WTS, WTW, BCB, BCS.
- Typically five soil cores per site (sometimes 3–4), with dedicated core labeling (e.g., TPP1–TPP5). Depth targeted up to 1 m, but constrained by rock or site conditions.

## Dataset structure and sampling design
- A diverse set of sites representing different vegetation and disturbance regimes (peatland plateaus, thaw features; burnt/unburnt forests).
- Core labeling and sampling depths reflect site-specific conditions; some cores sampled to shallower depths when deeper sampling was not feasible.
- Notes indicate that core and flux data codes may match, but the actual soil profile and flux locations are not spatially identical.

## Sampling methods and instrumentation
- Frozen-ground sites use distinct methods from non-frozen sites:
  - Frozen-ground: upper core via tin foil insertion, then drilling deeper with a powerhead corer to obtain 10–15 cm sections; cores wrapped and secured for transport.
  - Non-frozen ground: tin foil sampling for upper 40 cm; deeper portions via Russian corer; samples wrapped in PVC tubes.
- Samples transported frozen from Canada to the UK for analysis.

## Laboratory processing and data products
- In the UK: cores are cut with volumes recorded; upper portions sampled at 1 cm resolution for lead dating; deeper portions typically in ~10 cm increments based on horizon transitions.
- All samples freeze-dried; dry weights used to calculate bulk density.
- Subsamples weighed in tin capsules and analyzed for carbon and nitrogen with a C/N analyzer; results expressed as percent carbon and nitrogen on a dry-mass basis.
- Calibration standards run with each batch to derive concentrations.

## Data structure, fields, and interpretation notes
- Remarks field may note:
  - Potential over- or underestimation of bulk density due to thick roots or sampling recovery.
  - Vegetation changes associated with thaw (Postthaw vs Pre-thaw peat).
  - Presence of Tephra (White River Ash) layers in some cores.
- Important interpretation caveat: while soil profile codes (e.g., TPP1) mirror flux data codes, soil profiles and CO2/CH4 flux data originate from different locations; GPS coordinates in the soil data file do not necessarily match flux data locations.

## Data governance, provenance, and accessibility considerations
- Data collection occurred in 2013–2014; samples were stored frozen in Canada and shipped to the UK for analysis, indicating cross-border provenance handling.
- Documentation highlights the non-spatially aligned coding between soil profiles and flux data, underscoring the need for clear metadata linking and coordinate documentation.
- For data stewards, ensure metadata includes:
  - Site descriptions and codes, sampling year, core IDs (e.g., TPP1–TPP5), depth intervals, and horizon delineations.
  - Detailed sampling protocols for frozen vs non-frozen sites, including equipment and sequence.
  - Lab methods and calibration details for CN analyses and bulk density calculations.
  - Explicit notes on Postthaw vs Pre-thaw peat transitions and Tephra layers.
  - GPS coordinates for soil cores and a clear mapping to any related flux datasets, noting any spatial misalignment.

## Quality and risk considerations for Data Stewards
- Potential gaps in user needs or metadata completeness requiring augmentation with standardized metadata fields (variables, units, method flags).
- Timeliness and consistency of data sharing across large datasets and multiple sites/formats.
- Interoperability challenges due to differing sampling instruments and horizon delineations across sites.
- Handling large, multi-format datasets and ensuring robust versioning and provenance tracking.
- Outdated or legacy databases may require bespoke data curation approaches to maintain usability.

## Practical notes for reuse
- Users should be aware of depth resolution differences (1 cm for upper cores; ~10 cm for deeper horizons) and horizon-based depth assignment.
- When integrating with flux data, treat soil profile coordinates as separate from flux coordinates and rely on explicit metadata links rather than assumed spatial alignment.