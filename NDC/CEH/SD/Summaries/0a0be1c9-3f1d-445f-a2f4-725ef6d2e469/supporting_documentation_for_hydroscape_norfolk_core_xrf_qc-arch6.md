# hydroscape_norfolk_xrf_cores_qc.csv

## Overview
- Describes the QA/QC table of XRF measurements performed on standard reference materials during co-measurement of core sediments.
- Purpose: assess instrument stability and reliability of element identification; compare measured values to certified values.
- Key quality metric: recovery (percent difference between measured and certified values); 95–105% recovery is considered very good.

## What the document contains
- A table structure linking core codes to measured reference standards and statistics.
- For each sediment standard (BR1, LKSD2, JLK1): mean and standard deviation of measured concentrations, certified values, and the recovery percentage.
- Element concentration data organized by units: major elements as percent dry mass and trace elements as micrograms per gram (µg/g).

## Data fields and structure
- Core and standard information:
  - Core_Code_Measured_Reference Standard_statistics: sediment core name and reference sediment (WBID_Core Code) with standard reference sediments.
  - Measured_Mean_BR1, Measured_SD_BR1: mean and SD for BR1 runs.
  - Certified_Value_BR1: certified value for BR1 element(s).
  - %Recovery_BR1: recovery percentage for BR1.
  - Measured_Mean_LKSD2, Measured_SD_LKSD2: mean and SD for LKSD2 runs.
  - Certified_Value_LKSD2: certified value for LKSD2.
  - %Recovery_LKSD2: recovery percentage for LKSD2.
  - Certified_Value_JLK1, %Recovery_JLK1: certified value and recovery for JLK1.
- Major element concentrations (percent dry mass):
  - Na_%, Mg_%, Al_%, Si_%, P_%, S_%, Cl_%, K_%, Ca_%, Ti_%.
- Trace element concentrations (µg/g or % where indicated):
  - V_µg/g, Cr_µg/g, Mn_%, Fe_%, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g.

## QA/QC purpose and interpretation
- Uses standard reference materials to monitor instrument stability and measurement accuracy over runs.
- Recovery values indicate closeness to certified values; target range 95–105% for high reliability.
- Presence of both mean and standard deviation supports assessment of measurement precision across runs.

## References (standard reference materials)
- Ref 1: Epstein MS, Diamondstone BI, Gills TE. A new river sediment standard reference material. Talanta (1989).
- Ref 2: Lynch, J. Provisional Elemental Values for LKSD and related reference materials. Geostandards Newsletter (1990).
- Ref 2 (Terashima et al.): Elemental concentrations in nine new GSJ sedimentary rock reference samples. Geostandards Newsletter (1990).

## Practical use for data consumers
- Validate chemistry data quality before using for policy, reporting, or research.
- Incorporate QA/QC metrics into dashboards or reports to demonstrate instrument stability.
- Compare outputs against certified values to flag potential drifts or anomalies.
- Use recovery figures to communicate confidence in major and trace element measurements.