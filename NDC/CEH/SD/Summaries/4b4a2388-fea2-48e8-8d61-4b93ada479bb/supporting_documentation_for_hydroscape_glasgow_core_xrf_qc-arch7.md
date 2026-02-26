# hydroscape_glasgow_xrf_cores_qc.csv

## Overview
- QA/QC dataset for XRF measurements of core sediments, used to verify machine stability and measurement reliability (QA/QC).
- Contains measured values, certified reference values, and recovery (percent difference) for elements in sediment standards.
- Helps ensure data produced from core analyses are accurate before map-based visualization and GIS analyses.

## What the data describe
- Measurements are taken against two reference standards run with sediment cores: JLK-1 and LKSD2.
- For each run, the table includes:
  - Measured mean and standard deviation of sediment element concentrations across runs.
  - Certified reference values for each standard.
  - Recovery (% difference between measured and certified values), with 95–105% considered very good.
  - Run Code (UCL): identifies the sample by reference sediment type and date.
- Elements covered and units:
  - Major elements (as % dry mass): Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, Mn, Fe.
  - Trace elements (as µg/g): V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb.
- Mn%, Fe%, and Mn/Fe-related entries indicate concentration expressed as % dry mass for those elements.

## Data fields and structure
- Reference standards:
  - JLK-1 Reference Standards with core run (Description: sediment core standard sample run).
  - LKSD2 Reference Standards with core run (Description: sediment core standard sample run).
- Measured values:
  - Measured Mean: mean concentration from all runs.
  - Measured SD: standard deviation of concentration values across runs.
- Certified reference values:
  - Certified JLK-1 Ref Value.
  - Certified LKSD2 Ref Value.
- Recovery:
  - JLK-1 %Recovery.
  - LKSD2 %Recovery.
- Run and sample identifiers:
  - Run Code (UCL): sample ID combining reference sediment type and date.
- Element concentration fields:
  - Major elements (% dry mass): Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, Mn%, Fe%.
  - Trace elements (µg/g): V, Cr, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb.

## Data quality and usage notes for GIS work
- Recovery guidance: 95–105% recovery is considered very good, indicating reliable measurements for mapping.
- Data integration:
  - Use Run Code (UCL) to join XRF QA/QC data to core-level GIS attributes or to spatially-referenced core metadata.
  - Combine with other core metadata (position, depth, age) to produce element distribution maps.
- Units and interpretation:
  - Distinguish between major element concentrations (% dry mass) and trace element concentrations (µg/g) when creating thematic layers or choropleth maps.
- Data limitations:
  - Data are focused on QA/QC runs; ensure you apply these values to validated core measurements, not preliminary data.
  - Resolution and completeness depend on the availability of the Run Code and corresponding core metadata.
- Relevance to GIS storytelling:
  - Enables visualization of elemental composition across cores and cores’ positions, supporting investigations into sediment provenance, depositional environments, or environmental conditions.

## References
- TERASHIMA, S., ANDO, A., OKAI, T., et al. (1990). Elemental concentrations in nine new GSJ rock reference samples 'sedimentary rock series'. Geostandards Newsletter, 14(1), 1-5.
- Lynch, J. (1990). Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials LKSD-1, LKSD-2, LKSD-3, LKSD-4, STSD-1, STSD-2, STSD-3 and STSD-4. Geostandards Newsletter, 14, 153-167. https://doi.org/10.1111/j.1751908X.1990.tb00070.x