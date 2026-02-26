# File name: hydroscape_norfolk_xrf_cores_qc.csv

- Purpose and scope
  - Describes the table of results from XRF measurements of standard reference materials collected during co-measurement of core sediments.
  - Aims to ensure the stability of the XRF instrument during operation and to assess the reliability of measurements for identifying elements (QA/QC).
  - Compares measured values with certified reference values for the sediments; uses mean, standard deviation, and percent recovery (%Recovery).

- Key metrics and data structure
  - Core and standards identifiers:
    - Core_Code_Measured_Reference Standard_statistics: name of the sediment core (WBID_Core Code) and named standard reference sediment; includes statistics.
  - QA/QC statistics per standard:
    - Measured_Mean_BR1, Measured_SD_BR1: mean and standard deviation of BR1 measurements across runs.
    - Certified_Value_BR1: certified value for BR1 elements.
    - %Recovery_BR1: percent difference between measured and certified values for BR1.
    - Measured_Mean_LKSD2, Measured_SD_LKSD2: mean and SD for LKSD2.
    - Certified_Value_LKSD2: certified value for LKSD2.
    - %Recovery_LKSD2: percent recovery for LKSD2.
    - Certified_Value_JLK1, %Recovery_JLK1: corresponding values for JLK1.
  - Elemental concentration measurements (dry mass basis):
    - %dry_mass: Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti.
    - µg/g: V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb.

- Data interpretation
  - The table presents the measured mean and SD across runs for each standard, alongside certified values and the resulting %Recovery.
  - A recovery range of 95–105% is considered very good, indicating strong agreement between measurements and certified references.

- References and standards
  - Ref 1: Epstein MS, Diamondstone BI, Gills TE. A new river sediment standard reference material. Talanta (1989).
  - Ref 2: Lynch J. Provisional Elemental Values for LKSD reference materials. Geostandards Newsletter (1990).
  - Ref 3: Terashima et al. Elemental concentrations in nine new GSJ rock reference samples (sedimentary rock series). Geostandards Newsletter (1990).
  
- Relevance for monitoring framework authors
  - Provides explicit QA/QC metrics, traceability to certified references, and clear data provenance essential for monitoring frameworks.
  - Highlights the importance of metadata clarity (core code, standards, runs, element units) to support data governance, sharing, and reuse.
  - Demonstrates how standardized QC benchmarks (percent recovery) are used to validate instrument performance and data reliability in environmental health monitoring.