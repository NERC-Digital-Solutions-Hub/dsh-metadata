# Metadata: Quality control and data editing

## Overview
- Describes the Plynlimon 7-hourly intensive hydrochemistry dataset, including a Raw Data Archive (RDA) and an Edited data version.
- RDA contains unaltered measurements with minimal lab-verified corrections; intended for documentation and transparency, not routine analyses.
- Edited data are high-confidence values, cleaned to remove erroneous or questionable data while preserving plausible real signals.

## Data Versions and Provenance
- Raw Data Archive (RDA)
  - Raw measurements as reported; corrections traceable to original lab files.
  - Aims for completeness and transparency about subsequent edits.
  - Not recommended for routine analyses due to known errors in many values.
- Edited data
  - Measurements with high confidence; problematic values removed or corrected.
  - Uses consistency checks and expert judgment to delete or adjust blocks or individual values.
  - Includes documentation of major edits, sample-by-sample changes, and notable data-swaps (e.g., Trip 80 vs Trip 81).

## Sampling and Data Structure
- Sampling sites:
  - Rainfall: Carreg Wen (CR)
  - Streams: Lower Hafren (LHF) and Upper Hafren (UHF)
- Sampling regime:
  - Rainfall and stream samples collected approximately every 7 hours for ~2 years (7-hourly dataset).
  - Long-term weekly sampling at CR, LHF, and UHF for comparison with weekly bulk samples.
- Methodology notes:
  - Some measurements from settled (unfiltered) samples; others from filtered samples (0.45 µm for cations/metals, GF/C for others).
  - Unique sample codes combine site designation with a sequential number.
  - Data organized into analyte groups (first inorganic/ion chromatography/electrochemical analyses, then cations/metals by ICPOES/ICP-MS).

## Editing Approach and Procedure
- Editing principles:
  - Use consistency checks (e.g., SO4 vs S, Alk vs pH, charge balance) to validate data.
  - Apply expert judgment to omit blocks or samples with implausible variability or calibration issues.
  - Cull data affected by carryover from check standards (notably trace metals) and by calibration problems.
  - Address artifacts such as the “picket fence” due to check standards; where possible, correct or remove affected values.
- Data-block handling:
  - Large-scale edits often involve removing entire analytical blocks or problematic trips (e.g., Trip 80/81 swap corrections).
  - Documented decisions are tied to specific samples, analytical blocks, or sampling trips.
- Notes on comparability:
  - Where 7-hourly and weekly data diverge, expert judgment selects the more plausible values for editing.
  - Some discrepancies between datasets are retained if not large and if they reflect plausible differences.

## Analyte Group Insights (Notes at a Glance)
- General editing themes:
  - Conductivity and pH: culled when inconsistent with other chemistry indicators (e.g., alkalinity, gran alkalinity).
  - Gran alkalinity: culled when inconsistent with pH or Ca-related patterns.
  - DOC/TDN/DON: edited to reflect correlations; DON computed from edited TDN, NO3, NO2, NH4.
  - NO3-N, NO2-N, NH4-N: culled or retained based on consistency with TDN and flow; some caution advised for NH4 due to potential contamination.
  - SO4 and Cl: culling of singletons and problematic blocks; SO4_by_ICP derived from edited S values.
  - Halogens and metals (F, Br, Na, K, Ca, Mg, Sr, Li, Be, Al, Si, S, etc.): numerous block-level and singleton flyers culled; many issues linked to calibration, carryover, or block transitions.
  - Trace metals (Mn, Co, Fe, Ni, Cu, Zn, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Pb, U): widespread culling of erroneous values; several blocks adjusted or removed due to calibration or carryover; tungsten (W) omitted entirely due to pervasive issues; U values are near detection limits and interpreted with caution.
- Notable anomolies addressed:
  - A documented swap between analytical trips (Trip 80 and Trip 81) affecting multiple elements; corrective editing aligns SO4 from IC with SO4_by_ICP.
  - Repetitive “picket fence” patterns (e.g., Ca, Sc) attributed to carryover or block boundaries; mitigated by culling or small value shifts.
  - Occasional large biweekly spikes (e.g., Ca, alkalinity) at LHF attributed to contamination rather than natural signals; spikes culled.
- Iodine data (I) deemed too short for robust editing; not edited.
- Some data limitations:
  - Very low-concentration elements (e.g., W) largely unusable and removed.
  - Absolute values for ultra-trace constituents (e.g., U) should be interpreted with caution; relative patterns are more robust.

## Site and Temporal Context for GIS Work
- Temporal resolution:
  - 7-hourly time series with a parallel weekly dataset for validation and comparison.
- Data linkage:
  - Each sample linked to a site code (CR, LHF, UHF) and a sequential sample number for traceability in maps and time-series visualizations.
- Data versions available for GIS integration:
  - RDA: raw, fully traceable edits; useful for documenting data lineage and potential re-editing.
  - Edited: cleaned, consistently edited values suitable for routine GIS analyses and map-based visualizations.

## Implications for GIS and Data Use
- Prefer edited data for map-based products and routine analyses; use RDA for documentation and provenance checks.
- When mapping or querying time-series, link samples by site code and sample number; be aware of blocks or trips that were removed or swapped.
- Be cautious with low-concentration and highly variable analytes (e.g., W, U) and with data blocks known to contain calibration issues or carryover artifacts.
- Use documented caveats (e.g., 7-hourly vs weekly discrepancies, Ca spikes at LHF likely contamination) to annotate maps and time-series visuals.

## How to Use This Document in GIS Projects
- Reference the two data versions (RDA vs Edited) to justify data selection in spatial analyses.
- Annotate maps with sampling-site notes and known data issues (carryover, calibration blocks, blocked edits, sample swaps).
- Use sample codes and trip/block metadata to correlate time-series features with analytical runs, improving interpretability of spatial-temporal patterns.
- When integrating multiple analytes, rely on edited data with established cross-analyte consistency checks and documented correlations.