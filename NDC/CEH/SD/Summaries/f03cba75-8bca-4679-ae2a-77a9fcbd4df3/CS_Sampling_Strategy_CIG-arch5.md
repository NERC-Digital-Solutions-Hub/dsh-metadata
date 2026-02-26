# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Documents the field survey sampling framework used by Countryside Survey up to 2007.
  - Emerges from a 30-year lineage of the ITE Land Classification intended to stratify GB land for representative ecological surveying.
  - Emphasises the need for time-series data to detect change in habitats and landscapes.

- Core concepts and data structures
  - ITE Land Classification: a stratified environmental classification of GB used to partition the landscape into discrete land classes for sampling.
  - Sampling unit: 1 km square; sampling is conducted within classified squares.
  - Stratified, random sampling to ensure representativeness and minimize bias; avoids extremes that pure random sampling might produce.
  - Indicator Species Analysis (ISA) as an early multivariate method used to group quadrats into land classes.

- Evolution of the sampling framework by survey
  - 1978 (Initial Land Classification and field survey)
    - 32 land classes; centre squares of a 15 x 15 km grid across GB classified (1228 squares); four surrounding squares included (total 6039 km squares considered).
    - 8 squares per land class surveyed (256 total); national habitat areas estimated by class proportions multiplied by class areas.
  - 1984 (Second land-use survey)
    - 12 squares per land class (384 total); continued use of the 1978 Land Classification for national estimates.
  - 1990 (All Squares Land Classification; CS1990)
    - Revision to classify all 1 km squares in GB; 508 squares surveyed.
    - Addition of Land Cover Map from satellite data; broader data collection (habitat mapping and repeated quadrats).
    - Some squares reclassified; results published in CS1990 main report.
  - 1998 (Revised Land Classification; CS1990 results extended)
    - Land Classification expanded to 40 classes to support regional/local estimates; Scotland reporting enabled.
  - 2000 (CS2000)
    - Enables separate country estimates (England & Wales vs Scotland) by subdividing classes into country-unit versions; total 40 strata.
    - Additional squares added to ensure adequate representation; upland habitats module introduced to improve England/Wales upland estimates.
    - Isle of Man squares replaced; maps and tables show distribution and sampling rates.
  - 2007 (CS2007; Wales-specific considerations)
    - Wales reporting requirements lead to Welsh-specific class subdivisions (five new Welsh classes) and 45 strata.
    - Added 43 Welsh squares to ensure minimum representation; some English classes reduced to 4 squares per class due to distribution, with minor precision impact considered acceptable.
    - Wales and England now have distinct country-unit sampling layouts; updated maps and class maps presented.

- Country reporting and upland focus
  - Separate country estimates (England with Wales; Scotland) introduced for policy and legislation needs.
  - Wales required more intensive sampling, prompting Welsh-class subdivisions and additional Welsh squares.
  - Uplands module added in CS2000 to boost statistical accuracy for upland habitats in England and Wales.

- Data interpretation and consistency notes
  - Changing the basic land classification used for national estimates affects cross-survey comparability; CS literature recommends using the latest classification for country estimates, while older classifications aid cross-survey consistency.
  - National estimates can be derived with different classifications; explicit crosswalks and documentation are provided to maintain traceability.

- Data governance implications for Data Stewards
  - Versioning and provenance: maintain clear records of Land Classification versions (1978, 1990, 1998, 2000, 2007) and their corresponding sample frames.
  - Metadata and crosswalks: document classifications, class definitions, country-unit subdivisions, and how squares map to classes across surveys.
  - Data lineage and updates: track reclassification of squares and adjustments for country reporting; preserve historical data alongside revised classifications.
  - Data quality and representativeness: monitor under-representation in certain classes (noted in CS2000/CS2007 adjustments) and ensure sufficient sample sizes per class and per country unit.
  - Interoperability and sharing: align data structures across England, Wales, Scotland, and Isle of Man contributions; provide transparent methods for combining or separating country estimates.
  - Documentation for reuse: include comprehensive methodology notes, rationale for class subdivisions, upland module details, and notes on the impact of classification changes on estimates.

- Key outputs and references
  - Tables and figures document the number of squares, strata, and sampling rates per survey (CS1978, CS1984, CS1990, CS2000, CS2007).
  - Appendix and historical narrative summarize the development of the ITE Land Classification and its application to successive Countryside Survey iterations.
  - Notable publications linked to methodology and results include CS1990 main report, CS2000 scoping and Wales reporting studies, and CS2007 Wales-focused reporting documents.

- Takeaway for data stewardship
  - The Sampling Strategy is a foundational, versioned framework driving how ecological data are collected, classified, and reported across UK nations.
  - Effective data stewardship requires rigorous documentation of classifications, sampling design, country-unit adjustments, and data updates to support accurate discovery, reuse, and policy-relevant reporting.