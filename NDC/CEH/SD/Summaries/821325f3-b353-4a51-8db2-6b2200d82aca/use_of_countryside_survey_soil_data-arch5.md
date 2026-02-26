# Sampling design

- Overview
  - Soils were sampled across Countryside Survey (CS) in 1978, 1998, 2007 and 2019, with a rolling survey starting in 2019 aiming to measure about 100 squares per year for five years before repeating.
  - Power analyses (Emmett et al. 2008) guided the number of samples needed to detect significant change.
  - A pilot survey occurred in 2018; 2019 marked the start of ongoing annual sampling.

- Data structure and identifiers
  - Sampling locations are CS X-plots within CS squares; each square contains 5 X-plots.
  - X-plots are not true replicates due to differing land uses and soil types; locations may relocate over time.
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1). Samples with the same ID originate from the same location, though exact positions may shift ~2–3 m within a 2 m × 2 m plot.
  - Some plots have been destroyed or access denied, leading to relocations; tracking of locations and IDs is essential.

- Sampling methods
  - Soils are collected from the top 15 cm (8 cm for invertebrates); 1998 onward used a soil core hammered in and pulled out; 1978 used a soil pit.
  - In some cases, full 15 cm cores could not be obtained due to stones or shallow soils.
  - Core photographs and dimensions were recorded in 2007 for two of the four cores (black cores and N mineralization cores).
  - A rolling CS survey method has been adopted since 2019.

- Measurements and laboratory analyses
  - 1978: only pH and loss-on-ignition (LOI).
  - 1990: some soil mapping conducted.
  - 1998, 2007, and rolling survey (2018/2019–2023): multiple cores per X-plot; different cores have different measurements.
  - Chemical analyses by horizon were not performed; samples are homogenized before pH and LOI measurements.
  - Bulk density measured in 2007 and 2018/19–2023, but not using ISO bulk-density methods (which require full cores).
  - Full methodological implications are documented (Emmett et al. 2008).

- Statistical analysis considerations
  - Analyses should account for the structure of CS and potential land-class confounding; ignoring land-class structure can yield unweighted stock/change estimates rather than nationally weighted estimates.
  - Bootstrapping is not consistently used; a mixed model approach with square as a random factor is recommended to account for multiple X-plots (up to five) within each CS square.
  - Design-based approaches with dispersed observations can increase precision and regional coverage; spatial structure is not a central aim.
  - Users are advised to consult UKCEH prior to analysis and interpretation and to review published CS data analyses available on the CS website.

- Data quality, completeness, and curation
  - Not all measurements were made on all samples; not all cores have the same measurement suite across years.
  - None of the chemical analyses are performed by horizon; homogenization precedes pH and LOI.
  - Variability in core collection methods and non-ISO bulk-density methods introduce comparability considerations.
  - Documentation and cross-year method changes are critical for proper interpretation.

- Data governance and sharing considerations
  - Clear metadata should capture sampling design changes, plot relocations, repeat identifiers, and measurement histories to support reproducibility.
  - Versioning and provenance are essential given evolving rolling survey methods and sampling resolutions.
  - Users should be directed to UKCEH guidance and existing CS publications for appropriate analysis context.
  - Ensure that data releases include method details (sampling depth, core handling, measurements per core, and any deviations) and a crosswalk to older datasets.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.