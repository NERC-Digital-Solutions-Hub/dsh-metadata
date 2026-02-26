# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview
- Describes how Countryside Survey field sampling is designed using the ITE Land Classification to create spatially stratified, random samples of GB land for ecological and habitat estimates.
- Aims to produce national, regional and country-specific data products (maps and statistics) linked to a land-class framework for clear spatial interpretation.
- Emphasizes map-based data products, data provenance, and the need for representative sampling across diverse landscapes and jurisdictions (England, Scotland, Wales, Isle of Man).

## Core concepts for GIS use
- Stratified random sampling: divides land into discrete strata (Land Classes) to reduce bias and improve estimations of ecological features.
- ITE Land Classification: evolves from classifying 1 km squares using environmental attributes, to nationwide coverage across GB with refined classifications; foundational for selecting sample squares and for mapping habitat distributions.
- Time-series continuity: the sampling framework is tightly linked to prior survey methods; changes in classification affect comparability across surveys, requiring careful treatment for national estimates.

## Evolution of the ITE Land Classification and sampling (key milestones)
- 1978 (Initial Land Classification and 1st Field Survey)
  - ISA-based classification of 1 km squares; centre square of a 15×15 km grid classified (1228 squares); four surrounding squares also classified.
  - 32 Land Classes; 256 squares surveyed (8 per class).
  - National habitat estimates derived from mean per-square values times class area; maps and tables published later.
- 1984 (2nd Field Survey)
  - Sample increased to 12 squares per class (384 total); eight squares per class from 1978 retained.
  - Aimed at improving estimates and supporting policy-relevant change statistics; results published later.
- 1990 (All Squares Land Classification; 3rd Field Survey)
  - Land Classification revised to classify every GB square; 508 squares surveyed.
  - Linked to the first Land Cover Map of GB; additional squares allocated only to larger classes.
  - Results published in Countryside Survey 1990 main report.
- 2000 (Developments for CS2000)
  - Needed country-specific estimates (England & Wales; Scotland) and upland habitat estimates; classification extended to ensure representation across all squares.
  - Class sub-division to create country-unit versions; distribution adjustments led to 40 strata (vs 32 previously).
  - 19 additional squares added to ensure adequate representation; upland module introduced to improve upland habitat estimates; revised maps for England with Wales and Scotland.
- 2007 (Developments for CS2007)
  - Wales reporting tightened with Wales-specific class sub-divisions (five new Welsh classes: 5w, 6w, 7w, 15w, 18w); total strata increased to 45.
  - Wales gained 43 additional sample squares; England sampling adjusted accordingly (two English classes left with 4 squares each).
  - Upland sampling module retained to improve country-specific upland habitat estimates.
  - Revised land-class maps and sample-squares maps produced for England, Wales and Scotland.

## Sampling framework by survey and country units
- Strategy across surveys involves GB-wide sampling with country-oriented adaptations:
  - CS1978/CS1984: GB-wide stratified sampling by Land Classes; regional estimates derived from class-area proportions.
  - CS1990: All GB squares classified; 508 squares surveyed; introduction of Land Cover mapping; aims to improve regional estimates.
  - CS2000: Separate country-unit estimates introduced; creation of country-specific class versions; increased strata to 40; additional upland sampling.
  - CS2007: Wales-focused adjustments; Welsh sub-classes introduced; more Welsh squares to improve Wales-only estimates; overall Wales sampling emphasized.
- Isle of Man: previously sampled squares replaced to better align country-unit estimates (Isle of Man squares no longer used for country-unit estimates).

## Outputs and GIS data products
- Land Classification maps:
  - GB-wide maps, including England-with-Wales and Scotland configurations (Figure references in the document).
- Sampling maps:
  - Maps showing Countryside Survey sample squares for England, Wales, and Scotland.
- Tabular outputs:
  - Tables detailing the number of squares surveyed per Land Class per survey (including CS2007 adjustments), sampling rates, and strata area.
- Data provenance and notes:
  - Documentation on how estimates are computed (e.g., using mean habitat area per square within a class multiplied by class area) and cautions about comparing estimates across different Land Classings.
  - Notes on consistency: changing Land Classification affects national estimates; recommended approach for consistency is to use the latest classification for within-survey estimates, while older classifications may be used for cross-survey comparisons.

## Practical considerations for GIS specialists
- Map-based interpretation:
  - Use Land Classification maps to understand spatial distribution of habitat types and to contextualize sample-square locations.
  - Leverage country-unit subdivisions (England with Wales; Scotland) for policy-relevant, jurisdiction-specific analyses.
- Data integration and time-series:
  - Be mindful of classification changes across CS1990, CS2000, and CS2007 when aggregating or comparing across surveys; document the classification version used for each estimate.
- Data completeness and quality:
  - Acknowledge the upland and Welsh-class subdivisions introduced to address under-sampling in certain regions and habitat types.
- Data products useful for policy and public-facing GIS:
  - Land Classification maps (with class IDs and descriptions) and sample-square distributions enable transparent visualization of habitat extent and sampling coverage.
  - Country-specific outputs support regional planning and environmental policy reporting.

## Endnotes and references
- The document includes detailed histories, figures, and tables, and references to supporting literature for deeper methodological context (e.g., CS1990 main report, CS2000 scoping studies, and Welsh/England-specific CS2007 work).