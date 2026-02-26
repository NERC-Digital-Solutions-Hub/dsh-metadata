# hydroscape_glasgow_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials co-measured with core materials.
- Purpose: QA/QC to ensure XRF instrument stability and to assess reliability for element identification.
- Compares measured sediment element concentrations to certified values; includes mean, standard deviation across runs, and % recovery (difference between measured and certified values).
- A recovery of 95-105% is considered very good.

## Data structure and key concepts
- Reference standards and core runs:
  - JLK-1: Reference standard sediment sample run.
  - LKSD2: Reference standard sediment sample run.
- Core run metadata:
  - Run Code (UCL): Sample ID combining reference sediment type and run date.
- Quality metrics:
  - Measured Mean: Mean sediment concentration value from all runs.
  - Measured SD: Standard deviation of sediment concentration values from all runs.
  - Certified Ref Value: Certified concentration values for elements in the standard sediment (for Ref 1 and Ref 2).
  - %Recovery: (Measured value − Certified value) / Certified value × 100; indicates agreement with certified values.

## Columns and data content
- Element concentration columns (examples and units):
  - Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti% (expressed as % dry mass for some elements/parts)
  - V µg/g, Cr µg/g, Mn%, Fe%, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g, As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g
- Run Code (UCL): Identifier combining sediment type and date of run.
- Description fields clarify that element concentrations are expressed as either % dry mass or µg/g of dry sediment, depending on the element.

## Purpose and interpretation for data use
- Enables QA/QC analysis of XRF measurements by comparing measured concentrations with certified reference values.
- The %Recovery metric helps assess measurement accuracy and instrument stability across runs.
- Facilitates data-driven assessment of sediment core composition with standardized references for cross-run comparability.

## References
- Ref 1: TERASHIMA, S., et al. (1990). Elemental concentrations in nine new GSJ rock reference samples “sedimentary rock series”. Geostandards Newsletter, 14(1), 1-5.
- Ref 2: LYNCH, J. (1990). Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials LKSD-1, LKSD-2, LKSD-3, LKSD-4, STSD-1, STSD-2, STSD-3 and STSD-4. Geostandards Newsletter, 14, 153-167.