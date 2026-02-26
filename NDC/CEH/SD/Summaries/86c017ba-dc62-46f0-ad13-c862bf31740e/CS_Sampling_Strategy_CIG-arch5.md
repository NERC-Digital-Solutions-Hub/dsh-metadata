# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Describes the field survey sampling strategy used for the Countryside Survey up to 2007.
  - Synthesizes three decades of development of the ITE Land Classification, which provides the framework for stratified ecological sampling across Great Britain.
  - Highlights how the sampling framework underpins national, regional, and country-specific estimates of habitats and land use.

- Core concepts for data governance
  - Stratified sampling to ensure representative coverage of diverse ecological land types.
  - ITE Land Classification: a hierarchical set of land classes derived from environmental attributes used to stratify the population of 1 km squares.
  - Sampling units: 1 km squares (center squares of a 15 × 15 km grid), with surrounding squares allocated to classes to ensure robust classification and linkage to field data.
  - Longitudinal linkage: the current sampling framework is built on prior surveys (1978, 1984, 1990, 2000) to enable time-series analysis and change detection.

- Evolution of the ITE Land Classification and sampling (chronology)
  - 1978 (Initial Land Classification and first field survey)
    - Indicator Species Analysis (ISA) used to create 32 land classes from environmental data for 1228 center squares; four surrounding squares added per center to total 6039 km squares classified.
    - Field survey of eight squares per land class (256 total) to produce national estimates.
  - 1984 (Second field survey)
    - 12 squares surveyed per land class (384 total). National estimates still based on the 1978 Land Classification.
  - 1990 (All Squares Land Classification; third field survey)
    - Expanded to classify every square in GB; 508 squares surveyed.
    - Land Cover Map of GB linked to this program; results published in Countryside Survey 1990 main report.
  - 1998 (Revised Land Classification; fourth field survey)
    - Land Classification updated to allow Scotland-only reporting; number of Land Classes increased to 40.
    - Distinct reporting and data handling for Scotland began; caveats about consistency across surveys noted.
  - 2007 (Revised Land Classification; fifth field survey)
    - Wales-specific reporting requirements drive further classification changes; five new country-unit classes created (5w, 6w, 7w, 15w, 18w).
    - 45 strata total; additional Welsh squares added to ensure adequate representation; some English classes reduced in sample due to Wales-focused adjustments.
    - Wales becomes the most intensively sampled country unit; England and Scotland adjusted accordingly.

- Country-specific estimates and sampling adjustments
  - Separate country estimates introduced to provide England with Wales, and Scotland-specific results.
  - Changes include sub-division of land classes into country-unit versions, aggregation where necessary, and additional sampling squares to ensure adequate representation of new classes.
  - The 2007 framework includes detailed distribution of sample squares by class and country, with Wales receiving significant expansion to support Wales-only reporting.

- Upland habitat module (CS2000)
  - An additional module added to improve estimates for uplands in England and Wales.
  - 30 extra squares allocated to land classes occurring in upland areas to enhance statistical precision for upland habitats.

- Data, documentation, and national estimates
  - Documentation emphasizes the importance of using a consistent Land Classification when producing national estimates, noting that switching classifications can affect comparability across surveys.
  - Note Regarding the Creation of National Estimates (2006) discusses trade-offs between using the latest classification (country-specific versions) versus maintaining consistency with the original global approach; recommends the latest approach for internal consistency.
  - Table 4 illustrates historical sample sizes per class across CS1978, CS1984, CS1990, CS2000, and CS2007 to aid users in understanding changes in sampling design.

- Practical data management implications for Data Stewards
  - Data lineage and versioning: the Land Classification framework has evolved multiple times; datasets should be versioned and tagged with the classification version used for estimation.
  - Metadata and provenance: documents should capture the sampling frame (center square concept, surrounding squares), the number of squares per class, and any country-unit sub-divisions.
  - Data storage and accessibility: national and country-specific results are embedded in Countryside Survey reports (CS1990, CS2000, CS2007) and associated maps; ensure access to both the raw square-level data and the derived estimates.
  - Reproducibility and updates: when new surveys occur, clearly indicate which Land Classification and sampling frame are in use; provide mapping between old and new classifications to maintain comparability.
  - Governance of data sharing: coordinate with policy requirements for Wales, Scotland, and England reporting; preserve the ability to extract Wales-only, Scotland-only, and England-with-Wales results as needed.
  - Data quality considerations: upland module adds complexity; ensure clear documentation of how upland squares are selected and how that affects estimates.
  - Data interoperability: the Land Classification links to various outputs (maps, tables, reports); maintain consistent class descriptions and wipe/replace legacy classifications with careful crosswalks when publishing cross-survey comparisons.

- Data products and references
  - Key outputs include the Countryside Survey reports (CS1990 main report; CS1990 vol.2; CS2000 summary; CS2007 UK results) and associated figures/maps (land class maps and sampling frameworks for England, Wales, and Scotland).
  - Appendices and further reading provide detailed historical context on the development and application of the ITE Land Classification.

- Endnotes and acknowledgments
  - Acknowledgments highlight statistical guidance and data synthesis support; multiple references document the methodological development and application of the land classification over time.