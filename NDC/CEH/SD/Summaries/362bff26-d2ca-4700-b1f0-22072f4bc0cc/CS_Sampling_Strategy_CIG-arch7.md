# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Documents the sampling framework and evolution of the ITE Land Classification used to stratify Countryside Survey field surveys from 1978 through 2007.
  - Emphasises the linkage between time-series data and the classification system, and how sampling design supports national and country-level estimates.

- Core concepts relevant to GIS work
  - ITE Land Classification: a stratified environmental framework that partitions Great Britain into land classes based on environmental attributes (e.g., altitude, geology, climate) to ensure representative sampling.
  - Stratified random sampling: avoids bias by ensuring samples cover all strata; sample units are 1 km squares, with surrounding squares allocated to each classified centre square.
  - Temporal evolution: classifications and sampling frames have been revised to support Scotland-only, England-and-Wales, and Wales-only reporting, while maintaining comparability across surveys.

- Timeline of key developments
  - 1978 (Initial Land Classification)
    - Indicator Species Analysis used to create 32 land classes from 1228 central 1 km squares (centre of 15x15 km grid).
    - Sampling: eight squares per class; total of 256 samples; nationwide estimates derived from class proportions and square-level data.
  - 1984 (2nd field survey)
    - Expanded sampling to 12 squares per class (384 total); updated framework retained 1978 classification for national estimates.
  - 1990 (CS1990; All Squares Land Classification)
    - Extended classification to include all 1 km squares in GB; 508 squares surveyed.
    - Linked to the first Land Cover Map of GB; national estimates now based on a more comprehensive classification.
  - 1998 (Revised Land Classification)
    - Classification expanded to 40 classes to support Scottish reporting; results published for CS1990; 569 squares surveyed.
  - 2000 (CS2000; Separate country estimates)
    - Adjusted framework to enable country-unit estimates (England with Wales, Scotland) by subdividing classes and aggregating where necessary.
    - Added 19 extra squares to ensure adequate representation of new classes; upland habitats module introduced for England and Wales to improve upland estimates.
    - Wales received increased sampling, enabling Wales-only reporting; Isle of Man removed from country-unit estimates.
  - 2007 (CS2007; Welsh and upland emphasis)
    - Wales-only reporting requirements drove further class subdivisions (creating 5w, 6w, 7w, 15w, 18w) and an expanded 45 strata.
    - Additional 43 Welsh squares added; two English classes (5e, 15e) left with fewer samples than ideal but deemed acceptable for reporting.
    - England did not receive additional Welsh squares; uplands module retained with 30 extra squares for England and Wales.
    - Overall, CS2007 incorporated Wales-specific data while maintaining England and Scotland comparability.

- Country-specific sampling and estimates
  - Separate country-unit estimates introduced to improve policy alignment and reporting (England with Wales, Scotland).
  - Wales received targeted enhancements to sampling density and class subdivisions to enable Wales-only statements.
  - Isle of Man samples were replaced in country-unit reporting.

- Upland module
  - A dedicated uplands survey component added in CS2000 for England and Wales; 30 extra squares placed in upland and marginal upland land classes to improve statistical precision for upland habitat estimates.

- Outputs and data considerations for GIS users
  - Land Classification maps have been revised multiple times; cross-survey comparability requires attention to changes in class definitions and country-unit subdivisions.
  - National estimates are derived from class means and the land-class areas; changes in classification can affect stock estimates and trend analyses.
  - The dataset contains structured strata and square-level data aligned to land classes, enabling spatial analyses by class, country unit, or upland modules.
  - Acknowledges the trade-off between precision (more squares per class) and practicality, especially when Welsh-class representations are introduced or adjusted.

- Practical implications for GIS specialists
  - When aggregating across years, be aware of reclassifications and country-unit dissections that may shift class boundaries or sample allocations.
  - Leverage the Land Classification maps to perform stratified analyses, quantify change by class, and compare Wales, England, and Scotland outputs.
  - Plan for integrating upland modules and separate country estimates to support policy-specific GIS applications.
  - Ensure data standards and metadata capture the version of the Land Classification used for each survey to maintain temporal consistency.

- Acknowledgements and references
  - Historical credits and references to various researchers and reports that shaped the Land Classification and Countryside Survey methodology.
  - Notable sources include CS1978, CS1984, CS1990, CS2000, and CS2007 main reports and related methodological papers.