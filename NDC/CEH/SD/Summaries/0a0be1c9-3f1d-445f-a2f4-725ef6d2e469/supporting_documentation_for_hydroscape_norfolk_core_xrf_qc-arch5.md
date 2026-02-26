# hydroscape_norfolk_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials during co-measurement of core materials.
- Purpose: QA/QC to ensure instrument stability and reliability in identifying elements.
- Includes: measured values, certified values for sediments, mean and standard deviation across runs, and % recovery (difference between measured and certified values).
- A recovery of 95-105% is considered very good.

## Data structure and key fields
- Core_Code_Measured_Reference_Standard_statistics: identifies the sediment core (WBID_Core Code) and the named standard reference sediment; includes statistics.
- BR1 standard measurements:
  - Measured_Mean_BR1: mean concentration from all runs
  - Measured_SD_BR1: standard deviation across runs
  - Certified_Value_BR1: certified value for BR1
  - %Recovery_BR1: recovery percentage
- LKSD2 standard measurements:
  - Measured_Mean_LKSD2, Measured_SD_LKSD2, Certified_Value_LKSD2, %Recovery_LKSD2
- JLK1 standard measurements:
  - Certified_Value_JLK1, %Recovery_JLK1
- Element concentrations (percent dry mass):
  - Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti
- Trace element concentrations (micrograms per gram of dry sediment):
  - V_µg/g, Cr_µg/g, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g
- Note: Some fields include footnotes (e.g., “1”) indicating data type or handling, as shown in the original descriptions.

## References and provenance
- Ref 1: Epstein MS, Diamondstone BI, Gills TE. (1989) A new river sediment standard reference material. Talanta.
- Ref 2: Lynch, J. (1990). Provisional Elemental Values for LKSD reference materials. Geostandards Newsletter.
- Ref 2 (another entry): Terashima et al. (1990). Elemental concentrations in nine new GSJ rock reference samples (sedimentary rock series). Geostandards Newsletter.
- Provides the basis for the Certified_Value fields and the QA/QC framework.

## Data quality and governance considerations for Data Stewards
- QA/QC nature: serves to verify instrument stability and measurement reliability for element identification.
- Metadata to preserve: core code, reference standard names, measured means/SDs, certified values, and % recovery for each standard.
- Provenance: includes external standard references to validate calibration and accuracy.
- Sharing and updates: data should be stored with clear versioning and linked to the corresponding QA/QC standards; document any updates to standard values or measurement procedures.
- Interoperability and usability: ensure consistent naming (BR1, LKSD2, JLK1) and unit standards across systems; map to common data dictionaries to aid discovery.
- User needs alignment: data supports downstream users needing reliable QA/QC metrics for XRF core measurements and comparative element concentration data.

## Practical considerations for users
- Use %Recovery_BR1/LKSD2/JLK1 to assess measurement accuracy against certified standards.
- Treat 95-105% recovery as a benchmark of high-quality QA/QC performance.
- Refer to the specified element concentration fields to interpret core composition, distinguishing between %dry mass and µg/g units.
- Consider provenance and references for calibration when integrating with other datasets or performing cross-study comparisons.