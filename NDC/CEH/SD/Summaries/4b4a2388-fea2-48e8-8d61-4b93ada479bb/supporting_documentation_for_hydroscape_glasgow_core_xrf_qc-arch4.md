# hydroscape_glasgow_xrf_cores_qc.csv

## Purpose and scope
- Describes the QA/QC table of results from XRF measurements of standard reference materials co-measured with core sediments.
- Aims to ensure instrument stability during operation and assess measurement reliability for elemental identification.

## Data contents and structure
- Includes both measured values from the runs and certified values for the sediments (reference standards JLK-1 and LKSD2).
- Key metrics per run:
  - Run Code (UCL): sample ID combining reference sediment type and run date.
  - Measured Mean and Measured SD: average and variability of sediment concentrations across all runs.
  - Certified Reference Values (for Ref 1 and Ref 2): official sediment standard values.
  - %Recovery: difference between measured and certified values expressed as a percentage (used to gauge accuracy).
- Recovery benchmark:
  - 95–105% recovery is considered very good.
- Measured variables and units:
  - Major elements: Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, Mn% (and others as listed).
  - Trace elements: V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb (expressed as µg/g for many trace elements or % for some majors, as indicated).
- Data layout supports comparison between measured values and certified values across multiple runs.

## Reference standards and provenance
- Reference materials:
  - JLK-1 Reference Standards with core run (sediment standard sample).
  - LKSD2 Reference Standards with core run (sediment standard sample).
- References for certified values:
  - TERASHIMA et al. (1990) GSJ rock reference sediments.
  - LYNCH (1990) Provisional elemental values for LKSD reference materials.
- Mentions specific publication details and DOIs for traceability of certified values.

## Data quality indicators and usage
- The table provides a direct QA/QC metric (recovery) to assess accuracy against certified sediment values.
- Means and standard deviations across runs provide a measure of precision and reproducibility.
- The structure supports validation of data products and instrument performance over time.

## Data stewardship, metadata, and discoverability
- Clear labeling of Run Code, sediment reference type, and run date improves traceability.
- Detailed description of each measured element and its unit enhances metadata quality and discoverability for downstream users.
- Alignment with established reference standards supports data integrity and auditability.

## Implications for Data Leaders
- Demonstrates a robust QA/QC workflow essential for trustworthy data products in sediment core analysis.
- Highlights the importance of maintaining reference standards, documented metadata, and quantitative accuracy metrics (recovery).
- Supports broader data strategy goals: understanding data quality, ensuring discoverability of QA/QC metrics, and enabling co-ownership of data products through clear provenance and performance indicators.

## Considerations and potential challenges
- Mixed units (%, µg/g) across elements require consistent interpretation and potential unit standardization when integrating with other data products.
- Dependence on external published reference values necessitates ongoing maintenance of provenance and versioning for certified data.
- Sector-wide coordination and shared communities of practice can enhance harmonization of QA/QC standards across projects.