# Details of data structure to 'Digestate_HF_and_NW_NH3_v2.csv'

- Overview
  - This document supplements supporting documentation for data series and describes the data structure for Digestate_HF_and_NW_NH3_v2.csv.
  - Dataset: 8 columns and 304 rows from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW).
  - Measurements concern NH3 emissions from plots amended with different digestate treatments, collected using wind tunnels.

- Treatments and sources
  - Digestate sources:
    - HF: digestate from anaerobic digestion of food waste (Fre-energy, Wrexham).
    - NW: digestate from anaerobic digestion of food waste (Holsworthy).
  - Treatments (codes):
    - D = digestate
    - AD = acidified digestate (pH 5.5 at HF; pH 3 at NW)
    - DNI = digestate with nitrification inhibitor (DMPP)
    - ADNI = acidified digestate with DMPP

- Measurements and timepoints
  - Location/time coverage:
    - HF: NH3 emissions measured over 7 days at 4 h, 24 h, and 2, 3, 4, 5, 6, 7 days after digestate application.
    - NW: NH3 emissions measured over 7 days at 1 h, 3 h, 6 h, and 24 h, and at 2, 3, 4, 5, 6, 7 days after application.
  - Measurement method: wind tunnels with gas traps using phosphoric acid to capture NH3 (which converts to NH4 in traps).

- Dataset structure and fields
  - Site: HF or NW.
  - Midpoint_time: midpoint of the NH3 measurement period.
  - Hours_since_digestate_app: hours since digestate application.
  - Block: 1–4, blocking factor of randomised block design.
  - Plot: experimental plot identifier.
  - Treatment: D, AD, DNI, ADNI as defined above.
  - NH3_qa1: NH3-N emissions over the 7-day measurement period (units: kg NH3 ha^-1).
  - NH3_qa2: same as NH3_qa1 but negative NH3 fluxes replaced with 0.

- Data quality and processing notes
  - NH4 traps were changed 2–3 times per day on the first day at HF/NW due to expected high volatilization.
  - Detection limit: 0.01 mg NH4-N L^-1.
  - NH3 measurements are presented as NH3-N emissions; NH3 is captured as NH4 in the traps.