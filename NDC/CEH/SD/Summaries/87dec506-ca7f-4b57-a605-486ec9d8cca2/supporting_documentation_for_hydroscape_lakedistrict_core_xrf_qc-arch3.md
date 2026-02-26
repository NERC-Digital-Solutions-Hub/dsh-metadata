# hydroscape_lakedistrict_xrf_cores_qc.csv

## Purpose
- Describes quality control (QC) results from XRF measurements of standard reference materials co-measured with core sediments to ensure instrument reliability and accurate element identification.

## What the dataset contains

- Table 1: Core_run_and_reference_sediment_used
  - Details the reference sediments (JLK-1 Terashima et al. 1990; LKSD2 Lynch 1990), sample IDs, run codes, and descriptions.
  - Element concentrations are listed for each sample:
    - % dry mass: Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti
    - µg/g dry sediment: V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb

- Table 2: Certified reference values
  - Provides certified (reference) concentrations for the same elements in JLK-1 and LKSD2.
  - Entries marked Not Cert where no published value exists.
  - Notes recovery as the percent difference between XRF-measured value and certified value.

## Key concepts and metrics

- Recovery: expressed as a percentage difference between measured and certified values; a recovery of 95–105% is considered very good.
- Not Cert: indicates no certified value exists for that element in the given reference material.
- Units: some elements reported as %dry mass; others (V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb) as µg/g.

## Data provenance

- References for reference materials:
  - Terashima, S. et al. (1990). Elemental concentrations in nine new GSJ rock reference samples “sedimentary rock series”.
  - Lynch, J. (1990). Provisional elemental values for eight new lake sediment and stream sediment reference materials LKSD-1, LKSD-2, etc.
- Both cited in Geostandards Newsletter.

## Relevance for monitoring frameworks

- Provides a structured QC framework to validate XRF measurements used in environmental health monitoring and policy evaluation.
- Enables assessment of data quality, comparability, and traceability through documented reference materials and recovery metrics.
- Highlights data governance considerations:
  - Need to share underlying QC data and metadata.
  - Identify gaps where certifications are missing or Not Cert.

## Practical implications for implementation

- Use Table 1/2 as a benchmark to calibrate and verify XRF instruments across monitoring programs.
- Track recovery over time to ensure consistent instrument performance.
- Clearly document Not Cert elements and interpret their impact on analyses.
- Align QC data with data sharing and metadata standards to support transparent decision-making.