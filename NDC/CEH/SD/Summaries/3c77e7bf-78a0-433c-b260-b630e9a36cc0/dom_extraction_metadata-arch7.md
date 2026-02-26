# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

- Purpose
  - Provides water chemistry and dissolved organic matter (DOM) composition data from UK freshwaters (2018–19), prepared for analysis and comparison of DOM extraction methods.
  - Data are quality controlled, including treatment of values below detection limits.

- Data holdings (five CSV files)
  - DOMextraction SITES
    - Waterbody type (headwater, stream, lake/loch, reservoir inlet, reservoir, reservoir outlet)
    - Site numbers; elevation (m asl); catchment area (km²)
    - pH, DOC (mg C L⁻¹), POC (mg C L⁻¹)
    - Dominant soil type (peat or mineral soils)
    - For each waterbody type: minimum and maximum values across sites
  - DOMextraction CHN
    - Site number; DOC concentration (mg C L⁻¹)
    - Extraction method used (e.g., DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, dialysis variants)
    - Raw % contents: Total C, Total % N, Total % H, Organic C %
    - Rate (mL h⁻¹); Time from start to final DOM sample; Recovery %
    - Relative % content values compared to reference (RE) samples
  - DOMextraction REreps
    - Site number; Replicate method (A, B, etc.)
    - Raw % contents: Total C, Total % N, Total % H
  - DOMextraction RECOVERY
    - Site number; Method used
    - Volume (mL); DOM mass (mg); DOM total C (%); DOC mass (mg); DOC mass per volume (mg L⁻¹); DOC concentration (mg C L⁻¹)
    - Recovery % (relative to original water DOC concentration)
  - DOMextraction SCORES
    - For each method: number of samples, mean rate (mL h⁻¹), mean recovery %, standard error of recovery
    - Cost per sample (£) and large equipment cost (£)
    - Score components: Rate, Recovery, Cost, Large equipment penalty
    - Sum of scores and final Rank (1–9)

- Methods and quality control
  - Data collection and generation methods described in the accompanying manuscript: A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020
  - Quality control applied; detection-limit handling acknowledged (values below detection limits QC’d)
  - Extraction methods include multiple approaches (e.g., DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, DIA-FD, DIA-FH)

- GIS-relevant considerations
  - Spatial attributes: site-level data with elevation and catchment-area context, enabling spatial mapping of waterbody types and DOM properties
  - Enables mapping and visualization of DOC and POC distributions across UK freshwaters, and comparison by waterbody type
  - Data can be joined across files by Site number to combine chemistry with extraction method details and processing metrics
  - Aggregation (min/max) by waterbody type supports type-level thematic maps and overview analyses

- Practical notes for GIS work
  - Ensure consistent units across fields (e.g., DOC mg C L⁻¹, C/N/H percentages)
  - Handle fields with 'n.a.' or method-relative interpretations carefully (e.g., Relative to RE)
  - Temporal frame is 2018–19; consult the accompanying manuscript for broader temporal context and methodology

- Provenance and access
  - Data deposit accompanies a methodological manuscript; QC performed
  - Contents include five CSV files with detailed field descriptions as listed above