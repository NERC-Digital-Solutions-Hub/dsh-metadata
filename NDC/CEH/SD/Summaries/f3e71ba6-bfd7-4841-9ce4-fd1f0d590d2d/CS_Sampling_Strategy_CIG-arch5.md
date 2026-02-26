# THE SAMPLING STRATEGY FOR COUNTRYSIDE SURVEY

## Overview
- Documents the evolution and methodology of the field survey component of Countryside Survey (CS) up to 2007.
- Central idea: use the ITE Land Classification as a stratification framework to produce representative, stratified, random samples of Great Britain for estimating habitat areas and changes over time.
- Emphasises link between sampling design, land classification, and the ability to generate national and country-specific estimates.

## Key Concepts and Data Assets
- ITE Land Classification
  - Began in the 1970s to stratify land into homogeneous units for ecological surveying.
  - Based on environmental attributes (e.g., altitude, geology, climate) using multivariate classification (Indicator Species Analysis historically).
  - Initial 1 km square sampling framework led to 32 Land Classes (with surrounding squares classified for context).
  - Evolved over time to include more classes and country-specific versions (Scotland, England, Wales), and later country-unit subdivisions (e.g., 5w, 6w, 7w, 15w, 18w for Wales/England).
- Stratified, random sampling
  - Early CS: eight squares per Land Class (256 total) in 1978.
  - 1984: increased to 12 squares per class (384 total).
  - 1990: “All Squares” Land Classification; 508 squares surveyed; linked to first Land Cover Map of GB.
  - 2000: new framework to enable England and Wales vs Scotland country estimates; expanded to 40 strata with additional squares; uplands module added.
  - 2007: Wales-focused adjustments; five new country-unit sub-classes; increased Welsh sampling to ensure six squares per class; overall GB sampling raised to 591 squares.
- Outputs and scope
  - National habitat estimates derived from mean habitat area per square within each Land Class multiplied by the total area of that class.
  - Across surveys: CS1978, CS1984, CS1990, CS2000, CS2007 reports and tables; maps and figures accompany results.
  - Separate country estimates (England & Wales; Scotland) implemented from CS2000 onward; Wales required additional sub-division and sampling to meet policy needs.
  - Uplands module (England & Wales) introduced in CS2000 to improve accuracy for upland habitats.

## Evolution Timeline (Core Changes by Year)
- 1978 (Initial Land Classification & Field Survey)
  - 32 Land Classes; 8 squares per class; 6039 km squares classified around centre squares.
  - National estimates calculated from class-area proportions.
- 1984 (2nd Field Survey)
  - 12 squares per Land Class; total 384 squares; used 1978 classification for national estimates.
- 1990 (All Squares Land Classification; 3rd Field Survey)
  - Classification expanded to include all GB squares; 508 squares surveyed.
  - First Land Cover Map linked to the programme; broader data collection (habitat mapping, soils, quadrats repeated).
- 1998 (Revised Land Classification; 4th Field Survey)
  - Separate reporting for Scotland introduced; Land Classes increased to 40.
- 2000 (CS2000)
  - England & Wales and Scotland country estimates formalised; sub-division of Land Classes into country units; 40 strata expanded to 45; additional squares added to improve representation; uplands module introduced.
- 2007 (CS2007)
  - Wales-focused sampling adjustments to enable Wales-only reporting; five new country-unit classes (5w, 6w, 7w, 15w, 18w); 43 additional Welsh squares; England adjusted correspondingly; total GB sample squares reached 591.
  - Wales and England results prepared to support devolution-era policy needs.

## National Estimates and Data Handling
- Estimation approach
  - National estimates derived by multiplying the mean habitat area per square (within each Land Class) by the total area of that class, across the surveyed squares.
  - Tables and figures document the number of squares surveyed by class and country, sampling rates, and stratum areas.
- Consistency and comparability
  - Changing Land Classification across surveys affects cross-time comparability of national estimates.
  - For consistency, newer classifications are preferred for country-specific estimates, while older classifications may be used for cross-survey consistency.
- Country-specific reporting
  - From CS2000 onward, England & Wales and Scotland are reported separately; Wales required additional sampling and explicit country-unit class definitions.
  - Isle of Man samples were replaced to ensure they did not skew country estimates.

## Data Governance and Stewardship Considerations
- Classification versioning
  - Land Classification evolves; maintain clear versioning and crosswalks to ensure traceability of estimates to a specific classification version.
- Metadata and lineage
  - Document class definitions, subdivision logic (country units), sampling frames, and the exact number of squares per year/class.
- Data accessibility and reuse
  - Data products include公開 reports (CS2007 UK Results, etc.), maps, and tables; ensure availability of underlying stratification, sample counts, and stratum areas for replication and secondary analyses.
- Data quality and representativeness
  - Weighting and sampling rate transparency are essential; uplands module and country-unit sampling decisions should be reflected in data dictionaries.
- Lessons for governance
  - Any future surveys should plan for devolution-driven reporting needs, ensure adequate sampling per new sub-classes, and preserve compatibility with historical classifications where possible.

## Challenges and Considerations for Data Stewards
- Incomplete alignment of user needs with evolving classifications and country-specific reporting requirements.
- Timeliness and sufficiency of data collection, particularly for underrepresented regions or sub-classes (notably Wales in earlier years).
- Handling multiple, changing systems and formats (land classes, country-unit versions, upland modules) while maintaining backward compatibility.
- Transferring and integrating large geospatial datasets (1 km squares, land classes) across time and across national boundaries.
- Ensuring clear documentation of methodology changes to prevent misinterpretation in longitudinal analyses.

## Endnotes and Further Reading
- Official CS reports and related methodological papers provide detailed class descriptions, maps, and tables (CS1978–CS2007; Welsh, English, and Scottish reporting adjustments).
- The document includes extensive historical appendices detailing class evolution, sampling counts, and crosswalks between classifications.