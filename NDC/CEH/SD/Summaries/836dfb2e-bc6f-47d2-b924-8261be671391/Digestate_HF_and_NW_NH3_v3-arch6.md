# Details of data structure to 'Digestate_HF_and_NW_NH3_v2.csv'

- Purpose and scope
  - Supplement to supporting documentation for CINAg experiments.
  - Data series capturing NH3 emissions from a 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW), Rothamsted Research.
  - 8 columns and 304 rows.

- Dataset context
  - Sites: HF (Henfaes) and NW (North Wyke).
  - Treatments (Digestate-related): D = digestate, AD = acidified digestate, DNI = digestate with nitrification inhibitor (DMPP), ADNI = acidified digestate with DMPP.
  - Measurements recorded over the 7-day post-application period, with site-specific measurement timings.

- Column definitions (8 columns; with units)
  - Site: HF or NW.
  - Midpoint_time: midpoint of the NH3 measurement period.
  - Hours_since_digestate_app: hours since digestate application.
  - Block: 1, 2, 3, or 4 (randomised block design).
  - Plot: experimental plot identifier.
  - Treatment: D, AD, DNI, ADNI (see above).
  - NH3_qa1: NH3-N emissions over the 7-day measurement period. Unit: kg NH3 ha^-1.
  - NH3_qa2: same as NH3_qa1, but negative NH3 fluxes replaced with 0.

- Measurement methodology
  - NH3 captured as NH4 after reaction with acid; traps used phosphoric acid.
  - Air circulated from wind tunnels to traps via two pipes placed at the start and middle of the plot, using an extractor.
  - NH4 traps changed 2–3 times per day on the first day at HF/NW due to expected high volatilization.

- Data quality and notes
  - NH3_qa2 adjusts NH3_qa1 by replacing negative flux values with 0 (non-negative emissions data).
  - Detection limit: 0.01 mg NH4-N L^-1.

- Site-specific measurement timings
  - HF: NH3 measured over 7 days at 4 and 24 hours, and 2–7 days post-application.
  - NW: NH3 measured over 7 days at 1, 3, 6, and 24 hours, and 2–7 days post-application.

- How the data can be used
  - Compare NH3 emissions across digestate treatments and sites.
  - Combine with other measurements or metadata to build dashboards or data products for monitoring emissions.
  - QA-enabled analyses thanks to NH3_qa2 adjustment and detailed timing/plot information.