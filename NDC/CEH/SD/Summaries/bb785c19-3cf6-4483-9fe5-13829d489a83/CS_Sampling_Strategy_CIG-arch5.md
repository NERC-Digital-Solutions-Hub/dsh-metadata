# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and context
  - Documents the field survey sampling strategy used for Countryside Survey up to 2007, building on a 30-year lineage of the ITE Land Classification (started in 1978).
  - Emphasizes that the current methodology is inseparable from its predecessors and that understanding prior developments is essential for interpreting time-series data.

- Core concepts
  - Stratified sampling to ensure representative coverage of GB land strata and to reduce bias from purely random samples.
  - The ITE Land Classification as the primary stratification framework, originally created by environmental attributes (e.g., altitude, geology, climate) and refined over time.
  - Use of 1 km2 sample units (center squares of a 15 × 15 km grid) with surrounding squares included to populate class characterisation.
  - Gradual expansion from ecological quadrats and soils (1978) to land use, habitat mapping, and land cover data (1984–1990).

- Evolution of the Land Classification and sampling framework
  - 1978 (Initial Land Classification)
    - Indicator Species Analysis used to derive 32 land classes from environmental attributes for classified 1 km squares (center squares of a 15 × 15 km grid).
    - 256 squares surveyed (8 per class) to estimate national habitat areas by class means multiplied by class area.
  - 1984 (Second land use survey)
    - Sampling increased to 12 squares per class (total 384); used the 1978 classification; focus shifted to land use features.
  - 1990 (All Squares Land Classification; CS1990)
    - Expanded to classify every GB square; 508 squares surveyed; addition of Land Cover Map via satellite data; replication of prior vegetation quadrats.
    - Resulted in revised estimates and the need for classification updates for regional/local accuracy.
  - 1998 (Revised Land Classification for CS1990; CS1990 onward)
    - Extended to allow separate Scottish reporting; number of land classes increased to 40; framework prepared for regional estimates.
  - 2000 (CS2000; CS2000 changes)
    - Introduction of country-unit estimates (England with Wales, Scotland separately) with sub-division of land classes and aggregation where necessary to ensure adequate representation.
    - Added 19 extra squares to improve class representation; upland habitat sampling module planned to improve upland estimates.
  - 2007 (CS2007; Wales-focused adjustments)
    - Wales-specific reporting requirements prompted new country-unit classes (5w, 6w, 7w, 15w, 18w) and 45 strata.
    - Wales received 43 additional squares; England adjusted accordingly to maintain representativeness; Wales upland sampling enhanced; overall distribution mapped across England, Wales, and Scotland.

- Country-specific estimates and upland module
  - Distinct country units were created to provide England with Wales and Scotland-specific estimates, requiring class sub-division and class-aggregation to form 40–45 strata.
  - Wales required more intensive sampling for Wales-only reporting; England received some compensatory adjustments.
  - An uplands module added to CS2000/CS2007 to improve habitat estimates in upland England and Wales.

- Data products and reporting
  - National estimates are calculated by combining mean habitat area per square within each Land Class with the total area of that class.
  - Tables and figures (e.g., sampling numbers by class and country; maps of revised land classes and sample squares) document the distribution, sampling rates, and class compositions.
  - Separate country maps and estimates are produced to satisfy policy and regulatory needs (England with Wales; Scotland; and Wales-specific reporting).

- Documentation and transparency
  - Acknowledges the methodological changes across surveys and notes the impact of changing classifications on cross-survey comparability.
  - Includes extensive references and appendices detailing the history of the ITE Land Classification and its applications.
  - Emphasizes the importance of documenting the classification version used for any given national estimate to maintain consistency and reproducibility.

- Data governance implications for Data Stewards
  - Version control: Track Land Classification versions (1978, 1990, 1998, 2000, 2007) and country-unit adaptations to ensure reproducibility of time-series estimates.
  - Metadata: Include detailed metadata on classification scheme, class definitions, sampling frames, number of squares per class, country-specific tweaks, and upland modules.
  - Provenance: Preserve chain-of-custody from initial stratification to final national estimates, including the rationale for class subdivisions (e.g., 5w, 6w, 7w, 15w, 18w) and Wales-specific adjustments.
  - Data integration: Manage cross-survey harmonization challenges when multiple classifications are used for national estimates; ensure clear mappings between old and new classifications.
  - Access and sharing: Provide access to stratification maps, sample square coordinates, class assignments, and country-specific estimates with clear disclaimers about differences across classification versions.
  - Quality and governance controls: Maintain audit trails for additions of upland modules and extra squares; document any reclassification of squares and its impact on estimates.

- Acknowledgements and references
  - Acknowledges contributions from DETR, CEH, and ITE personnel; extensive bibliographic references detailing the development and application of the ITE Land Classification and Countryside Survey results.

- Practical takeaway for data stewardship
  - The Countryside Survey sampling framework is a carefully versioned, country-specific, stratified, and adaptive system designed to produce robust, comparable habitat estimates over time.
  - Effective data stewardship requires rigorous metadata, transparent versioning, and clear documentation of country-specific adjustments and upland modules to support reuse and policy-relevant analysis.