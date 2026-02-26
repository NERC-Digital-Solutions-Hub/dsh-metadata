# Digestate_HF_and_NW_NH3_cum.csv

## Overview
- Supplement to the supporting documentation for data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Dataset from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- 6 columns and 32 rows, recording cumulative ammonia-nitrogen (NH3-N) emissions over a 7-day period.
- Treatments include digestate and acidified/differ nitrification-inhibitor variants.
- Two NH3 emission metrics are provided: NH3_qa1 (cumulative NH3-N) and NH3_qa2 (same, with negative fluxes replaced by 0).

## Data structure and content
- Columns (6 total): Site, Block, Plot, Treatment, NH3_qa1, NH3_qa2.
- Site: HF (Henfaes) or NW (North Wyke).
- Block: 1 through 4 (randomised block design).
- Plot: HF plots (5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40) and NW plots (1–16).
- Treatment: D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- NH3_qa1: Cumulative NH3-N emissions over the 7-day measurement period (kg N ha^-1).
- NH3_qa2: Same as NH3_qa1, but negative NH3 flux values replaced with 0.

## Experimental setup and context
- Digestate sources: from anaerobic digestion of food waste (HF: Fre-energy, Wrexham; NW: Holsworthy).
- Experimental design: plots amended with different digestate treatments in a randomized block design (Blocks 1–4).
- Wind tunnels used to measure NH3 emissions from plots.

## Treatment definitions
- D: Digestate only.
- AD: Acidified digestate (pH 5.5 at HF; pH 3 at NW).
- DNI: Digestate with nitrification inhibitor DMPP (BASF).
- ADNI: Acidified digestate with DMPP.

## NH3 emission measurement method
- NH3 captured as NH4 in phosphoric acid traps.
- Traps located at the beginning and middle of the plot on both sides of the wind tunnels; air circulated from the wind tunnel to traps using an extractor.
- NH4 traps changed 2–3 times per day on the first day at HF/NW due to higher expected volatilization.
- Detection limit: 0.01 mg NH4-N L^-1.

## Time points and duration
- HF (Henfaes): NH3 emissions measured over 7 days with sampling at 4 hours, 24 hours, and days 2–7 after digestate application.
- NW (North Wyke): NH3 emissions measured over 7 days with sampling at 1 hour, 3 hours, 6 hours, 24 hours, and days 2–7 after application.

## Data provenance and scope
- Data originate from the 2017 digestate wheat trial at HF and NW.
- Dataset is labeled as Digestate_HF_and_NW_NH3_cum.csv and comprises 32 observations across the two sites.
- Indicates specific methodological details for reproducibility and traceability, including trap chemistry, sampling cadence, and treatment definitions.