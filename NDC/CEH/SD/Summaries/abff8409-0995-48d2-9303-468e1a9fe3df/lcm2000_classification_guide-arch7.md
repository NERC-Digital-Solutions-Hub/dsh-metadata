# LCM2000 Final Report

- Purpose
  - Document calibration of LCM2000 against CS2000 field survey data to support UK Biodiversity Action Plan broad habitat assessments.
  - Provide methodologies to map Broad Habitats (BHs) and derive BH/Target class statistics from satellite-derived data.

- Background and classifications
  - LCM2000 is a thematic, spectral-classification framework that can be combined into thematic components and BHs; Subclasses and Variants refine distinctions where possible.
  - Mapping aims to distinguish BHs where feasible, with aggregate 10-class reporting for consistency with related datasets.
  - BHs are mapped with attention to display at national/regional scales; some rare or small classes are aggregated for clarity.

- Data and calibration approach
  - CS2000 field survey (FS) data: 569 one-km squares across GB (549 in 1998, rest in 1999); NI data not yet digital for testing.
  - Calibration vs validation: inter-comparison treated as calibration; FS data are not ground truth due to resolution differences and timing.
  - ARC/Info GIS workflow: 569 FS squares and corresponding LCM2000 map sections analyzed with three tests.

- Tests and correspondence levels
  - Per-pixel comparisons: direct overlay; captures all spatial differences (e.g., image resolution, MMU, timing, class definitions).
  - Per-segment comparisons: segment labels vs FS-dominant class for the segment.
  - Per-parcel comparisons: FS parcels vs LCM2000-derived parcel labels.
  - Correspondence levels examined at: BH level (excluding some features), Target class level, and Aggregate class level.
  - Confidence estimation: bootstrapping to derive 95% confidence intervals; avoids treating FS as ground truth.

- Overall correspondence results
  - BH level (GB): ~58% (range 57–60% Scotland-specific differences noted).
  - Per-pixel (GB): ~54% (England/Wales ~60%; Scotland ~44%).
  - Per-segment (GB): ~58% (England/Wales ~64%; Scotland ~47%).
  - Per-parcel (GB): ~62% (England/Wales ~69%; Scotland ~48%).
  - Target class level: higher concordance (GB ~65% per parcel; England/Wales ~73%; Scotland ~51%).
  - Aggregate class level: close alignments between LCM2000 and FS.

- Key interpretive points on accuracy
  - FS vs LCM2000 differences arise from resolution, timing, and classification scheme differences.
  - MMU mismatch (FS parcels >0.04 ha vs LCM2000 >0.5 ha) explains much of the disparity, especially for small features.
  - Time differences (FS mainly 1998 vs images 1998–2001) contribute to mismatches; up to ~15% of differences attributed to underlying data structure.
  - Best achievable accuracy likely around 85–87% at the Target class level; overall accuracy capped by FS repeatability (~88%).

- Habitat-specific notes and challenges
  - Woodland (Broadleaved/mixed and Coniferous): general area matches, but small woodlands often fall below LCM2000’s MMU, causing misalignment with FS.
  - Arable and horticultural land: spectral confusions with grass/urban, and rotation effects across years; some misclassifications between arable and built-up land.
  - Grasslands (Improved vs Semi-natural; Neutral/Calcareous/Acid): difficult spectral distinctions; soil acidity and management practices cause misclassifications; rough grassland often mapped as Neutral grassland in LCM2000, differing from FS.
  - Fen, marsh, swamp and Bracken: FS includes more fen/marsh in places; spectral masking for peat depth affects bog vs heath distinctions; peat depth used as a control but may under-represent bog extent.
  - Heath, bog, montane, inland bare ground: complex distinctions; altitude-based montane mapping may misrepresent actual habitat, and peat/bog definitions complicate separation from heath.
  - Water, coastal BHs, and boundary/linear features: inland water mapping aligns reasonably with FS for standing water; coastal BHs are small and often underrepresented or aggregated; boundary/linear features were not targeted in LCM2000 (treated as less reliable at the 1 km scale).

- Change detection
  - Between 1990 and 2000, changes are expected to be small and often surpassed by measurement error.
  - Satellite-based mapping alone is insufficient for robust change detection; an intelligent, multi-dataset approach is recommended.
  - Calibration results indicate under- and over-estimates in 2000 that should inform change analyses; integrating FS change expectations (1990 vs 1998) can improve detection.

- Practical implications for GIS work
  - Target and Aggregate class reporting provides more reliable results than BH-level mappings due to resolution and classification ambiguities.
  - Use of BHs as aggregate constructs; when possible, work at Variant/Subclass levels for greater pattern visibility (e.g., dense bracken, dwarf shrub heath).
  - Data integration: combine LCM2000 with field-derived data and other datasets (e.g., soil acidity, peat depth) to improve habitat discrimination.
  - Change detection workflows should leverage calibration insights to separate genuine change from classification error.

- Visual and data products
  - Table 2 maps LCM2000 class variants to broad habitats with color schemes; supports map displays at national/regional scales.
  - Coastal and marine BHs are treated as aggregates for reporting due to small extents and resolution constraints.
  - Display conventions preserve general BH patterns while allowing subclass/variant detail to be explored with user-defined color schemes.

- Appendix and supplementary insights
  - Appendix I reviews distinguishing features of Broad Habitats in relation to LCM2000 mapping, highlighting practical limitations in spectral discrimination and the role of field-based corrections.
  - Highlights the need for ongoing integration efforts among LCM2000, FS, and external datasets to refine peatlands, rough grasslands, and peat depth interpretations.