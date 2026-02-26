# 1990 Countryside Survey: Quality Assurance Exercise

- A comprehensive evaluation of the quality assurance (QA) processes used in the 1990 Countryside Survey, including results, interpretation, and recommendations to improve accuracy and confidence in survey statistics and GIS-ready data products.

## Purpose and scope
- Quantify accuracy of field recording and its impact on change statistics.
- Explain differences in recording due to observer error, seasonality, plot location, and information type.
- Compare QA findings with previous ITE surveys and advise methodology improvements for future surveys.
- Focus on map-based data production: vegetation cover, land-use mapping, and plot relocation fidelity.

## Methods and data types
- Two QA series:
  - Autumn 1990: 21 original survey squares assessed by two independent evaluators using original sketch maps.
  - 1991: Expanded QA with photographs of plots; included self-assessment in 1 km squares, with 28 of 32 terrain classes revisited.
- Plot types (six types in main survey): 200 m2 quadrats (X plots) and 4 m2 quadrats (Y plots), plus linear features (road verges, hedges, streamsides, boundaries).
- Relocation exercises:
  - Relocated plates (corner markers) and plots using sketch maps, photographs, and metal detectors.
  - 1/4 of each square resurveyed to include representations of all plot types.
- Data examined:
  - Species lists per plot, presence/absence, and cover estimates at nine predetermined points per quarter.
  - Land-use mapping codes (primary and re-descriptive codes) and boundary codes.
  - Photographs used to re-establish plot locations; plate relocation success rates recorded.
- Analytical approaches:
  - Multiple concordance indices for species (e.g., simple agreement, adjusted agreement, accuracy).
  - DECORANA analysis to examine ecological gradients and axis shifts between survey periods.
  - Assessment of efficiency of recording and source of variation (A–J categories: mis-ID, overlooked species, mis-location, seasonal/management changes, etc.).
  - Statistical tests for cover data and species-frequency changes.

## Key findings

- Overall recording accuracy and concordance
  - Initial autumn 1990 QA showed moderate concordance between T1 and T2 data; full 1991 QA indicated a higher overall concordance (about 60.9% to 74% efficiency depending on metric).
  - When seasonal changes and data not available in the QA year were removed, initial efficiency of recording approached 74%.
  - Across all plots, a significant increase in mean species per plot from 1990 to 1991 (from ~20.7 to ~23.4) was detected; this was significant overall but varied by plot type and land class.
  - Annual/seasonal variation is a major component of observed changes; drought year (1990) vs relatively normal year (1991) influenced detectability and species lists, especially in lowland and marginal areas.
- Plot relocation and use of photographs
  - Plate relocation success varied by plot type and year; autumn 1990: 71% recovery with a 5-minute search; 1991 QA: plate and plot relocation improved when photographs were used (plates found ~65%; plots found ~87%).
  - Using photographs markedly improved relocation accuracy, especially for X plots; Y plots remained more challenging. Metal plates were effective for enclosed land but time-consuming in unenclosed uplands.
  - Recommendations emphasize annotating photographs and relating them to plots, including distances to nearby features to improve relocation.
- Species recording quality and error sources
  - Approximately 40% of species mismatches occurred when comparing individual plot data (T1 vs T2), but aggregated trends across plots showed useful consistency.
  - Major error sources identified:
    - Mis-identification or mis-coding
    - Species overlooked at T1 or T2
    - Plot mis-location or mis-orientation
    - Seasonal/annual changes in species composition
    - Management/crop changes affecting species presence
  - Seasonal effects were substantial for many taxa; drought vs non-drought years contributed to apparent changes in species richness.
- Land-use and boundary coding
  - Primary land-use codes were reliably applied (high concordance, ~88–95%), whereas boundary codes showed slightly lower concordance (around 80–83% overall), partly due to reassessment by different assessors.
  - Two levels of coding (primary and qualifying) introduced interpretive variation; however, overall coder performance was consistent, with similar results across assessor pairs and survey years.
  - Complexity in mapping (many codes) can reduce reproducibility; differences were particularly evident for fine-scale habitat distinctions and bryophyte-related coding.
- Vegetation cover mapping and species dominance
  - Cover estimates showed limited concordance for species recorded at both times; many species showed significant changes in cover between surveys, but these often reflected seasonal/management changes rather than true abundance shifts.
  - Two most prevalent species per vegetation unit or land-use parcel tended to be more reproducible between surveys when limited to dominant species; broader cover for multiple co-dominants yielded substantially lower repeatability.
  - The mapping of species cover benefits from focusing on the most prevalent species and clarifying cover measurement rules.
- Land-use codes and boundary features
  - Primary land-use codes demonstrated high reliability; boundary codes had slightly lower concordance, with most differences attributable to interpretation and qualifying codes.
  - Suggested simplifications to mapping codes to improve reproducibility (e.g., dichotomous decisions for some land-use categories) and clearer definitions for boundary-related codes.
- Decorrelation of ecological gradients over time
  - DECORANA analysis showed axis shifts consistent with broad vegetation changes over time, with upland vs lowland gradients maintaining separation; the 1990–1991 shift was not statistically significant in some aggregates but aligned with longer-term trends observed in earlier work.
  - The combined analyses indicate both land-use changes and climatic variation contribute to observed ecological gradients.

## Implications for GIS data products

- Data quality and comparability
  - Cross-year comparisons require careful handling of seasonality and crop/management changes to avoid misinterpreting data as ecological change.
  - QA should be conducted in the same year as the main survey where possible; when not possible, explicitly account for seasonal differences.
- Data structure and reporting
  - Land-use mapping benefits from focusing on primary codes and limiting emphasis on detailed cover classifications to improve reproducibility.
  - For vegetation mapping, emphasize dominant species per parcel or plot rather than exhaustive species lists per location.
  - Include photos and precise location markers as standard field products to facilitate future relocation and data integration.
- Documentation and standardization
  - Clarify definitions for borderline or ambiguous codes (especially for wetland, rush pastures, and upland grasslands); refine bryophyte inclusion rules for wetlands and semi-natural habitats.
  - Improve field handbooks with explicit guidance on locating plots, recording cover, and handling borrows in encroached or enclosed land.
- Training and QA practices
  - Targeted training on grasses and bryophytes, as well as vegetative IDs, to reduce mis-identifications.
  - Emphasize consistent measurement practices and use of simple, reproducible coding schemes.
  - Include bryophyte and selected rare taxa in QA exercises where relevant to the habitat type being surveyed.

## Recommendations (summarized)

- 1 Retain lichens in general surveys; provide training specimens with habitat context.
- 2 Conduct QA as close as practical to the initial survey date.
- 3 Surveyors annotate photographs and relate them to plots, including distances to nearby features.
- 4 Use metal marker plates to mark X plots wherever feasible, especially in enclosed land.
- 5 Define 4 m2 (Y) plots with a tape, oriented so the side — not the diagonal — is aligned N-S, and place the plot at the SE corner.
- 6 Ensure photographs clearly show the plot location and key nearby features to aid relocation.
- 7 Survey plots using the standard Countryside Survey 1990 procedures.
- 8 Consider subdividing certain upland land-use codes (e.g., upland grassland) to reflect habitat distinctions (improved vs. unimproved).
- 9 Introduce a dedicated lowland rush pasture code.
- 10 Recognize wet heath as a distinctive, widespread vegetation type with a primary code.
- 11 Restrict primary boundary codes to hedge presence, with species composition captured by qualifying codes.
- 12 Record only the two most prevalent species for land-use parcel mapping to improve reproducibility (and limit over-detail in mapping).

## Conclusions

- Photographic documentation and plate-based relocation substantially improve plot relocation accuracy, particularly in unenclosed areas, and should be standard practice in future surveys.
- Seasons and year-to-year climatic variation significantly influence species lists and their interpretation; QA should be aligned with the same year or carefully controlled for seasonal effects.
- Land-use mapping can be made more robust by simplifying coding schemes, prioritizing primary codes, and focusing on dominant vegetation species for mapping outputs.
- While the QA revealed substantial variation in species-level data, broader mapping and land-use outputs show reliable consistency, enabling GIS-based data products to support policy and planning with appropriate caveats on year-to-year changes.
- The document underscores the importance of well-documented field methods, standardized codes, and the use of ancillary data (photos, markers) to enhance reproducibility and confidence in GIS-enabled countryside data products.