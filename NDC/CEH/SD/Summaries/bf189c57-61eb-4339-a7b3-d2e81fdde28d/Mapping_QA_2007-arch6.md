# Mapping Quality Assurance Exercise

## Introduction
- Reports on the 2007 Countryside Survey QA of mapped habitat data and associated attributes.
- Transition from post-survey manual digitising to field-based digital mapping using a dedicated software (Surveyor) to reduce interpretation errors and improve data clarity.
- Digital workflow included mandatory fields, prompts, visit-status tracking, and early data checks via an interactive wiki.
- QA teams conducted in-field and office-based checks, with dedicated QA visits to survey teams to ensure protocol adherence.
- QA aimed to enable rapid analysis and integration with national-scale spatial datasets in a geodatabase.

## Extent and Sampling
- QA covered 23 x 1 km squares across Great Britain, with emphasis on representing land classes and locations.
- Areas with access refusals were excluded; analyses focused on common surveyed areas between QA and CS datasets.
- QA squares were selected to represent diverse land classes and to ensure broad geographic coverage.

## Approach and Methods
- Direct, raster, and point-based comparative approaches applied to multiple feature types (areas, lines, and points).
- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA).
- 4.2 Raster data comparisons: polygons converted to 10 x 10 m rasters within each 1 km square to compare dominant Broad Habitats and locations.
- 4.3 100-point grid: overlay of 100 points per square to compare habitat concordance at a defined resolution; used to assess commonality of Broad Habitats.
- 4.4 Attribute comparisons: reference ID layers created to compare species attributes for matched areas, lines, and points.
- Data were exported to SAS for aggregate analysis; GIS-based methods used for spatial analyses and masking of unsurveyed or refused areas.

## Data Collection and Tools
- Field data collected with Surveyor tablets; data uploaded to a wiki for rapid QA feedback.
- Mandatory fields and standardized prompts improved data completeness (e.g., dominant species per area).
- Digital system facilitated visit-status tracking and enhanced field-based data verification and consistency.

## Key Findings: Habitat Agreement and Variability
- Overall agreement: in many cases, QA and CS agreed closely on Broad Habitats (BH).
- 6.1 Direct comparison of aggregate areas:
  - 81% of squares recorded the same Broad Habitat by CS and QA.
  - Mean differences between QA and CS BH proportions were generally small: under 1% for 13 BHs, 1–2% for 5 BHs, and under 3.5% for the remaining two BHs (with some larger differences in a few cases).
  - Some potential issues flagged for particular habitats (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and certain upland mosaics).
- 6.2 Raster data comparisons:
  - Overall raster agreement averaged about 76% across squares.
  - Highest agreement in some squares (e.g., 364 at 98%; 488 at 94%), with notable low agreement in others (e.g., 773 at 23%; 261 at 49–58% depending on BH).
  - Agreement by habitat varied; some BHs showed strong concordance, others had more discrepancies.
- 6.3 100-point primary land cover codes and habitats:
  - Concordance varied by square; typical good matches in many squares, but some notable mis-matches (e.g., 773 only 19% concordance; 261 around 41–58%).
  - The 100-point analysis showed overall good agreement for many BHs but highlighted issues in a subset of squares.
  - Matrix analysis indicated some habitat-specific mis-match patterns (e.g., overlaps between Neutral and Improved Grassland, and distinctions between Broadleaf vs Coniferous Woodland).
- 6.4 Polygon species attributes:
  - 1,081 QA polygons and 998 CS polygons matched spatially; about 45% of QA polygons had at least one listed species present in the matched CS polygon.
  - Species concordance varied by Broad Habitat; woodland and Improved Grassland showed higher likelihood of matching species lists.
  - For commonly recorded species (e.g., Lolium perenne), concordance was moderate (about 66% for CS vs QA in the matched set); other species showed varying levels of agreement.
  - Overall, species concordance was lower than habitat concordance, reflecting differences in dominance and cover assessments across habitats.

## Change Recording and Feature Change
- 2007 introduced detailed change coding: Real change (physical change), Error Change (correction of previous mapping), No change.
- Change field usage showed substantial agreement between CS and QA, particularly for linear and point features; habitat-level change had more complexity.
- Tables indicate strong agreement for linear change codes and reasonable agreement for point features; some discrepancies remained in the habitat-change context due to interpretation complexities.

## Surveyor Efficiency and Data Quality
- Digital workflow improved data completeness and efficiency:
  - Very small proportion of land not visited (average around 0.4% in many squares); some variations owing to refusals.
  - Mandatory fields increased species recording frequency and data richness.
- Operator consistency: QA and CS teams generally aligned on change coding and feature class allocations; some cross-confusion noted between certain woodland and dune habitats or urban classifications.

## Notable Issues and Implications
- Blanket Bog and Dwarf Shrub Heath: major mis-matches in certain squares; updates to the field handbook in 2007 and the complex boundary between wet heath and blanket bog contributed to discrepancies; calls for further refinement of habitat definitions and training.
- Upland mosaics: fine-scale mosaics led to mismatches when decomposed into component BHs; highlights challenges mapping continua of habitat types.
- Machair-related issues on Scottish dunes: localized habitat peculiarities can skew broader comparisons; suggested caution in cross-square extrapolation for rare habitats.
- Woodland definitions: ongoing need to clarify broad vs coniferous woodland boundaries and the allocation approach (historical field methods vs new matrix-based allocation).

## Species and Change: Summary of Key Points
- Species concordance on matched polygons around 40%, highlighting broader challenges in matching species lists across CS and QA datasets due to differences in dominance interpretation and habitat pull.
- 66% concordance for Lolium perenne in matched polygons; other species varied, with several showing notable discrepancies between teams.
- Change coding overall showed strong adherence to protocols, though habitat-level changes remained more challenging due to interpretation.

## Conclusions and Recommendations
- The 2007 mapping QA demonstrates substantial overall data quality improvements through digital field mapping, wiki-based QA, and standardized attributes.
- High levels of agreement between QA and CS for many habitat types validate the validity of the digital approach and QA methodology.
- Several habitat-specific discrepancies remain, particularly Blanket Bog, Dwarf Shrub Heath, Neutral/Improved Grasslands, and certain upland mosaics; these warrant targeted refinement of habitat definitions, enhanced training, and possibly re-evaluation of mapping rules in these contexts.
- Recommendations for future QA:
  - Continue refining habitat definitions and field guidelines, especially for complex upland and transitional habitats.
  - Enhance training for survey teams on mosaic mappings and the interpretation of canopy/coniferous verses broadleaf classifications.
  - Expand 100-point and raster analyses to further isolate systematic biases and improve consistency across large-scale habitat mapping.
  - Leverage change-coding insights to improve historical data alignment and facilitate more accurate change detection in subsequent surveys.