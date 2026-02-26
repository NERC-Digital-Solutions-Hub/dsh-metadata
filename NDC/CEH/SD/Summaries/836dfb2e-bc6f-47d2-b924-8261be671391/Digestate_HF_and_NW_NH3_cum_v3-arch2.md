# Digestate_HF_and_NW_NH3_cum.csv

## Overview
- Supplement to supporting documentation for data series referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- 32 rows and 6 columns of NH3 cumulative emission data from a digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Plots were amended with different digestate treatments and emissions were measured over 7 days using wind tunnels.
- Treatments include various forms of digestate, with and without acidification and with/without the nitrification inhibitor DMPP.

## Dataset structure and fields
- Columns (6 total):
  - Site: HF or NW (Henfaes or North Wyke).
  - Block: 1, 2, 3, or 4 (randomised block design).
  - Plot: Specific plot identifiers (HF: 5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40; NW: 1–16).
  - Treatment: D (digestate), AD (acidified digestate), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP).
  - NH3_qa1: Cumulative NH3-N emissions over the 7-day measurement period (kg N ha^-1).
  - NH3_qa2: Same as NH3_qa1, with negative NH3 fluxes replaced by 0.
- All values relate to cumulative NH3-N emissions over the 7-day period.

## Treatments and site context
- Digestate sources:
  - HF site: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham).
  - NW site: digestate from anaerobic digestion of food waste (Holsworthy).
- Acidified digestate details:
  - AD: acidified to pH 5.5 at HF and pH 3 at NW.
- Nitrification inhibitor:
  - DNI: digestate with DMPP (BASF).
  - ADNI: acidified digestate with DMPP (BASF).

## Measurements and timepoints
- HF (Henfaes):
  - NH3 emissions measured over 7 days at 4 h and 24 h, and at 2, 3, 4, 5, 6, and 7 days after digestate application.
- NW (North Wyke):
  - NH3 emissions measured over 7 days at 1, 3, 6, and 24 h, and at 2, 3, 4, 5, 6, and 7 days after digestate application.
- Emissions captured using wind tunnels with acid traps to collect NH3 as NH4.

## Measurement method and detection limits
- Gas traps containing phosphoric acid used to trap NH3 (converted to NH4 upon contact with acid).
- Sampling geometry:
  - At HF/NW plots, two pipes positioned to circulate air from the wind tunnel to the traps on both sides of the tunnel.
  - NH4 traps were changed 2–3 times per day on the first day due to expected higher volatilization.
- Detection:
  - Lower limit of detection for NH4-N is 0.01 mg per L.

## Data quality, usage, and provenance
- Data are structured for standardised environmental monitoring analysis and cross-site comparability.
- This dataset is a supplement to the main supporting documentation and details experiment design, data collection, and processing methods.
- As an environmental monitoring dataset, it adheres to general QA steps: data verification, quality assurance, cleaning, and transformation.
- Datasets are intended to be stored and uploaded to appropriate data portals as part of ongoing monitoring workflows.

## Additional notes
- Dataset emphasizes 6 columns across 32 rows, capturing site, blocking, plot-level treatments, and two NH3-qa measures (with and without adjustments for negative fluxes).
- The two NH3_qa fields enable handling of non-physical negative fluxes for downstream analyses.