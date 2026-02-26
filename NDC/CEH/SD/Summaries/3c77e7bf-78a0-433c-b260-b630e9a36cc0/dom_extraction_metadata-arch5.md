# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Overview
- Describes water chemistry and elemental content of dissolved organic matter (DOM) extracted from UK freshwaters in 2018–2019.
- Data were quality controlled (e.g., values below detection limits addressed).
- Methods are described in a companion manuscript: A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020.
- Data are provided in five CSV files, organized to support cross-site comparisons and method evaluation.

## Data structure and contents
- DOMextraction SITES
  - Content: Characteristics of water bodies used in the study; minimum and maximum values per waterbody type.
  - Key fields: Type of waterbody (headwater, stream, lake/loch, reservoir inlet/outlet), site numbers, elevation, catchment area, pH, DOC (mg C L−1) and other site-level descriptors, dominant soil type.
- DOMextraction CHN
  - Content: Dissolved organic carbon (DOC) concentration of initial water, elemental composition, processing details.
  - Key fields: Site, DOC (mg C L−1), Method (e.g., DRY-6, RE, RO-DF, RO-RE, SPE, DRY-F, FD, DIA-FD, DIA-FH), Raw %C, Total %C, Total %N, Total %H, OrganicC%, Rate (mL h−1), Time, Recovery%.
  - Notes: Values relative to RE samples for comparison.
- DOMextraction REreps
  - Content: Replicates of DOM extraction (A and B) for each site/method.
  - Key fields: Site, Method, Replicate, Raw %C, Total %C, Total %N, Total %H.
- DOMextraction RECOVERY
  - Content: Data used to calculate recovery percentage for each sample.
  - Key fields: Volume (mL), DOMmass (mg), DOMtotal%C, DOC mass (mg), DOC mass per volume (mg L−1), DOC (mg C L−1), Recovery%.
  - Notes: Recovery >100% possible due to differences in filtration sizes between DOM preparation (0.7 μm) and DOC analysis (0.45 μm).
- DOMextraction SCORES
  - Content: Method evaluation scores used to rank extraction methods.
  - Key fields: Method, N (samples), Rate (mL h−1), Recovery% (mean), Recovery SE, Cost per sample (£), Large equipment cost (£), Rate score, Recovery score, Cost score, Sum of scores, Large equipment penalty, Rank (1–9).

## Data quality, provenance, and limitations
- All data QCed; documented in the associated manuscript.
- Recovery calculations acknowledge methodological differences (e.g., filtration size) that can produce Recovery% > 100%.
- Data are tied to specific sites, methods, and replicates via consistent identifiers, enabling traceability and auditability.
- The dataset provides explicit method codes and units to support reproducibility and interoperability.

## Governance, discoverability, and reuse considerations for Data Stewards
- Structure supports discoverability and interoperability through clear file naming, consistent field definitions, and cross-file linkages via Site numbers and Method codes.
- Documentation reference to the companion manuscript is essential for full method descriptions and to interpret CHN and SCORES fields.
- Practical use cases: cross-site comparisons of DOM content, evaluation of extraction methods, meta-analyses of water chemistry in UK freshwaters.
- Potential updates: any future deposits should maintain identical identifiers and schemas to retain compatibility; update the SCORES if new methods or replication data are added.

## Practical notes for cataloguing and uptake
- Ensure metadata records capture:
  - Dataset title and year range
  - Five CSV file names and a brief contents map
  - Units and abbreviations (e.g., DOC mg C L−1, Rate mL h−1, Recovery%)
  - Method codes and their definitions (as in CHN)
  - Relationship to the companion Water Research manuscript
- Consider linking to the original publication for methodological context and to enable users to interpret raw vs. relative values (e.g., relative to RE DOM composition).

## Source and citation
- Data deposit accompanying Moody, C.S., Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19; full methods described in A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020.