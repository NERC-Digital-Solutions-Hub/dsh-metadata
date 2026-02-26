Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013. Rose, R.J., Marrs, R.H., O'Reilly, J. & Furness, M.

# Overview
- Long-term study of vegetation response to rotational burning and grazing at Moor House National Nature Reserve, initiated in 1954 on burnt blanket bog.
- Experimental design includes four blocks (A–D) with randomized split-plot treatments: Fenced vs Unfenced (grazing by sheep), and burning regimes: no burn (N), short rotation burn (S), long rotation burn (L).
- Data collected through two main methodologies across multiple decades, forming a time-series useful for policy evaluation and environmental health monitoring.

# Experimental design
- Four replicate blocks A–D (altitudes 594–625 m) arranged to face uphill.
- Each block divided into two strips (fenced and unfenced) and further into three 30 m × 30 m cells (total 90 m × 60 m per block).
- Burning treatments within each strip randomly assigned to cells: N (no burn since 1954), S (short rotation burn), L (long rotation burn).
- Initial burning occurred in 1954; subsequent burns occurred in 1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07, and 2016/17 (note 2006/07 burn delayed by two years).

# Data collection methods and sampling regimes
- 1961 and 1965: Quadrat method
  - Post-burn vegetation recorded using 1 m × 1 m quadrats with Domin cover estimates.
  - 1961: 25 quadrats per block (intersection of a 5 m grid); 1965: 10 quadrats per plot (points 6–15).
  - DOMIN scale converts cover to scores (from -1 to 9 based on percentage cover).
- 1972 onwards: Pin (pin-frame) method
  - Data collected during the 8th growing season (July–August) in 1972, 1982, 1992, 2001, and 2013.
  - Each 30 m × 30 m cell contains a central recording plot (14 m × 6 m) with 7 transects and 6 quadrats per transect (total 82 1 m × 1 m quadrats per plot).
  - Pin frame with 10 pins provides height-strata data across four vegetation layers (>30 cm, 20–30 cm, 10–20 cm, 0–10 cm) for vascular plants; non-vascular plants and abiotic features recorded as unstratified.
  - Data recorded as absolute counts (touches) for vascular plants and presence/absence for non-vascular plants; bryophytes, lichens, and litter recorded unstratified in some surveys.
  - In 1972/1982, some data were unstratified; by 1992, 2001, and 2013, stratified vascular plant data were commonly recorded.
- Fieldwork practices and instruments
  - Permanent fences and posts mark blocks and treatment extents; central recording plots are clearly delineated for consistency.
- Quality control
  - Surveys conducted by experienced botanists in pairs, maintaining consistent methods and equipment across years.

# Data structure and datasets
- Quadrat method dataset (1961 and 1965)
  - Columns: Year (1961, 1965), Block (A–D), Treatment (S, L, N), Fenced (UF or F), Quadrat (1–25), DOMIN score (-1 and 1–9), Species number (VESPAN code), Species name (updated nomenclature).
- Pin method dataset (1972 onwards)
  - Columns: Year (1972, 1982, 1992, 2001, 2013), Block (A–D), Treatment (S, L, N), Fenced (UF or F), Stratified (s or u), Transect (A–G, with left/right designations), Quadrat (1–6), Frame (1–5), Pin (1–10 per frame position), Strata (1 (>30 cm), 2 (20–30 cm), 3 (10–20 cm), 4 (0–10 cm), 99 unstratified), Score (touch counts where applicable), Species number, Species name.
  - Note: Stratified categories (1–4) used for vascular plants; bryophytes/lichens and some unrecorded vascular plants use 99 (unstratified).
- Datasets are part of the Environmental Change Network (ECN) database and are stored as CSV files with detailed metadata describing variables and coding.

# Metadata, data governance, and openness
- Metadata and species nomenclature have been updated over time to maintain consistency with modern classifications.
- Data are publicly shareable where permissible; underlying data sharing is considered in the context of governance and openness standards.
- Documentation and quality control emphasis ensures traceability, comparability across years, and data usability for policy evaluation and future decision-making.

# Data provenance and supporting documents
- Related publications and guides:
  - Marrs et al. (1986): guide to recording methods and the Moor House database.
  - Adamson & Kahl (2001): vegetation changes within sheep exclosure plots.
  - ECN website: www.ecn.ac.uk
- These documents provide context, methodological details, and historical insights for monitoring and interpreting long-term vegetation changes.

# Relevance for monitoring frameworks
- Demonstrates a robust, long-term monitoring framework with controlled experimental manipulations (burning and grazing) and standardized data collection methods.
- Provides two complementary data collection approaches (quadrats and pin frames) enabling cross-method validation and richer temporal insights.
- Highlights key considerations for environmental health monitoring: data standardization, metadata completeness, data governance, and clear communication of complex findings to stakeholders.
- Illustrates practical challenges for monitoring programs: maintaining consistent methods over decades, integrating datasets, and ensuring data accessibility across organizations and time.