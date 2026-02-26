# Digestate_HF_and_NW_NH3_cum.csv

- Overview
  - Data set: 32 rows, 6 columns
  - Trials from digestate wheat experiment (2017) at two sites: Henfaes (HF) and North Wyke (NW)
  - Emissions: cumulative NH3-N emissions over 7 days for different digestate treatments
  - Measurement method: wind tunnels with NH3 traps; NH4 traps captured NH3 after conversion to NH4
  - Data supports GIS-based visualization of spatial patterns across plots and treatments

- Data structure and columns
  - Site: HF or NW
  - Block: 1, 2, 3, or 4 (randomised block design)
  - Plot: HF plots (5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40) and NW plots (1–16)
  - Treatment: D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
  - NH3_qa1: cumulative NH3-N emissions over 7 days, in kg N ha^-1
  - NH3_qa2: same as NH3_qa1 with negative NH3 flux values replaced by 0

- Measurement timing and scope
  - HF: measurements over 7 days at 4 h, 24 h, and days 2–7 after digestate application
  - NW: measurements over 7 days at 1 h, 3 h, 6 h, 24 h, and days 2–7 after application

- Methodology details
  - Gas traps: phosphoric acid traps to capture NH3; NH4 traps used to quantify NH4 after NH3 contact with acid
  - Sampling setup: two pipes around wind tunnels feeding traps; air moved from outside to inside plots
  - Trap maintenance: NH4 traps changed 2–3 times per day on the first day due to higher volatilization
  - Detection limit: 0.01 mg NH4-N L^-1

- Digestate sources by site
  - HF: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham); includes acidified digestate, digestate with DMPP, and acidified digestate with DMPP
  - NW: digestate from anaerobic digestion of food waste (Holsworthy); includes acidified digestate, digestate with DMPP, and acidified digestate with DMPP

- Notes relevant for GIS use
  - Spatial granularity: plot-level data across two experimental sites
  - Temporal aggregation: data represents 7-day cumulative emissions
  - Categorical variables: site, block, plot, treatment
  - Data quality considerations: NH3_qa2 caps negative fluxes at zero; detailed measurement timings vary by site
  - Units: NH3-N emissions expressed as kilograms of nitrogen per hectare (kg N ha^-1)