# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

## Purpose and scope
- Assesses consistency and reliability of the CS2000 field programme due to many recorders and surveyors.
- Focuses on a QA exercise: 38 squares (out of 519), one quarter resurveyed, analyzing 234 species plots across nine plot types.
- Evaluates plot relocation efficiency, species concordance, accuracy of % cover estimates, bias in habitat change detection, comparability with CS1990, landuse mapping accuracy, and recording of changes.

## Aims
- Quantify field recording accuracy in CS2000 and assess change statistics.
- Examine plot relocation efficiency and reasons for differences (observer error, plot location/orientation, management/seasonal effects).
- Relate findings to CS1990 to gauge consistency over time.
- Provide an objective basis for data quality and governance of CS2000 data.

## Methods overview
- Sample: 38 squares; one quarter resurveyed; 234 plots analyzed across plot types; 34 squares previously included in CS1990 QA.
- Plate and plot relocation: attempted relocation of buried plates; comparison with 1990 QA and evaluation of accuracy eight years on.
- Data elements examined: location of plates/plots, landcover mapping (primary, secondary, boundary, and hedge/wall categories), and changes in landuse codes.
- Performance categories for relocation:
  - I: Plate and plot located (clear evidence from records).
  - II: Plate not found, but plot location closely matches.
  - III: Plate not found; plot only approximately relocated.
  - IV: Insufficient information to locate; plot abandoned.
- Metrics include species concordance, counts of species per plot, and cover estimates, plus code concordance for landcover and boundaries.

## Key QA findings

### Plot relocation
- Overall relocation efficiency: about 86.7% recovered for full plot searches; eight-year relocation success comparable to 12-month results from earlier QA.
- CS2000 surveyors accurately relocated approximately 60% of plots; ~25% relocated with some accuracy; ~15% inadequately relocated.
- Plate recovery: assessors located 69.3% of plates; surveyors’ success varied; some misplacements or transfers to new plates occurred.
- Comparison with QA: CS2000 plate/plot relocation results generally similar to prior QA benchmarks, indicating robust but imperfect relocation practices over time.

### Species concordance
- Mean species per plot: CS2000 17.9; QA 20.4 (QA tended to list more species).
- Two measures of agreement (TI and T2) used to compare pre- and post-survey species lists; combined TI+T2 variation indicates 26.9% total mis-matches.
- Major sources of variation:
  - Overlooked species (largest contributor, ~39.8% of TI errors).
  - Mis-identifications (couplets and non-couplets) and orientation/placement errors.
  - Management/seasonal effects contributed to some T2 variations.
- Seasonal and plot-location factors influenced concordance; no strong directional bias detected in overall axis (DECORANA) scores between CS2000 and QA.

### Vegetation cover
- Coverage estimates for key species compared between CS2000 and QA; general agreement good but notable differences for some grasses.
- Examples of significant differences (survey vs QA) include Holcus lanatus (p=0.029), Dactylis glomerata (p=0.005), Anthoxanthum odoratum (p=0.040), and Eriophorum vaginatum (p=0.018), indicating systematic but species-specific discrepancies.
- Overall, cover coding tended to be similar for many species, though some grasses showed larger discrepancies, partially attributable to seasonal effects and interpretation of cover bands.

### Landcover mapping and coding
- Primary landcover codes: high concordance; overall primary landcover agreement around 87–88% (excluding BAP codes).
- BAP (broad habitat) codes showed lower concordance (around 77%), reflecting broader habitat classification challenges.
- Primary boundary features: very high concordance for boundary coding (code concordance ~92%), with hedge/stone-wall coding showing some variability.
- Change in landcover: analysis indicated substantial portion of observed changes since 1990 were misrecorded or missed; some changes were attributed to miscodings or mis-location rather than real landscape change.

### Hedge diversity and boundary features
- Hedge diversity plots showed good overall species concordance (common species list broadly matched; total species record ~124; agreement ~74.2%; surveyor efficiency ~77.4%).
- Boundary features (walls/hedges) exhibited reasonable agreement on height and stockproof status, but with some code-level mismatches, especially in hedge shape classifications and wall condition codes.

### Arable plots
- Only five arable margin plots analyzed; concordance was very poor, likely due to seasonal variation and surveyors’ limited familiarity with ruderal species, suggesting need for additional visits or targeted training for arable margins.

### Overall methodological and directional findings
- DECORANA ordination shows no directional bias between CS2000 and QA results for axis 1 across plot types; mean axis scores were not significantly different.
- When grouped by landclass (LC, LG, MA, UP), no consistent directional bias detected between CS2000 and QA within landclasses.
- The mapping and coding framework (primary/qualifying codes, boundaries, hedges) generally performed well, with moderate to high concordance, though some codes and change records require refinement.

## Data quality implications for data stewards

- Provenance and lineage
  - QA provides a quantitative baseline for survey reliability and identifies where data provenance (survey vs QA assessment) should be captured in metadata.
- Metadata and coding schemes
  - Documentation of code sets (primary, secondary, cover, boundary, BAP) and the QA assessment of these codes is essential for future data users.
  - Changes in codes over time (e.g., introduction of new hedge/boundary codes) require versioning and clear metadata about which code set was used.
- Data accuracy and confidence indicators
  - Relocation accuracy, species concordance, and cover agreement are key confidence metrics that can be incorporated as data quality indicators in a dataset catalog.
- Change detection and attribution
  - The relatively low overall change concordance (about 51%) highlights the need for explicit handling of change versus measurement error, including guidance on how to treat unsubstantiated or ambiguous changes.
- Temporal comparability
  - Differences in survey timing, seasonal effects, and plot relocation methods should be reflected in data documentation to ensure comparability with CS1990 and future surveys.
- Data sharing and governance considerations
  - Provide access to QA methodology annexes, scoring rubrics, and summary tables to enable secondary analyses and reproducibility.
  - Document limitations, such as arable plot small sample size and potential biases due to seasonality or species misidentification.
- Data quality controls and recommendations
  - Emphasize the importance of rigorous plot location/orientation verification, especially for long-term comparisons.
  - Suggest training enhancements for species identification in vegetative states and standardized cover estimation protocols.
  - Recommend two visits for arable margins in future work to improve reliability.

## Recommendations and governance considerations for data sharing

- Include QA provenance in data packages: clearly label which plots/squares underwent QA, the time frame, and the plot types involved.
- Attach coding schemas and change-handling rules: primary/secondary/cover/BAP/ boundary codes; clearly document updates or additions to codes.
- Expose data quality flags: relocation accuracy, species concordance category, cover agreement, and change-concordance indicators to assist users in filtering analyses by confidence level.
- Maintain versioned datasets: capture CS2000 baseline and QA-adjusted data separately where appropriate, with metadata linking to CS1990 comparability analyses.
- Provide guidance on limitations: highlight potential biases from seasonality, plot orientation errors, and arable margin sampling when using the data for trend analyses.
- Plan for future QA cycles: establish routine QA protocols to monitor ongoing data quality, especially when expanding plot coverage or adapting coding schemes.