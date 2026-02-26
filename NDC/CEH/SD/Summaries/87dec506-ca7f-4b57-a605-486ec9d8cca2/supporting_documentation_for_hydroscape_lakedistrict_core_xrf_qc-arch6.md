# hydroscape_lakedistrict_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials co-measured with core sediments to QA the instrument and assess measurement reliability for element identification.
- Includes measured element concentrations for standard reference sediments run with core sediment samples, enabling assessment of measurement accuracy via comparison to certified reference values.
- Recovery is defined as the percent difference between XRF-measured values and certified values; 95–105% recovery is considered very good.
- References standard sediment materials Terashima et al. (JLK-1) and Lynch (LKSD-2) used as references; Table 2 lists their published certified values.

## Data Tables

### Table 1: Core_run_and_reference_sediment_used
- Content: Name of sediment core standard sediment sample run with (e.g., JLK1 for Terashima et al. 1990; LKSD2 for Lynch et al. 1990), Run_Code, Description, and date run.
- Measured element concentrations (per sample), with units varying by element:
  - Major/trace elements: Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti often reported as % dry mass.
  - Trace elements: V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb reported in µg/g (some are denoted with specific suffixes like V_µg_g, Cr_µg_g, etc.).
- Purpose: Provide the data used for quality control of XRF measurements and to enable comparison against certified references.

### Table 2: Certified reference values
- Content: For each element, certified reference values are given for JLK-1 (Terashima et al. 1990) and LKSD2 (Lynch 1990).
- Notable points:
  - Some elements have certified values for both references, some only for one, and some entries show Not Cert where no certified value exists.
  - Examples of certified values:
    - Na_per: JLK-1 = 0.78; LKSD2 = 1.41
    - Mg_per: JLK-1 = 1.05; LKSD2 = 1.03
    - Al_per: JLK-1 = 8.85; LKSD2 = 6.5
    - Si_per: JLK-1 = 26.7; LKSD2 = Not Cert
    - K_per: JLK-1 = 2.33; LKSD2 = 2.16
    - Ti_per: JLK-1 = 0.4; LKSD2 = 0.35
    - V_µg_g: JLK-1 = 117; LKSD2 = 77
    - Fe_per: JLK-1 = 4.84; LKSD2 = 4.3
    - Pb_µg_g: JLK-1 = 43.7; LKSD2 = 44
- Purpose: Establish reference values to compute recovery and assess measurement accuracy across runs.

## Key Concepts for Data Quality

- Recovery: (Measured value – Certified value) / Certified value × 100%; targeted range 95–105% for very good accuracy.
- Not Cert: Indicates no certified reference value exists for that element in the given standard; these entries are flagged for data interpretation.
- Reference materials: JLK-1 and LKSD2 serve as standardized checks to evaluate instrument performance and data reliability across measurements.

## How this supports Data Work

- Enables quality assurance dashboards to monitor XRF performance over time (per run, per element, per reference material).
- Facilitates data cleaning and calibration steps for core sediment datasets by incorporating recovery metrics.
- Allows data users to understand measurement limitations (e.g., elements lacking certified values, or uncertain recoveries).
- Provides provenance and traceability by linking measured values to published certified references.

## Considerations and Potential Challenges

- Heterogeneous units across elements (percent dry mass vs. µg/g) require careful normalization when combining with core data.
- Notcert entries require caution in interpreting recoveries for affected elements.
- Data from two distinct reference materials (JLK-1 and LKSD2) with potentially different certification statuses should be reconciled in any comparative analyses or dashboards.