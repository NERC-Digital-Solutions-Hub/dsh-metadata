# 1990 Countryside Survey: Quality Assurance Exercise

## Overview
- A comprehensive quality assurance (QA) of the 1990 Countryside Survey to quantify recording accuracy, explain observer/seasonal/location differences, relate findings to prior work, and propose methodological improvements for future surveys.
- QA scope included two phases in 1990–1991 across multiple 1 km squares and a variety of plot types, with a focus on ensuring the spatial data (land use, vegetation, and boundaries) produced are robust for GIS-based analysis and map-based products.

## Aims
- Quantify the accuracy of field recording and the reliability of change statistics.
- Explain recording differences in terms of observer error, time of year, plot location, information type, and site factors (e.g., drought).
- Relate conclusions to previous ITE survey work.
- Recommend methodological modifications to improve accuracy and confidence of statistics for future surveys.

## Methods
- Two QA series:
  - Autumn 1990: 21 original survey squares assessed using sketch maps for plot relocation by two independent assessors.
  - 1991: Expanded QA with photographs of plots; 1 km squares from 32 terrain classes; each square analyzed with multiple plot types; three self-assessment “self-check” squares added.
- Plot types and spatial scope:
  - Quadrats: X plots (200 m2) and Y plots (4 m2).
  - Linear plots along road verges; hedges; streamsides; and boundaries.
  - For each quarter of a square, 9 predetermined points were recorded for land cover and boundaries.
- Relocation and data capture:
  - Plots relocated using sketch maps, photographs, and metal plates where possible.
  - 1 km square coverage included a mix of lowland and upland landclass aggregates (LC, LG, MA, UP).
- Data quality measures:
  - Species concordance between T1 (original) and T2 (QA) records using multiple indices.
  - Cover assessments for species exceeding 5% cover.
  - Mapping accuracy through primary land-use codes, boundary codes, and descriptive qualifiers.
  - DECORANA ordination (axis scores) to assess ecological gradient shifts between survey years.
- Annexes and tables provide detailed metrics (not reproduced here).

## Key Findings

### Plot Relocation and Data Capture
- Plate relocation recovery: Autumn 1990 = 71% (with ~5-minute search); 1991 data showed 65% plate relocation and 87% plot relocation success.
- Plot relocations varied by plot type:
  - Road verges and hedges relatively easier to relocate.
  - X plots more accurately relocated than Y plots; Y plots particularly difficult.
- Photographs markedly improved relocation accuracy and reduced misalignment between surveys.

### Species Recording and Change Statistics
- Overall species agreement between 1990 and 1991 QA assessments: about 60.9% (better than the earlier autumn 1990 QA figure of ~45%).
- Initial accuracy of recording (1990 survey) averaged around 74% after accounting for variations (season, year, etc.).
- Between 1990 and 1991, there was an across-the-board increase in mean species per plot (1990 ≈ 20.7; 1991 ≈ 23.4), with upland plots showing less seasonal effect than lowland areas.
- Seasonal and drought effects:

  - Some apparent species increases reflect genuine population changes (e.g., Taraxacum agg., Lapsana communis, Alliaria petiolata).
  - Apparent decreases or non-detections often reflect under-recording in the initial survey, particularly for certain grasses and bryophytes.
  - In upland areas, annual variation was more pronounced, suggesting recording efficiency differs by land class and habitat type.

### Land Use Mapping and Coding
- Primary land-use codes: high concordance (~88.7%).
- Boundary codes and descriptive qualifiers: slightly lower concordance (~80% range), with some dependence on whether same assessors re-visited the same squares.
- General finding: mapping codes were robust, but some codes caused misclassifications (e.g., marsh/wetland vs. improved grassland; upland vs. moorland separation).
- Recommendations to refine codes (see Recommendations) and to limit reliance on detailed qualifiers for reproducibility.

### Vegetation Cover Mapping
- Dominant species at fixed points showed substantial but imperfect reproducibility:
  - For single dominant species at a point, about 81% chance of being recorded as dominant at both times.
  - For two co-dominants, concordance dropped to ~34%.
  - Overall, detailed cover data had limited reproducibility across surveys; therefore the process is best simplified for GIS products.
- Recommendation: record only the two most prevalent species per vegetation unit to improve reproducibility; reduce reliance on fine-grained cover values.

### Ecological Gradient and Species Groups
- DECORANA analysis indicated shifts along an ecological gradient between years, with upland plots showing a distinct, stable signal and lowland plots more susceptible to year-to-year variation and crop/management changes.
- Group-level species frequency changes largely did not show significant differences across years, though some species did reflect climatic/management changes (e.g., Holcus spp. and Taraxacum agg.).

## Data Quality and Sources of Variation
- Primary sources of variation:
  - Mis-identifications and mis-codings in T1 data.
  - Species overlooked in T1 (seasonal and annual effects).
  - Over-recording or “zealous” recording near plot boundaries.
  - Plot mis-location or mis-orientation at T2.
  - Seasonal and management changes affecting species presence.
- Overall conclusion: many apparent T1 errors derive from genuine seasonal/management changes and year-to-year variation rather than pure recording mistakes.

## Recommendations (Key Points)
- General QA and field practice:
  - Conduct QA in the same year as the initial survey to minimize seasonal/annual differences.
  - Use high-quality photographs to re-establish plot positions; annotate photographs with plot context.
  - Use metal marker plates to aid relocation, especially in enclosed land; allocate additional manpower for upland relocation where plates are harder to locate.
  - Improve positioning for small plots (Y plots) with enhanced ground-truthing techniques; ensure photographs clearly show surrounding features.
  - Include distance and bearing data on sketches; ensure consistent orientation and documentation with photographs.
- Plot types and measurement:
  - Standardize Y plot orientation: use a fixed side (N-S alignment), place at SE corner, and use survey tape for boundaries.
- Vegetation recording and species:
  - Target bryophytes and grasses during training; consider including additional bryophyte species in lists for habitat-specific surveys.
  - Limit species mapping to the two most prevalent taxa per land parcel to improve reproducibility.
- Land-use coding and mapping:
  - Broaden and simplify primary land-use codes; subdivide ambiguous upland codes (e.g., 102 upland grassland) to distinguish between upland improved vs. upland unimproved grassland.
  - Introduce explicit codes for lowland rush pasture and wet heath; recognize wet heath as a distinct vegetation type at the primary code level.
  - Restrict and better define boundary codes (e.g., hedge vs. mixed boundaries) and associated qualifiers; minimize misuses of undefined forb-cover codes.
  - Increase emphasis on dichotomous land-use codes rather than detailed cover for reproducibility.
- Mapping and data-product implications:
  - For GIS data products, document QA-derived uncertainties, relocation error, and potential seasonal effects; provide guidance on aggregating across land classes.
  - Maintain metadata on plot types, relocation methods, and year of survey to enable correct interpretation of change statistics.
  - Map only the most robust features (dominant species, primary land-use codes) for stable, reproducible GIS layers; treat detailed cover codes as less reliable for cross-year comparisons.
- Future QA program:
  - Include a consistent, year-aligned QA with photographs and metal plates; limit seasonal and year-to-year variation in QA samples; emphasize same-year comparisons for change analyses.

## Implications for GIS Specialists
- QA findings underscore the importance of clear metadata, documented relocation accuracy, and standardized land-use coding for reliable GIS analyses.
- When building map-based data products from this survey:
  - Use robust land-use primary codes and hedge/boundary classifications with clear qualifiers.
  - Represent vegetation at the species level only when high confidence exists; otherwise, rely on dominant taxa per parcel.
  - Include uncertainty indicators for plot relocation and boundary placement, especially for small or unenclosed plots.
  - Provide documentation on the time frame of data capture (year, season) to inform temporal analyses and change detection.

## Conclusions
- The 1990 Countryside Survey QA demonstrated meaningful improvements in plot relocation and species recording when photographs and enhanced documentation were used, but highlighted persistent challenges with small plots, seasonal variation, and complex land-use classifications.
- Overall, the QA achieved a reasonable level of concordance (about 60.9%) and revealed opportunities to improve data consistency and reproducibility for GIS-related data products.
- The report provides concrete, actionable recommendations to enhance future surveys: same-year QA, better plotting techniques, refined coding schemes, streamlined vegetation mapping, and targeted training focused on key taxonomic groups and land-use distinctions.