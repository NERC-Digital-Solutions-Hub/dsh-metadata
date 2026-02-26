# hydroscape_norfolk_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials co-measured with core materials.
- Purpose: QA/QC to ensure instrument stability and assess reliability of element identification.
- Compares measured values with certified reference values for sediments and reports mean, standard deviation, and percent recovery (measured vs certified).
- Recovery of 95–105% is considered very good.

## Data content and structure
- Core and reference information:
  - Core_Code_Measured_Reference Standard_statistics: sediment core name (WBID_Core Code) and the named standard reference sediment, plus statistics.
  - Measured_Mean_BR1, Measured_SD_BR1: mean and standard deviation for BR1 standard runs.
  - Certified_Value_BR1: certified value for elements in BR1 sediment.
  - %Recovery_BR1: percent recovery for BR1.
  - Measured_Mean_LKSD2, Measured_SD_LKSD2: mean and standard deviation for LKSD2 standard runs.
  - Certified_Value_LKSD2: certified value for LKSD2.
  - %Recovery_LKSD2: percent recovery for LKSD2.
  - Certified_Value_JLK1: certified value for JLK1 (reference sediment).
  - %Recovery_JLK1: percent recovery for JLK1.
- Element concentration fields (sediment composition):
  - %dry mass measurements: Na_%, Mg_%, Al_%, Si_%, P_%, S_%, Cl_%, K_%, Ca_%, Ti_%.
  - Concentration in dry sediment: V_µg/g, Cr_µg/g, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g.
  - Note: some fields show a trailing “1” in the description (likely formatting artifact) but represent µg/g concentrations or %dry mass as stated.

## QA/QC metrics and interpretation
- Recovery (%): difference between measured and certified values expressed as a percentage.
- Emphasis on recovery ranges to gauge measurement reliability; a recovery of 95–105% indicates very good agreement with standards.

## References (provenance)
- Ref 1: Epstein MS, Diamondstone BI, Gills TE. (1989). A new river sediment standard reference material.
- Ref 2: Lynch, J. (1990). Provisional elemental values for LKSD-1 to LKSD-4 and other sediment references.
- Ref 3: Terashima et al. (1990). Elemental concentrations in nine new GSJ rock reference samples (sedimentary rock series).

## GIS relevance and usage
- Purpose-built for validating XRF-derived sediment element data before spatial mapping.
- Provides a traceable QA/QC backbone: use BR1, LKSD2, and JLK1 recoveries to flag datasets with poor calibration.
- Enables confident integration of core-derived element concentrations into GIS layers and thematic maps.
- Useful for data provenance: link core codes to QA/QC metrics and reference standards in spatial analyses.