# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

- Purpose: Assess consistency and reliability of CS2000 fieldwork across relocation, species recording, vegetation cover, landcover mapping, and boundary features; compare CS2000 with CS1990 and evaluate change statistics.
- Scope: QA on 38 of 519 squares surveyed in 1998; resurvey of one quarter in each square; analysis based on 234 plots across seven main CS2000 plot types (quadrats and linear plots) and additional landuse/boundary mapping codes.

## Methods and Scope

- Sample: 38 squares (out of 519); one quarter resurveyed per square; 234 species plots analyzed; 34 squares previously included in 1990 QA.
- Plot types: Quadrats and linear plots (including road verges, streamsides, hedges, arable margins, and other land classes). X, Y, U plots and BAP-related plots were included; some arable margin plots discussed but small in number.
- Plate relocation: Assessed ability to relocate buried plates eight years after burial; used original 1990 sketch maps, photographs, and metal detectors. Categorized relocation success into four classes (I–IV).
- Data comparison: Compared CS2000 survey data (TI) with QA data (T2) to quantify concordance and errors in species records, cover estimates, and landcover codes.
- Mapping and boundary assessment: Evaluated primary land cover codes, descriptive/cover codes, and boundary features (including hedges and walls); included assessment of Hedge/Boundary qualifiers and hedge shapes coding.
- Change assessment: Analyzed changes in landuse and habitat strings between 1990 and 1998; examined concordance in recorded changes and identified potential omissions or miscodings.

## Key Findings

- Plot relocation and plate recovery
  - Overall relocation: 60% of plots accurately relocated; ~25% relocated but not exactly; ~15% inadequately relocated.
  - Plate recovery: 69.3% of plates recovered by QA; comparable to 65.2% recovery in 1991 QA of CS1990.
  Availability of plates varied; many CS2000 plots used new plates, complicating longitudinal relocation.
  - Four relocation classes defined; many instances of mis-location or mis-orientation observed (e.g., wrong bank/side of features).

- Species concordance and richness
  - Mean species per plot: CS2000 17.9; QA 20.4 (increase due to QA).
  - Overall agreement: high, with substantial overlap in species lists; increases in species counts largely reflect recording thoroughness and seasonal effects rather than fundamental bias.
  - Nature of mismatches: mis-identifications (especially grasses), overlooked species, and location/orientation errors contributed most to non-concordances.
  - Frequency of species: broad patterns largely consistent between surveyors and assessors, though some species (particularly grasses and certain forbs) showed greater disagreement; mosses frequently under-recorded.

- Vegetation cover and abundance
  - Cover estimates for principal species generally aligned between CS2000 and QA, but several notable differences existed for key grass species (e.g., Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum, Eriophorum vaginatum) with some results achieving statistical significance.
  - Overall cover concordance for selected species around moderate levels; some species showed lower concordance due to seasonal effects and identification challenges.

- Landcover mapping and boundary coding
  - Primary land cover codes: high concordance between CS2000 and QA; overall primary land cover agreement around 87–88%.
  - BAP codes: lower agreement (~77–78%), reflecting difficulty in distinguishing certain broad habitat types and boundaries; some misclassifications tied to boundary type changes.
  - Primary boundary features: strong concordance (~85% for primary codes); boundary code concordance high (~92%), indicating consistency in identifying boundary features when present.
  - Hedge and wall attributes: Hedge-related codes and wall condition showed moderate concordance (hedge shapes coding had limited success; many hedges omitted or misclassified).
  - Boundary height and stockproof status: high agreement; minor omissions noted.

- Change detection and change coding
  - Overall change concurrence: about 51%; a substantial portion of changes recorded by CS2000 were not substantiated by QA (≈14.7% occurred but QA did not confirm; ≈33.9% changes were not noted by CS2000).
  - Many changes since 1990 were missed or misrecorded; this raises caution for relying solely on CS2000 strings to evaluate habitat change over time.
  - Some changes reflected true land-use or habitat shifts; a number of discrepancies were due to mis-coding, mis-location, or mis-orientation.

- Arable plots
  - Very small sample (five plots); concordance was poor, with substantial seasonal variability; suggests the need for multiple visits to accurately capture arable margin changes.

- Overall synthesis
  - CS2000 fieldwork demonstrates robust spatial mapping and high concordance for primary land cover and boundary coding, with areas for improvement in: boundary hedge coding, change detection, and precise plot relocation/orientation.
  - Seasonal effects and observer errors (misidentifications, overlooked taxa) remain key sources of variation in species and cover data.

## GIS Implications and Quality Considerations

- Spatial accuracy and reliability
  - High confidence in primary land cover mapping and boundary delineations; BAP codes and hedge-related features less certain.
  - Plot relocation and plate recovery indicate that eight-year-latent spatial data can be recovered with moderate success, but accurate longitudinal analyses require careful handling of relocation uncertainty and potential new plate placements.
  - Orientation and location errors significantly affect species mis-matches and cover misassignment, impacting habitat classification and change analyses.

- Data integration and harmonization
  - The CS2000 approach combines multiple plot types and landclass codes; robust QA is essential when integrating across plot types for GIS analyses.
  - Differences in species lists and cover values between surveyors and QA highlight the need for standardized identification aids and explicit documentation of seasonal effects.

- Change detection caution
  - With only about half of changes concordant between CS2000 and QA, GIS-based change detection should rely on plot-level evidence and be cautious about attributing observed changes to true ecological shifts without supporting QA data.

- Arable margins and seasonal effects
  - Arable plots show high variability and low concordance; GIS workflows should flag these areas for additional sampling or caution when interpreting change over time in arable habitats.

- Coding and classification nuances
  - High concordance for primary codes and boundaries suggests reliable spatial classifications; lower concordance for hedge shapes and certain landuse qualifiers indicates areas where GIS databases may require supplementary notes or validation.

## Recommendations and Practical Takeaways

- Strengthen plot relocation protocols
  - Improve marking and documentation to reduce orientation errors; consider standardized marking practices to improve long-term relocatability.
  - When re-surveying, employ consistent boundary reference points and enhanced digital mapping aids to minimize misplacements.

- Improve boundary and hedge coding
  - Review hedge-shape coding scheme for practicality; consider simplifying or expanding categories to reduce omissions and misclassifications.
  - Ensure boundary feature checks reflect current conditions to minimize changes not captured by QA.

- Enhance change detection reliability
  - Treat CS2000 change strings with caution; cross-validate with QA and, where possible, field notes or photographic evidence.
  - For long-term habitat change analyses, rely on plot-level QA metrics to calibrate change statistics.

- Address species recording challenges
  - Provide targeted training on grasses and problematic taxa; reinforce use of reference keys and seasonal considerations.
  - Maintain explicit QA steps for species that are frequently overlooked or misidentified.

- Arable plots: plan multiple visits
  - Given high seasonality and identification challenges, allocate additional visits to arable margin plots to improve data reliability.

- Reporting standards
  - Maintain clear documentation of QA metrics (plot relocation success, concordance rates by code group, and change concordance) to inform end-users of data uncertainty and reliability for GIS analyses.

- Data integration strategy for GIS workflows
  - Incorporate QA-derived confidence indicators (e.g., relocation accuracy, code concordance, and change concurrence) into GIS attribute schemas to support uncertainty-aware analyses.

- Overall takeaway for GIS specialists
  - CS2000 maps and attribute data provide solid spatial foundations for habitat and landcover analyses, with strong performance in core mapping categories and boundary delineation.
  - Use QA findings to guide cautious interpretation of change data, hedge-related codes, and arable margins, and to drive improvements in future field-data collection and coding schemes.