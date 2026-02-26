hydroscape_lakedistrict_xrf_cores_qc.csv

## Overview
- Describes the table of results from XRF measurements of standard reference materials co-measured with core sediments.
- Purpose: quality control of the XRF instrument and assessment of measurement reliability for element identification.
- Outputs include measured element concentrations in core-related samples and comparisons to published reference values.

## Data structure and content

- Table 1: Core_run_and_reference_sediment_used
  - Columns include: Run_Code, Description (sediment core standard, e.g., JLK1 or LKSD2), Sample ID, and element concentrations.
  - Elements presented with units: Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti (percent dry mass); V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb (micrograms per gram or percent where noted).
  - Sediment standards referenced: JLK-1 ( Terashima et al., 1990 ) and LKSD2 ( Lynch, 1990 ).
  - Includes descriptive run information (e.g., run date) and the reference sediment type.

- Table 2: Elemental reference values and recovery context
  - For each element, shows certified values for JLK-1 and LKSD2 where available.
  - Entries may be labeled Not Cert where no published certified value exists.
  - Recovery concept: difference between XRF-measured values and certified values expressed as a percentage; 95–105% recovery is considered very good.

- References for reference materials
  - Terashima, S. et al. (1990). Elemental concentrations in nine new GSJ rock reference samples.
  - Lynch, J. (1990). Provisional elemental values for eight new geochemical lake sediment and stream sediment reference materials.
  - Publication context: Geostandards Newsletter, various volumes.

## Methods and quality assurance

- QA purpose: verify instrument performance and ensure reliable elemental identifications in core sediments.
- Approach: measure core samples alongside standard reference sediments to evaluate accuracy against certified values.
- Data characteristics:
  - Table 1 provides raw/measured concentrations and metadata about the run and sediments used.
  - Table 2 provides corresponding certified reference values for calibration/validation.
  - Recovery percentages guide assessment of measurement accuracy (target 95–105%).
- Data handling notes:
  - Not Cert entries indicate unavailable certified values for those element-species in the given reference.
  - Units vary by element (percent dry mass vs. µg/g), requiring careful unit consistency for data integration.

## Provenance and references

- Core samples and reference materials:
  - JLK-1: Terashima et al., 1990.
  - LKSD-2: Lynch, 1990.
- Certification benchmarks drawn from Geostandards Newsletter references:
  - Terashima et al. 1990; Lynch 1990.

## Data governance and stewardship considerations

- Metadata stewardship:
  - Capture explicit linkages between core samples and the precise reference material (JLK-1 or LKSD2) used for QA.
  - Document run codes, dates, sample IDs, and the exact element units.
- Data quality controls:
  - Store and compute recoveries to track instrument reliability over time.
  - Flag Not Cert values and document any gaps in certified references.
- Interoperability and standards:
  - Ensure consistent units and naming for elements across datasets.
  - Maintain traceability to the published reference materials and their provenance.

## Usage guidance and flags

- How to use:
  - Compare measured Table 1 values to Table 2 certified values to assess accuracy (recoveries).
  - Identify elements with acceptable recoveries (approx. 95–105%) as reliably measured.
  - Use Not Cert markings to note where certified benchmarks are not available.
  - Record and report any discrepancies or require re-measurement or recalibration if recoveries fall outside acceptable range.
- Documentation and reproducibility:
  - Include run_code, sample_id, reference_sediment, and element units in data releases.
  - Link back to Terashima et al. (1990) and Lynch (1990) for provenance.

## Limitations and caveats

- Not Cert entries indicate missing certified reference values for certain elements, limiting validation for those cases.
- Some elements have dual reporting units (percent dry mass vs. µg/g), requiring careful unit handling during integration.
- The accuracy assessment depends on the availability and quality of the reference materials (JLK-1 and LKSD2) and their published cert values.

## Reference information

- TERASHIMA, S., et al. (1990). Elemental concentrations in nine new GSJ rock reference samples 'sedimentary rock series'. Geostandards Newsletter, 14(1), 1-5.
- LYNCH, J. (1990). Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials LKSD-1, LKSD-2, LKSD-3, LKSD-4, STSD-1, STSD-2, STSD-3 and STSD-4. Geostandards Newsletter, 14, 153-167. https://doi.org/10.1111/j.1751-908X.1990.tb00070.x