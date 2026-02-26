# Digestate_HF_and_NW_NH3_v2.csv

## Overview
- Supplement to supporting documentation for data series; dataset contains 8 columns and 304 rows from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke Research Station (NW).
- Emissions data are NH3-N collected using wind tunnels and acid traps; multiple digestate treatments were tested.
- Data organized at the plot level with site, experimental design (block/plot), treatment, and time-related fields suitable for map-based visualization and spatial analyses.

## Data scope and structure
- Sites: Henfaes (HF) and North Wyke (NW).
- Measurements span 7 days post-application with site-specific time points:
  - HF: NH3 measurements at 4 h, 24 h, and days 2–7 after application.
  - NW: NH3 measurements at 1 h, 3 h, 6 h, 24 h, and days 2–7 after application.
- Treatments (Digestate-related, abbreviations):
  - D = digestate
  - AD = acidified digestate (pH 5.5 at HF; pH 3 at NW)
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with DMPP
- Measurements:
  - NH3_qa1: NH3-N emissions over the 7-day period (unit: NH3 kg ha-1)
  - NH3_qa2: same as NH3_qa1 but negative NH3 fluxes replaced with 0
- Measurement method details:
  - Gas traps with phosphoric acid; air drawn via wind tunnels to traps
  - NH4 captured (NH3 converts to NH4 on contact with acid)
  - Traps changed multiple times per day on HF/NW due to high volatilization
  - Detection limit: 0.01 mg NH4-N L-1

## Column definitions (8 columns)
- Site: HF or NW
- Midpoint_time: midpoint of the NH3 measurement period (time point not explicitly unit-specified)
- Hours_since_digestate_app: hours since digestate application
- Block: 1, 2, 3, or 4 (randomized block design)
- Plot: experimental plot identifier
- Treatment: D, AD, DNI, ADNI
- NH3_qa1: NH3-N emissions over 7-day period (NH3 kg ha-1)
- NH3_qa2: NH3_qa1 with negative fluxes replaced by 0

## Data quality and provenance
- Data originate from the 2017 digestate wheat trials at two sites with distinct digestate sources:
  - HF: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham)
  - NW: digestate from anaerobic digestion of food waste (Holsworthy)
- Wind tunnel-based NH3 measurement approach and acid-trap collection described; lower detection limit stated.

## GIS considerations and usage
- Plot-level and site identifiers (Site, Plot, Block) enable mapping NH3 emissions across locations and treatments.
- NH3_qa1 and NH3_qa2 provide a basis for time-series visualization by treatment and site.
- Potential analyses:
  - Spatial distribution of emissions by site and treatment
  - Temporal trends across measurement times
  - Comparison of digestate vs. acidified digestate and with/without DMPP
- Can be joined with GIS layers representing plots, blocks, and site polygons for spatial context.

## Notes
- This dataset is a structured data supplement; refer to the associated supporting documentation for methodological details and data handling practices.