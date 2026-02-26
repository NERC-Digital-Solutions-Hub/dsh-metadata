Digestate_HF_and_NW_NH3_cum.csv

## Overview
- Supplemental documentation detailing the data structure and measurement methods for NH3 cumulative emissions from the digestate wheat trial conducted in 2017 at Henfaes Research Center (HF) and North Wyke (NW).
- Supports data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.

## Dataset scope
- Size: 6 columns and 32 rows.
- Subjects: Digestate treatments applied to plots, with NH3 emissions measured over 7 days following digestate application.
- Treatments:
  - D: digestate
  - AD: acidified digestate (pH 5.5 at HF, pH 3 at NW)
  - DNI: digestate with nitrification inhibitor (DMPP)
  - ADNI: acidified digestate with nitrification inhibitor (DMPP)

## Data structure and fields
- Columns (with meaning and units):
  - Site: HF (Henfaes) or NW (North Wyke)
  - Block: 1–4 (randomised block design)
  - Plot: Specific plot identifiers (HF: 5,6,8,10,13,14,15,18,24,28,29,30,33,36,38,40; NW: 1–16)
  - Treatment: D, AD, DNI, ADNI
  - NH3_qa1: Cumulative NH3-N emissions over the 7-day measurement period
  - NH3_qa2: Same as NH3_qa1, but negative NH3 flux values replaced with 0
- Units:
  - NH3_qa1 and NH3_qa2 in kg N ha^-1 over 7 days

## Measurements and methodology
- Emission measurement method:
  - Wind tunnels with acid traps (phosphoric acid) to capture NH3, which is measured as NH4 after trapping.
  - Air from the wind tunnel circulated to traps via pipes placed at two positions (beginning and middle of the plot).
  - NH4 traps were replaced multiple times per day on the first day due to high volatilization.
- Digestate sources:
  - HF: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham)
  - NW: digestate from anaerobic digestion of food waste (Holsworthy)

## Data processing and quality notes
- NH3 measurements are reported as NH3-N after conversion to NH4 in traps.
- NH3_qa2 ensures non-negative values by replacing any negative fluxes with 0.
- Dataset represents 7-day cumulative emissions following digestate application.

## Detection limits and data handling
- Detection limit: 0.01 mg NH4-N L^-1 (for trap measurements).

## Data provenance and references
- Supplemented by the broader supporting documentation for CINAg experiments (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Data reflect field trials at two sites (HF and NW) in 2017, using multiple digestate treatments and wind-tunnel measurement approaches.