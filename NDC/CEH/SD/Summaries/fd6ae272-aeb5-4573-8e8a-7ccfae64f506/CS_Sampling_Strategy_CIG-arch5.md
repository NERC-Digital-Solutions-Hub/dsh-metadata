# The Sampling Strategy for Countryside Survey (up to 2007)

- Overview
  - Describes the evolution of the ITE Land Classification and its use as the sampling framework for Countryside Survey field surveys from 1978 to 2007.
  - Emphasises the importance of stratified, representative sampling and the linkage between classification, sample allocation, and national habitat estimates.
  - Highlights the goal of understanding changes over time while preserving the ability to compare across surveys.

- Core concepts for data governance
  - The ITE Land Classification provides the stratification framework: 1 km squares classified into land classes based on environmental attributes.
  - Sampling design combines stratification with random selection to minimize bias and enable robust national estimates.
  - Across surveys, the classification evolved (32 → 40 → 45 classes) to improve regional, Scotland-only, and Wales-only reporting.
  - Changes in classification impact national estimates; consistency considerations are documented (cross-walks between classifications, and notes on comparability).

- Evolution of the ITE Land Classification (history and why it matters for datasets)
  - Early development (1970s): 1 km squares classified using environmental attributes; ISA (Indicator Species Analysis) used to group quadrats into vegetation/land classes.
  - 1978 survey: initial sampling of 256 squares (8 per class) from 32 classes; basis for national habitat area estimates.
  - 1984 survey: expanded to 12 squares per class (384 total); continued use of the 1978 classification for national estimates.
  - 1990 survey: all GB squares reclassified within an expanded framework; 508 squares surveyed; linked to the first Land Cover Map of GB.
  - 1998 revision: classification expanded to 40 classes to support Scotland reporting; national estimates based on revised classifications.
  - 2000 update: further refinement to support England, Scotland, and Wales country-level estimates; introduction of country-unit classes and 40 strata; upland habitat module added.
  - 2007 update: Welsh-specific sub-divisions (5 new Welsh classes) and expanded Wales sampling to improve Wales-only reporting; total strata increased to 45.

- Sampling framework by survey (major milestones)
  - 1978 (Initial Land Classification & first field survey)
    - ISA-based 32 land classes from 1 km squares; center square and surrounding squares classified; 6039 km squares represented.
    - 256 squares surveyed (8 per class).
  - 1984 (Second field survey)
    - 12 squares per land class (384 total); continued use of 1978 classification for national estimates.
  - 1990 (All Squares Land Classification & third field survey)
    - Classification revised to include all GB squares; 508 squares surveyed.
    - National estimates produced using 1990 classification; Land Cover Map introduced.
  - 1998 (Revised Land Classification & fourth field survey)
    - Separate reporting for Scotland; land classes increased to 40.
    - Field survey expanded to 569 squares; new methods to account for regional reporting.
  - 2000 (Developments for Countryside Survey 2000)
    - England, Scotland, and Wales country estimates introduced; 40 strata created by subdividing classes into country-unit variants.
    - Additional 19–43 squares added in Wales to ensure representation of new Wales-specific classes; upland habitat module implemented for better upland estimates.
  - 2007 (Developments for Countryside Survey 2007)
    - Wales-focused sampling enhanced with country-unit class subdivisions (five new Welsh classes); 45 strata total.
    - Wales received 43 additional squares; England adjustments made to maintain representation; Welsh classes 5w, 6w, 7w, 15w, 18w introduced.
    - Upland habitat emphasis maintained to improve country-specific reporting.

- Data structure and outputs
  - Data are organized by Land Classes and by country (England, Scotland, Wales) with dedicated sampling rates and class counts per survey.
  - Tables and maps document the spatial distribution of sample squares and the evolving classification maps (e.g., original 1978, revised 1990, 2000, 2007 frameworks).
  - National estimates are generated through class-based computations: mean habitat area per square multiplied by land-class area, with adjustments for country-specific sampling.

- Endnotes, caveats, and documentation for data users
  - Note on consistency: changing the underlying Land Classification affects national stock estimates; preferred approach is to use the latest classification for country-specific estimates while recognizing historical comparability challenges.
  - Crosswalks and appendices provide historical context and the rationale for reclassification and sampling adjustments across surveys.
  - Acknowledgements, further reading, and references document the methodological lineage and statistical guidance that underpin the sampling strategy.

- Practical implications for data stewardship
  - Maintain versioned classifications: track Land Class definitions and their temporal changes to ensure traceability of estimates over time.
  - Preserve crosswalks and method documents: ensure datasets can be reinterpreted or reweighted if reclassification occurs.
  - Annotate country-unit distinctions: clearly separate England & Wales vs. Scotland reporting and note class subdivisions that affect estimates.
  - Archive sample allocations and spatial mappings: store the exact squares used per survey, along with class maps, to support reproducibility and longitudinal analyses.
  - Reference primary sources and metadata: rely on the Countryside Survey reports (1990, 2000, 2007) and associated appendices for dataset provenance and methodological details.