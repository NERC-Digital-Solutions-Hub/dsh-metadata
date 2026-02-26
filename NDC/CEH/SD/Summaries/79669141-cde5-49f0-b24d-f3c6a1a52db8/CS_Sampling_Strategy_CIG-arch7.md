# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose: Outline the sampling framework used for Countryside Survey field surveys, linking it to the evolution of the ITE Land Classification and ensuring representative, plannable data for national, regional, and country-specific habitat estimates.

- Core approach: Stratified, random sampling of 1 km squares across Great Britain, using the ITE Land Classification to define strata. Each square is characterized by environmental attributes to enable robust estimation of habitat areas.

- Key data product workflow for GIS:
  - Use land classification strata to select survey squares.
  - Link field observations to classified squares and, where relevant, to the 1990 Land Cover Map derived from satellite imagery.
  - Compute national estimates of habitat extent as the product of mean habitat area per square within a class and the total area of that class.
  - Produce map-based outputs and time-series that reflect changes in habitat extent.

- Beginning, middle, and end emphasis:
  - Beginning: origins in the 1970s with a need for representative ecological sampling and the development of an objective stratification system.
  - Middle: successive surveys (1978, 1984, 1990, 2000, 2007) and the evolution of the Land Classification to improve representativeness, enable regional/country reporting, and address policy needs.
  - End: 2007 adjustments to support Wales-only reporting, introduction of country-unit subdivisions, upland sampling, and expanded Welsh representation; implications for time-series consistency and national estimates.

## The ITE Land Classification: origins and methodology

- Purpose of classification: Create homogeneous ecological strata to ensure representative sampling and robust national estimates.

- Basis: Environmental attributes (e.g., altitude, geology, climate) used to group land into land classes; initial use of Indicator Species Analysis (ISA) at smaller scales was scaled up to 1 km squares.

- Sampling rationale: Stratified, random sampling reduces bias and ensures representation of diverse land types; around 1 km square units were selected from classified classes for field survey.

- Time-series relevance: The classification has repeatedly been revised to reflect improved data and policy needs, while maintaining continuity with previous frameworks to preserve time-series validity.

## Evolution of the sampling framework across surveys

- 1978 – Initial Land Classification (CS1978)
  - ISA-based classification produced 32 land classes from environmental data for center 1 km squares (1228 central squares classified; 4 surrounding squares allocated per center).
  - Sample: 8 squares per class (total 256 squares) for field surveys.
  - National estimates: derived by applying the mean habitat area per square within each Land Class to the total area of that class.

- 1984 – Second GB Land Use Survey (CS1984)
  - Framework retained but expanded: 12 squares per class (total 384 squares), building on 1978 centers.
  - Emphasis shifted toward land use and habitat mapping.

- 1990 – Countryside Survey 1990 (CS1990) and All Squares Land Classification
  - Land Classification revised to incorporate data from all GB squares; urban and sea corrections added.
  - Survey volume: 508 squares; repeated 1978/1984 features plus a repeat of vegetation quadrats.
  - Link to first Land Cover Map of GB derived from satellite imagery.
  - Result: broader, all-squares approach for classification while maintaining continuity with prior class descriptions.

- 1998 – Developments leading to CS1990-era refinements and broader regional applicability
  - The Land Classification expanded to improve regional estimations; 40 land classes introduced for broader representativeness and to support Scotland reporting improvements.

- 2000 – Countryside Survey 2000 (CS2000) and separate country estimates
  - Rationale: policy needs to deliver separate estimates for England with Wales and for Scotland (and later Wales-specific reporting).
  - Changes:
    - Sub-division of land classes into country-unit versions (creating more strata; 40 to 45 strata).
    - Additional squares to ensure adequate representation of new classes per country.
    - Reallocation and aggregation to maintain balanced representation when country-specific counts were low.
    - Added upland module to improve accuracy for upland habitats in England and Wales (an extra 30 squares).
  - Outputs: detailed country-specific sampling maps and a refined sampling framework to support England & Wales vs Scotland estimates.

- 2007 – Countryside Survey 2007 (CS2007) and Wales-only reporting
  - Welsh reporting needs prompted further refinements:
    - Sub-division of Land Classes into country-unit versions for England & Wales and for Scotland, resulting in 45 strata.
    - Addition of 43 Welsh squares to ensure adequate representation of new Welsh classes; minimum of 6 squares per Welsh class.
    - England adjustments: two Welsh squares removed; some English classes (5e, 15e) maintained with 4 squares per class, deemed acceptable by scoping study.
  - Wales-specific class set expansions: five new Welsh country-unit classes (5w, 6w, 7w, 15w, 18w) created from sub-divided original classes.
  - Outputs: England, Wales, and Scotland sample maps and updated tables detailing square counts and sampling rates by class and country.
  - Publication: Countryside Survey – UK Results from 2007 (CEH) with country-specific results.

## Country units and sampling design

- Country-unit framework: England & Wales treated together vs Scotland for some estimates, with dedicated sub-divisions to produce Wales-only and Scotland-only results as policy contexts required.

- Representativeness and balance: Sub-dividing classes and adding squares ensured adequate representation of all classes within each country unit, improving precision for country-level estimates.

- Isle of Man: Removed from country-unit estimates for consistency with country-specific reporting.

## Upland-focused data and time-series considerations

- Upland module (CS2000): Additional squares placed in upland and marginal upland land classes to improve statistical accuracy for upland habitats within England and Wales.

- Time-series consistency: Acknowledgement that changing the Land Classification affects national stock estimates; within a survey, the latest classification is preferred for consistency, while cross-survey comparability may require crosswalks or reclassification to a common baseline.

## Outputs and implications for GIS work

- Maps and data products:
  - Land Classification maps for each survey (original 32 classes; expansions to 40, then 45 with country-unit subdivisions).
  - Maps showing survey squares across GB, including country-specific allocations (England & Wales; Scotland; Wales).
  - Tables detailing the number of squares per class, per country, and the sampling rate.

- Data interoperability:
  - Time-series analysis requires careful handling of classification changes; GIS workflows may need crosswalks between versions or reclassification to a common framework for comparability.
  - Linkage to satellite-derived Land Cover Maps (1990) enhances spatial interpretation and validates field-derived classifications.

- Practical GIS considerations:
  - Maintain documented crosswalks when classifications are revised to ensure historical comparisons are meaningful.
  - Preserve spatial extents and class definitions at the country-unit level to support policy-driven reporting.
  - Use classified squares as the primary units for aggregation when computing national and country-level habitat estimates.

## Appendix and historical context

- The document includes an Appendix with a brief history of the ITE Land Classification, outlining the evolution from 1978 through 2007 and detailing the methodologies and rationale behind each revision.

- Acknowledgements and references provide context for the statistical and methodological foundations of the sampling strategy.