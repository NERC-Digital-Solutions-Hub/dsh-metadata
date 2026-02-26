# 1990 COUNTRYSIDE SURVEY: QUALITY ASSURANCE EXERCISE

- Purpose: Outline scope, results, and recommendations of quality assurance (QA) for the 1990 Countryside Survey to assess accuracy and reliability of field recording and methodology, and to guide future improvements.

## Aims

- Quantify accuracy of field recording and its impact on change statistics.
- Explain differences in recording due to observer error, season, plot location, information type, and regional factors (e.g., drought).
- Relate findings to previous ITE survey work.
- Recommend methodological modifications to improve accuracy and confidence of statistics.

## Methods

- Two QA series:
  - Autumn 1990: 21 of the original survey squares; independent assessors used original sketch maps for plot relocation.
  - Summer 1991: Expanded to include photographs of selected plots; additional self-assessment squares; 1 km squares across 32 terrain classes.
- Plot types assessed (divided within squares): 
  - Quadrats: 200 m2 (X-plots) and 4 m2 (Y-plots)
  - Linear plots: Roadverges
  - Hedges, streamsides, verges, boundaries (and other linear features)
  - A subset of plots was relocated using sketch maps, photographs, and metal plates; a portion used plate relocation to test ground locateability.
- Sampling within squares: quarter-square relocations to include representative plot types; nine pre-determined points for landcover/boundary features.
- Data quality metrics:
  - Species concordance across survey times (T1 vs T2) using multiple indices (percent agreement, common species-based measures, and accuracy measures).
  - Plate/plot relocation success rates; captures of location accuracy with time effort.
  - Cover estimates for selected species; comparison of cover values between survey times.
  - Mapping and coding assessment: land-use primary codes, boundary codes, and descriptive qualifiers; evaluation of consistency and level-of-agreement across time and between assessors.
  - DECORANA ordination (first axis) to evaluate ecological gradient shifts between times.
- Annexes and tables classify results by plot type, landclass, and code categories; includes detailed recommendations and error-source analysis.

## Key Findings

- Plot relocation and plate recovery
  - Autumn 1990: Plate+plot relocation recovery around 65-71% depending on plot type; overall 71% plate recovery within a five-minute search.
  - 1991 QA with photographs: substantial improvement in plot relocation accuracy when photographs were used; greater ability to re-establish exact positions.
- Species recording and concordance
  - Initial 1990 QA showed relatively modest concordance between T1 and T2 species lists (around 45-47% depending on method), with a meaningful portion of discrepancies due to seasonality and changes in plots.
  - 1991 QA demonstrated a real increase in mean species per plot (about 2.7 additional species on average) between years, largely attributed to true ecological differences (season, drought effects) rather than solely observer error.
  - Seasonal effects: drought year (1990) vs a more normal year (1991) contributed substantially to differences; caution urged when comparing across years or land uses with high annual variation.
  - Within plots, common species often showed different frequencies across years, with some species clearly genuinely changing in abundance, while others appeared under-recorded or mis-recorded in the initial survey.
- Cover estimates
  - Repeated cover estimates generally showed similar trends for dominant species but several significant differences for common taxa; differences often reflect seasonal/annual changes or recording inconsistency rather than true ecological change.
  - The study recommends more explicit rules for recording tree and shrub cover and consistency in cover data usage in analyses.
- Land-use mapping and boundary coding
  - Primary land-use codes are generally reliable; high concordance for main categories (arable lowland, lowland grassland).
  - Boundary codes showed slightly lower concordance; overall mapping code performance remained robust across time and assessors.
  - Qualifiers and descriptive codes exhibited greater variability; issues often stemmed from interpretation and ambiguous definitions.
  - Repeated surveys by the same assessor produced higher agreement than between different assessors, underscoring the subjective element in code application.
- Mapping of species cover and vegetation units
  - Point-grid comparisons show good concordance for dominant species at a point (about 80% for a single dominant species across times); co-dominants show lower concordance (about 34%).
  - Across all plots, concordance for mapping of vegetation units remains modest when multiple species are present; strongest concordance occurs for the most evident species.
- DECORANA analysis and ecological gradients
  - Axis 1 shifts between years align with expected ecological gradients (shade tolerance, land-use changes) but differ by landclass and plot type.
  - UP (upland) plots show more stable axis scores; lowland plots display more pronounced shifts associated with crop changes and land management.
  - The combined 1978-1991 comparison indicates that changes in lowland areas followed expected historical trends, while upland areas showed some year-to-year perturbations, possibly drought-related.
- Overall data product implications
  - Land-use mapping is robust for major classifications; minor categories are under-tested due to limited sampling.
  - Ground-truthing and relocation accuracy remain critical for reliable GIS products, especially in unenclosed upland areas.
  - The current field handbook and coding schemes are largely effective but require refinements to reduce misinterpretation, especially for bryophytes, certain grasses, marsh/wetland, and boundary/hedge coding.

## Recommendations (selected)

- Data collection and QA timing
  - QA should be conducted as close as practical to the time of the original survey to reduce seasonality and vegetation-change confounds.
  - Conduct seasonal QA in the same year or same growing season when feasible.
- Use of photographs and relocation
  - Photographs dramatically improve plot relocation accuracy; ensure surveyors annotate photos and relate them to the corresponding plots.
- Plot positioning and markers
  - Use metal plates to mark X plots where possible; for difficult upland or unenclosed areas, allocate additional manpower for relocation.
  - For small Y plots, position with a survey tape and orient so the side aligns to N-S; position the SE corner consistently.
- Documentation and annotation
  - Improve annotation of sketches and photographs with distances, bearings, and distinguishing nearby features to aid relocation.
- Bryophytes and key taxa
  - Increase emphasis on bryophyte recording and vegetative identification of grasses in training; consider expanding allowable bryophytes in lists for certain habitats.
- Land-use/coding structure
  - Subdivide categories to reflect ecologically meaningful distinctions (e.g., separate upland grassland types; recognize marsh/wetland as a distinct primary habitat type).
  - Limit or standardize the use of descriptive qualifiers to reduce ambiguity.
  - Consider introducing a specific code for lowland rush pasture and for wet heath as distinct primary codes.
  - Restrict primary boundary code use to hedge with accompanying qualifying codes for composition.
- Mapping of vegetation cover
  - Record only the most prevalent species at a point to improve reproducibility; emphasize mapping of land-use parcels over exhaustive species-level cover detail.
  - Document and standardize the treatment of co-dominants and multiple canopy layers to improve repeatability.
- Data quality and metadata
  - Ensure that mapping and species data include clear metadata about time of year, observer, plot relocation method, and any seasonal effects.
  - Develop guidelines for handling and reporting seasonal or annual variation in change statistics.

## Implications for GIS Specialists

- Data quality governance
  - QA results confirm robustness of major land-use classifications but highlight ongoing uncertainties in boundary coding, rare categories, and fine-scale species mapping.
- Standardization and reproducibility
  - Emphasis on standard codes, explicit definitions, and consistent application across assessors to improve interoperability of GIS datasets.
- Documentation and provenance
  - Necessity for detailed metadata on survey year, plot type, relocation method, and whether photographs or plates were used.
- Data design adjustments
  - Suggest simplifying mapping outputs by prioritizing primary land-use codes and dominant species, while treating ancillary species data as optional or for higher-resolution analyses.
- Future QA integration
  - Align QA activities with data production cycles to minimize seasonal variance and maximize comparability across survey years.

## Conclusions

- The 1990 QA exercise demonstrates that the Countryside Survey field methods produced reliable GIS-ready land-use maps and vegetation data for major categories, with strong relocation using photographs and metal plates.
- Substantial variation exists at finer taxonomic levels and for boundary/qualifier codes, driven by observer interpretation, seasonality, and plot relocation challenges, especially in unenclosed upland areas.
- The integration of photographs, standardized coding, and targeted training (including bryophytes and grasses) will enhance repeatability and the utility of data products for policy, clients, and the public.
- The study supports using year-appropriate QA and refined mapping protocols to improve future surveys and GIS data products, while acknowledging genuine ecological changes between years, particularly under drought conditions.