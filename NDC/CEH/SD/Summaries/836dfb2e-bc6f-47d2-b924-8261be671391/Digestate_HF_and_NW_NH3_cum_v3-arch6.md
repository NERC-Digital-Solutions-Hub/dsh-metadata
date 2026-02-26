# Details of data structure to ' Digestate_HF_and_NW_NH3_cum.csv '

- Overview
  - Supplement to supporting documentation for data series; describes the data structure of the Digestate_HF_and_NW_NH3_cum.csv dataset.
  - Data come from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW).
  - 6 columns and 32 rows; 2 sites, multiple plots, and several digestate treatments.
  - Measures cumulative NH3-N emissions over a 7-day period, using wind tunnels and acid traps; NH4 traps captured ammonium after NH3 is absorbed.

- Dataset structure
  - Columns and meanings:
    - Site: HF (Henfaes) or NW (North Wyke)
    - Block: 1–4, randomised block design
    - Plot: specific experimental plots (HF: 5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40; NW: 1–16)
    - Treatment: D (digestate), AD (acidified digestate), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP)
    - NH3_qa1: cumulative NH3-N emissions over 7 days (kg N ha^-1)
    - NH3_qa2: same as NH3_qa1 with negative NH3 fluxes replaced by 0
  - Data context: values collected from plots subjected to different digestate treatments, with data formatted for direct use in analyses and dashboards.

- Measurements and methods
  - Emissions measurement: NH3 captured as NH4 after absorption in phosphoric acid traps; air circulated from wind tunnels to traps.
  - Trap deployment: two sampling points at the plot sides of wind tunnels; traps changed 2–3 times per day on the first day due to high expected volatilization.
  - Detection limit: 0.01 mg NH4-N L^-1 (conversion from NH3 to NH4/NH4-N measurement).

- Timepoints and site differences
  - HF (Henfaes): NH3 measured at 4 hours, 24 hours, and on days 2–7 following digestate application.
  - NW (North Wyke): NH3 measured at 1 hour, 3 hours, 6 hours, 24 hours, and days 2–7 following digestate application.
  - Note: timepoint sets differ slightly between sites, but both cover a 7-day post-application window.

- Context and usage
  - This dataset is a structured data structure supplement to broader CINAg experiments documentation.
  - Designed to support data exploration, cross-study integration, and creation of self-serve analyses or visualisations (e.g., dashboards, pivot-style reports).
  - Indicates data quality considerations (e.g., handling of negative fluxes in NH3_qa2) and the data collection workflow for transparency and re-use.