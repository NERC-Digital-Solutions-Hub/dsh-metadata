# File name: hydroscape_lakedistrict_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials used during co-measurement of core sediments.
- Purpose: quality control of the XRF instrument and assessment of measurement reliability for elemental identifications.
- Includes measured element concentrations in samples alongside published certified/reference values; differences are expressed as recovery percentages.
- Recovery of 95–105% is considered very good.

## Data structure and content
- Table 1: Core_run_and_reference_sediment_used
  - Describes the sediment core standard used, run code/date, and sample IDs.
  - Elemental concentrations reported as:
    - Na_per, Mg_per, Al_per, Si_per, P_per, S_per, Cl_per, K_per, Ca_per, Ti_per (percent dry mass)
    - V_µg_g, Cr_µg_g, Mn_per, Fe_per, Co_µg_g, Ni_µg_g, Cu_µg_g, Zn_µg_g, Ga_µg_g, As_µg_g, Br_µg_g, Rb_µg_g, Sr_µg_g, Y_µg_g, Nb_µg_g, Ba_µg_g, Pb_µg_g (various units)
  - Reference sediments include JLK-1 (Terashima et al. 1990) and LKSD2 (Lynch et al. 1990).
- Table 2: Certified reference values
  - For each element, provides certified values for JLK-1 and LKSD2 where available.
  - Notations:
    - Not Cert where a certified value does not exist.
    - Values are given in the same units as Table 1 (e.g., %dry mass or µg/g).
  - Examples of certified values include Na_per, Mg_per, Al_per, Si_per, P_per, S_per, K_per, Ca_per, Ti_per, V_µg_g, Cr_µg_g, Mn_per, Fe_per, Co_µg_g, Ni_µg_g, Cu_µg_g, Zn_µg_g, Ga_µg_g, As_µg_g, Br_µg_g, Rb_µg_g, Sr_µg_g, Y_µg_g, Nb_µg_g, Ba_µg_g, Pb_µg_g.
- References
  - Terashima, S. et al. (1990) Geostandards Newsletter: Elemental concentrations in nine new GSJ rock reference samples.
  - Lynch, J. (1990) Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials.

## Quality metrics and interpretation
- Recovery is calculated as the percent difference between XRF-measured values and certified values.
- Target recovery range is 95–105% for very good accuracy.
- Some elements have Not Cert status in one or both reference materials (e.g., Si_per for LKSD2, Cl_per, P_per, etc.), indicating uncertified reference values for those cases.
- Data traceability:
  - Measurements linked to standard reference materials (JLK-1 and LKSD2) to verify instrument performance and measurement reliability.
  - Documented run information (Run_Code, date) supports reproducibility and auditability.

## Data governance and implications for Data Leaders
- Provenance and trust:
  - Clear lineage through standard references and published certificates.
  - Includes both measured data and corresponding certified values, enabling calculation of accuracy metrics.
- Metadata and discoverability:
  - Essential metadata includes sample IDs, reference sediment type, run code, date, and units for each element.
  - Table 2 provides certified benchmarks to assess future data quality and comparability.
- Data quality considerations:
  - Not Cert entries highlight gaps where interpretation should be cautious or where re-measurement or alternative references may be necessary.
  - Documented recovery targets guide ongoing QC practices for XRF analyses.
- User and collaboration context:
  - The approach supports broader data quality systems by enabling cross-checks against established references and enabling consistent reporting of analytical accuracy.
  - Useful for teams coordinating multi-lab analyses or integrating core sediment chemistry data into larger datasets.

## Practical implications for practice
- Use Table 1 data to monitor instrument performance over time via recovery against Table 2 certified values.
- Flag results with Not Cert and review methodology or reference material selection before downstream use.
- Maintain and share metadata to ensure datasets remain discoverable and interpretable within a data ecosystem and across partner networks.

## References
- TERASHIMA, S., ANDO, A., OKAI, T., KANAI, Y., TANIGUCHI, M., TAKIZAWA, F., & ITOH, S. (1990). Elemental concentrations in nine new GSJ rock reference samples 'sedimentary rock series'. Geostandards Newsletter, 14(1), 1-5.
- LYNCH, J. (1990). Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials LKSD-1, LKSD-2, LKSD-3, LKSD-4, STSD-1, STSD-2, STSD-3 and STSD-4. Geostandards Newsletter, 14, 153-167.