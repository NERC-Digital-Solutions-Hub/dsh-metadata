# Digestate_HF_and_NW_NH3_cum.csv

- Data scope and purpose
  - Supplement detailing the structure of the dataset Digestate_HF_and_NW_NH3_cum.csv from the 2017 digestate wheat trials.
  - Two field sites: Henfaes (HF) and North Wyke (NW); experiments conducted at Henfaes Research Center and North Wyke Research Station.
  - 32 observations (rows) across 16 plots at each site (total 32 rows), using a randomized block design (Blocks 1–4).

- Dataset structure
  - Columns (6 total) with explanations and units:
    - Site: HF or NW
    - Block: 1–4
    - Plot: HF plots (5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40) and NW plots (1–16)
    - Treatment: D (digestate), AD (acidified digestate), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP)
    - NH3_qa1: Cumulative NH3-N emissions over the 7-day measurement period (kg N ha^-1)
    - NH3_qa2: Same as NH3_qa1 but negative NH3 flux values replaced with 0
  - Structure indicates 32 total observations (16 plots at HF + 16 plots at NW)

- Measurement details and timeline
  - HF (Henfaes): NH3 cumulative emissions measured over 7 days with measurements at 4 hours, 24 hours, and days 2–7 after digestate application.
  - NW (North Wyke): NH3 cumulative emissions measured over 7 days with measurements at 1, 3, 6, 24 hours, and days 2–7 after application.
  - Digestate sources: HF site used digestate from anaerobic digestion of food waste (Fre-energy, Wrexham); NW site used digestate from anaerobic digestion of food waste (Holsworthy).

- Sampling and capture methodology
  - Emissions captured using wind tunnels with gas traps containing phosphoric acid to trap NH3 (converted to NH4 in acid).
  - The NH4 traps were changed 2–3 times on the first day, with higher expected volatilization rates.
  - Detection limit: 0.01 mg NH4-N L^-1.

- Data quality and processing notes
  - NH3_qa2 data handling step replaces negative NH3 flux values with 0 to reflect non-physical negative emissions.
  - The dataset enumerates cumulative emissions per plot and treatment over the 7-day period, enabling comparison across digestate formulations and the influence of nitrification inhibitor (DMPP) treatments.

- Relevance and potential uses for data leaders
  - Enables assessment of how different digestate treatments (including acidification and DMPP) affect ammonia emissions under field conditions.
  - Facilitates cross-site comparisons (HF vs NW) and evaluation of the impact of nitrification inhibitors on cumulative NH3-N losses.
  - Useful for data governance around experimental metadata, treatment coding, measurement timing, and data cleaning (handling of negative fluxes).
  - Serves as a concrete example of structured, site-specific emission datasets suitable for aggregation in broader data ecosystems or networks.