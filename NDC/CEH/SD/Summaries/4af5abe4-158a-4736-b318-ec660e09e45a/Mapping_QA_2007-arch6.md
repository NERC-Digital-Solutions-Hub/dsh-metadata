# Mapping Quality Assurance Exercise

- Purpose: Evaluate the quality and consistency of the digitised countryside mapping from the 2007 Countryside Survey using a digital workflow (Surveyor software, wiki data checks) and QA comparisons between surveyors and QA teams.
- Data workflow: Surveyors map in the field with mandatory fields; data uploaded to an interactive wiki for early QA; Quality Control teams visit survey teams to ensure protocol adherence; data integrated into a geodatabase for analysis.

## Extent

- QA covered 23 1km squares, selected to represent land classes and locations across Great Britain.
- Not all areas were surveyed due to access refusals; analyses focused on common surveyed areas between QA and survey data.

## Approach

- QA teams mapped in parallel to survey teams, often in near-simultaneous visits to minimise temporal vegetation changes.
- Data collected on standard tablets and consolidated into a single geodatabase; unsurveyed or refused areas excluded from both datasets for comparability.
- Analyses used a combination of direct comparisons, rasterization, and point grids to assess accuracy across areas, lines, and points.

## Analysis methods

- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA).
- 4.2 Comparisons of raster data: convert polygons to 10x10 m raster cells; compare dominant Broad Habitats and locations.
- 4.3 100-point grid overlap: overlay 10x10 grid, compare Broad Habitat matches, compute concordance per square.
- 4.4 Attribute comparisons: generate reference ID layers to compare species attributes for matched features.

## Surveyor efficiency

- In-field use of visit status and mandatory fields improved data completeness and species recording compared with past surveys.
- Not-visited land was low on average (about 0.4% in many squares; 0% for most QA squares); some areas remained inaccessible.
- Slightly more species were recorded per area under the digital system (Table 5.2 trend).

## Results: Habitat and raster concordance (6.x)

- 6.1 Direct aggregate areas: in 81% of squares, Broad Habitats (BH) were recorded by both CS and QA. Mean differences between QA and CS were generally small (often <1–3.5% of habitat extent); some habitats showed larger SDs, indicating potential misallocations (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral sand/maritime habitats).
- 6.2 Raster data: overall raster agreement averaged around 76%, with several squares showing high concordance (e.g., 364, 488) and some lower (e.g., 261, 773). Per-habitat agreement varied by square.
- 6.3 100-point grid: general agreement across many squares; notable exceptions where concordance was low (e.g., squares 773 and 261). Overall, positive concordance was common, but some mosaics and upland mosaics produced mismatches.
- 6.4 Polygon/species attributes: about 45% of QA polygons had at least one listed species matching the spatially matched CS polygon; 77% of those had a matching Broad Habitat. Species concordance was around 40% overall, with higher concordance for woodlands and Improved Grassland. Dominant species differed where habitats were diverse or mosaicked.

- Notable issues:
  - Blanket Bog: major discrepancies between QA and CS, linked to evolving definitions and field handbook revisions in 2007; square 773 particularly affected by mis-match between Dwarf Shrub Heath and Blanket Bog.
  - Urban vs grassland classifications and the boundary between Neutral/Improved Grassland caused some misallocations.
  - Upland mosaics: small-scale variability and mosaicking of habitats increased matching difficulty.
  - Machair on Scottish dunes presented localized anomalies, highlighting landscape- and location-related confounding factors.

## Results: Linear features and points

- 7.1 Linear features: overall lengths were similar between QA and CS with small differences; different land-use themes (banks, fences, forestry belts, etc.) showed strong alignment; few cases of mismatch (e.g., fence vs wall) but overall consistency high.
- 7.2 Land-use themes for linear features: high consistency in land-use coding between QA and CS; few instances where QA recorded but CS did not, indicating robust cross-checking.
- 8.1 Points: total point counts per square were broadly consistent; minor differences attributable to interpretation of land-use themes for points.
- 8.2 Point habitat codes: surveyors and QA largely agreed on point habitat codes; rare confusions around woodland/forest coding.

## Change recording (9)

- Change codes captured as Real Change, Error Change, or No Change; the digital workflow allowed more detailed change codes and potential data updates.
- Tables 9.1–9.3 show generally high agreement between CS and QA on change classification across broad habitats, linear features, and point features, though some complexities remained, especially for habitat-based change assessments.
- The digital change-coding process helped identify and correct mis-allocations where appropriate, albeit with initial learning curves for surveyors.

## Conclusion and implications for data support

- The 2007 digital QA exercise significantly improved data quality and the ability to compare survey data with QA data within a geodatabase framework.
- Overall habitat agreement was substantial, with most discrepancies being explainable by habitat definitions, mosaics, or landscape context (especially Blanket Bog and upland mosaics).
- The exercise highlighted the need for:
  - Ongoing refinement of habitat definitions (notably Blanket Bog) and clear guidance for woodland classification.
  - Improved training in complex habitats and mosaic mapping to reduce misallocations.
  - Further exploration of species concordance in mosaicked habitats to understand how BH allocation influences dominant species selection.
- The findings support continued data quality improvements and suggest targeted areas for definitional clarification and training to enhance future survey consistency.